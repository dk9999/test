
<h1>Goagent</h1>
======================

注：这是只是一个方便国内用户使用的镜像，由我个人copy。

本镜像的目的，是测试依附于Github的网络传播自由，并为无法访问google code的墙内朋友提供一个替代方案。原网址请访问：https://code.google.com/p/goagent/

goagent 3.1.16 正式版下载 https://nodeload.github.com/goagent/goagent/legacy.zip/3.0

Github上的最新版下载：https://github.com/goagent/goagent/archive/3.0.zip

注：goagent需要自行部署GAE服务端，如果嫌麻烦，可以选择使用预设了公共服务端的<a href="https://github.com/dk9999/test/tree/master/g_ga/README.md">greatagent</a>项目。

=======================

 <p>
    goagent 3.1.16 正式版下载
    <a href="https://nodeload.github.com/goagent/goagent/legacy.zip/3.0" rel="nofollow">
        http://goo.gl/qFyRk
    </a>
</p>
<h2>
    <a name="公告">
    </a>
    公告
    <a href="#公告" class="section_anchor">
    </a>
</h2>
<blockquote>
    更新到最新版以后，google 仍然卡的用户，可以配置 [ipv4/hosts]www.google.com = google_cn 和 [ipv4/hosts]www.google.com.hk
    = google_cn
</blockquote>
<h2>
    <a name="最近更新">
    </a>
    最近更新
    <a href="#最近更新" class="section_anchor">
    </a>
</h2>
<ul>
    <li>
        <tt>
            [0605 否]
        </tt>
        2014-06-05 20:30 更新, 缩短 iplist 筛选时间。
    </li>
    <li>
        <tt>
            [0604 否]
        </tt>
        2014-06-04 22:40 更新, 使用新的 https 连接方式。（ps: 需要更长的iplist筛选时间）
    </li>
    <li>
        <tt>
            [0601 否]
        </tt>
        2014-06-01 21:20 更新, 修复 ipv6 环境 dns_resolve 的 too many values to unpack
        错误。
    </li>
    <li>
        <tt>
            [0601 否]
        </tt>
        2014-06-01 14:35 更新, 所有 google 系网站加入 fakehttps， 改善 google 网站访问性.
    </li>
    <li>
        <tt>
            [0531 否]
        </tt>
        2014-05-31 23:20 更新, 加入 www.google.com 到 fakehttps.
    </li>
    <li>
        <tt>
            [0531 否]
        </tt>
        2014-05-31 23:15 更新, 启用本地 dns 解析 iplist.
    </li>
</ul>
<h2>
    <a name="简易教程">
    </a>
    简易教程
    <a href="#简易教程" class="section_anchor">
    </a>
</h2>
<ul>
    <li>
        部署 goagent
    </li>
    <ol>
        <li>
            申请Google Appengine并创建appid。
        </li>
        <li>
            下载goagent最新版
            <a href="https://code.google.com/p/goagent/" rel="nofollow">
                https://code.google.com/p/goagent/
            </a>
        </li>
        <li>
            修改local\proxy.ini中的
            <tt>
                [gae]
            </tt>
            下的appid=你的appid(多appid请用|隔开)
        </li>
        <li>
            双击server\uploader.bat 开始上传, 成功后即可使用了(地址127.0.0.1:8087)
        </li>
        <ul>
            <li>
                MacOS/Linux 请在 Terminal 执行 cd server &amp;&amp; python uploader.zip
            </li>
        </ul>
    </ol>
    <li>
        使用 goagent
    </li>
    <ul>
        <li>
            Chrome请安装
            <a href="https://chrome.google.com/webstore/detail/dpplabbmogkhghncfbfdeeokoefdjegm"
            rel="nofollow">
                SwitchySharp
            </a>
            插件（拖放 SwitchySharp.crx 到扩展设置），然后导入 SwitchyOptions.bak
        </li>
        <li>
            Firefox请安装
            <a href="https://addons.mozilla.org/zh-cn/firefox/addon/foxyproxy-standard/"
            rel="nofollow">
                FoxyProxy
            </a>
            ，Firefox需要导入证书，方法请见
            <a href="/p/goagent/wiki/FAQ">
                FAQ
            </a>
        </li>
        <li>
            IE/Opera 用户请右击 goagent.exe 托盘图标设置 IE 代理。
        </li>
    </ul>
</ul>
<h2>
    <a name="图文教程">
    </a>
    图文教程
    <a href="#图文教程" class="section_anchor">
    </a>
</h2>
<ul>
    <li>
        <a href="https://github.com/dk9999/test/tree/master/ga/wiki/InstallGuide.md">
            本站镜像页面
        </a>
    </li>
    <li>
        <a href="https://code.google.com/p/goagent/wiki/InstallGuide" rel="nofollow">
            原始页面
        </a>
    </li>
</ul>
<h2>
    <a name="常见问题">
    </a>
    常见问题
    <a href="#常见问题" class="section_anchor">
    </a>
</h2>
<ul>
    <li>
        <a href="https://github.com/dk9999/test/tree/master/ga/wiki/FAQ.md">
            本站镜像页面
        </a>
    </li>
    <li>
        <a href="https://code.google.com/p/goagent/wiki/FAQ" rel="nofollow">
            https://code.google.com/p/goagent/wiki/FAQ
        </a>
    </li>
</ul>
<h2>
    <a name="配置介绍">
    </a>
    配置介绍
    <a href="#配置介绍" class="section_anchor">
    </a>
</h2>
<ul>
    <li>
        <a href="https://github.com/dk9999/test/tree/master/ga/wiki/ConfigIntroduce.md">
            本站镜像页面
        </a>
    </li>
    <li>
        <a href="https://code.google.com/p/goagent/wiki/ConfigIntroduce" rel="nofollow">
            https://code.google.com/p/goagent/wiki/ConfigIntroduce
        </a>
    </li>
</ul>
<h2>
    <a name="更新历史">
    </a>
    更新历史
    <a href="#更新历史" class="section_anchor">
    </a>
</h2>
<ul>
    <li>
        <a href="https://code.google.com/p/goagent/wiki/History" rel="nofollow">
            https://code.google.com/p/goagent/wiki/History
        </a>
    </li>
</ul>
<h2>
    <a name="贡献列表">
    </a>
    贡献列表
    <a href="#贡献列表" class="section_anchor">
    </a>
</h2>
<ul>
    <li>
        <a href="https://code.google.com/p/goagent/wiki/ContributorList" rel="nofollow">
            https://code.google.com/p/goagent/wiki/ContributorList
        </a>
    </li>
</ul>
