## get URL Query params with jquery & js

// Assuming "?order=1&total=30"  
  
var urlParams = new URLSearchParams(window.location.search);  
  
console.log(urlParams.has('order')); // true  
console.log(urlParams.get('order')); // "order"  
console.log(urlParams.getAll('order')); // \["order"\]  
console.log(urlParams.toString()); // "order=1&total=30""  
console.log(urlParams.append('currency', 'usd')); // "?order=1&total=30&active=usd"

`URLSearchParams` also provides familiar `Object` methods like `keys()`, `values()`, and `entries()`:

var keys = urlParams.keys();  
for(key of keys) {   
  console.log(key);   
}  
// post  
// action

var entries = urlParams.entries();  
for(pair of entries) {   
  console.log(pair\[0\], pair\[1\]);   
}

Javascript fallback

While `URLSearchParams` is ideal, not all browsers support that API. There's a [polyfill available](https://github.com/WebReflection/url-search-params) but if you want a tiny function for basic query string parsing, the following is a function stolen from the A-Frame VR toolkit which parses the query string to get the key's value you'd like:

function getUrlParameter(name) {  
    name = name.replace(/\[\\\[\]/, '\\\\\[').replace(/\[\\\]\]/, '\\\\\]');  
    var regex = new RegExp('\[\\\\?&\]' + name + '=(\[^&#\]\*)');  
    var results = regex.exec(location.search);  
    return results === null ? '' : decodeURIComponent(results\[1\].replace(/\\+/g, ' '));  
};

With the function above, you can get individual parameter values:

getUrlParameter('order'); // "1"