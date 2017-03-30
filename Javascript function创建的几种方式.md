Javascript函数的创建方式  
=======================
1.声明函数 
-----
最普通最标准的声明函数方法，包括函数名及函数体。
>>>>>function fn1(){}

2.创建匿名函数表达式 
-----
创建一个变量，这个变量的内容为一个函数
>>>>>var fn1=function (){}

3.创建具名函数表达式 
-------------
创建一个变量，内容为一个带有名称的函数
>>>>>var fn1=function xxcanghai(){};

****注意：具名函数表达式的函数名只能在创建函数内部使用     
即采用此种方法创建的函数在函数外层只能使用fn1不能使用xxcanghai的函数名。xxcanghai的命名只能在创建的函数内部使用 

4.Function构造函数 
------------
>>>>>let fn1 =  new Function('a','b','alert(a+b)')

****方法内只能传入字符串  Function F要大写

5.自执行函

--------
```js
    //传入参数  在最后写（）内直接传入
    (function (a) {
      alert(a);
    }) (5);
    
    (function fn1() {
      alert(1);
    }) ();
```

6.将方法作为一个对象
-------------------
```js
　　// 作为对象方法
    var obj = {
        funName:function(){
            alert('这个必须放在一个对象内部，放在外边会出错！');
        }
    }
    
    // 调用方法
    obj.funName();
```


7.构造函数中给对象添加方法，通常在构造函数中用到。
--------------
javascript中的每个对象都有prototype属性，Javascript中对象的prototype属性的解释是：返回对象类型原型的引用。

```js
    　// 给对象添加方法
    var funName = function(){}
    funName.prototype.myfun = function(){
        alert('这是在funName函数上的原始对象上加了一个myfun方法，构造函数中用到');
    }
    // 调用
    var funname = new funName();// 创建对象
    funname.myfun();
```
在给对象添加方法时可以用一下方式添加多个方法：

```js
　　// 给对象添加多个方法
    var funName = function(){}
    funName.prototype = {
        fun1:function(){
            alert('fun1');
        }
        ,fun2:function(){
            alert('fun2');
        }
    }
    // 调用
    var funname = new funName();// 创建对象
    funname.fun1();
    funname.fun2();
```
