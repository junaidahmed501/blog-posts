## Invalid key hash. The key hash does not match any stored key hashes

This is how i solved this problem

Download your APK to your PC in java jdk\\bin folder

bin folder might look like this

C:\\Program Files\\Java\\jdk1.7.0\_121\\bin

go to java jdk\\bin folder and run cmd then  
copy the following command in your cmd

keytool -list -printcert -jarfile yourapkname.apk

Copy the SHA1 value, which looks like this

CD:A1:EA:A3:5C:5C:68:FB:FA:0A:6B:E5:5A:72:64:DD:26:8D:44:84

and open [http://tomeko.net/online\_tools/hex\_to\_base64.php](http://tomeko.net/online_tools/hex_to_base64.php) to convert your SHA1 value to base64.  
This is what Facebook requires. Copy base64 value and paste it in key hashes under settings->Basic -> Key hashes