# myBlog
my first blog
### 1. new Set()
可能有人知道ES6中提供了新的数据结构 Set，但是能够灵活运用的人或许不多。利用Set数据结构我们能够轻松的去重一个数组，比如：
```
let arr = [1, 2, 2, 3];
let set = new Set(arr);
let newArr = Array.from(set); // Array.from方法可以将 Set 结构转为数组。

console.log(newArr); // [1, 2, 3]
```
###  2. Object.assign()
Object.assign()也是ES6中提供的对象的扩展方法，其可以用于对象的合并拷贝，比如：
```
let obj1 = {a: 1};
let obj2 = {b: 2};
let obj3 = Object.assign({}, obj1, obj2);

console.log(obj3); // {a: 1, b: 2}
```
### 3. map()
map方法用于遍历数组，有返回值，可以对数组的每一项进行操作并生成一个新的数组，有些时候可以代替for和forEach循环，简化代码，比如：
```
let arr3 = [1, 2, 3, 4, 5];

let newArr3 = arr3.map((e, i) => e * 10); // 给数组每一项乘以10

console.log(newArr3); // [10, 20, 30, 40, 50]
```
### 4. filter()
filter方法同样用于遍历数组，顾名思义，就是过滤数组，在每一项元素后面触发一个回调函数，通过判断，保留或移除当前项，最后返回一个新的数组，比如：
```
let arr4 = [1, 2, 3, 4, 5];

let newArr4 = arr4.filter((e, i) => e % 2 === 0); // 取模，过滤余数不为0的数

console.log(newArr4); // [2，4]
```
### 5. some()
some方法用于遍历数组，在每一项元素后面触发一个回调函数，只要一个满足条件就返回true，否则返回false，类似于 || 比较，比如：
```
let arr5 = [{result: true}, {result: false}];

let newArr5 = arr5.some((e, i) => e.result); // 只要一个为true，即为true

console.log(newArr5); // true
```
### 6.every()
every方法用于遍历数组，在每一项元素后面触发一个回调函数，只要一个不满足条件就返回false，否则返回true，类似于 && 比较，比如：
```
let arr6 = [{result: true}, {result: false}];

let newArr6 = arr6.every((e, i) => e.result); // 只要一个为false，即为false

console.log(newArr6); // false
```
