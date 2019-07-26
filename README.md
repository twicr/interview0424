# Interview
# 每日三问——0423
> [github项目](https://github.com/haizlin/fe-interview?utm_source=ZHShareTargetIDMore&utm_medium=social&utm_oi=750848792785354752) 问题解答
# HTML
### 简述下html5的离线存储原理，同时说明如何使用？
localStorage 没有时间限制的存储

sessionStorage 针对一个session的数据存储
# CSS
### 清除浮动的方式有哪些及优缺点？
* 外部盒子添加overflow:hidden，可能造成溢出部分不显示
* 在外部盒子底部添加clear属性的空盒子，引入了冗余元素
* 外部盒子添加浮动，可能需重新布局
* 通过伪元素添加clear属性
# JS
### 写一个加密字符串的方法
通过Unicode编码加密，可能无法解密
```javascript
function demo(str){
	return str.split('').map(s => {
		return String.fromCharCode(s.charCodeAt() + Math.floor(Math.random() * 10));
	}).join('');
}
```
