---
title: ECMAScript 6|2015|新 js
date: 2018-12-05 09:33:01
categories:
  - 前端学习记录
tags:
  - js
---

## 变量的声明方式

1.**const**：声明常量的时候使用

    注意：
    ①使用 const 生命的变量不可修改。
    ②const 声明变量时把大括号当做作用域，不能重复声明，没有声明提升。

2.**let**：声明变量。

    注意：
    let声明变量时也把大括号当做作用域，不能重复声明，也没有声明提升。

## 解构赋值

### 数组

```js
const arr = [1, 2, 3];
const [num1, num2, num3] = arr;
console.log(num1, num2, num3);
```

### 字符串

```js
const str = 'hello';
const first = str.charAt(0);
console.log(first);
const [first, second] = str;
console.log(first, second);
```

### 对象

```js
const userInfo = {
  username: 'erha',
  userage: 2,
  color: 'grey'
};
// 变量名要和对象的属性名相同，顺序无所谓
const { userage, username } = userInfo;
console.log(userage, username);
// 对象解构赋值的另一个用法“函数参数的解构赋值”
function fun({ username }) {
  console.log(username);
}
fun(userInfo);
```

## 箭头函数

**写法**

    (参数) => {语句}
    例如：
    const add = (a,b) => {
      const res = a + b
      return res
    }
    const result = add(1,2)
    console.log(result)

1.**当参数为一个的时候可以省略小括号，当函数内部只有返回值的时候，可以省略大括号和 return 例如：**

2.**箭头函数没有大括号的时候，箭头后面就是返回值。**

3.**普通函数内的 this 指向，在调用函数的时候去找；而箭头函数内的 this 指向，声明函数的时候就定义好了。**

```js
const fun = a => 10;
const b = fun(100);
console.log(b);
const arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 0];
const newArr = arr.filter(ele => ele > 5);
```

## 字符串模板
