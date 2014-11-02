to-learn
============
- [ ] about callback
- [ ] 闭包 自调用
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



new knowledge
============
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
