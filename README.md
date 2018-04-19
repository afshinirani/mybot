<?php

	$botToken ="496610612:AAFMF6xPaQBgdrqFh8eW-4p2dgFqYZllfnM";
	$website="http://api.telegram.org/bot".$botToken;

	$update=file_get_cotntents("php://input");

	$updateArray =jason_decode($update,true);
	
	$text=$updateArray["result"][0]["message"]["chat"]["id"];
	file_get_cotntents($website."/sendmessage?chatid="$chatId."$text=test");
	
	print_r($chatid);

?>
