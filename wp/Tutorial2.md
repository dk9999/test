注：这是只是一个方便国内用户使用的镜像项目，由我个人copy。

本镜像项目的主页：https://github.com/dk9999/test

wallproxy的项目主页：https://code.google.com/p/wallproxy/

wallproxy项目主页的镜像：https://github.com/dk9999/test/tree/master/wp

本页面镜像自：https://code.google.com/p/wallproxy/wiki/Tutorial2

=============================


 <p></p><ul><ul><li><a href="#第一步：下载wallproxy，运行wallproxy">第一步：下载wallproxy，运行wallproxy</a></li><li><a href="#第二步：配置浏览器代理">第二步：配置浏览器代理</a></li><li><a href="#第三步：向浏览器导入证书">第三步：向浏览器导入证书</a></li><ul><li><a href="#配置方式一：_Firefox_+_WallProxy">配置方式一： Firefox + WallProxy</a></li><li><a href="#配置方式二：配合_Chrome_+_SwitchySharp_使用方法">配置方式二：配合 Chrome + SwitchySharp 使用方法</a></li><li><a href="#配置方式三：配合_Firefox_+_FoxyProxy_使用方法">配置方式三：配合 Firefox + FoxyProxy 使用方法</a></li><li><a href="#配置方式四：配合_Firefox_+_AutoProxy_使用方法">配置方式四：配合 Firefox + AutoProxy 使用方法</a></li></ul><li><a href="#第四步：申请GAE空间并创建新的的app_id（已有可�">第四步：申请GAE空间并创建新的的app_id（已有可跳过）</a></li><li><a href="#第五步：上传至Google_App_Engine应用">第五步：上传至Google App Engine应用</a></li><li><a href="#第六步：仔细阅读FAQ文档，成为_Wallproxy_高手">第六步：仔细阅读FAQ文档，成为 Wallproxy 高手</a></li></ul></ul> <hr><p></p><h2><a name="第一步：下载wallproxy，运行wallproxy"></a>第一步：下载wallproxy，运行wallproxy<a href="#第一步：下载wallproxy，运行wallproxy" class="section_anchor"></a></h2><ol><li>下载wallproxy并解压；最新地址：<a href="https://code.google.com/p/wallproxy/" rel="nofollow">https://code.google.com/p/wallproxy/</a> </li><li>运行local文件夹下<tt>WallProxy.exe</tt>或者Run.bat（非Windows用户运行startup.py，Windows若提示是否允许安装证书，请允许），可显示下图： </li><blockquote><img src="http://wallproxy.googlecode.com/git/wiki/Tutorial.files/image011.png"> 
