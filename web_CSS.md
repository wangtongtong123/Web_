###1、CSS选择符有哪些？那些属性可以继承？优先级算法如何计算？CSS3新增伪类选择器有哪些？
  （1）、id选择器（#myid）   （2）、类选择器（.myclassname） （3）、标签选择器（div,h1,p）</br>
  （4）、相邻选择器（h1 + p）（5）、子选择器（ul<li）   （6）、后代选择器（li  a） </br>
  （7）、通配符选择器（ * ） （8）、属性选择器（a[rel = "external"]） </br>
  （9）、伪类选择器（a: hover,li:nth - child）</br>
  
  可继承的样式： font-size font-family color,UL LI DL DD DT;</br>
  不可继承的样式：border padding margin width height；</br>
  优先级就近原则，同权重情况下样式定义最近者为准;</br>
  载入样式以最后载入的定位为准;</br>
  
  优先级权重的顺序为：
  !important > id > class > tag important比内联优先级高
  
 
###2、CSS3新增伪类举例：
  p:first-of-type 选择属于其父元素的首个元素的每个元素。</br>
  p:last-of-type 选择属于其父元素的最后元素的每个元素。</br>
  p:inly-of-type 选择属于其父元素的唯一元素的每个元素。</br>
  p:only-child 选择属于其父元素的唯一子元素的每个元素。</br>
  p:nth-child(2) 选择属于其父元素的第二个子元素的每个元素。</br>
  :enabled : disabled 控制表单控件的禁用状态。</br>
  :checked 单选框或复选框被选中。</br>
  

###3、如何居中DIV？如何居中一个浮动元素?
  给div设置一个框度，然后给div添加 margin:0 auto属性
  div{ width:200px; margin:0 auto;}
  
  居中一个浮动元素：
  
  我们可以先设置一个大盒子，给定一个宽高 ，例如宽500 高300以及外边局的数值，然后可以用position:relative;
  相对定位,设置一个 background-color:pink这样方便看效果 left:50% ; top: 50%;
  
  1.block像块元素一样显示、none像行内元素一样显示、inline-block像行元素一样显示，但其内容像块类型元素一样显示 、
  list-item像块类型元素一眼显示，并添加样式列表标记。</br>
  2.absolute 生成绝对定位的元素，相对于static定位以外的第一个父元素进行定位。</br>
   fixed(老IE不支持) 生成绝对定位的元素，相对于浏览器窗口进行定位。</br>
   relative 生成相对定位元素，相对于其正常位置进行定位。</br>
   static默认值没有定位，元素出现在正常流中 *(忽略 top,bottom,left,right z-index 声明)。</br>
   inherit 规定从父元素继承position属性的值。
   
  
###4、为什么要初始化CSS样式？
    因为浏览器存在兼容性问题，不同浏览器对有些标签的默认值是不同的，如果没对CSS样式初始化往往会出现浏览器之间的页面
  差异。除此之外，初始化也会对SEO有一定的影响，但是鱼与熊掌不可兼得，所以只能力求在影响最小的情况下初始化，最简单的
  方法就是： * {padding: 0 ;margin: 0;}

