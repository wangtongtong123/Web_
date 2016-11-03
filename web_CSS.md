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
     因为浏览器存在兼容性问题，不同浏览器对有些标签的默认值是不同的，如果没对CSS样式初始化往往会出现浏览器之间的
   页面差异。除此之外，初始化也会对SEO有一定的影响，但是鱼与熊掌不可兼得，所以只能力求在影响最小的情况下初始化，
   最简单的方法就是： * {padding: 0 ;margin: 0;}


###5、absolute的containing block计算方式跟正常流有什么不同？

###6、position跟display'margin collapse overflow'float这些特性相互叠加会怎样?

###7、对BFC规范的理解？
    BFC叫做k=块级格式化上下文，我们可以说BFC是一个页面上隔离的独立容器，容器里的子元素不会影响到外
    面的元素。反之也是如此。BFC的区域不会与float boxchongdie。BFC和常规的块级元素一样，默认垂直方向排列。
    
###8、CSS定义的权重？
    以下是权重规则：
       标签的权重为1，
       class的权重为10，
       id的权重为100，如果权重相同，则最后定义的样式会起作用。
    
###9、解释下浮动和它的工作原理？以及清除浮动的技巧？
    浮动就是使元素脱离正常的文档流并使其移动到其父元素的“最左边”或“最右边”
    工作原理：当浮动元素碰到包含它的边框或者浮动元素的边框时它就会停止
    清除浮动的技巧：由于浮动引起了一些问题，所以要解决它，我们得知道它出现了什么问题：
    1）：父元素的高度无法被撑开，影响与父元素同级的元素
    2）：与浮动元素同级的非浮动元素（内联元素）会跟随其后
    3）：如若不是第一个浮动元素浮动，则该元素之前的元素也需要浮动，否则会影响页面显示的结构
    如果想解决2),3)的问题，那么就使用CSS中clear:both属性来清除元素的浮动就可以解决
    如果遇到1）的问题那么我们就给clearfix样式：
         .clearfix:after{content:".";display:block;height:0;clear:both;visiblity:hidden;}
         .clearfic{display:inline-block;}
         
     清除浮动的几种方法：
     1]，额外标签法，它的缺点就是因为增加了额外标签使HTNL的结构看起来不整洁。
     2]，使用after伪类：
     #parent:after{
     content:".";
     height:0;
     visibility:block;
     clear:both;
     }
     
     3],设置‘overflow’为‘hidden’或者auto.
     
 
###10、CSS3有哪些新特性？
     CSS3实现圆角（border-radius）、阴影（box-shadow）、对文字加特效（text-shadow）
     线性渐变（gradient）、旋转（transform） transform:rotate(deg) scale(0.0,0.0)
     translate(px,px) skew(deg,deg)它增加了旋转，缩放，定位，倾斜  增加了更多的CSS选
     择器，和更多的背景 rgba
     
###11、经常遇到的CSS的兼容性问题有哪些？原因是什么？解决方法是什么？
     例如:网页背景半透明、清除浮动、浮动IE6双边距、文字大小和行高不兼容、img下的留白、图片和文字同行等。
     原因：不同浏览器内核和不同浏览器版本对网页代码的解析不一致。
     解决方法：
     
###12、介绍一下CSS的盒子模型？
      （1）有两种，IE盒子模型、标准W3C盒子模型：IE的content部分包含了border和padding;
      （2）盒模型：内容（content）、填充（padding）、边界（margin）、边框（border).
      
###13、CSS的基本语句构成是？
选择器{属性 1：值 1；属性 2：值 2；......}

###14、前端页面有哪三层构成，分别是什么？作用是什么？
   结构层 HTML 表示层 CSS 行为层 js</br>
   结构层：</br>
   由HTML或XHTML之类的标记语言负责创建。标签，也就是那些出现在尖括号里的单词，对网页内容的语义含义
   做出了描述，但这些标签不包含于如何显示有关内容的信息。</br>
   表示层：</br>
   由CSS负责创建。CSS对"如何显示有关内容"的问题做出了解答。</br>
   行为层：</br>
   负责回答”内容应该如何对事件作出反应“这一问题。这是Javascript语言和DOM主宰的领域。</br>
      
###15、对WEB及W3C的理解与认识？
    标签闭合、标签小写、不乱嵌套、提高搜索机器人搜索几率、使用外链CSS和js脚本、结构行为表现的分离、
   文件下载与页面速度更快、内容能被更多的用户以及设备所访问、更少的代码和组件，容易维护、改版方便，
   不需要变动页面内容、提供打印版本而不需要复制内容。
   
