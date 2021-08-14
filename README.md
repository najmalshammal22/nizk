# nizk
Welcome To Nizk Source 
$botid =0000; # 1903586293
$step1 = json_decode(file_get_contents("https://api.telegram.org/bot".API_KEY."/getChatMember?chat_id=$chat_id&user_id=$botid"),true);

$step3 = $step1['result']
['can_change_info'];
$step4 =  $step1['result']['can_delete_messages'];
$step5 = $step1['result']['can_restrict_members'];
$step6 = $step1['result']
['can_invite_users'];
$step7 = $step1['result']
['can_pin_messages'];
$step8 = $step1['result']
['can_promote_members'];

if($step3 == 1){
$check3 = '✅';
}elseif($step3 != 1){
$check3 = '❌';
}if($step4 == 1){
$check4 = '✅';
}elseif($step4 != 1){
$check4 = '❌';
}if($step5 == 1){
$check5 = '✅';
}elseif($step5 != 1){
$check5 = '❌';
}if($step6 == 1){
$check6 = '✅';
}elseif($step6 != 1){
$check6 = '❌';
}if($step7 == 1){
$check7 = '✅';
}elseif($step7 != 1){
$check7 = '❌';
}if($step8 == 1){
$check8 = '✅';
}elseif($step8 != 1){
$check8 = '❌';
}

if($text =="كشف البوت"){
bot("deleteMessage",["chat_id"=>$chat_id,
"message_id"=>$message_id]);
$get=bot('sendMessage', [
'chat_id'=>$chat_id,
'text'=>"*⌯︙ اهلا بك عزيزي 🙋🏽‍♂
⌯︙هذهۃ صلاحيات البوت ادناهۃ !
⌯︙علامة ❪✅❫ مفتوحة ❪❌❫ مقفولة↯
ـ• ┉ • ┉ • ┉ • ┉ • ┉ • 
$check3 ︙تغيير معلومات المجموعة
$check6 ︙دعوهۃ الاعضاء الجديدة
$check7 ︙تثبيت رسائل الاعضاء
$check5 ︙حظر تقيد الاعضاء
$check8 ︙اضافهۃ مشرفين
$check4 ︙حذف الرسائل
• ┉ • ┉ • ┉ • ┉ • ┉ • 
⌯ ¦ Ch ⋙ @Godlovers7
",'parse_mode'=>"MARKDOWN",
]);
}
