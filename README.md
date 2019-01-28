<h1>Requirement</h1>
go to https://openload.co/account#usersettings
get your Api Login and Api key

## Simple code
```php
<?php
  include('./upload.php');
  $url='$yourFileUrl';
  $id =json_decode(remoteAdd($url),true)['result']['id'];
  $resultUpload = json_decode(cekRemoteUpload($id),true);
  $exitid = $resultUpload['result'][''.$id.'']['extid'];
  renameFile($exitid,"renamedFile.mp4");
  
?>
```