</blockquote></ol><h2><a name="第二步：配置浏览器代理"></a>第二步：配置浏览器代理<a href="#第二步：配置浏览器代理" class="section_anchor"></a></h2><ol><li>设置代理地址127.0.0.1:8087；如需使用PAC，设置<a href="http://127.0.0.1:8086/proxy.pac" rel="nofollow">http://127.0.0.1:8086/proxy.pac</a>；如需使用<tt>SwitchySharp/AutoProxy</tt>等浏览器扩展（<tt>SwitchySharp用户可导入配置local\misc\SwitchyOptions.bak</tt>），见图文教程（如果使用GUI，GUI应该选择“禁用切换”）；如需使用智能代理（使无法使用PAC或扩展的程序也做到该走代理走代理，不该走就不走），设置127.0.0.1:8086为代理即可。 </li><li>导入<a href="http://127.0.0.1:8086/CA.crt" rel="nofollow">http://127.0.0.1:8086/CA.crt</a>为浏览器根证书可消除浏览器证书警告（cmd窗口提示时间与导入后查看到的时间相同基本就是导入成功了，升级版本时请保留cert目录，以免需要再次导入） </li><li>可通过<a href="http://127.0.0.1:8086" rel="nofollow">http://127.0.0.1:8086</a>或<a href="http://wallproxy" rel="nofollow">http://wallproxy</a>访问Web配置界面 </li><li>双击托盘图标，可出现控制台窗口，注意不要直接关闭该窗口，正确的方法是再次双击托盘图标来隐藏。 </li><blockquote><img src="http://wallproxy.googlecode.com/git/wiki/Tutorial.files/image012.jpg"> 
</blockquote><blockquote>FWD说明走了转发（没走代理或走了hosts规则，不消耗GAE流量），GAE说明走了GAE，PAAS说明走了PAAS(PHP)。 
</blockquote><li>托盘左键菜单用于配置代理，右键菜单配置程序。 </li><blockquote><img src="http://wallproxy.googlecode.com/git/wiki/Tutorial.files/image013.png"> 
</blockquote><ol><li>直接连接：强制浏览器不使用代理； </li><li>GAE代理：强制浏览器使用127.0.0.1:8087作为代理（除部分google网站外，大部分网站都走GAE）； </li><li>智能代理：强制浏览器使用127.0.0.1:8086作为代理，由wallproxy智能判断是否需要走GAE，如果直连失败，可自动改走GAE； </li><li>自动代理：由浏览器通过PAC判断是否需要走GAE，与智能代理相比性能损失小，但无法做到在直连失败时改走GAE； </li><li>禁用切换：强制IE不使用代理；以上4个选择在每次运行<tt>WallProxy.exe</tt>时都会去修改IE代理为所选择项，而选择“禁用切换”后下次运行不会对IE代理做任何修改。<strong>使用<tt>SwitchySharp/AutoProxy</tt>等浏览器扩展管理代理的用户，请选择此项</strong> 。 </li></ol><li>如果需要自定义这些菜单，可以选择“设置代理”菜单项： </li><blockquote><img src="http://wallproxy.googlecode.com/git/wiki/Tutorial.files/image014.png"> 
</blockquote><blockquote>勾选“退出时恢复无代理”可在退出<tt>WallProxy.exe</tt>时将IE代理修改为无代理，以免影响正常使用；勾选“禁用代理切换”效果类似于“禁用切换”菜单。 
如果使用如图所示的拨号上网方式，将连接名称填入上图“连接名称”，例如下图“连接 宽带连接”，将“宽带连接”填入即可。 
<blockquote><img src="http://wallproxy.googlecode.com/git/wiki/Tutorial.files/image015.jpg"> 
</blockquote></blockquote><li>打开浏览器输入：<a href="http://www.facebook.com" rel="nofollow">http://www.facebook.com</a>，并成功访问。  </li><blockquote><img src="http://wallproxy.googlecode.com/git/wiki/Tutorial.files/image016.jpg"> 
</blockquote><li>自定义代理规则，访问<a href="http://wallproxy/" rel="nofollow">http://wallproxy/</a>或者<a href="http://127.0.0.1:8086/" rel="nofollow">http://127.0.0.1:8086/</a>，再点击“自定义规则”，输入要走GAE的规则后保存即可： </li><blockquote><img src="http://wallproxy.googlecode.com/git/wiki/Tutorial.files/image017.jpg"> 
</blockquote></ol><h2><a name="第三步：向浏览器导入证书"></a>第三步：向浏览器导入证书<a href="#第三步：向浏览器导入证书" class="section_anchor"></a></h2><blockquote><h3><a name="配置方式一：_Firefox_+_WallProxy"></a>配置方式一：<tt>Firefox + WallProxy</tt><a href="#配置方式一：_Firefox_+_WallProxy" class="section_anchor"></a></h3>
<ol><li>使用系统代理 </li><blockquote><img src="http://wallproxy.googlecode.com/git/wiki/Tutorial.files/image019.jpg"> 
</blockquote><li>导入根证书 </li><blockquote><img src="http://wallproxy.googlecode.com/git/wiki/Tutorial.files/image020.jpg"> 
<img src="http://wallproxy.googlecode.com/git/wiki/Tutorial.files/image021.png"> 
</blockquote><li>检查导入是否正确（可选），时间相同，说明没有导错： </li><blockquote><img src="http://wallproxy.googlecode.com/git/wiki/Tutorial.files/image022.jpg"> 
<img src="http://wallproxy.googlecode.com/git/wiki/Tutorial.files/image023.jpg"> 
</blockquote></ol><h3><a name="配置方式二：配合_Chrome_+_SwitchySharp_使用方法"></a>配置方式二：配合<tt>Chrome + SwitchySharp</tt>使用方法<a href="#配置方式二：配合_Chrome_+_SwitchySharp_使用方法" class="section_anchor"></a></h3>
<blockquote><a href=""></a><strong>如果使用GUI，GUI左键菜单选择“禁用切换”</strong> ；按下图导入配置，之后“直接连接”、“GAE代理”、“智能代理”、“自动代理”作用与<tt>WallProxy.exe</tt>相同。 
<blockquote><img src="http://wallproxy.googlecode.com/git/wiki/Tutorial.files/image024.jpg"> 
<img src="http://wallproxy.googlecode.com/git/wiki/Tutorial.files/image025.png"> 
</blockquote></blockquote><h3><a name="配置方式三：配合_Firefox_+_FoxyProxy_使用方法"></a>配置方式三：配合<tt>Firefox + FoxyProxy</tt>使用方法<a href="#配置方式三：配合_Firefox_+_FoxyProxy_使用方法" class="section_anchor"></a></h3>
<blockquote><a href=""></a><strong>如果使用GUI，GUI左键菜单选择“禁用切换”</strong> ；如图所示依次添加“GAE代理”127.0.0.1:8087，“智能代理”127.0.0.1:8086，“自动代理”<a href="http://127.0.0.1:8086/proxy.pac" rel="nofollow">http://127.0.0.1:8086/proxy.pac</a>。 
<blockquote><img src="http://wallproxy.googlecode.com/git/wiki/Tutorial.files/image026.jpg"> 
<img src="http://wallproxy.googlecode.com/git/wiki/Tutorial.files/image027.jpg"> 
<img src="http://wallproxy.googlecode.com/git/wiki/Tutorial.files/image028.jpg"> 
</blockquote></blockquote><h3><a name="配置方式四：配合_Firefox_+_AutoProxy_使用方法"></a>配置方式四：配合<tt>Firefox + AutoProxy</tt>使用方法<a href="#配置方式四：配合_Firefox_+_AutoProxy_使用方法" class="section_anchor"></a></h3>
<blockquote><a href=""></a><strong>如果使用GUI，GUI左键菜单选择“禁用切换”</strong> ；相比之下<tt>AutoProxy</tt>是比个弱的代理扩展，如果找不到以下对话框从哪些菜单找出来，还是改用<tt>WallProxy.exe</tt>或者<tt>FoxyProxy</tt>吧。 
<blockquote><img src="http://wallproxy.googlecode.com/git/wiki/Tutorial.files/image029.png"> 
<img src="http://wallproxy.googlecode.com/git/wiki/Tutorial.files/image030.png"> 
<img src="http://wallproxy.googlecode.com/git/wiki/Tutorial.files/image031.png"> 
</blockquote></blockquote></blockquote><h2><a name="第四步：申请GAE空间并创建新的的app_id（已有可�"></a>第四步：申请GAE空间并创建新的的app_id（已有可跳过）<a href="#第四步：申请GAE空间并创建新的的app_id（已有可�" class="section_anchor"></a></h2><ul><li>因为上面操作均使用默认Appid，到默认Appid流量有限，所以要想获得流畅的用户体验，需要自行申请Appid </li></ul><ol><li>打开刚才配置好的浏览器浏览器，输入<a href="https://appengine.google.com/" rel="nofollow">https://appengine.google.com/</a>，输入gmail用户密码登入(如果没有gmail账号请前往<a href="https://accounts.google.com" rel="nofollow">https://accounts.google.com</a>注册)。 </li><blockquote><img src="http://wallproxy.googlecode.com/git/wiki/Tutorial.files/image001.jpg"> 
</blockquote><li>点击“Create an Application”。 </li><blockquote><img src="http://wallproxy.googlecode.com/git/wiki/Tutorial.files/image002.jpg"> 
</blockquote><li>申请GAE需要用手机认证，输入自己的手机号(也可以选择通过电话认证，方法类似)，注意前面需要写+86（如无法收到短信验证码，可尝试在+86后加一空格再输手机号）。 </li><blockquote><img src="http://wallproxy.googlecode.com/git/wiki/Tutorial.files/image003.jpg"> 
</blockquote><li>手机收到验证码后输入验证，验证成功后GAE申请完成。 </li><blockquote><img src="http://wallproxy.googlecode.com/git/wiki/Tutorial.files/image004.jpg"> 
</blockquote><li>创建新app_id，比如这里我使用了seoceshi，注意记下该app_id，后面还会再用到。至于app title,可填可不填。 </li><blockquote><img src="http://wallproxy.googlecode.com/git/wiki/Tutorial.files/image005.jpg"> 
</blockquote><li>填好以后进入下个页面，如下： 则表示成功。 </li><blockquote><img src="http://wallproxy.googlecode.com/git/wiki/Tutorial.files/image006.jpg"> 
</blockquote></ol><h2><a name="第五步：上传至Google_App_Engine应用"></a>第五步：上传至Google App Engine应用<a href="#第五步：上传至Google_App_Engine应用" class="section_anchor"></a></h2><ol><li>运行server文件夹下uploader.bat(非Windows用户运行uploader.py)，输入appid上传（一次只能上传同一个帐号下的appid，多appid用|分隔，提示Set Proxy时尽量输入1来提高上传成功率）； </li><blockquote><img src="http://wallproxy.googlecode.com/git/wiki/Tutorial.files/image007.png"> 
</blockquote><ol><li>如果出现如下提示，删除旧appid，重新申请新appid； </li><blockquote><img src="http://wallproxy.googlecode.com/git/wiki/Tutorial.files/image008.jpg"> 
</blockquote><li>如果出现如下提示，到<a href="https://www.google.com/settings/security" rel="nofollow">https://www.google.com/settings/security</a>停用“两步验证”；或者在<a href="https://accounts.google.com/b/0/IssuedAuthSubTokens" rel="nofollow">https://accounts.google.com/b/0/IssuedAuthSubTokens</a> 申请一个程序专用密码 使用这个密码来配合gmail账户上传部署服务器就好了。（账户不变，密码使用此专用密码） </li><blockquote><img src="http://wallproxy.googlecode.com/git/wiki/Tutorial.files/image009.jpg"> 
<blockquote>给新手解释，两步验证就是谷歌推出的进阶安全机制，给应用生成专属密码来访问你的账户，避免主密码被盗。 
</blockquote></blockquote><li>如果出现如下提示，说明在提示“Set proxy?”时选择了使用代理上传，若当时选择了1，请确保已经运行可以正常使用的wallproxy，若没有可用代理，请在提示“Set proxy?”时输入0或直接回车。 </li><blockquote><img src="http://wallproxy.googlecode.com/git/wiki/Tutorial.files/image010.jpg"> 
</blockquote></ol><li>访问<a href="http://127.0.0.1:8086/#proxy_ini" rel="nofollow">http://127.0.0.1:8086/#proxy_ini</a>，找到如下部分（56行左右）并修改appid = 后面为自己的appid，点右上角的“保存”； </li><pre class="prettyprint"><span class="pun">[</span><span class="pln">gae</span><span class="pun">]</span><span class="pln"><br></span><span class="pun">;是否启用</span><span class="pln">GAE</span><span class="pun">服务端</span><span class="pln"><br>enable </span><span class="pun">=</span><span class="pln"> </span><span class="lit">1</span><span class="pln"><br></span><span class="pun">;服务端</span><span class="pln">appid</span><span class="pun">（多个用|分隔，个数不限）</span><span class="pln"><br>appid </span><span class="pun">=</span><span class="pln"> appid1</span><span class="pun">|</span><span class="pln">appid2</span></pre><li>等待重启完毕，即可畅快使用wallproxy给你带来的一切了。 </li></ol><h2><a name="第六步：仔细阅读FAQ文档，成为_Wallproxy_高手"></a>第六步：仔细阅读FAQ文档，成为<tt>Wallproxy</tt>高手<a href="#第六步：仔细阅读FAQ文档，成为_Wallproxy_高手" class="section_anchor"></a></h2><ul><li><a href="https://code.google.com/p/wallproxy/wiki/FAQ" rel="nofollow">https://code.google.com/p/wallproxy/wiki/FAQ</a> </li></ul><hr><p>编写者：www.ehust，wwqgtxx </p>
