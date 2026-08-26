---
title: "golang环境搭建"
description: "golang 环境搭建步骤:(windows) 阅读全文 »"
pubDate: 2019-06-25
category: "Golang"
tags: ["资料"]
---
<h3 id="golang-环境搭建步骤-windows"><a href="#golang-环境搭建步骤-windows" class="headerlink" title="golang 环境搭建步骤:(windows)"></a>golang 环境搭建步骤:(windows)</h3>
<h4 id="一-安装-Go-语言-go1-7-1-windows-amd64-msi"><a href="#一-安装-Go-语言-go1-7-1-windows-amd64-msi" class="headerlink" title="一 .安装 Go 语言,go1.7.1.windows-amd64.msi"></a>一 .安装 Go 语言,go1.7.1.windows-amd64.msi</h4><blockquote>
<p>下载地址<a href="https://studygolang.com/dl" target="_blank" rel="noopener">https://studygolang.com/dl</a></p>
</blockquote>
<h4 id="二-Go-环境变量"><a href="#二-Go-环境变量" class="headerlink" title="二 .Go 环境变量:"></a>二 .Go 环境变量:</h4><p>1.安装 go 的时候，安装程序会自动把相关目录写到系统环境。但是如果是 zip 的安装，需要自己手动添加。</p>
<blockquote>
<p>主要配置以下几个：</p>
<ul>
<li>GOROOT：Go 安装后的根目录（例如：D:\Go），安装过程中会由安装程序自动写入系统环境变量中。(重点)</li>
<li>GOBIN：Go 的二进制文件存放目录（%GOROOT%\bin）</li>
<li>PATH：需要将 %GOBIN% 加在 PATH 变量的最后，方便在命令行下运行。</li>
</ul>
</blockquote>
<p>2.计算机-&gt;属性-&gt;高级系统设置-&gt;环境变量</p>
<blockquote>
<p>注意：</p>
<p>1.需要将 GOPATH 路径，手动写入到系统环境变量。(重点)</p>
<p>2.不要把 GOPATH 设置成 Go 的安装路径</p>
<p>3.你自己创建依赖的 package，也要放到 GOPATH 目录下，这样才能够被引用到。</p>
</blockquote>
<p><img src="/legacy-assets/f1fdeae5f7-go_environment.png" alt=""></p>
<h4 id="三-Go-工作空间-代码目录"><a href="#三-Go-工作空间-代码目录" class="headerlink" title="三 .Go 工作空间(代码目录):"></a>三 .Go 工作空间(代码目录):</h4><p>1.GOPATH : Go 的工作空间，就是我们的开发和依赖包的目录（eg： C:\Go1.2） ，此目录需要手动配置到系统环境变量</p>
<blockquote>
<p>GOPATH 工作空间是一个目录层次结构，其根目录包含三个子目录：</p>
<ul>
<li>src：包含 Go 源文件，注意：你自己创建依赖的 package，也要放到 GOPATH 目录下，这样才能够被引用到。</li>
<li>pkg：包含包对象，编译好的库文件</li>
<li>bin：包含可执行命令</li>
</ul>
</blockquote>
<p>2.工程如下:</p>
<p><img src="/legacy-assets/14a9e54985-go_src.png" alt=""></p>
<h4 id="四-验证-Go-是否安装成功"><a href="#四-验证-Go-是否安装成功" class="headerlink" title="四 .验证 Go 是否安装成功:"></a>四 .验证 Go 是否安装成功:</h4><p>打开 cmd 输入 go version:</p>
<p><img src="/legacy-assets/b453e122e0-go_command.png" alt="你想输入的替代文字"></p>
<p>如图,go 安装成功!</p>
<h4 id="五-安装-vsCode"><a href="#五-安装-vsCode" class="headerlink" title="五 .安装 vsCode"></a>五 .安装 vsCode</h4><blockquote>
<p><a href="https://code.visualstudio.com" target="_blank" rel="noopener">https://code.visualstudio.com</a></p>
</blockquote>
<h4 id="六-打开-VSCode-安装-Go-扩展"><a href="#六-打开-VSCode-安装-Go-扩展" class="headerlink" title="六 .打开 VSCode,安装 Go 扩展"></a>六 .打开 VSCode,安装 Go 扩展</h4><p><img src="/legacy-assets/006f75ef1a-go_extension.png" alt=""></p>
<h4 id="至此结束"><a href="#至此结束" class="headerlink" title="至此结束"></a>至此结束</h4><h3 id="相关资料"><a href="#相关资料" class="headerlink" title="相关资料:"></a>相关资料:</h3><blockquote>
<p>1.学习资料: <a href="https://github.com/Unknwon/the-way-to-go_ZH_CN/blob/master/eBook/directory.md" target="_blank" rel="noopener">https://github.com/Unknwon/the-way-to-go_ZH_CN/blob/master/eBook/directory.md</a></p>
<p>2.golang 中文网: <a href="https://studygolang.com" target="_blank" rel="noopener">https://studygolang.com</a></p>
</blockquote>


    </div>
