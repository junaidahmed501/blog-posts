## Upload Picture and get download URL

Use getDownload as promise not observable.

firebase.storage().ref().child(‘some text’).getDownloadURL() .then(response => this.someTextUrl = response) .catch(error => console.log(‘error’, error))

check this out for more

[https://www.javascripttuts.com/using-firebase-storage-in-ionic/](https://www.javascripttuts.com/using-firebase-storage-in-ionic/)