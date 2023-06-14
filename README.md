JavaScript语言特点
解释型语言
动态类型语言
弱类型语言
基于原型的面向对象语言

---------------------------------------------------------------------------

JavaScript的实现
ECMAScript
DOM
BOM

HTML（结构），CSS（表现），Javascript（行为）

关键字：保留字：

----------------------------------------------------------------------

![image-20230613134352844](C:\Users\11608\AppData\Roaming\Typora\typora-user-images\image-20230613134352844.png)

模板字符串：
let age =10;
let name ="Mike";
let greeting = "I am"+name+". I am"+age+"years old".
ES6:
let greeting2= 'I am {$name}. I am {$age}years old'.
子字符串：
//slice()和substring()的区别</title> 

<script>
let myString = "hello world";
console.log(myString.slice(1,3));
console.log(myString.substring(1,3));
console.log(myString.slice(4)
console.log(myString);
// console.log(myString.substr(2,3));
</script>
//el
//el
//o world
//hello world

<script>
let myString = "hello world";
console.log(myString.slice(2,-3));
console.log(myString.substring(2,-3));
console.log(myString.substring(2,0));
console.log(myString);
// console.log(myString.substr(2,3));
</script>
llo wo
hel
he
hello world
复制代码
myString.slice(2,-3) 返回从第 2 个字符（包括）到倒数第 3 个字符（不包括）的子字符串，即 "llo wo"。

myString.substring(2,-3) 返回从索引 2 开始到索引 -3（小于 0，因此被视为 0）结束的子字符串，即 "hel"。

myString.substring(2,0) 返回从索引 2 开始到索引 0（顺序颠倒）结束的子字符串，即 "he"。

myString 原样输出，为 "hello world"。

类型转换：

对于将字符串类型转换成数值型，分别是parseInt和parseFloat 前者将字符串转换成整数，后者字符串转换浮点数。

for ...in语句

它通常来枚举对象的属性，for ...in语句作用是遍历对象的所有属性。

argument对象

通过argument对象，可以无需指出参数的名称就能直接访问它们。

*箭头函数： p58

p71 获取时间的相关方法：

返回从1970年起经过的毫秒数：oDate.getTime()

Math对象： 生成随机数的方法：

因为random返回的都是小数，如果想选择一个1到100之间的整数
let uNum =Math.floor(Math.random()*100+1)
希望2到99之间只有98个数字，第一个数字为2
let uNum =Math.floor(Math.random()*98+2)



引用类型和原始值包装类型的主要区别在于：对象的生命周期不同



不同数据结构的数组操作：

尾部增删：

·array.push() //将一个或多个元素添加到数组的末尾

const array = [1, 2, 3];

const length = array.push(4, 5);

console.log(array) // [1, 2, 3, 4, 5]

console.log(length) //5

·array.pop()//将删除数组的最后一个元素

const array = [1, 2, 3];

const poped = array.pop();

console.log(array) // [1, 2]

console.log(poped) //3

头部增删：

·array.unshift()//将一个或多个元素添加到数组的top

const array = [1, 2, 3];

const length = array.unshift(4, 5);

console.log(array) // [ 4, 5, 1, 2, 3]

console.log(length) //5

.array.shift()//将删除数组的第一个元素

const array = [1, 2, 3];

const shifted = array.shift();

console.log(array) // [2, 3]

console.log(shifted) //1

Map集合

对象和map集合是可以相互替换的；

Set集合p100

判断是否恒等？



P105

调用构造函数不带参数，以下代码等价
let p1 =new Point;
let p2 =new Point();

p107:
get distance()用于读取位置信息，计算原点的距离
set position()用于根据给定的位置参数，设置点x轴和y轴的坐标
class Point{
    constructor(x=0, y=0) {
        this.x = x;
        this.y = y;
    }
    move(deltaX, deltaY){
        this.x = this.x + deltaX;  //也可以使用 += 运算符
        this.y = this.y + deltaY;  //也可以使用 += 运算符
    }
    get distance(){
        return Math.sqrt(this.x * this.x + this.y * this.y);
    }
    set position(value){
        this.x = value.x;
        this.y = value.y;
    }
    draw(){
        console.log(`这是一个Point，位于(${this.x},${this.y})`);
        console.log(`与坐标原点相距 ${this.distance}`);
    }


}

let p = new Point();
p.position ={x:100,y:100};
Point.className();

这是一个Point，位于(100,100

与坐标原点相距 141.xxxxxx
p108
instance of运算符
*p113 继承
p124
划线部分可以看到4个文本节点，三个元素节点
p125代码：

<!DOCTYPE html>
<html>
<head>
<title>获取父节点</title>
<script>
function myDOMInspector(){
  let myItem = document.getElementById("cssLi");
  console.log(myItem.parentNode.tagName);   //访问父节点
}
</script>
</head>
<body onload="myDOMInspector()">
  <ul>
    <li>Java</li>
    <li id="cssLi">Node.js</li>
    <li>C#</li>
  </ul>
</body>
</html>



parentNode属性获取

UL



p134

事件流：

捕获阶段；xxxxxxxxx

到达阶段；xxxxxxx

冒泡阶段；xxxxxxx



