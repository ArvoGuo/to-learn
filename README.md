#2014

1225
	Fabric

```
	Fabric is a Python (2.5 or higher) library and command-line tool for streamlining the use of SSH for application deployment or systems administration tasks.
```
1220 谢了关于[qq地图覆盖物的jquery扩展](https://github.com/ArvoGuo/QQMap)，将与angular对接。

1210 写了关于[高德地图覆盖物的jquery扩展](https://github.com/ArvoGuo/GaodeMap)，将与angular对接。

1209 关于javascript的设计模式-观察者模式（发布订阅模式）（Publish/Subscribe）

1208 考虑到phonegap的各种局限性，如请求，各种api等功能，还是学习oc或者swift开发吧

1206 采用phonegap方式开发app

1205 开始写一个App

1202 留下一个思考
```
如何优雅的实现  导航 + 及时视图  这样结构的页面
以下是几个自己能想到的
	1.frameset 和 iframe
		可以嵌套多个页面，但是难以继承总窗体的css和js，即难以操作dom
		对于页面中的 <a href=""></a> 的target需要定义
	2.angular ui-view
		能够实现页面片段的载入和css，js的继承
		但是难以操作dom（这个不确定，个人目前做不到）
		<a ui-serf=""></a>
		跳转的属性变了，并且跳转是以锚点方式跳转，基于非angular标签定义的页面 存在问题。
	3.目前采用后端自定义模板方式
		在index.html 中写入 {{html}} ，后端做页面片段替换 再吐出
```
1202 写了一个[md to html平台](https://github.com/ArvoGuo/convertor)
1127 学习小结
```
现代居中的方式
1.translate(-50%,-50%)
2.flex

关于filter（滤镜）的了解
```
1125 学习方向
```
sass
gulp
angular
flex-box
es6-promise..

```
1123,css3的学习
```
@-webkit-keyframes [animation-name]{
	0%{
		//
	}
	100%{
		//
	}
}
-webkit-animation-name: [animation-name];
```
```
background-position + steps 逐帧动画的实现
```
1121,node的学习
```
fs.open(path,flags,[mode],[callback(err,fd)])

r 读
r+ 读写
w 写，不存在则创建
w+ 读写，不存在则创建
a 追加，不存在则创建
a+ 以读取追加模式打开，不存在则创建
```
```
原型继承
util.inherits(Sub,Base)
```
```
输出流和输入流
process.stdin.resume();
process.stdin.on('data',function(data){
	process.stdout.write('read forme consol: ' + data.toString());
})
```
1120,node的学习
```
REPL模式
意思是：read-eval-print loop   输入－求值－输出循环。
```
```
supervisor 实时监控代码改动
```
```
理解module.exports 和 exports的区别
```




















#Before 2014 1120
==============================
to-learn
============
- [X] about callback
- [X] 闭包 自调用
- [ ] node request 爬取数据
- [X] fiddler 如何使用
- [ ] css :table   table-cell  table-row
- [ ] css 双栏响应布局
- [ ] web components
- [X] 噢。。今天玩游戏
- [X] 今天要用github写个简历吧
- [ ] 要学学grunt工具了
- [ ] 今天去面试，被问到js的继承，面向对象模式。想到日常写的js都很少运用到，还是得研究一下。
      关于js的继承，js的继承派生，先把这个搞通
- [ ] 141024面试知识关于优雅的降级和优雅的升级，less的运用，meanjs站点的学习
- [ ] 关于D2前端技术会议的知识。 苏千的前后端分离，java－》node－》h5；祝犁的angularjs。
- [X] 从阿里回来后，脑海里更加明确，要好好努力的意义。所谓的人和工具的区别。
- [ ] 新的问题Less的使用，singlepage的实现，webcomponents
- [X] 要一个新的起点开始了，慢慢要定下方向了应该。基于javascript和css的动画特效交互？
- [ ] 有一件要事一直要做但是还没开始做， 为我的服务器启一个node服务器，发布一些日常写的静态资源。
- [ ] 关于jquery2.2版本  $(document).ready() undefined 问题
- [X] 留个问题，稍后做个demo测试下，关于new <div>（backgroundimg）  和 new <img>（src）是否都是会不断请求图片
	  解决，都不会不断请求 ，只会请求一次



new knowledge
============

-11.15
```
	1.  var fn = function(){}
	2.  function fn(){}

```
	关于1和2两种方式声明函数，1是采用变量方式，按声明顺序调用，2实际上是一种全局函数的声明方式，不够优雅

-[X]在屏幕坐标系中，y的正方向时向下，而数学系中正方向时向上
-[X]get懒加载的一种实现方式，
	1.将图片路径存起来
	2.window.onscroll  时监听图片位置与当前可视区
	document.documentElement.clientHeight + (document.documentElement.scrollTop || document.body.scrollTop)
	再进行加入图片元素
-[X]在zepto下的on方法不能绑定字符串的方式创建的元素事件，只能用live  X 应当更新版本，现zepto已模块分割
-[X]微信监听对象，后续操作对象时，不要尝试去创建对象，应当去改变对象的属性。
-[X]发get请求时后面要带随机数，否则会有缓存
```
		rand=function(){
			return (" "+Math.random()).split('.')[1];
		}
```
-[X]判断奇偶的性能优化
```
	方法一
	for (var i = 0,len = rows.length; i < len; i++){
		if(i % 2){
			className = 'even',
		} else {
			className = 'old'
		}
	方法二 , 32位数字的二进制底层表示，偶数最低位0，奇数最低位1，通过数字与数字进行按位与运算。
			但此数为偶数，那么按位与运算的结果是0，
			如果为奇数  ，那么按位与运算的结果是1
	for (var i = 0,len = rows.length; i < len; i++){
		if(i & 1){
			className = 'old',
		} else {
			className = 'even'
		}
}
```
-[X] 监听div内容的变化(例如用div模仿select标签的时候使用)
```
	$('#province').bind('DOMNodeInserted',function(){
    })
```
-[X] css文本超出以省略号结尾
```
	white-space: nowrap;
    text-overflow: ellipsis;
    overflow: hidden;
```
-[X] jquery 的克隆对象
```
	  当对象中包含对象的时候应当使用深层克隆 $.extend(true,{},obj);
	  否则对象中的对象也将只是引用
```
-[X] 盒子模型，ie6认为margin＋border＋padding ＝ 盒子长宽，而w3c标准则只包含内容
     在页面顶部加入doctype声明 就能够指定页面使用的盒子模型
