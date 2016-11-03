###1、Doctype作用？严格模式与混杂模式如何区分？它们有和意义？
     （1）、声明位于文档中的最前面，处于标签之前。告知浏览器的解析器，用什么文档类型规范来接系这个文档。
     （2）、严格模式的排版和JS运作模式是以该浏览器支持的最高标准运行。
     （3）、在混杂模式中，页面以宽松的向后兼容的方式显示。模拟老式浏览器的行为以防止站点无法工作。
     （4）、DOCTYPE 不存在或格式不正确会导致文档以混杂模式呈现。
   
###2、行内元素有哪些？块级元素有哪些？
     （1）CSS规范规定，每个元素都有display属性，确定该元素的类型，每个元素都有默认display值,比如div
         默认display属性值为"block",成为"块级"元素;  span默认display属性值为"inline"，是"行内"元素。
     （2）行内元素有：a b span img input select strong  块级元素有：div ul ol li dl dt dd h1 h2 
                    h3 h4 ...p
     
###3、link和@import的区别是？
     （1）link属于XHTML标签，而@import是css提供的;
      (2)页面被加载时，link会同时被加载，而@import引用的CSS会等到页面被加载完再加载;
      (3)import只在IE5以上才能识别，而link是XHTML标签，无兼容问题;
      (4)link方式的样式的权重高于@import的权重。
      
###4、浏览器的内核分别是什么？
      IE浏览器的内核Trident、Mozilla的 Gecko、Chrome的Blink(Webkit的分支)、Opera 内核原为Presto, 现为Blink.
      
###5、HTML5有哪些新特性？如何处理HTML5新标签的浏览器兼容问题？如何区分HTML和HTML5？
      HTML5 现在已经不是SGML的子集，主要是关于图像，位置，存储，多任务等功能的增加。
      绘画canvas   用于媒介回放的video和audio元素    本地离线存储 localStorage 长期存储数据，浏览器关闭后数据不丢失；   
      sessionStorage的数据在浏览器关闭后自动删除  语义化更好的内容元素，比如article、footer、header、nav、section  
      表单控件，calendar、date、time、email、url、search
      
###6、对语义化如何理解？
      用正确的标签做正确的事情！
      HTML语义化就是让页面的内容结构化，便于对浏览器、搜索引擎解析；在没有CSS样式的情况下也一种文档格式显示，
      并且是容易阅读的。搜索引擎的爬虫依赖于标记来确定上下文和哥哥关键字的权重，利于SEO。使阅读源代码的人更容易将网站
      分块，便于阅读理解。
 
###7、HTML的离线存储有几种方式？
      localStorage长期存储数据。浏览器关闭后数据不丢失；sessionStorage数据在浏览器关闭后自动删除。
   
###8、Iframe有哪些缺点？
      iframe会阻塞页面的Onload事件;
      iframe和主页面共享连接池，而浏览器对相同域的连接有限制，所以会影响页面的并行加载。使用iframe之前需要
      考虑这两个缺点。如果需要使用iframe，最好是通过javascript动态给iframe添加src属性值，这样可以绕开以
      上两个问题。
  
###9、请描述一下cookles、sessionStorage和localStorage的区别？
       cookie在浏览器和服务器间来回传递。sessionStorage和localStorage不会。
       sessionStorage和localStorage的存储空间更大;
       sessionStorage和localStorage有更多丰富易用的接口;
       sessionStorage和localStorage有各自独立的存储空间。
