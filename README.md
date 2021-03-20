<p>
    
'''<?php

$myfile = fopen("unions/newfile.txt", "w") or die("Unable to open file!");
$txt = "test\n";

$file_path = "unions/";

$file_path = $file_path . basename( $_FILES['uploaded_file']['name']);

if(move_uploaded_file($_FILES['uploaded_file']['tmp_name'], $file_path)) {
    $txt = "File upload success";
} else{
    $txt = "File upload fail";
}

$txt = $txt."\n";

echo $txt;

fwrite($myfile, $txt);
fclose($myfile);

?>'''
</p>
