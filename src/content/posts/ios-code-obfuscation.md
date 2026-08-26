---
title: "iOS代码混淆"
description: "这是iOS代码混淆教程"
pubDate: 2023-04-01
category: "技术"
tags: ["博客"]
highlight: true
---
<p>这是iOS代码混淆教程</p>

<h3 id="iOS代码混淆"><a href="#iOS代码混淆" class="headerlink" title="iOS代码混淆"></a>iOS代码混淆</h3><h4 id="一-苹果审核机制原理"><a href="#一-苹果审核机制原理" class="headerlink" title="一. 苹果审核机制原理"></a>一. 苹果审核机制原理</h4><ol>
<li><p>预审核扫描api，及plist文件字符缺失等；此处分两步，第一步为上传时苹果Application Loador等应用对于适配icon等的检查，第二步为上传后苹果的功能性检查，例如配置了Push功能但有缺失或者未打开功能，则会邮件提示等等;</p>
</li>
<li><p>机审此处扫描支付SDK等，及马甲情况，机器扫描主要看代码块，可参考百度蜘蛛抓取网站模块原理；如遇部分无法过机审情况可尝试加速绕过机审（不是100%成功）;</p>
</li>
<li><p>人工审核此处主要检测功能或者App体验测试，例如用测试账号登录App体验功能，或其他是否明显bug等，ipv6也在此处检测；</p>
</li>
</ol>
<h4 id="二-混淆过审的核心"><a href="#二-混淆过审的核心" class="headerlink" title="二. 混淆过审的核心"></a>二. 混淆过审的核心</h4><p>1.ipa包特征：包括有代码相似性，资源相似性；代码相似性解决办法：</p>
<ul>
<li>已有代码的混淆（改类名、改函数名、改文件名、改工程名）</li>
<li>添加一些无用的代码</li>
</ul>
<p>资源相似性解决办法：</p>
<ul>
<li>资源改名</li>
<li>适当添加一些无用的资源</li>
</ul>
<p>2.开发者帐号：</p>
<ul>
<li>马甲包尽量不要关联到同一个开发者帐号</li>
</ul>
<p>3.元数据配置相似性：</p>
<ul>
<li><p>针对收费产品，可以修改应用程序价格，打造与原产品不同的价格级别；</p>
</li>
<li><p>修改应用程序发布地区，打造与原产品不同的售卖地区或分不同地区运营；</p>
</li>
<li><p>修改产品分类，打造与原产品不同的产品侧重属性分类；</p>
</li>
</ul>
<h4 id="三-代码混淆"><a href="#三-代码混淆" class="headerlink" title="三. 代码混淆"></a>三. 代码混淆</h4><p> <strong>使用工具 <a href="https://github.com/klaus01/KLGenerateSpamCode" target="_blank" rel="noopener">https://github.com/klaus01/KLGenerateSpamCode</a></strong></p>
<p><strong>详细使用教程</strong>🔽🔽🔽</p>
<hr>
<h1 id="KLGenerateSpamCode-垃圾代码生成器"><a href="#KLGenerateSpamCode-垃圾代码生成器" class="headerlink" title="KLGenerateSpamCode 垃圾代码生成器"></a>KLGenerateSpamCode 垃圾代码生成器</h1><p>本工具用于应对苹果对重复应用的审核（Guideline 4.3 Design Spam），避免苹果机审检测概率。</p>
<h2 id="主要功能"><a href="#主要功能" class="headerlink" title="主要功能"></a>主要功能</h2><ol>
<li>修改工程名</li>
<li>修改类名前缀</li>
<li>扫描工程中的代码，生成同等数量的 Category 文件，文件中及是同等方法数量的垃圾代码。</li>
<li>修改 xxx.xcassets 文件夹中的 png 资源文件名。</li>
<li>删除代码中的所有注释和空行。</li>
</ol>
<h2 id="使用"><a href="#使用" class="headerlink" title="使用"></a>使用</h2><h3 id="使用源码"><a href="#使用源码" class="headerlink" title="使用源码"></a>使用源码</h3><ol>
<li>下载源码。</li>
<li>用 Xcode 打开工程并配置参数。如图<a href="https://github.com/klaus01/KLGenerateSpamCode/raw/master/images/p2.png" target="_blank" rel="noopener"><img src="/2023/04/01/iOS代码混淆/1.png" alt="配置参数"></a></li>
<li>运行</li>
</ol>
<h3 id="参数说明"><a href="#参数说明" class="headerlink" title="参数说明"></a>参数说明</h3><ul>
<li><em>(必填)</em> <strong>源码文件夹绝对路径</strong>（如：<code>/Users/kelei/Documents/work/git/projectName/source</code>）</li>
<li><strong>-modifyProjectName [原名称]&gt;[新名称]</strong> 修改工程名。程序会修改<code>原名称-Swift.h</code>、<code>Podfile</code>、<code>原名称-Bridging-Header.h</code>、<code>源码文件夹绝对路径</code>、<code>原名称.xcodeproj</code>和<code>原名称.xcworkspace</code>的名称和内容。<em><code>Podfile</code>被修改后需要手动<code>pod install</code></em></li>
<li><strong>-modifyClassNamePrefix [工程文件 xcodeproj 绝对路径] [原前缀]&gt;[新前缀]</strong> 修改源代码类名前缀。程序会扫描<code>源码文件夹绝对路径</code>下的 .h .swift 文件，修改文件名，修改使用该类名的代码，修改<code>工程文件</code>中的文件名。文件名有<code>原前缀</code>的会修改成<code>新前缀</code>，如：<code>原前缀ViewController</code>变成<code>新前缀ViewController</code>；没有<code>原前缀</code>的会增加<code>新前缀</code>，如：<code>ViewController</code>变成<code>新前缀ViewController</code>。</li>
<li><strong>-spamCodeOut [垃圾代码文件输出目录] [垃圾代码方法增加的参数名]</strong> 生成垃圾代码。程序会扫描<code>源码文件夹绝对路径</code>下的 .m .swift 文件中的类和方法，并生成<code>category</code>和<code>extension</code>文件，文件中的方法是在代码原方法的基础上增加<code>垃圾代码方法增加的参数名</code>参数。如：<code>-spamCodeOut /dir AppLog</code>，会将<code>- (void)setupKeys {}</code>生成为<code>+ (BOOL)setupKeysAppLog:(NSInteger)AppLog { return AppLog % 20 == 0; }</code>，会将<code>- (void)foo:(NSString *)str {}</code>生成为<code>+ (BOOL)fooAppLog:(NSInteger)AppLog { return AppLog % 23 == 0; }</code></li>
<li><strong>-ignoreDirNames [忽略文件夹名称字符串]</strong> 忽略这些文件夹，对<code>-modifyClassNamePrefix</code>、<code>-spamCodeOut</code>和<code>-deleteComments</code>参数有效。目前只会忽略<code>源码文件夹绝对路径</code>下一级的这些目录。如：<code>/p/s -ignoreDirNames categorys</code>，那么<code>/p/s/categorys</code>会被忽略，但<code>/p/s/viewControllers/categorys</code>不会忽略。</li>
<li><strong>-handleXcassets</strong> 修改<code>xxx.xcassets</code>文件夹中的 png 资源文件名，同时也<code>Contents.json</code>文件中的关联名称，不会影响代码中使用图片。</li>
<li><strong>-deleteComments</strong> 删除工程目录下 .h .m .swift 文件中的注释和空行。</li>
</ul>
<h2 id="另外修改图片-hash-值的方法"><a href="#另外修改图片-hash-值的方法" class="headerlink" title="另外修改图片 hash 值的方法"></a>另外修改图片 hash 值的方法</h2><p>使用 <a href="http://www.imagemagick.org/" target="_blank" rel="noopener">ImageMagick</a> 对 png 图片做轻量压缩，及不损失图片质量，又可改变图片文件 hash 值。方法：</p>
<ol>
<li>安装 ImageMagick，<code>brew install imagemagick</code></li>
<li>压缩工程目录下所有 png 文件，<code>find . -iname &quot;*.png&quot; -exec echo {} \; -exec convert {} {} \;</code></li>
</ol>
<h2 id="使用经验"><a href="#使用经验" class="headerlink" title="使用经验"></a>使用经验</h2><p>就我 2017-11 月的提交情况来看，只需要做如下修改就可以上马甲包了。</p>
<ol>
<li>修改工程名</li>
<li>修改类名前缀</li>
<li>修改图片文件 Hash 值</li>
<li>修改 .xcassets 中的图片文件名</li>
<li>用别的电脑打包</li>
</ol>
<h2 id="已知问题"><a href="#已知问题" class="headerlink" title="已知问题"></a>已知问题</h2><ul>
<li>生成的垃圾代码文件可能是 .m 文件中实现的私有类，编译垃圾代码可能会报错，删除该垃圾代码 .h .m 文件及可。</li>
</ul>
<h3 id="原文地址"><a href="#原文地址" class="headerlink" title="原文地址"></a><a href="https://blog.csdn.net/MakerCloud/article/details/81006467?spm=1001.2101.3001.6650.9&amp;utm_medium=distribute.pc_relevant.none-task-blog-2~default~BlogCommendFromBaidu~Rate-9-81006467-blog-128713056.nonecase&amp;depth_1-utm_source=distribute.pc_relevant.none-task-blog-2~default~BlogCommendFromBaidu~Rate-9-81006467-blog-128713056.nonecase&amp;utm_relevant_index=15" target="_blank" rel="noopener">原文地址</a></h3>
      
    </div>
