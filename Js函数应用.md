1.  JavaScript中函数可以分为两类，分别是_____________和_______________。

内置函数 自定义函数 

2.  事件的三要素分别是____________、________________、__________________。

事件源、事件名称、事件处理函数

二、简答

1. JavaScript匿名函数的形式有哪些（至少写出两种）？

    ```javascript
   var x = function (a, b) {
       return a * b
   };
   var z = x(4, 3);
    ```

   ```javascript
   (function (name) {
       alert('wish' + name + "delighted!" );
   })('Mike');
   ```

   

2. 写出常用的三个事件，并简要说明其触发场景？

(1) onfocus : 当某个元素获得焦点时触发 

(2) onselect: 当文本框中的文本被选中时触发 

(3) onsubmit:当用户提交表单时触发 

三

1. 以下哪个单词不属于javascript关键字;    B

A break

B float

C var

D return

2. 如下代码，会弹出来是什么 var a; alert(a);  **C**

A 报错

B a is not define

C undefined

D 0

3.  以下代码运行后弹出的结果是 var a = 888; ++a; alert(a++ + 1); **C**

A 888

B 889

C 890

D 891

1. 编写一个函数。随机生成10个0-9的数字，并将该这些数字累加得到结果，并返回该运算式，在页面输出该运算式。完成函数的定义与调用过程。效果如图所示：

   ```javascript
           //第一题函数
           function randomsum () {
           	function randomcreate (a,b) {
   			    var num = Math.floor(Math.random()*(a-b)+b);
   			    return num;			
   		    }
           	for(var i = 0;i < 10;i++){
   			    arr[i] = randomcreate(0,10);
   			    sum += arr[i]
   			    document.write(arr[i]);
   			    if(i < 9){
   				    document.write('+');
   			    }else{
   				    document.write('=' + sum);
   			    }
   		    }
           }
           randomsum ();
   ```

    2.  编写一个函数，实现如下图所示效果，函数可以具有参数表示生成的行数，函数的返回值为，共打印n个*。n为实际打印*个数。完成函数定义与调用过程，目标效果如图所示：

   例如：传入行数为9

   ```javascript
           //第二题函数
           function starPrint (rownum) {
           	var sumstar = 0
   		    for(var i = 1;i <= rownum;i++){
   			    for(var j = 1;j <= 2 * i -1 ;j++){
   				    document.write('*');
   				    if(j == 2 * i - 1){
   					    document.write('<br/>');
   					    sumstar += j;
   				    }
   			    }
   			    j = 1;
   		    }
   		    document.write("共打印"+ sumstar +"个*");
           }
           starPrint (9);
   ```

   3.  现有字符串, "hello,world,nice,to,meet,you",定义函数，将该字符串中各单词的逗号分隔符替换成自定义的其它分隔符，该自定义分隔符通过函数参数传入，该函数返回替换后的字符串。完成的函数的定义与一次调用过程。

   例如：

   传入-时

   替换前："hello,world,nice,to,meet,you"   

   替换后："hello-world-nice-to-meet-you"

   传入*时

   替换前："hello,world,nice,to,meet,you"   

   替换后："hello * world * nice * to * meet*you"

   ```javascript
           //第三题函数
           function streplace (char1) {
           	// body... 
           	var str = "hello,world,nice,to,meet,you";
           	var str2 = str.split(",");
           	var str3 = str2.join(char1);
           	document.write(str3);
           }
           streplace ('-');
   ```

   

   