---
title: "js原型链"
description: "关于 js 原型链的简单理解 阅读全文 »"
pubDate: 2019-02-13
category: "HTML"
tags: ["方法总结"]
---
<h3 id="关于-js-原型链的简单理解"><a href="#关于-js-原型链的简单理解" class="headerlink" title="关于 js 原型链的简单理解"></a>关于 js 原型链的简单理解</h3>
<h3 id="1、原型链设计的意义"><a href="#1、原型链设计的意义" class="headerlink" title="1、原型链设计的意义:"></a>1、原型链设计的意义:</h3><p><strong>为了实现 OO 编程中的继承. 顶层是 null , js 万物皆 Object,一些类似 api 的函数或者属性定义在 Object 的 prototype 中.</strong></p>
<blockquote>
<p>eg:<br>1.hasOwnProperty()<br>判断对象自身属性中是否具有指定的属性。<br>obj.hasOwnProperty(‘name’)</p>
<p>3.Object.assign(target,source1,source2,…)<br>该方法主要用于对象的合并，将源对象 source 的所有可枚举属性合并到目标对象 target 上,此方法只拷贝源对象的自身属性，不拷贝继承的属性。</p>
<p>4.Object.keys(obj)<br>返回一个由一个给定对象的自身可枚举属性组成的数组，数组中属性名的排列顺序和使用 for…in 循环遍历该对象时返回的顺序一致 （两者的主要区别是 一个 for-in 循环还会枚举其原型链上的属性）。</p>
</blockquote>
<h3 id="2、js-是如何实现继承："><a href="#2、js-是如何实现继承：" class="headerlink" title="2、js 是如何实现继承："></a>2、js 是如何实现继承：</h3><p><img src="/legacy-assets/dfa8da318d-js_explain.png" alt="你想输入的替代文字"></p>
<blockquote>
<p>1.对象有属性__proto__,指向对象的构造函数的原型对象.<br>2.函数除了有属性__proto__,还有属性 prototype，prototype 指向该方法的原型对象。<br>3.原型对象也有__proto__,指向原型对象的构造函数的原型对象.(这就是原型链!!!)<br>4.原型对象:包含构造函数,以及其他对象或者函数(共享的属性和方法).</p>
</blockquote>
<h3 id="3、proto-prototype-constructor-联系："><a href="#3、proto-prototype-constructor-联系：" class="headerlink" title="3、proto prototype constructor 联系："></a>3、proto prototype constructor 联系：</h3><figure class="highlight javascript"><table><tr><td class="gutter"><pre><span class="line">1</span><br><span class="line">2</span><br><span class="line">3</span><br><span class="line">4</span><br></pre></td><td class="code"><pre><span class="line"><span class="keyword">var</span> M = <span class="function"><span class="keyword">function</span> (<span class="params">name</span>) </span>&#123; <span class="keyword">this</span>.name = name; &#125; (即 <span class="keyword">constructor</span>)</span><br><span class="line">var a = new M('o1')</span><br><span class="line">a.__proto__ === M.prototype (都指向原型对象)</span><br><span class="line">M.prototype 包含 M .</span><br></pre></td></tr></table></figure>
<h3 id="4、instanceof-原理："><a href="#4、instanceof-原理：" class="headerlink" title="4、instanceof 原理："></a>4、instanceof 原理：</h3><p><img src="/legacy-assets/cd1313238d-js_instanceof.png" alt="你想输入的替代文字"></p>
<figure class="highlight javascript"><table><tr><td class="gutter"><pre><span class="line">1</span><br><span class="line">2</span><br><span class="line">3</span><br></pre></td><td class="code"><pre><span class="line"><span class="keyword">var</span> M = <span class="function"><span class="keyword">function</span> (<span class="params">name</span>) </span>&#123; <span class="keyword">this</span>.name = name; &#125;</span><br><span class="line"><span class="keyword">var</span> a = <span class="keyword">new</span> M(<span class="string">'o2'</span>)</span><br><span class="line">a.__proto__ === M.prototype <span class="comment">// instanceof 原理就是判断这个等式是否成立</span></span><br></pre></td></tr></table></figure>
<h3 id="5、原理图："><a href="#5、原理图：" class="headerlink" title="5、原理图："></a>5、原理图：</h3><p><img src="/legacy-assets/3f2d17ad67-1.jpeg" alt="你想输入的替代文字"></p>
<h3 id="Tips"><a href="#Tips" class="headerlink" title="Tips"></a>Tips</h3><p>1.原型链详解 简书: <a href="https://www.jianshu.com/p/dee9f8b14771" target="_blank" rel="noopener">链接</a><br>2.__proto__和 prototype 详解: <a href="https://www.cnblogs.com/fydxx/p/6656278.html" target="_blank" rel="noopener">链接</a></p>


    </div>
