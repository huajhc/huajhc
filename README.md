- 👋 Hi, I’m @huajhc
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
huajhc/huajhc is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
$from_id = $message->from->id; $name = $message->from->first_name; $text = $message->text;
$mid = $message->message_id; $name2 = $update->callback_query->from->first_name; $message_id2 = $update->callback_query->message->message_id; $chat_id2 = $update->callback_query->message->chat->1768045259;
$from_id2 = $update->callback_query->from->id; $message_id = $update->callback_query->message->message_id; $data = $update->callback_query->data;
$username = $message->from->username;
mkdir("carlos");
$Dev = array("1710485251", "1768045259" ); //1768045259
$car = 1768045259; //1768045259
$tiger = file_get_contents("carlos/tiger.txt");
$tigerannel = file_get_contents("carlos/tigerannel.txt");
if($text == "تفعيل" or $text == "حظر" or $text == "1768045259" or $text == "كتم" or $text == "تقيد" or $text == "الاوامر" or $text == "الاعدادات" or $text == "رتبتي" or $text == "كشف" or $text == "الرتبه" or $text == "رتبته" or $text == "اضف رد" or $text == "حذف رد" or $text == "تاك" or $text == "حذف امر" or $text == "اضف امر" or $text == "تاك للكل" or $text == "/start"){
if($tigerannel == "on"){
$join = file_get_contents("https://api.telegram.org/bot".API_KEY."/getChatMember?chat_id=@$tiger&user_id=".$from_id);
if($message && (strpos($join,'"status":"left"') or strpos($join,'"Bad Request: USER_ID_INVALID"') or strpos($join,'"status":"kicked"'))!== false){
bot('sendMessage',[
'chat_id'=>$chat_id,
'text'=>"♻️┇ مرحبا عزيزي\n🎖┇عليك الاشتراك في قناة البوت اولا [@$tiger]\n🚸┇ ليمكنك استخدامه",
'parse_mode'=>'markdown','reply_to_message_id'=>$message->message_id,
'reply_markup'=>json_encode([
'inline_keyboard'=>[
[['text'=>"🎖اضغط هنا 🎖",'url'=>"t.me/$tiger"]],]])]);
 bot("sendmessage",[
      "chat_id"=>$car,
      "text"=>"📮┇ مرحبأ عزيزي المطور 
┉ ┉ ┉ ┉ ┉ ┉ ┉ ┉
🎖┇اليك معلومات العضو قام بدخول قناة

🎖┇اسم العضو ~⪼ $name
🎖┇معرف العضو ~⪼ @$username
🎖┇ايدي العضو ~⪼ $from_id
┉ ┉ ┉ ┉ ┉ ┉ ┉ ┉
🎖┇قناة الاشتراك الاجباري ~⪼ @$JJJJS1",
      ]);
      die('اا');
  }
bot('sendMessage',['chat_id'=>$chat_id, 'text'=>" ",'reply_to_message_id'=>$message->message_id,]);}}

$set = file_get_contents("carlos/set.txt");
$tiger = file_get_contents("carlos/tiger.txt");
if(in_array($from_id,$Dev)){
if ($text == "تغيير الاشتراك الاجباري" or $text == "تعيين الاشتراك الاجباري" or $text == "تغيير قناة الاشتراك" or $text == "تعيين قناة الاشتراك"){
file_put_contents("carlos/set.txt","tiger");
bot("sendMessage",["chat_id"=>$chat_id,"text"=>"*📥┇مرحبا بك الان قم بأرسال معرف قناة مندون @*\n",'parse_mode'=>"MARKDOWN",'reply_to_message_id'=>$message_id,]);}
if($text && $set =="tiger" and in_array($from_id,$Dev)){
file_put_contents("carlos/tiger.txt",$text); 
file_put_contents("carlos/set.txt","");
bot("sendmessage",["chat_id"=>$chat_id,"text"=>"📥┇تم حفظ معرف لقناة \n🎖┇الان قم برفعي داخل قناتك\n🎗┇وثم ارسال تفعيل الاشتراك الاجباري",'parse_mode'=>"MARKDOWN",'reply_to_message_id'=>$message_id,]);}}

if(in_array($from_id,$Dev)){
if($text == "مسح قناة الاشتراك" or $text == "حذف قناة الاشتراك"){
file_put_contents("carlos/tiger.txt","");
bot("sendMessage",["chat_id"=>$chat_id,"text"=>"📥┇مرحبا بك تم حذف قناة الاشتراك الاجباري",'parse_mode'=>"MARKDOWN",'reply_to_message_id'=>$message_id,]);}

if($text == "جلب قناة الاشتراك" or $text == "قناة الاشتراك" or $text == "الاشتراك الاجباري" or $text == "قناة الاشتراك الاجباري"){
bot("sendMessage",["chat_id"=>$chat_id,"text"=>"📥┇مرحبا بك اليك قناة الاشتراك - @$setch",'parse_mode'=>"MARKDOWN",'reply_to_message_id'=>$message_id,]);}
}

if($text =="تعطيل الاشتراك الاجباري"){
if (in_array($from_id,$Dev)){
bot('sendmessage',['chat_id'=>$chat_id,'text'=>"📥┇تم تعطيل الاشتراك الاجباري",'parse_mode'=>"markdown",'disable_web_page_preview'=>true,'reply_to_message_id'=>$message_id,]);
file_put_contents("carlos/tigerannel.txt","off");}}

if($text =="تفعيل الاشتراك الاجباري"){
if (in_array($from_id,$Dev)){
bot('sendmessage',['chat_id'=>$chat_id,'text'=>"📥┇تم تفعيل الاشتراك الاجباري",'parse_mode'=>"markdown",'disable_web_page_preview'=>true,'reply_to_message_id'=>$message_id,]);
file_put_contents("carlos/tigerannel.txt","on");}}

