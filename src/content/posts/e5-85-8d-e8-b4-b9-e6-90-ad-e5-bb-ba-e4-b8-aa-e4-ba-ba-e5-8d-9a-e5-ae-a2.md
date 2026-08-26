---
title: "免费搭建个人博客"
description: "倒腾了2天算是把小窝安顿下来了,下面我就傻瓜式地讲解:如何免费搭建自己的博客. (HEXO + Github + Mac) 阅读全文 »"
pubDate: 2018-02-03
category: "前端"
tags: ["博客"]
---
<p>倒腾了2天算是把小窝安顿下来了,下面我就傻瓜式地讲解:如何免费搭建自己的博客.<br>(HEXO + Github + Mac)<br><br>在开始之前先弄清楚几个概念,因为毕竟我(们)是小白.</p>
<h3 id="相关概念"><a href="#相关概念" class="headerlink" title="相关概念"></a>相关概念</h3><h4 id="Hexo是什么"><a href="#Hexo是什么" class="headerlink" title="Hexo是什么"></a>Hexo是什么</h4><blockquote>
<p><a href="https://www.cnblogs.com/mophy/p/7016331.html" target="_blank" rel="noopener">Hexo</a>一款博客框架,一款支持<a href="https://baike.baidu.com/item/markdown/3245829?fr=aladdin" target="_blank" rel="noopener">Markdown</a>的可拓展性框架.(简而言之,写博客只需要编辑.md文件,Hexo帮你解释成HTML前端页面)</p>
</blockquote>
<h4 id="Markdown是什么"><a href="#Markdown是什么" class="headerlink" title="Markdown是什么"></a>Markdown是什么</h4><blockquote>
<p>一种可以使用普通文本编辑器编写的标记语言，通过简单的标记语法，它可以使普通文本内容具有一定的格式。(Markdown有自己的语法,按照语法进行博客编辑即可)</p>
</blockquote>
<h4 id="Github是什么"><a href="#Github是什么" class="headerlink" title="Github是什么"></a>Github是什么</h4><blockquote>
<p>软件项目的托管平台.(这里我们需要将hexo搭建的博客部署到github,这样别人就能访问了)</p>
</blockquote>
<hr>
<p><strong>在开始之前,你需要一个账号,去<a href="https://github.com" target="_blank" rel="noopener">https://github.com</a>注册一个自己的github账号吧,开启新世界的大门.<br>那么,下面我们开始:</strong></p>
<h3 id="配置环境"><a href="#配置环境" class="headerlink" title="配置环境"></a>配置环境</h3><h4 id="1-安装Node-必须"><a href="#1-安装Node-必须" class="headerlink" title="1.安装Node(必须)"></a>1.安装Node(必须)</h4><blockquote>
<p>作用：用来生成静态页面的. 到Node.js<a href="https://nodejs.org/en/" target="_blank" rel="noopener">官网</a>下载相应平台的最新版本，一路安装即可。</p>
</blockquote>
<h4 id="2-安装Git-必须"><a href="#2-安装Git-必须" class="headerlink" title="2.安装Git(必须)"></a>2.安装Git(必须)</h4><blockquote>
<p>如果你有xcode那么恭喜你已经安装好Git.如果没有,那么去<a href="https://git-scm.com/book/zh/v1/起步-安装-Git" target="_blank" rel="noopener">Git安装教程</a>.(Git是免费、开源的分布式版本控制系,svn是经典的集中式版本控制系统).</p>
</blockquote>
<h4 id="3-正式安装HEXO"><a href="#3-正式安装HEXO" class="headerlink" title="3.正式安装HEXO"></a>3.正式安装HEXO</h4><blockquote>
<p>Node和Git都安装好后，可执行如下命令安装hexo :(打开终端直接输入)</p>
</blockquote>
<figure class="highlight plain"><table><tr><td class="gutter"><pre><span class="line">1</span><br></pre></td><td class="code"><pre><span class="line">$ sudo npm install -g hexo</span><br></pre></td></tr></table></figure>
<hr>
<h3 id="创建本地博客"><a href="#创建本地博客" class="headerlink" title="创建本地博客"></a>创建本地博客</h3><p>上面已经安装好必要的环境配置,下面开始创建你的博客.</p>
<h4 id="1-初始化"><a href="#1-初始化" class="headerlink" title="1.初始化"></a>1.初始化</h4><p>创建一个文件夹，如：Blog，cd到Blog里执行hexo init的。命令：<br><figure class="highlight plain"><table><tr><td class="gutter"><pre><span class="line">1</span><br></pre></td><td class="code"><pre><span class="line">hexo init</span><br></pre></td></tr></table></figure></p>
<p>那么,恭喜你,你的本地博客至此已经创建好了.(纳尼😱?)<br>是的没错,可是,我的本地博客在哪里呢?闲话少说,我们继续~~</p>
<h4 id="2-生成静态页面"><a href="#2-生成静态页面" class="headerlink" title="2.生成静态页面"></a>2.生成静态页面</h4><p>打开终端,cd到你的Blog目录下,执行如下命令:<br><figure class="highlight plain"><table><tr><td class="gutter"><pre><span class="line">1</span><br></pre></td><td class="code"><pre><span class="line">hexo generate （hexo g  也可以）</span><br></pre></td></tr></table></figure></p>
<h4 id="3-本地启动"><a href="#3-本地启动" class="headerlink" title="3.本地启动"></a>3.本地启动</h4><p>仍然在你的Blog目录下.<br>启动本地服务，进行文章预览调试,执行如下命令:</p>
<figure class="highlight plain"><table><tr><td class="gutter"><pre><span class="line">1</span><br></pre></td><td class="code"><pre><span class="line">hexo server</span><br></pre></td></tr></table></figure>
<p>浏览器输入<a href="http://localhost:4000" target="_blank" rel="noopener">http://localhost:4000</a>(这就是你的本地博客了~~)<br>虽然很简陋，但好歹有了一个属于自己的小窝了。本地已经简单的设置好了，但是现在域名和服务器都是基于自己的电脑，接下来需要跟github进行关联。</p>
<hr>
<h3 id="配置Github"><a href="#配置Github" class="headerlink" title="配置Github"></a>配置Github</h3><h4 id="1-建立Repository"><a href="#1-建立Repository" class="headerlink" title="1.建立Repository"></a>1.建立Repository</h4><p>建立与你用户名对应的仓库，仓库名必须为【your_user_name.github.io】，固定写法 (your_user_name 替换成你的  Github账户的 username)</p>
<h4 id="2-和本地建立关联"><a href="#2-和本地建立关联" class="headerlink" title="2.和本地建立关联"></a>2.和本地建立关联</h4><p>然后建立关联，终端cd到你的Blog目录下,文件有以下：</p>
<blockquote>
<p>Blog<br>｜<br>｜－－ _config.yml<br>｜－－ node_modules<br>｜－－ public<br>｜－－ source<br>｜－－ db.json<br>｜－－ package.json<br>｜－－ scaffolds<br>｜－－ themes </p>
</blockquote>
<p>现在我们需要_config.yml文件，来建立关联，双击打开该文件,并翻到最下面，增加如下配置:(注意： : 后面要有空格.切记切记!!!这里曾经坑了我)</p>
<figure class="highlight plain"><table><tr><td class="gutter"><pre><span class="line">1</span><br><span class="line">2</span><br><span class="line">3</span><br><span class="line">4</span><br></pre></td><td class="code"><pre><span class="line">deploy:</span><br><span class="line">type: git</span><br><span class="line">repository: https://github.com/leopardpan/leopardpan.github.io.git</span><br><span class="line">branch: master</span><br></pre></td></tr></table></figure>
<p>修改完成后记得保存_config.yml文件.</p>
<h4 id="3-将本地Blog部署到Git"><a href="#3-将本地Blog部署到Git" class="headerlink" title="3.将本地Blog部署到Git"></a>3.将本地Blog部署到Git</h4><p>然后执行如下命令才能使用git部署:</p>
<figure class="highlight plain"><table><tr><td class="gutter"><pre><span class="line">1</span><br></pre></td><td class="code"><pre><span class="line">npm install hexo-deployer-git --save</span><br></pre></td></tr></table></figure>
<p>最后,执行部署命令:<br><figure class="highlight plain"><table><tr><td class="gutter"><pre><span class="line">1</span><br></pre></td><td class="code"><pre><span class="line">hexo deploy</span><br></pre></td></tr></table></figure></p>
<p>至此,你的本地Blog已经部署到git了,然后在浏览器中输入<a href="http://your_username.github.io/" target="_blank" rel="noopener">http://your_username.github.io/</a>就行了<br>(your_username替换成你的Github账户名).</p>
<p>每次部署的步骤，可按以下三步来进行。<br><figure class="highlight plain"><table><tr><td class="gutter"><pre><span class="line">1</span><br><span class="line">2</span><br><span class="line">3</span><br><span class="line">4</span><br></pre></td><td class="code"><pre><span class="line">nvm use v13.14.0</span><br><span class="line">hexo clean</span><br><span class="line">hexo generate</span><br><span class="line">hexo deploy</span><br></pre></td></tr></table></figure></p>
<h3 id="写在最后"><a href="#写在最后" class="headerlink" title="写在最后"></a>写在最后</h3><p>这里为了避免混淆,并没有介绍如何发布博客,修改主题等等配置相关的部分.</p>
<hr>
<h3 id="Tips"><a href="#Tips" class="headerlink" title="Tips"></a>Tips</h3><p>Hexo语法与使用 官网:<a href="https://hexo.io" target="_blank" rel="noopener">https://hexo.io</a><br>Markdown 基本语法 <a href="https://www.zybuluo.com/mdeditor?url=https://www.zybuluo.com/static/editor/md-help.markdown" target="_blank" rel="noopener">Cmd Markdown 简明语法手册</a><br>Windows10搭建Hexo: 简书 <a href="https://www.jianshu.com/p/3f2fe426edff" target="_blank" rel="noopener">https://www.jianshu.com/p/3f2fe426edff</a><br>本文内容源自:简书 <a href="https://www.jianshu.com/p/465830080ea9" target="_blank" rel="noopener">https://www.jianshu.com/p/465830080ea9</a></p>


    </div>
