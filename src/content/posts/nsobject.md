---
title: "iOS 对象原理"
description: "关于 NSobject 阅读全文 »"
pubDate: 2020-08-18
category: "iOS"
tags: ["方法总结"]
---
<h1 id="关于-NSobject"><a href="#关于-NSobject" class="headerlink" title="关于 NSobject"></a>关于 NSobject</h1>
<p>NSobject-&gt; A -&gt; B</p>
<figure class="highlight plain"><table><tr><td class="gutter"><pre><span class="line">1</span><br><span class="line">2</span><br><span class="line">3</span><br></pre></td><td class="code"><pre><span class="line">struct NSObject_IMPL &#123;</span><br><span class="line">    ``Class isa; ``// 8个字节</span><br><span class="line">&#125;;</span><br></pre></td></tr></table></figure>
<figure class="highlight plain"><table><tr><td class="gutter"><pre><span class="line">1</span><br><span class="line">2</span><br><span class="line">3</span><br><span class="line">4</span><br><span class="line">5</span><br></pre></td><td class="code"><pre><span class="line">@``interface` `A : NSObject</span><br><span class="line">&#123;</span><br><span class="line">    ``int` `_no;</span><br><span class="line">    ``int` `_age;</span><br><span class="line">&#125;</span><br></pre></td></tr></table></figure>
<figure class="highlight plain"><table><tr><td class="gutter"><pre><span class="line">1</span><br><span class="line">2</span><br><span class="line">3</span><br><span class="line">4</span><br><span class="line">5</span><br></pre></td><td class="code"><pre><span class="line">struct A &#123;</span><br><span class="line">    ``Class NSObject_IMP NSObject_IVARS;</span><br><span class="line">    ``int` `_no;</span><br><span class="line">    ``int` `_age;</span><br><span class="line">&#125;;</span><br></pre></td></tr></table></figure>
<figure class="highlight plain"><table><tr><td class="gutter"><pre><span class="line">1</span><br><span class="line">2</span><br><span class="line">3</span><br><span class="line">4</span><br><span class="line">5</span><br></pre></td><td class="code"><pre><span class="line">struct A &#123;</span><br><span class="line">    ``Class isa;</span><br><span class="line">    ``int` `_no;</span><br><span class="line">    ``int` `_age;</span><br><span class="line">&#125;;</span><br></pre></td></tr></table></figure>
<figure class="highlight plain"><table><tr><td class="gutter"><pre><span class="line">1</span><br><span class="line">2</span><br><span class="line">3</span><br><span class="line">4</span><br><span class="line">5</span><br><span class="line">6</span><br><span class="line">7</span><br><span class="line">8</span><br><span class="line">9</span><br><span class="line">10</span><br><span class="line">11</span><br><span class="line">12</span><br><span class="line">13</span><br><span class="line">14</span><br><span class="line">15</span><br></pre></td><td class="code"><pre><span class="line">@``interface` `B : A</span><br><span class="line">&#123;</span><br><span class="line">    ``int` `_birthday;</span><br><span class="line">&#125;</span><br><span class="line">struct B &#123;</span><br><span class="line">    ``Class NSObject_IMP NSObject_IVARS;</span><br><span class="line">    ``int` `_no;</span><br><span class="line">    ``int` `_age;</span><br><span class="line">&#125;;</span><br><span class="line">struct B &#123;</span><br><span class="line">    ``Class isa;   (Class NSObject_IMP) </span><br><span class="line">    ``int` `_no;   (NSObject_IVARS)</span><br><span class="line">    ``int` `_age;  (NSObject_IVARS)</span><br><span class="line">    ``int` `_birthday;</span><br><span class="line">&#125;;</span><br></pre></td></tr></table></figure>
<p><img src="/legacy-assets/9eb0110fcd-1.png" alt="内存结构"></p>
<p><img src="/legacy-assets/ae9aa41df2-3.png" alt="官方解释图"></p>
<blockquote>
<ul>
<li><code>instance</code>的<code>isa</code>指向<code>class</code></li>
<li><code>class</code>的<code>isa</code>指向<code>meta-class</code></li>
<li><p><code>meta-class</code>的<code>isa</code>指向基类的<code>meta-class</code></p>
</li>
<li><p><code>class</code>的<code>superclass</code>指向父类的<code>class</code>，<strong>如果没有父类，superclass指针为nil</strong></p>
</li>
<li><code>meta-class</code>的<code>superclass</code>指向父类的<code>meta-class</code>,<strong>基类的meta-class的superclass指向基类的class</strong></li>
</ul>
<p>isa(of instance) –&gt; isa(of class) –&gt; isa(of meta-class)</p>
<p>面试题解答</p>
<ul>
<li>对象的isa指针指向哪里？</li>
</ul>
<ol>
<li><code>instance</code>对象的<code>isa</code>指针指向<code>class</code>对象</li>
<li><code>class</code>对象的<code>isa</code>指针指向<code>meta-class</code>对象</li>
<li><code>meta-class</code>对象的<code>isa</code>指针指向基类（也就是NSObject）的<code>meta-class</code>对象</li>
</ol>
<ul>
<li>OC的类信息存放在哪里？</li>
</ul>
<ol>
<li>对象方法，属性信息，成员变量信息，协议信息，存放在<code>class</code>对象中</li>
<li>类方法，存放在<code>meta-class</code>对象中</li>
<li>成员变量的具体值，存放在<code>instance</code>对象中</li>
</ol>
</blockquote>


    </div>
