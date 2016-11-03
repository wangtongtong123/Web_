###1、CSS定位方式有哪些？position属性的值有哪些？它们之间的区别是什么？
      定位方式以及属性值：position：relative；  position：absolute；
                       position：static；    position：fixed；  
       
      区别:relative： 不脱离文档流，参考自身静态位置通过top,botton,left,right,定位，并且可以通过z-index
                   进行层次分级。
          absolute： 脱离文档流，通过top,botton,left,right定位。选其最近的父级定位元素，当父级position
                   为static时，absolute元素将以body坐标原点进行定位，可以通过z-index进行层次分级。
          static： 没有特别的设定，遵循基本的定位规定，不能通过 z-index进行层次分级
          fixed：  固定定位，这里他所固定的对象是可视窗口而并非是body或是父级元素。可通过z-index进行层次分级
          
###2、函数的几种定义方法?
     functiona(){},
     var a = function(){}
     
###3、对象的定义方法？
    a = new Object(),a = {}
###4、类的定义方法（prototype）(继承)
     Var a = function(){}
     a.prototype = {}
     new a();
###5、this关键字的指向
     obj.foo() == obj         //方法调用模式，this指向obj
     
     foo() == window;         //函数调用模式，this指向window
     
     new obj.foo() == obj     //构造器调用模式，this指向新建立的对象
     
     foo.call(obj) == obj     //APPLY调用模式，this指向obj
        
