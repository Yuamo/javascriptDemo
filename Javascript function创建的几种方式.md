Javascript�����Ĵ�����ʽ  
=======================
1.�������� 
-----
����ͨ���׼���������������������������������塣
>>>>>function fn1(){}

2.���������������ʽ 
-----
����һ���������������������Ϊһ������
>>>>>var fn1=function (){}

3.���������������ʽ 
-------------
����һ������������Ϊһ���������Ƶĺ���
>>>>>var fn1=function xxcanghai(){};

****ע�⣺�����������ʽ�ĺ�����ֻ���ڴ��������ڲ�ʹ��     
�����ô��ַ��������ĺ����ں������ֻ��ʹ��fn1����ʹ��xxcanghai�ĺ�������xxcanghai������ֻ���ڴ����ĺ����ڲ�ʹ�� 

4.Function���캯�� 
------------
>>>>>let fn1 =  new Function('a','b','alert(a+b)')

****������ֻ�ܴ����ַ���  Function FҪ��д

5.��ִ�к�

--------
```js
    //�������  �����д������ֱ�Ӵ���
    (function (a) {
      alert(a);
    }) (5);
    
    (function fn1() {
      alert(1);
    }) ();
```

6.��������Ϊһ������
-------------------
```js
����// ��Ϊ���󷽷�
    var obj = {
        funName:function(){
            alert('����������һ�������ڲ���������߻����');
        }
    }
    
    // ���÷���
    obj.funName();
```


7.���캯���и�������ӷ�����ͨ���ڹ��캯�����õ���
--------------
javascript�е�ÿ��������prototype���ԣ�Javascript�ж����prototype���ԵĽ����ǣ����ض�������ԭ�͵����á�

```js
    ��// ��������ӷ���
    var funName = function(){}
    funName.prototype.myfun = function(){
        alert('������funName�����ϵ�ԭʼ�����ϼ���һ��myfun���������캯�����õ�');
    }
    // ����
    var funname = new funName();// ��������
    funname.myfun();
```
�ڸ�������ӷ���ʱ������һ�·�ʽ��Ӷ��������

```js
����// ��������Ӷ������
    var funName = function(){}
    funName.prototype = {
        fun1:function(){
            alert('fun1');
        }
        ,fun2:function(){
            alert('fun2');
        }
    }
    // ����
    var funname = new funName();// ��������
    funname.fun1();
    funname.fun2();
```
