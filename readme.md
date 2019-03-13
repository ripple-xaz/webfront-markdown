# 前端笔记

***

该文件用来记录前端一些基本的知识和用法，包括CSS、js的基本语法，npm,nodejs,webpack，canvas，svg,vue，react,等等一系列的相关知识点

***

## JavaScript必备知识点
- 数据类型
- 

### 数据类型

#### 原始（Primitive）类型
- js有6种原始类型，boolean，null，undefined，number，string，symbol
- 首先原始类型存储的都是值，是没有函数可以调用的，比如 undefined.toString()
![](https://i.imgur.com/nFoGBtV.png)
- typeof null 会输出 object，但是这只是 JS 存在的一个悠久 Bug。在 JS 的最初版本中使用的是 32 位系统，为了性能考虑使用低位存储变量的类型信息，000 开头代表是对象，然而 null 表示为全零，所以将它错误的判断为 object 。虽然现在的内部类型判断代码已经改变了，但是对于这个 Bug 却是一直流传下来。

#### 对象（Object）类型
- 原始类型存储的是值,对象类型存储的是地址（指针）。当你创建了一个对象类型的时候，计算机会在内存中帮我们开辟一个空间来存放值

- 对于常量 a 来说，假设内存地址（指针）为 #001，那么在地址 #001 的位置存放了值 []，常量 a 存放了地址（指针） #001
```
const a = []
```

- 当我们将变量赋值给另外一个变量时，复制的是原本变量的地址（指针），也就是说当前变量 b 存放的地址（指针）也是 #001，当我们进行数据修改的时候，就会修改存放在地址（指针） #001 上的值，也就导致了两个变量的值都发生了改变。
```js
const a = [];
const b = a;
b.push(1)
```

```js
function test(person) {
  person.age = 26
  person = {
    name: 'yyy',
    age: 30
  }

  return person
}
const p1 = {
  name: 'yck',
  age: 25
}
const p2 = test(p1)
console.log(p1) // 
console.log(p2) // 
```

