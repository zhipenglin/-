# 前端面试题

### 一、初级篇

1.JavaScript的数据类型都有什么

答案：Undefined、Null、布尔值（Boolean）、字符串（String）、数值（Number）、对象（Object）在es6中定义了第七种类型Symbol。

2.使用onclick绑定事件和使用addEventLinstener绑定事件有什么不同？

答案：onclick是DOM0级事件，addEventLinstener绑定的是DOM2级事件。onclick只能同时在一个DOM上绑定一个处理函数，重复绑定则后面覆盖前面。addEventLinstener可以绑定多次不会覆盖。

3.请简述JavaScript中的事件模型，以及在ie浏览器上的兼容性问题？

答案：在各种浏览器中存在三种事件模型:原始事件模型( original event model),DOM2事件模型,IE事件模型.在原始模型中事件一旦发生就直接调用事件句柄,没有其它的事件传播过程。在DOM2模型中事件有一个特殊的传播过程,分为三个阶段: (1)capturing phase:事件被从document一直向下传播到目标元素,在这过程中如果有哪个祖先元素对该事件感兴趣可以注册自己的处理函数. (2)target phase:事件到达目标元素,执行目标元素的事件处理函数。IE模型也提供了一个event对象封装了事件的详细信息,但是IE不把该对象传入事件处理函数,由于在任意时刻只会存在一个事件,所以IE把它作为全局对象window的一个属性,IE中的事件传播模式对应于DOM2的第二和第三阶段,首先执目标元素的处理函数,然后向上传播到达document,ie中只能能捕捉鼠标事件,而DOM2中可以捕捉所有的事件,IE中注册和删除事件处理函数的方法也不同于DOM2.事件处理函数的注册和删除是通过元素的attachEvent( "eventType","handler") and detachEvent("eventType","handler" ),与dom2不同的是eventType有on前缀

4.请简述==与===的区别

答案："==="是严格运算符，左右两边必须严格相等才为true，"=="叫做相等运算符，左右两边进行类型转换后相等就为true

5.typeof的作用是什么，instanceof的作用是什么？

答案：typeof A用来检测A量属于那种基本类型，A nstanceof B用来检测一个实例是否属于它的父类型

6.已知数组var stringArray = [“我”, “爱”, “传统“,“文化"]alert输出”我爱传统文化“

答案：
``` javascript
alert(stringArray.join(''));
```
7.用js实现随机选取10–100之间的10个数字，存入一个数组，并排序

答案：

``` javascript
var iArray = [];
funtion getRandom(istart, iend){
  var iChoice = istart - iend +1;
  return Math.floor(Math.random() * iChoice + istart;
}
for(var i=0; i<10; i++){ 
  iArray.push(getRandom(10,100)); 
} 
iArray.sort();
```
}

for(var i=0; i

8.行内元素与块级元素的区别，行内元素有哪些？块级元素有哪些？

答案：行内非替换元素设定width、height无效，宽度可以通过设定padding和margin拉宽，高度可以通过设定line-height定位行内框的高度。 常用行内元素：a img input textarea strong code span,lable 常用块级元素：div ul h123456 table form center p

9.有哪项方式可以对一个DOM设置它的CSS样式？

答案：外部样式表，引入一个外部css文件 内部样式表，将css代码放在 <head> 标签内部 内联样式，将css样式直接定义在 HTML 元素内部

10.CSS都有哪些选择器?

派生选择器（用HTML标签申明） id选择器（用DOM的ID申明） 类选择器（用一个样式类名申明） 属性选择器 后代选择器（利用空格间隔，比如div .a{ }） 群组选择器（利用逗号间隔，比如p,div,#a{ }）

11.如何让一个元素水平垂直居中？

答案：方法太多，不一一详述，能实现就好

12.如何实现一个三列布局使得左右两列定宽，中间一列占有剩余宽度

答案：方法太多，不一一详述，能实现就好

13.默认情况下，img标签和在它下方的文字之间有十几像素的空白，如何清除这个空白

答案：line-height:0，或者设置图片display:block

14.如何清除浮动

答案：方法太多，不一一详述，能实现就好
