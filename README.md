# -issue_20190606_2
CMSMadeSimple Software Babel Modules 1.9.4.2 Open Redirection

# Vulnerable Source Code : [ redirect.php ]
**************************************
<?php
error_reporting(0);
if(!isset($_GET["newurl"]) ){
	header("location: index.php");
}else{
	if(isset($_GET["newlang"]))	setcookie('usrlang',$_GET["newlang"],time()+86400*30,'/');
	header("location: ".$_GET["newurl"]);
}
