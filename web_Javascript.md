###1、javascript的typeof返回那些数据类型
    Object number function booleanunderfind
###2、例举3种强制类型转换和2种隐式类型转换？
    强制（parseInt,parseFloat,number）
    隐式（== 、 ===）
    
###3、split()join()的区别
     split是切割成数组的形式，join是将数组转换成字符串
  
###4、数组方法pop() push() unshift() shift()
      Push()尾部添加 pop()尾部删除
      Unshift()头部添加 shift()头部删除
      
###5、事件绑定和普通事件有什么区别？
     事件绑定就是针对DOM元素的事件，绑定在DOM元素上
     普通事件即为非针对DOM元素的事件
     
###6、IE和DOM事件流的区别
     1）、执行顺序不一样
     2）、参数不一样
     3）、事件加不加 on
     4）、this指向问题
     
###7、IE和标准下有哪些兼容性的写法？
     Varev = ev || window.event
     
       document.documentElement.clientWidth ||
     document.body.clintWidth
     
     Var target = ev.srcElement||ev.target
     
###8、call和apply的区别
     Object.call（this,obj1,obj2,obj3）
     Object.apply(this,atguments)
     
###9、事件委托是什么？
     事件委托就是利用冒泡的原理，把事件加到父级上，触发执行效果。
     优点就是提高性能。
     
###10、闭包是什么，有什么特性，对页面有什么影响？
      闭包：闭包是指可以包含自由比那量的代码块；这些变量不是在这个代码块内部或者任何全局上下文中
      定义的，而是在定义代码快的环境中定义。
      特性：在函数内部再定义一个函数，内部函数使用了外部函数的变量，并且在外部函数最后将内部函数作为结果
           返回，当外部函数执行结束后，外部函数内之前被使用的局部变量不会被释放。
      影响：由于闭包时，变量的值都保存到内存中，会导致页面加载时内存消耗很大，IE的话会导致内在泄漏，因此
           尽量少用或用时要及时删除。
           
###11、如何阻止事件冒泡和默认事件？
     阻止冒泡事件用cancelBubble事件对象，用return false阻止默认事件。
     
###12、添加删除替换插入到某个节点的方法
    obj.appenfChild()
    obj.innersetBefore
    obj.replaceChild
    obj.removeChild

###13、javascript的本地对象，内置对象和宿主对象？
      本地对象为 array objregexp等可以 new实例化
      内置对象为 gload Math 等不可以实例化的
      宿主为浏览器自带的 document,window等
      
###14、document.onload和document ready的qubie
     document.onload 是在结构和样式加载完才执行js
     document.ready原声种没有这个方法，jquery中有$().ready(function)
     
###15、”==“和”===“的不同
      前者会自动转换类型 后者不会
      前者是判断 后者是绝对等于
      
###16、javascript的同源策略
     一段脚本只能读取来自于同一来源的窗口和文档的属性，这里的同一来源指的是主机名、协议和端口号的组合
     
###17、编写一个数组去重的方法
     function oSort(arr)
     {
     var result = {};
     varneweArr = [];
     for(vari = 0; i<arr.length; i ++)
     {
     if(!result[arr])
     {
     newArr.push(arr)
     result[arr]=1
     }
     }
     return newArr
     }
     </arr.length;i++>
     
