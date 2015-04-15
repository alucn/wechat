# wechat
PHP版微信公共平台消息主动推送2015-04-15发布

模拟登录微信公共平台，实现主动信息发送；

突破订阅号一天只能发送一条信息的限制。

使用编码UTF-8


使用方法： 

$arr = array(
	'account' => '公众平台帐号',
	'password' => '密码'
);

$w = new Weixin($arr);

//$w->getAllUserInfo();//获取所有用户信息
$w->getUserInfo($groupid, $fakeid);//获取单个用户的信息，如果是默认组，则$groupid传0

$w->sendMessage('群发内容'); //群发给所有用户

$w->sendMessage('群发内容',$userId); //群发给特定用户，这里的userId是fakeid


本实例仅供参考，由此引发的法律风险，本人概不负责。谢谢。
