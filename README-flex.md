#### Flexible Box - 2009年，W3C提出了一种新的方案----Flex布局
- display: box; 将对象作为弹性伸缩盒显示。（伸缩盒最老版本）（CSS3）

```
display: -moz-box;
display: -webkit-box;
display: box;

-moz-box-flex: 1;
-webkit-box-flex: 1;
box-flex: 1;
```

- display: flexbox; 将对象作为弹性伸缩盒显示。（伸缩盒过渡版本）（CSS3）
- [display: flex;](https://jsfiddle.net/galaxybing/01w47nge/) 将对象作为弹性伸缩盒显示。（伸缩盒最新版本）（CSS3） - 声明容器是flex布局 - 需要ie9+以上
	- [Flex 布局教程：语法篇 - 20150712](http://www.ruanyifeng.com/blog/2015/07/flex-grammar.html)
	- [介绍了Flexbox模块所有基本概念 - 20170219 ](http://www.w3cplus.com/css3/understanding-flexbox-everything-you-need-to-know.html)
		- Flexbox格式化上下文（Flexbox formatting context）
	- [flex-container 父容器的属性：](http://www.cnblogs.com/yjf512/p/4900066.html)
		- display:flex。 表明这个容器是flex布局。
		- flex-direction: row | row-reverse | column | column-reverse; 表明容器里面的子元素的排列方向。
		- flex-wrap: nowrap | wrap | wrap-reverse; 如果子元素溢出父容器的时候是否进行换行。
		- flex-flow: 是 flex-direction 和 flex-wrap 两个属性的速记属性。
		- justify-content: flex-start | flex-end | center | space-between 空隙只在中间 | space-around 两边各有一边空隙
			- 这一个容器子元素横向排版在容器的哪个位置
		- align-items: flex-start | flex-end | center | baseline | stretch; 这个容器子元素纵向排版在容器的哪个位置
		- align-content: flex-start | flex-end | center | space-between | space-around | stretch; 当容器内有多行项目的时候，项目的布局
	- flex-item 子元素的属性：
		- order: ; 子元素的排序
		- flex-grow: ; 分配剩余空间的比例
		- flex-shrink: ; 分配溢出空间的比例
		- flex-basis: | auto; 指定Flex项目的初始大小，注意：如果flex-basis属性的值是0时，也需要使用单位。flex-basis: 150px;
			- flex-basis: auto; 宽度被自动计算时，是基于Flex项目内包含的内容的大小而计算
		- flex: none | [ <'flex-grow'> <'flex-shrink'>? || <'flex-basis'> ] 在容器中占比;
			- flex: 0 0 auto; 等于 flex: none; `宽度是被自动计算，不过弹性项目不会伸展或者收缩（因为二者都被设置为零）。`
			- flex: 1 1 auto; 等于 flex: auto;
			- flex: 2 1 0; 等于 flex: 2;
		- align-self: auto | flex-start | flex-end | center | baseline | stretch; 特定某个子元素的排布情况
			- align-self: auto; 将目标Flex项目的值设置为父元素的 align-items值，或者如果该元素没有父元素的话，就设置为 stretch
		- `margin: auto;` Flex项目上使用 margin: auto 时，值为 auto 的方向（左、右或者二者都是）会占据所有剩余空间。
	- [Flexbox的 bug 列表及其变通方法](https://github.com/philipwalton/flexbugs)
