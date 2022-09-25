## Ionic 3 image uploading through camera as well as camera gallery

```
ploadPic() {  
let that=this  
let imagefile = this.base64Image.split(',')[1] //this gets rid of the "data:image/jpeg;base64," part of the file  
  
let uploadTask = firebase  
  .storage()  
  .ref(this.uid)  
  .child("profile_pic")  
  .putString(imagefile, "base64", { contentType: "image/jpg" });  
uploadTask.on(  
  firebase.storage.TaskEvent.STATE_CHANGED, // or 'state_changed'  
  function(snapshot:any) {  
    // Get task progress, including the number of bytes uploaded and the total number of bytes to be uploaded  
    var progress = snapshot.bytesTransferred / snapshot.totalBytes * 100;  
    console.log("Upload is " + progress + "% done");  
    switch (snapshot.state) {  
      case firebase.storage.TaskState.PAUSED: // or 'paused'  
        console.log("Upload is paused");  
        break;  
      case firebase.storage.TaskState.RUNNING: // or 'running'  
        console.log("Upload is running");  
        break;  
    }  
  },  
  function(error) {  
    alert("error:"+JSON.stringify(error));  
  },  
  function() {  
    // Upload completed successfully, now we can get the download URL  
    console.log("got to downloadURL")  
    that.downloadURL = uploadTask.snapshot.downloadURL;  
    that.updateAuthUser();  
  }  
);
```

You can find similar code in the firebase docs here:

[https://firebase.google.com/docs/storage/web/upload-files](https://firebase.google.com/docs/storage/web/upload-files)