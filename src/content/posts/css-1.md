---
title: "CSS_1"
description: "CSS基础第一课. 阅读全文 »"
pubDate: 2018-02-06
category: "HTML"
tags: ["CSS"]
---
<p>CSS基础第一课.</p>

<hr>
<h1 id="课程目标"><a href="#课程目标" class="headerlink" title="课程目标:"></a>课程目标:</h1><blockquote>
<ol>
<li>学会使用CSS选择器</li>
<li>熟记CSS样式和外观属性</li>
<li>熟练掌握CSS各种选择器</li>
<li>熟练掌握CSS各种选择器</li>
<li>熟练掌握CSS三种显示模式</li>
<li>熟练掌握CSS背景属性</li>
<li>熟练掌握CSS三大特性</li>
<li>熟练掌握CSS盒子模型</li>
<li>熟练掌握CSS浮动</li>
<li>熟练掌握CSS定位</li>
<li>熟练掌握CSS高级技巧强化CSS</li>
</ol>
<hr>
</blockquote>
<h1 id="引入CSS样式表（书写位置、重要）"><a href="#引入CSS样式表（书写位置、重要）" class="headerlink" title="引入CSS样式表（书写位置、重要）"></a>引入CSS样式表（书写位置、重要）</h1><p>CSS可以写到那个位置？ 是不是一定写到html文件里面呢？</p>
<h2 id="行内式（内联样式）"><a href="#行内式（内联样式）" class="headerlink" title="行内式（内联样式）"></a>行内式（内联样式）</h2><p>是通过标签的style属性来设置元素的样式，其基本语法格式如下：</p>
<figure class="highlight plain"><table><tr><td class="gutter"><pre><span class="line">1</span><br></pre></td><td class="code"><pre><span class="line">&lt;标签名 style=&quot;属性1:属性值1; 属性2:属性值2; 属性3:属性值3;&quot;&gt; 内容 &lt;/标签名&gt;</span><br></pre></td></tr></table></figure>
<p>语法中style是标签的属性，实际上任何HTML标签都拥有style属性，用来设置行内式。其中属性和值的书写规范与CSS样式规则相同，行内式只对其所在的标签及嵌套在其中的子标签起作用。</p>
<h2 id="内部样式表（内嵌式）"><a href="#内部样式表（内嵌式）" class="headerlink" title="内部样式表（内嵌式）"></a>内部样式表（内嵌式）</h2><p>内嵌式是将CSS代码集中写在HTML文档的head头部标签中，并且用style标签定义，其基本语法格式如下：</p>
<figure class="highlight html"><table><tr><td class="gutter"><pre><span class="line">1</span><br><span class="line">2</span><br><span class="line">3</span><br><span class="line">4</span><br><span class="line">5</span><br></pre></td><td class="code"><pre><span class="line"><span class="tag">&lt;<span class="name">head</span>&gt;</span></span><br><span class="line"><span class="tag">&lt;<span class="name">style</span> <span class="attr">type</span>=<span class="string">"text/CSS"</span>&gt;</span><span class="undefined"></span></span><br><span class="line"><span class="undefined">    选择器 &#123;属性1:属性值1; 属性2:属性值2; 属性3:属性值3;&#125;</span></span><br><span class="line"><span class="undefined"></span><span class="tag">&lt;/<span class="name">style</span>&gt;</span></span><br><span class="line"><span class="tag">&lt;/<span class="name">head</span>&gt;</span></span><br></pre></td></tr></table></figure>
<p>语法中，style标签一般位于head标签中title标签之后，也可以把他放在HTML文档的任何地方。</p>
<h2 id="外部样式表（外链式）"><a href="#外部样式表（外链式）" class="headerlink" title="外部样式表（外链式）"></a>外部样式表（外链式）</h2><p>链入式是将所有的样式放在一个或多个以.CSS为扩展名的外部样式表文件中，通过link标签将外部样式表文件链接到HTML文档中，其基本语法格式如下：</p>
<figure class="highlight html"><table><tr><td class="gutter"><pre><span class="line">1</span><br><span class="line">2</span><br><span class="line">3</span><br></pre></td><td class="code"><pre><span class="line"><span class="tag">&lt;<span class="name">head</span>&gt;</span></span><br><span class="line">  <span class="tag">&lt;<span class="name">link</span> <span class="attr">href</span>=<span class="string">"CSS文件的路径"</span> <span class="attr">type</span>=<span class="string">"text/CSS"</span> <span class="attr">rel</span>=<span class="string">"stylesheet"</span> /&gt;</span></span><br><span class="line"><span class="tag">&lt;/<span class="name">head</span>&gt;</span></span><br></pre></td></tr></table></figure>
<p>注意：  link 是个单标签哦!!!</p>
<p>该语法中，link标签需要放在head头部标签中，并且必须指定link标签的三个属性，具体如下：</p>
<figure class="highlight plain"><table><tr><td class="gutter"><pre><span class="line">1</span><br><span class="line">2</span><br><span class="line">3</span><br></pre></td><td class="code"><pre><span class="line">href：定义所链接外部样式表文件的URL，可以是相对路径，也可以是绝对路径。</span><br><span class="line">type：定义所链接文档的类型，在这里需要指定为“text/CSS”，表示链接的外部文件为CSS样式表。</span><br><span class="line">rel：定义当前文档与被链接文档之间的关系，在这里需要指定为“stylesheet”，表示被链接的文档是一个样式表文件。</span><br></pre></td></tr></table></figure>
<h2 id="三种样式表总结"><a href="#三种样式表总结" class="headerlink" title="三种样式表总结"></a>三种样式表总结</h2><table>
<thead>
<tr>
<th>样式表</th>
<th>优点</th>
<th>缺点</th>
<th>使用情况</th>
<th>控制范围</th>
</tr>
</thead>
<tbody>
<tr>
<td>行内样式表</td>
<td>书写方便，权重高</td>
<td>没有实现样式和结构相分离</td>
<td>较少</td>
<td>控制一个标签（少）</td>
</tr>
<tr>
<td>内嵌样式表</td>
<td>部分结构和样式相分离</td>
<td>没有彻底分离</td>
<td>较多</td>
<td>控制一个页面（中）</td>
</tr>
<tr>
<td>外部样式表</td>
<td>完全实现结构和样式相分离</td>
<td>需要引入</td>
<td>最多，强烈推荐</td>
<td>控制整个站点（多）</td>
</tr>
</tbody>
</table>
<p># </p>
<h1 id="CSS字体样式属性"><a href="#CSS字体样式属性" class="headerlink" title="CSS字体样式属性"></a>CSS字体样式属性</h1><h2 id="font-size-字号大小"><a href="#font-size-字号大小" class="headerlink" title="font-size:字号大小"></a>font-size:字号大小</h2><p>font-size属性用于设置字号，该属性的值可以使用相对长度单位，也可以使用绝对长度单位。其中，相对长度单位比较常用，推荐使用像素单位px，绝对长度单位使用较少。具体如下：</p>
<p><img src="/2018/02/06/CSS-1/dd.png"></p>
<h2 id="font-family-字体库"><a href="#font-family-字体库" class="headerlink" title="font-family:字体库"></a>font-family:字体库</h2><p>font-family属性用于设置字体。网页中常用的字体有宋体、微软雅黑、黑体等，例如将网页中所有段落文本的字体设置为微软雅黑，可以使用如下CSS样式代码：</p>
<p>p{ font-family:”微软雅黑”;}</p>
<p>可以同时指定多个字体，中间以逗号隔开，表示如果浏览器不支持第一个字体，则会尝试下一个，直到找到合适的字体。</p>
<blockquote>
<p><img src="/2018/02/06/CSS-1/good.png">常用技巧：</p>
</blockquote>
<figure class="highlight plain"><table><tr><td class="gutter"><pre><span class="line">1</span><br><span class="line">2</span><br><span class="line">3</span><br><span class="line">4</span><br><span class="line">5</span><br><span class="line">6</span><br></pre></td><td class="code"><pre><span class="line">1. 现在网页中普遍使用14px。</span><br><span class="line">2. 尽量使用偶数的数字字号。ie6等老式浏览器支持奇数会有bug。</span><br><span class="line">3. 各种字体之间必须使用英文状态下的逗号隔开。</span><br><span class="line">4. 中文字体需要加英文状态下的引号，英文字体一般不需要加引号。当需要设置英文字体时，英文字体名必须位于中文字体名之前。</span><br><span class="line">5. 如果字体名中包含空格、#、$等符号，则该字体必须加英文状态下的单引号或双引号，例如font-family: &quot;Times New Roman&quot;;。</span><br><span class="line">6. 尽量使用系统默认字体，保证在任何用户的浏览器中都能正确显示。</span><br></pre></td></tr></table></figure>
<h2 id="CSS-Unicode字体（了解）"><a href="#CSS-Unicode字体（了解）" class="headerlink" title="CSS Unicode字体（了解）"></a>CSS Unicode字体（了解）</h2><p>在 CSS 中设置字体名称，直接写中文是可以的。但是在文件编码（GB2312、UTF-8 等）不匹配时会产生乱码的错误。xp 系统不支持 类似微软雅黑的中文。</p>
<p>方案一： 你可以使用英文来替代。 比如 font-family:”Microsoft Yahei”。</p>
<p>方案二： 在 CSS 直接使用 Unicode 编码来写字体名称可以避免这些错误。使用 Unicode 写中文字体名称，浏览器是可以正确的解析的。<br>font-family: “\5FAE\8F6F\96C5\9ED1”，表示设置字体为“微软雅黑”。</p>
<p><img src="/2018/02/06/CSS-1/shs.png"></p>
<table>
<thead>
<tr>
<th>字体名称</th>
<th>英文名称</th>
<th>Unicode 编码</th>
</tr>
</thead>
<tbody>
<tr>
<td>宋体</td>
<td>SimSun</td>
<td>\5B8B\4F53</td>
</tr>
<tr>
<td>新宋体</td>
<td>NSimSun</td>
<td>\65B0\5B8B\4F53</td>
</tr>
<tr>
<td>黑体</td>
<td>SimHei</td>
<td>\9ED1\4F53</td>
</tr>
<tr>
<td>微软雅黑</td>
<td>Microsoft YaHei</td>
<td>\5FAE\8F6F\96C5\9ED1</td>
</tr>
<tr>
<td>楷体_GB2312</td>
<td>KaiTi_GB2312</td>
<td>\6977\4F53_GB2312</td>
</tr>
<tr>
<td>隶书</td>
<td>L</td>
<td>\96B6\4E66</td>
</tr>
<tr>
<td>幼园</td>
<td>YouYuan</td>
<td>\5E7C\5706</td>
</tr>
<tr>
<td>华文细黑</td>
<td>STXihei</td>
<td>\534E\6587\7EC6\9ED1</td>
</tr>
<tr>
<td>细明体</td>
<td>MingLiU</td>
<td>\7EC6\660E\4F53</td>
</tr>
<tr>
<td>新细明体</td>
<td>PMingLiU</td>
<td>\65B0\7EC6\660E\4F53</td>
</tr>
</tbody>
</table>
<p>为了照顾不同电脑的字体安装问题，我们尽量只使用宋体和微软雅黑中文字体</p>
<h2 id="font-weight-字体粗细"><a href="#font-weight-字体粗细" class="headerlink" title="font-weight:字体粗细"></a>font-weight:字体粗细</h2><p>字体加粗除了用 b  和 strong 标签之外，可以使用CSS 来实现，但是CSS 是没有语义的。</p>
<figure class="highlight html"><table><tr><td class="gutter"><pre><span class="line">1</span><br></pre></td><td class="code"><pre><span class="line">font-weight属性用于定义字体的粗细，其可用属性值：normal、bold、bolder、lighter、100~900（100的整数倍）。</span><br></pre></td></tr></table></figure>
<p><img src="/2018/02/06/CSS-1/good.png">小技巧： </p>
 <figure class="highlight css"><table><tr><td class="gutter"><pre><span class="line">1</span><br></pre></td><td class="code"><pre><span class="line">数字 400 等价于 <span class="selector-tag">normal</span>，而 700 等价于 <span class="selector-tag">bold</span>。  但是我们更喜欢用英文来表示。</span><br></pre></td></tr></table></figure>
