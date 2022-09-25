## Simultaneously write/update to multiple locations in Firebase

According to google docs:

To simultaneously write to specific children of a node without overwriting other child nodes, use the `update()` method.

When calling `update()`, you can update lower-level child values by specifying a path for the key. If data is stored in multiple locations to scale better, you can update all instances of that data using [data fan-out](https://firebase.google.com/docs/database/web/structure-data#fanout).

For example, a social blogging app might create a post and simultaneously update it to the recent activity feed and the posting user’s activity feed using code like this:

function writeNewPost(uid, username, picture, title, body) {  
  // A post entry.  
  var postData = {  
    author: username,  
    uid: uid,  
    body: body,  
    title: title,  
    starCount: 0,  
    authorPic: picture  
  };

  // Get a key for a new Post.  
  var newPostKey = firebase.database().ref().child('posts').push().key;

  // Write the new post's data simultaneously in the posts list and the user's post list.  
  var updates = {};  
  updates\['/posts/' + newPostKey\] = postData;  
  updates\['/user-posts/' + uid + '/' + newPostKey\] = postData;

  return firebase.database().ref().update(updates);  
}

This example uses `push()` to create a post in the node containing posts for all users at `/posts/$postid`and simultaneously retrieve the key. The key can then be used to create a second entry in the user's posts at `/user-posts/$userid/$postid`.

Using these paths, you can perform simultaneous updates to multiple locations in the JSON tree with a single call to `update()`, such as how this example creates the new post in both locations. Simultaneous updates made this way are atomic: either all updates succeed or all updates fail.

Read further here to get an overview of how to [Read and Write Data](https://firebase.google.com/docs/database/web/read-and-write#updating_or_deleting_data) and [Save Data](https://firebase.google.com/docs/database/admin/save-data) in firebase.