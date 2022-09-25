## Ionic resolve file url

Uploading an image in ionic is a tedious job which have caused me troubles over time. Using base64 data is easy but that can lead to app crashes as base64 string is large string which mobile has to process and app crashes occur in some lower tier phones.  
But if I am not using base64 and instead I’m using FILE\_URI then there is an issue where we don’t have actual file to send to the server. To resolve this issue I use this method with few other helper methods to get a file and also do few more things like checking file size before sending to the server.

So first of all install ‘File’ from ionic native and import File and DomSanitizer like this

**import** {File} **from "@ionic-native/file"**;  
**import** {DomSanitizer} **from "@angular/platform-browser"**;

Pass file\_uri data to this method and inside this method you can assign values to your form or variable and do your other processing you want.

resolveFile(imageData) {  
  **let** context = **this**;  
  **this**.file.resolveLocalFilesystemUrl(imageData).then(**function** (fileEntry: **any**) {  
  
    fileEntry.file(**function** (file) {  
      **if** ((file.**size** / 1024 / 1024) > 5) {  
        context.presentAlert(**'Cannot upload the image'**,  
          **'The image exceeds the max allowed size of 5 MB'**)  
      }  
  
      context.**stepOneDataCpy**.patchValue({  
        **image**: imageData,  
      });  
      context.**imagePlaceholder** \= context.sanitizer.bypassSecurityTrustUrl(*normalizeURL*(imageData));  
      context.**loader**.dismiss();  
    });  
  });  
}