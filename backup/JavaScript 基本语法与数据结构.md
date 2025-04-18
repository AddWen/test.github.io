# js

1. 变量

   ```javascript
   let num=1 //ES6新增，var已经淘汰
   ```

   常量  一经定义就不可以被修改的数值型

   ```
   const MAX=10
   ```

2. 数据类型  可以用typeof()方法检验数据类型

   ```javascript
   console.log(typeof(MAX)); //number
   let name='张三'       //string 字符串
   let age=18            //number 数值类型
   let single=true       //false boolean 布尔类型
   let money=null        //用于清空变量内容，表示空
   let phone             //undefined 未定义类型
   ```

3. 运算符

   数学运算符(加减乘除 取余)

   ```javascript
   let num1 =1+2       //1+2=3
   let num2 =2-1       //2-1=1
   let nun3 =1*2       //1x2=2
   let num4 =1/2         //1÷2=0 js中除法默认采用向下取整 即保留商的整数部分
   let num5 =5%2        //1 取余相当于求两数相除后的余数5÷2=2余1
   ```

​	自增,自减

```javascript
let i=1 
console.log(i++);//1   区别：++i相当于先自增1后使用
console.log(++i);//2   i++相当于先使用后自增1  自减相似
```

​	逻辑运算符(与或非)

```javascript
// 与 &&    两侧可以为布尔值 只有两边都为真结果才为真
// 或 ||    两侧可以为布尔值 只有两边结果都为假才为假
// 非 ！    将原本的布尔值类型反过来  ！true = false
```

4. 分支

   ```javascript
   //if(boolean) boolean为true将会执行后面的第一条语句，否则不执行
   if(i===1){
       console.log('我会执行');   
   }
   else{
       console.log('我不会执行');
   }
   ```

5. 循环

   ```javascript
   // for循环
   // for(初始化语句;判断条件;控制条件)
   let sum1=0
   for(let i=1;i<=MAX;i++)//求1-10累加和
   {
       sum1+=i//等价于sum=sum+i  -= *= /= 类似
   }
   console.log(sum1);
   
   // while循环
   // while(boolean) boolean为true将会执行后面的第一条语句，否则不执行
   let sum2=0
   while (i<=MAX){
       sum2+=i
       i++
   }
   console.log(sum2);
   ```

6. 函数

   ```javascript
   // 函数调用之后才能执行，可通过函数名的方式调用 
   // () 内可以无参数，也可以传参数  函数名(参数1,参数2....)
   // 函数执行到 return 语句
   function getSum(a,b){
       let sum=a+b//a,b为局部变量，假设外部有同名变量，不会改变其值
       return sum
   }
   // 下列语句可以写成 console.log(getSum(1,1))
   let result=getSum(1,1)
   console.log(result);
   ```

7. 数组

   ```javascript
   // 数组对象的作用是：使用单独的变量名来存储一系列的值，这些值必须是同一数据类型
   let numArray=[1,2,3,4,5]//可以直接赋值
   numArray.push(6)// 数组末尾添加新元素
   numArray.pop()// 删除数组末尾最后一个元素
   numArray.shift()// 删除数组开头第一个元素
   numArray.unshift(1)// 数组开头添加新元素
   console.log(numArray);
   
   let myFriends = [];//[]内可以加上数字表示数组长度，不加则表示空数组
   	myFriends[0] = "李四";
   	myFriends[1] = "王五";
   	myFriends[2] = "赵六";
   // 数组的遍历
   // 最基本的输出方式  
   for (let i=0;i<myFriends.length;i++){//数组名.length() 可自动获取数组长度
       console.log(myFriends[i],i)  
   }
   //这种方法更简洁
   myFriends.forEach(function(value,index){
       console.log(value,index);
       
   })
   ```

8. 对象 对象是拥有属性和方法的数据

   ```javascript
   let student={
       name:'赵六',
       age:18,
       single:true
   }
   console.log(student);
   // 对象的遍历
   for(let k in student){
       console.log(k,student[k]);
       
   }
   ```

9. 对象数组 object

   ```javascript
   let students=[
       {
           name:'张三',
           age:18,
           single:true
       },
       {
           name:'李四',
           age:19,
           single:false
       },
       {
           name:'王五',
           age:17,
           single:true
       }
   ]
   // 对象数组也可以使用pop(),push()等方法往里面添加对象
   students.push(student)
   console.log(students);
   ```

   