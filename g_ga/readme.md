
<h1>greatagent(原名：wwqgtxx-goagent)</h1>
======================

注：这是只是一个方便国内用户使用的镜像，由我个人copy。

本镜像的目的，是测试依附于Github的网络传播自由，并为无法访问google code的墙内朋友提供一个替代方案。

<a href="https://github.com/dk9999/test/blob/g_ag/dl_g_ag.md">本镜像整理的greatagent2系列下载地址</a>

======================

<h2>项目宗旨</h2>

本项目的宗旨是为goagent/新版wallproxy提供公共开放的的服务端，同时做出一些优化和加强，并且提供免配置，集成大量优良插件的firefox，以便于大家的使用。在此先感谢goagent和wallproxy作者为我们无私的奉献，向他们敬礼!

<h2>下载与使用</h2>

========================

<h3>下载地址</h3>

由于存在自动更新，谷歌code页面的downloads中永远是最新的稳定版。Github中是最新版本。请根据下文说明选择greatagent2-ga/greatagent2-wp/greatagent2-esr版本，最好选择自带火狐浏览器的版本。

<ul>
  <li><a href="https://github.com/dk9999/test/blob/g_ag/dl_g_ag.md">本镜像整理的greatagent2系列下载地址</a><li>
</ul>

<ul>
  <li><a href="https://code.google.com/p/greatagent/wiki/downloads">谷歌code下载 1</a></li>
  <li><a href="https://code.google.com/p/greatagent-ga/wiki/downloads">谷歌code下载 2</a></li>
  <li><a href="https://code.google.com/p/greatagent-wp/wiki/downloads">谷歌code下载 3</a></li>
  <li><a href="https://github.com/greatagent2/ga/archive/master.zip">github下载 greatagent2-ga</a></li>
  <li><a href="https://github.com/greatagent2/wp/archive/master.zip">github下载 greatagent2-wp</a></li>
  <li><a href="https://github.com/greatagent2/esr/archive/master.zip">github下载 greatagent2-esr</a></li>
</ul>

<h3>版本区别</h3>
  <ul>
    <li>greatagent2-<b>ga</b>--使用secure-goagent系列版本构建，抗封锁能力较强，速度较慢（适合用于看网页，上facebook，twitter，google+等），提供自动更新功能。<a href="https://github.com/greatagent2/ga/archive/master.zip">github下载</a></li>
    <li>greatagent2-<b>wp</b>--使用wallproxy2系列构建，抗封锁能力一般，速度一般，但看电影速度很快（特别适合YouTube）用于看只要gae可以访问的电影的电影，使用无限制电影appid，保证你畅快的电影享受，提供自动更新功能。<a href="https://github.com/greatagent2/wp/archive/master.zip">github下载</a></li>
    <li>greatagent2-<b>esr</b>--使用secure-goagent系列版本构建，抗封锁能力较强，速度较慢（适合用于看网页，上facebook，twitter，google+等），提供自动更新功能。本版本为经典版本，速度十分可观，所以除了进行流量升级之外，很少会进行软件上的升级了。<a href="https://github.com/greatagent2/esr/archive/master.zip">github下载</a></li>
  </ul>
========================
<h3>使用提示</h3>
  <ul>
    <li>温馨提醒：GreatAgent2系列的noFirefox版本已经改名为Standalone版本，请用户注意选择版本下载</li>
    <li>好消息：greatagent2当前可以提供FireFox、Chrome、Opera、Maxthon(遨游浏览器)版本和独立(Standalone)版本，当然FireFox版本将继续是主要维护版本。</li>
    <li>GreatAgent2-GA版本和GreatAgent2-ESR版本已经启用强制加密传输（RSA + RC4加密），给用户更安全的体验（不会影响到速度）</li>
    <li>chrome 出现证书错误警告的话， 可以通过添加 --ignore-certificate-errors</li> <li>启动参数忽略证书错误，也可以使用downloads中的firefox代替。</li>
    <li>强烈推荐大家使用开源的firefox浏览器，拥抱自由的互联网。</li>
    <li>请各位电影族使用greatagent2-wp，内置专1210个用电影id，可以看任何电影。</li>
    <li>请参考：https://code.google.com/p/greatagent/wiki/proxymyini</li>
  </ul>
============================
<h3>使用帮助</h3>
  <ul>
    <li>greatagent2-ga傻瓜式教程：https://code.google.com/p/greatagent/wiki/greatagent2ga</li>
    <li>greatagent2-wp傻瓜式教程：https://code.google.com/p/greatagent/wiki/greatagent2wp</li>
    <li>greatagent2-esr傻瓜式教程：https://code.google.com/p/greatagent/wiki/greatagent2esr</li>
  </ul>
==========================

<h2>公共服务端说明</h2>

  <font color="#F08080"><a name="帮助同胞翻越长城："></a>帮助同胞翻越长城：<a href="/p/greatagent/wiki/DonateAppid">捐赠Appid</a><a href="#帮助同胞翻越长城：" class="section_anchor"></a></font>

<h3>剩余流量查询：</h3>

greatagent-ga流量查询:https://greatagent-ga.appspot.com/page/greatagent-ga
greatagent-wp流量查询:https://greatagent-wp.appspot.com/page/greatagent-wp

<h2>备注</h2>
请各位多多堆广本项目，大家使用的好才是项目发展的动力
<ul>
<li>出现server is update 说明您的客户端程序更新了，请各位重新启动客户端程序，等待自动更新(可能会需要等待一段时间，使服务器保持同步)。</li>
<li>刚刚启动是无法链接正常，程序需要自动更新，寻找可用服务端。</li>
<li>当遇到反复循环刷新Appid时，请确定是循环刷新(就是同一个Appid在程序输出中输出了一遍又一遍，不是同一个Appid就不是循环刷新)，一般的刷新是正常的，循环刷新表示当天流量已经用尽，需要等待北京时间下午4点重置流量之后使用(请关闭程序后再打开)</li>
<li>欢迎大家到Issues中提出意见</li>
<li>刚开启时无法连接，因为刚开启时greatagent会逐一寻找可用的服务端</li>
<li>发现360系列软件会严重干扰本程序运行，请各位用户使用本项目产品时务必停止使用所有360产品(因为360会监视你的一举一动并发送给网警部门，小心被请喝茶)
(注：如果你的安全要求很高，请全部用国外的杀毒和防火墙，如：用小红伞代替360杀毒，用ZoneAlarm、Comodo代替一切国内防火墙！)</li>
</ul>

<h3>项目主页</h3>
<ul>
<li>主项目地址：<a href="https://code.google.com/p/greatagent/">greatagent</a></li>
<li>备份项目地址1：<a href="https://code.google.com/p/greatagent-ga/">greatagent-ga</a></li>
<li>备份项目地址2：<a href="https://code.google.com/p/greatagent-wp/">greatagent-wp</a></li>
</ul>
<h3>源代码</h3>
<ul>
<li><a href="https://github.com/greatagent/ga" rel="nofollow">https://github.com/greatagent/ga</a></li>
<li><a href="https://github.com/greatagent/wp" rel="nofollow">https://github.com/greatagent/wp</a></li>
<li><a href="https://github.com/greatagent2/ga" rel="nofollow">https://github.com/greatagent2/ga</a></li>
<li><a href="https://github.com/greatagent2/wp" rel="nofollow">https://github.com/greatagent2/wp</a></li>
</ul>