<h2 id="font-style-字体风格"><a href="#font-style-字体风格" class="headerlink" title="font-style:字体风格"></a>font-style:字体风格</h2><p>字体倾斜除了用 i  和 em 标签之外，可以使用CSS 来实现，但是CSS 是没有语义的。</p>
<p>font-style属性用于定义字体风格，如设置斜体、倾斜或正常字体，其可用属性值如下：</p>
<p>normal：默认值，浏览器会显示标准的字体样式。</p>
<p>italic：浏览器会显示斜体的字体样式。</p>
<p><img src="/2018/02/06/CSS-1/good.png">小技巧： </p>
 <figure class="highlight plain"><table><tr><td class="gutter"><pre><span class="line">1</span><br></pre></td><td class="code"><pre><span class="line">平时我们很少给文字加斜体，反而喜欢给斜体标签（em，i）改为普通模式。</span><br></pre></td></tr></table></figure>
<h2 id="font-综合设置字体样式-重点-连写"><a href="#font-综合设置字体样式-重点-连写" class="headerlink" title="font:综合设置字体样式 (重点)连写"></a>font:综合设置字体样式 (重点)连写</h2><p>font属性用于对字体样式进行综合设置，其基本语法格式如下：</p>
<figure class="highlight css"><table><tr><td class="gutter"><pre><span class="line">1</span><br><span class="line">2</span><br><span class="line">3</span><br></pre></td><td class="code"><pre><span class="line">选择器&#123;</span><br><span class="line">  <span class="attribute">font</span>: font-style  font-weight  font-size  font-family;</span><br><span class="line">&#125;</span><br></pre></td></tr></table></figure>
<figure class="highlight plain"><table><tr><td class="gutter"><pre><span class="line">1</span><br><span class="line">2</span><br><span class="line">3</span><br></pre></td><td class="code"><pre><span class="line">使用font属性时，必须按上面语法格式中的顺序书写，不能更换顺序，各个属性以空格隔开。</span><br><span class="line"></span><br><span class="line">注意：其中不需要设置的属性可以省略（取默认值），但必须保留font-size和font-family属性，否则font属性将不起作用。</span><br></pre></td></tr></table></figure>
<h1 id="开发者工具（chrome）"><a href="#开发者工具（chrome）" class="headerlink" title="开发者工具（chrome）"></a>开发者工具（chrome）</h1><p>此工具是我们的必备工具，以后代码出了问题，我们首先第一反应就是：</p>
<p>“按F12”或者是 “shift+ctrl+i”   打开 开发者工具。</p>
<p>菜单：   右击网页空白出—查看 </p>
<p><img src="/2018/02/06/CSS-1/chrome.png"></p>
<p><img src="/2018/02/06/CSS-1/good.png">小技巧：</p>
<ol>
<li>ctrl+滚轮 可以 放大开发者工具代码大小。</li>
<li>左边是HTML元素结构   右边是CSS样式。</li>
<li>右边CSS样式可以改动数值和颜色查看更改后效果。</li>
</ol>
<h1 id="选择器（重点）"><a href="#选择器（重点）" class="headerlink" title="选择器（重点）"></a>选择器（重点）</h1><p>要想将CSS样式应用于特定的HTML元素，首先需要找到该目标元素。在CSS中，执行这一任务的样式规则部分被称为选择器（选择符）。</p>
<p><img src="/2018/02/06/CSS-1/ax.png"></p>
<p>如上图所以，要把里面的小黄人分为2组，最快的方法怎办？  </p>
<p>很多， 比如 一只眼睛的一组，剩下的一组  </p>
<p>这就用到基础选择器组：</p>
<h1 id="基础选择器（掌握）"><a href="#基础选择器（掌握）" class="headerlink" title="基础选择器（掌握）"></a>基础选择器（掌握）</h1><h2 id="标签选择器（元素选择器）"><a href="#标签选择器（元素选择器）" class="headerlink" title="标签选择器（元素选择器）"></a>标签选择器（元素选择器）</h2><p>标签选择器是指用HTML标签名称作为选择器，按标签名称分类，为页面中某一类标签指定统一的CSS样式。其基本语法格式如下：</p>
<figure class="highlight plain"><table><tr><td class="gutter"><pre><span class="line">1</span><br></pre></td><td class="code"><pre><span class="line">标签名&#123;属性1:属性值1; 属性2:属性值2; 属性3:属性值3; &#125;</span><br></pre></td></tr></table></figure>
<p>标签选择器最大的优点是能快速为页面中同类型的标签统一样式，同时这也是他的缺点，不能设计差异化样式。</p>
<p>课堂案例：</p>
<p> 传智简介</p>
<h2 id="类选择器"><a href="#类选择器" class="headerlink" title="类选择器"></a>类选择器</h2><p>类选择器使用“.”（英文点号）进行标识，后面紧跟类名，其基本语法格式如下：</p>
<figure class="highlight plain"><table><tr><td class="gutter"><pre><span class="line">1</span><br></pre></td><td class="code"><pre><span class="line">.类名&#123;属性1:属性值1; 属性2:属性值2; 属性3:属性值3; &#125;</span><br></pre></td></tr></table></figure>
<figure class="highlight plain"><table><tr><td class="gutter"><pre><span class="line">1</span><br></pre></td><td class="code"><pre><span class="line">标签调用的时候用 class=“类名”  即可。</span><br></pre></td></tr></table></figure>
<p>类选择器最大的优势是可以为元素对象定义单独或相同的样式。</p>
<p><img src="/2018/02/06/CSS-1/good.png">猜谜底游戏：</p>
<p><img src="/2018/02/06/CSS-1/midi.png" width="450">   你猜？</p>
<p>命名规范：  见附件（Web前端开发规范手册.doc）</p>
<p>命名是我们通俗约定的，但是没有规定必须用这些常用的命名。</p>
<p>课堂案例：</p>
<p> <img src="/2018/02/06/CSS-1/go.png"></p>
<figure class="highlight html"><table><tr><td class="gutter"><pre><span class="line">1</span><br><span class="line">2</span><br><span class="line">3</span><br><span class="line">4</span><br><span class="line">5</span><br><span class="line">6</span><br><span class="line">7</span><br><span class="line">8</span><br><span class="line">9</span><br><span class="line">10</span><br><span class="line">11</span><br><span class="line">12</span><br><span class="line">13</span><br><span class="line">14</span><br><span class="line">15</span><br><span class="line">16</span><br><span class="line">17</span><br><span class="line">18</span><br><span class="line">19</span><br><span class="line">20</span><br><span class="line">21</span><br><span class="line">22</span><br><span class="line">23</span><br><span class="line">24</span><br><span class="line">25</span><br><span class="line">26</span><br><span class="line">27</span><br><span class="line">28</span><br></pre></td><td class="code"><pre><span class="line"><span class="tag">&lt;<span class="name">head</span>&gt;</span></span><br><span class="line">        <span class="tag">&lt;<span class="name">meta</span> <span class="attr">charset</span>=<span class="string">"utf-8"</span>&gt;</span></span><br><span class="line">        <span class="tag">&lt;<span class="name">style</span>&gt;</span><span class="undefined"></span></span><br><span class="line"><span class="undefined">        span &#123;</span></span><br><span class="line"><span class="undefined">        	font-size: 100px;</span></span><br><span class="line"><span class="undefined">        &#125;</span></span><br><span class="line"><span class="css">        <span class="selector-class">.blue</span> &#123;</span></span><br><span class="line"><span class="undefined">        	color: blue;</span></span><br><span class="line"><span class="undefined">        &#125;</span></span><br><span class="line"><span class="css">        <span class="selector-class">.red</span> &#123;</span></span><br><span class="line"><span class="undefined">        	color: red;</span></span><br><span class="line"><span class="undefined">        &#125;</span></span><br><span class="line"><span class="css">        <span class="selector-class">.orange</span> &#123;</span></span><br><span class="line"><span class="undefined">			color: orange;</span></span><br><span class="line"><span class="undefined">        &#125;</span></span><br><span class="line"><span class="css">		<span class="selector-class">.green</span> &#123;</span></span><br><span class="line"><span class="undefined">			color: green;</span></span><br><span class="line"><span class="undefined">		&#125;</span></span><br><span class="line"><span class="undefined">        </span><span class="tag">&lt;/<span class="name">style</span>&gt;</span></span><br><span class="line">    <span class="tag">&lt;/<span class="name">head</span>&gt;</span></span><br><span class="line">    <span class="tag">&lt;<span class="name">body</span>&gt;</span></span><br><span class="line">    	<span class="tag">&lt;<span class="name">span</span> <span class="attr">class</span>=<span class="string">"blue"</span>&gt;</span>G<span class="tag">&lt;/<span class="name">span</span>&gt;</span></span><br><span class="line">    	<span class="tag">&lt;<span class="name">span</span> <span class="attr">class</span>=<span class="string">"red"</span>&gt;</span>o<span class="tag">&lt;/<span class="name">span</span>&gt;</span></span><br><span class="line">    	<span class="tag">&lt;<span class="name">span</span> <span class="attr">class</span>=<span class="string">"orange"</span>&gt;</span>o<span class="tag">&lt;/<span class="name">span</span>&gt;</span></span><br><span class="line">    	<span class="tag">&lt;<span class="name">span</span> <span class="attr">class</span>=<span class="string">"blue"</span>&gt;</span>g<span class="tag">&lt;/<span class="name">span</span>&gt;</span></span><br><span class="line">    	<span class="tag">&lt;<span class="name">span</span> <span class="attr">class</span>=<span class="string">"green"</span>&gt;</span>l<span class="tag">&lt;/<span class="name">span</span>&gt;</span></span><br><span class="line">    	<span class="tag">&lt;<span class="name">span</span> <span class="attr">class</span>=<span class="string">"red"</span>&gt;</span>e<span class="tag">&lt;/<span class="name">span</span>&gt;</span></span><br><span class="line">    <span class="tag">&lt;/<span class="name">body</span>&gt;</span></span><br></pre></td></tr></table></figure>
<h2 id="多类名选择器"><a href="#多类名选择器" class="headerlink" title="多类名选择器"></a>多类名选择器</h2><p>我们可以给标签指定多个类名，从而达到更多的选择目的。</p>
<p><img src="/2018/02/06/CSS-1/lei.png"></p>
<p>注意：</p>
<figure class="highlight plain"><table><tr><td class="gutter"><pre><span class="line">1</span><br><span class="line">2</span><br></pre></td><td class="code"><pre><span class="line">1. 样式显示效果跟HTML元素中的类名先后顺序没有关系,受CSS样式书写的上下顺序有关。</span><br><span class="line">2. 各个类名中间用空格隔开。</span><br></pre></td></tr></table></figure>
<p>多类名选择器在后期布局比较复杂的情况下，还是较多使用的。</p>
<figure class="highlight html"><table><tr><td class="gutter"><pre><span class="line">1</span><br><span class="line">2</span><br><span class="line">3</span><br><span class="line">4</span><br></pre></td><td class="code"><pre><span class="line"><span class="tag">&lt;<span class="name">div</span> <span class="attr">class</span>=<span class="string">"pink fontWeight font20"</span>&gt;</span>亚瑟<span class="tag">&lt;/<span class="name">div</span>&gt;</span></span><br><span class="line"><span class="tag">&lt;<span class="name">div</span> <span class="attr">class</span>=<span class="string">"font20"</span>&gt;</span>刘备<span class="tag">&lt;/<span class="name">div</span>&gt;</span></span><br><span class="line"><span class="tag">&lt;<span class="name">div</span> <span class="attr">class</span>=<span class="string">"font14 pink"</span>&gt;</span>安其拉<span class="tag">&lt;/<span class="name">div</span>&gt;</span></span><br><span class="line"><span class="tag">&lt;<span class="name">div</span> <span class="attr">class</span>=<span class="string">"font14"</span>&gt;</span>貂蝉<span class="tag">&lt;/<span class="name">div</span>&gt;</span></span><br></pre></td></tr></table></figure>
<h2 id="id选择器"><a href="#id选择器" class="headerlink" title="id选择器"></a>id选择器</h2><p>id选择器使用“#”进行标识，后面紧跟id名，其基本语法格式如下：</p>
<figure class="highlight plain"><table><tr><td class="gutter"><pre><span class="line">1</span><br></pre></td><td class="code"><pre><span class="line">#id名&#123;属性1:属性值1; 属性2:属性值2; 属性3:属性值3; &#125;</span><br></pre></td></tr></table></figure>
<p>该语法中，id名即为HTML元素的id属性值，大多数HTML元素都可以定义id属性，元素的id值是唯一的，只能对应于文档中某一个具体的元素。</p>
<p>用法基本和类选择器相同。</p>
<h2 id="id选择器和类选择器区别"><a href="#id选择器和类选择器区别" class="headerlink" title="id选择器和类选择器区别"></a>id选择器和类选择器区别</h2><p>W3C标准规定，在同一个页面内，不允许有相同名字的id对象出现，但是允许相同名字的class。</p>
<p>类选择器（class） 好比人的名字，  是可以多次重复使用的， 比如  张伟  王伟  李伟  李娜</p>
<p>id选择器     好比人的身份证号码，  全中国是唯一的， 不得重复。 只能使用一次。</p>
<p><strong><em>id选择器和类选择器最大的不同在于 使用次数上。</em></strong></p>
<p><img src="/2018/02/06/CSS-1/zfb.jpg"></p>
<p>命名小技巧：</p>
<figure class="highlight plain"><table><tr><td class="gutter"><pre><span class="line">1</span><br><span class="line">2</span><br><span class="line">3</span><br><span class="line">4</span><br></pre></td><td class="code"><pre><span class="line">1.长名称或词组可以使用中横线-来为选择器命名。</span><br><span class="line">2.不建议使用“_”下划线来命名CSS选择器。</span><br><span class="line">3.建议使用有意义的英文来命名。</span><br><span class="line">例如：header，top，bottom，banner，logo，nav等</span><br></pre></td></tr></table></figure>
<p>​    输入的时候少按一个shift键;<br>　浏览器兼容问题 (比如使用<em>tips的选择器命名，在IE6是无效的)<br>　能良好区分JavaScript变量命名(JS变量命名是用“</em>”)</p>
<figure class="highlight plain"><table><tr><td class="gutter"><pre><span class="line">1</span><br></pre></td><td class="code"><pre><span class="line">3.不要纯数字、中文等命名， 尽量使用英文单词来表示。</span><br></pre></td></tr></table></figure>
<h2 id="通配符选择器"><a href="#通配符选择器" class="headerlink" title="通配符选择器"></a>通配符选择器</h2><p>通配符选择器用“*”号表 示，他是所有选择器中作用范围最广的，能匹配页面中所有的元素。其基本语法格式如下：</p>
<figure class="highlight plain"><table><tr><td class="gutter"><pre><span class="line">1</span><br></pre></td><td class="code"><pre><span class="line">* &#123; 属性1:属性值1; 属性2:属性值2; 属性3:属性值3; &#125;</span><br></pre></td></tr></table></figure>
<p>例如下面的代码，使用通配符选择器定义CSS样式，清除所有HTML标记的默认边距。</p>
<figure class="highlight css"><table><tr><td class="gutter"><pre><span class="line">1</span><br><span class="line">2</span><br><span class="line">3</span><br><span class="line">4</span><br></pre></td><td class="code"><pre><span class="line">* &#123;</span><br><span class="line">  <span class="attribute">margin</span>: <span class="number">0</span>;                    <span class="comment">/* 定义外边距*/</span></span><br><span class="line">  <span class="attribute">padding</span>: <span class="number">0</span>;                   <span class="comment">/* 定义内边距*/</span></span><br><span class="line">&#125;</span><br></pre></td></tr></table></figure>
<p>注意：</p>
<p>  这个通配符选择器，就像我们的电影明星中的梦中情人， 想想它就好了，但是它不会和你过日子。 </p>
<h1 id="CSS复合选择器（掌握）"><a href="#CSS复合选择器（掌握）" class="headerlink" title="CSS复合选择器（掌握）"></a>CSS复合选择器（掌握）</h1><h2 id="后代选择器（必须掌握）"><a href="#后代选择器（必须掌握）" class="headerlink" title="后代选择器（必须掌握）"></a>后代选择器（必须掌握）</h2><p>后代选择器又称为包含选择器，用来选择元素或元素组的后代，其写法就是把外层标签写在前面，内层标签写在后面，中间用空格分隔。当标签发生嵌套时，内层标签就成为外层标签的后代。</p>
<p><img src="/2018/02/06/CSS-1/hou.png"></p>
<p>子孙后代都可以这么选择。 或者说，它能选择任何包含在内 的标签。 </p>
<p><img src="/2018/02/06/CSS-1/li.png"></p>
<h2 id="子元素选择器，子代选择器"><a href="#子元素选择器，子代选择器" class="headerlink" title="子元素选择器，子代选择器"></a>子元素选择器，子代选择器</h2><p>子元素选择器只能选择作为某元素子元素的元素。其写法就是把父级标签写在前面，子级标签写在后面，中间跟一个 &gt; 进行连接，注意，符号左右两侧各保留一个空格。</p>
<p><img src="/2018/02/06/CSS-1/zi1.png"></p>
<p>白话：  这里的子 指的是 亲儿子  不包含孙子 重孙子之类。</p>
<figure class="highlight plain"><table><tr><td class="gutter"><pre><span class="line">1</span><br></pre></td><td class="code"><pre><span class="line">比如：  .demo &gt; h3 &#123;color: red;&#125;   说明  h3 一定是demo 亲儿子。  demo 元素包含着h3。</span><br></pre></td></tr></table></figure>
<p><img src="/2018/02/06/CSS-1/san.jpg"></p>
<p>复合选择器是由两个或多个基础选择器，通过不同的方式组合而成的,目的是为了可以选择更准确更精细的目标元素标签。</p>
<h2 id="交集选择器"><a href="#交集选择器" class="headerlink" title="交集选择器"></a>交集选择器</h2><p>交集选择器由多个选择器构成，其中第一个为标签选择器，第二个为class选择器，两个选择器之间不能有空格，如h3.special。</p>
<p><img src="/2018/02/06/CSS-1/jiao.png"></p>
<p><strong>记忆技巧：</strong></p>
<p>交集选择器 是 并且的意思。  即…又…的意思</p>
<figure class="highlight plain"><table><tr><td class="gutter"><pre><span class="line">1</span><br></pre></td><td class="code"><pre><span class="line">比如：   p.one   选择的是： 类名为 .one  的 段落标签。</span><br></pre></td></tr></table></figure>
<p>用的相对来说比较少，不太建议使用。</p>
<h2 id="并集选择器"><a href="#并集选择器" class="headerlink" title="并集选择器"></a>并集选择器</h2><p>并集选择器（CSS选择器分组）是各个选择器通过<strong style="color:#f00">逗号</strong>连接而成的，任何形式的选择器（包括标签选择器、class类选择器id选择器等），都可以作为并集选择器的一部分。如果某些选择器定义的样式完全相同，或部分相同，就可以利用并集选择器为它们定义相同的CSS样式。</p>
<p><img src="/2018/02/06/CSS-1/bing.png"></p>
<p>记忆技巧：</p>
<p>并集选择器  和 的意思，  就是说，只要逗号隔开的，所有选择器都会执行后面样式。</p>
<figure class="highlight plain"><table><tr><td class="gutter"><pre><span class="line">1</span><br></pre></td><td class="code"><pre><span class="line">比如  .one, p , #test &#123;color: #F00;&#125;  表示   .one 和 p  和 #test 这三个选择器都会执行颜色为红色。  通常用于集体声明。</span><br></pre></td></tr></table></figure>
<p><img src="/2018/02/06/CSS-1/hu.gif">  他和他，在一起， 在一起    一起的意思</p>
<h2 id="测试题"><a href="#测试题" class="headerlink" title="测试题"></a>测试题</h2><figure class="highlight html"><table><tr><td class="gutter"><pre><span class="line">1</span><br><span class="line">2</span><br><span class="line">3</span><br><span class="line">4</span><br><span class="line">5</span><br><span class="line">6</span><br><span class="line">7</span><br><span class="line">8</span><br><span class="line">9</span><br><span class="line">10</span><br><span class="line">11</span><br><span class="line">12</span><br><span class="line">13</span><br></pre></td><td class="code"><pre><span class="line"><span class="tag">&lt;<span class="name">div</span> <span class="attr">class</span>=<span class="string">"nav"</span>&gt;</span>    <span class="comment">&lt;!-- 主导航栏 --&gt;</span></span><br><span class="line">  <span class="tag">&lt;<span class="name">ul</span>&gt;</span></span><br><span class="line">    <span class="tag">&lt;<span class="name">li</span>&gt;</span>公司首页<span class="tag">&lt;/<span class="name">li</span>&gt;</span></span><br><span class="line">    <span class="tag">&lt;<span class="name">li</span>&gt;</span>公司简介<span class="tag">&lt;/<span class="name">li</span>&gt;</span></span><br><span class="line">    <span class="tag">&lt;<span class="name">li</span>&gt;</span>公司产品<span class="tag">&lt;/<span class="name">li</span>&gt;</span></span><br><span class="line">    <span class="tag">&lt;<span class="name">li</span>&gt;</span>联系我们<span class="tag">&lt;/<span class="name">li</span>&gt;</span></span><br><span class="line">  <span class="tag">&lt;/<span class="name">ul</span>&gt;</span></span><br><span class="line">  <span class="tag">&lt;<span class="name">div</span>&gt;</span> 收藏本站 <span class="tag">&lt;/<span class="name">div</span>&gt;</span></span><br><span class="line"><span class="tag">&lt;/<span class="name">div</span>&gt;</span></span><br><span class="line"><span class="tag">&lt;<span class="name">div</span> <span class="attr">class</span>=<span class="string">"sitenav"</span>&gt;</span>    <span class="comment">&lt;!-- 侧导航栏 --&gt;</span></span><br><span class="line">  <span class="tag">&lt;<span class="name">div</span> <span class="attr">class</span>=<span class="string">"site-l"</span>&gt;</span>左侧侧导航栏<span class="tag">&lt;/<span class="name">div</span>&gt;</span></span><br><span class="line">  <span class="tag">&lt;<span class="name">div</span> <span class="attr">class</span>=<span class="string">"site-r"</span>&gt;</span><span class="tag">&lt;<span class="name">a</span> <span class="attr">href</span>=<span class="string">"#"</span>&gt;</span>登录<span class="tag">&lt;/<span class="name">a</span>&gt;</span><span class="tag">&lt;/<span class="name">div</span>&gt;</span></span><br><span class="line"><span class="tag">&lt;/<span class="name">div</span>&gt;</span></span><br></pre></td></tr></table></figure>
<p>在不修改以上代码的前提下，完成以下任务：</p>
<ol>
<li><p>链接 登录 的颜色为红色。     </p>
</li>
<li><p>主导航栏里面的文字颜色为绿色。</p>
</li>
<li><p>主导航栏和侧导航栏里面文字都是20像素并且是楷体。</p>
</li>
<li><p>收藏本站  要求字体加粗。</p>
<p>​</p>
</li>
</ol>
<h2 id="伪类选择器"><a href="#伪类选择器" class="headerlink" title="伪类选择器"></a>伪类选择器</h2><p>  伪类选择器用于向某些选择器添加特殊的效果。比如给链接添加特殊效果， 比如可以选择 第1个，第n个元素。</p>
<figure class="highlight css"><table><tr><td class="gutter"><pre><span class="line">1</span><br></pre></td><td class="code"><pre><span class="line">为了和我们刚才学的类选择器相区别，  类选择器是一个点 比如 <span class="selector-class">.demo</span> &#123;&#125;   而我们的伪类 用 2个点 就是 冒号  比如  <span class="selector-pseudo">:link</span>&#123;&#125;</span><br></pre></td></tr></table></figure>
<h2 id="a链接伪类选择器"><a href="#a链接伪类选择器" class="headerlink" title="a链接伪类选择器"></a>a链接伪类选择器</h2><ul>
<li>:link      /<em> 未访问的链接 </em>/</li>
<li>:visited   /<em> 已访问的链接 </em>/</li>
<li>:hover     /<em> 鼠标移动到链接上 </em>/</li>
<li><p>:active    /<em> 选定的链接 </em>/</p>
<p> 注意写的时候，他们的顺序尽量不要颠倒  按照  lvha 的顺序。   love   hate  爱恨原则 记忆法 </p>
</li>
</ul>
<figure class="highlight css"><table><tr><td class="gutter"><pre><span class="line">1</span><br><span class="line">2</span><br><span class="line">3</span><br><span class="line">4</span><br><span class="line">5</span><br><span class="line">6</span><br><span class="line">7</span><br><span class="line">8</span><br></pre></td><td class="code"><pre><span class="line"><span class="selector-tag">a</span> &#123;   <span class="comment">/* a是标签选择器  所有的链接 */</span></span><br><span class="line">			<span class="attribute">font-weight</span>: <span class="number">700</span>;</span><br><span class="line">			<span class="attribute">font-size</span>: <span class="number">16px</span>;</span><br><span class="line">			<span class="attribute">color</span>: gray;</span><br><span class="line">		&#125;</span><br><span class="line"><span class="selector-tag">a</span><span class="selector-pseudo">:hover</span> &#123;   <span class="comment">/* :hover 是链接伪类选择器 鼠标经过 */</span></span><br><span class="line">			<span class="attribute">color</span>: red; <span class="comment">/*  鼠标经过的时候，由原来的 灰色 变成了红色 */</span></span><br><span class="line">&#125;</span><br></pre></td></tr></table></figure>
<h3 id="结构-位置-伪类选择器（CSS3"><a href="#结构-位置-伪类选择器（CSS3" class="headerlink" title="结构(位置)伪类选择器（CSS3)"></a>结构(位置)伪类选择器（CSS3)</h3><ul>
<li>:first-child :选取属于其父元素的首个子元素的指定选择器</li>
<li>:last-child :选取属于其父元素的最后一个子元素的指定选择器</li>
<li>:nth-child(n) ： 匹配属于其父元素的第 N 个子元素，不论元素的类型</li>
</ul>
<figure class="highlight css"><table><tr><td class="gutter"><pre><span class="line">1</span><br><span class="line">2</span><br><span class="line">3</span><br><span class="line">4</span><br><span class="line">5</span><br><span class="line">6</span><br><span class="line">7</span><br><span class="line">8</span><br><span class="line">9</span><br></pre></td><td class="code"><pre><span class="line"><span class="selector-tag">li</span><span class="selector-pseudo">:first-child</span> &#123; <span class="comment">/*  选择第一个孩子 */</span></span><br><span class="line">        		<span class="attribute">color</span>: pink; </span><br><span class="line">        	&#125;</span><br><span class="line"><span class="selector-tag">li</span><span class="selector-pseudo">:last-child</span> &#123;   <span class="comment">/* 最后一个孩子 */</span></span><br><span class="line">        		<span class="attribute">color</span>: purple;</span><br><span class="line">        	&#125;</span><br><span class="line"><span class="selector-tag">li</span><span class="selector-pseudo">:nth-child(4)</span> &#123;   <span class="comment">/* 选择第4个孩子  n  代表 第几个的意思 */</span> </span><br><span class="line">				<span class="attribute">color</span>: skyblue;</span><br><span class="line">        	&#125;</span><br></pre></td></tr></table></figure>
<h1 id="CSS注释"><a href="#CSS注释" class="headerlink" title="CSS注释"></a>CSS注释</h1><figure class="highlight plain"><table><tr><td class="gutter"><pre><span class="line">1</span><br></pre></td><td class="code"><pre><span class="line">CSS规则是使用     /*  需要注释的内容  */  进行注释的，即在需要注释的内容前使用 “/*” 标记开始注释，在内容的结尾使用 “*/”结束。</span><br></pre></td></tr></table></figure>
<p>   例如：</p>
<figure class="highlight css"><table><tr><td class="gutter"><pre><span class="line">1</span><br><span class="line">2</span><br><span class="line">3</span><br></pre></td><td class="code"><pre><span class="line"><span class="selector-tag">p</span> &#123;</span><br><span class="line">  <span class="attribute">font-size</span>: <span class="number">14px</span>;                 <span class="comment">/* 所有的字体是14像素大小*/</span></span><br><span class="line">&#125;</span><br></pre></td></tr></table></figure>


    </div>
