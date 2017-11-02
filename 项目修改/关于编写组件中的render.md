### 关于编写组件中的render

1. render函数里的JSX必须要有个一个容器包含里边的内容，例如：
```
render(){
	<div>1</div>
	<div>2</div>
}
```
</br>上面例子是不合法的，必须要有一个容器对其进行包裹，例如：
```
render(){
	<div>
		<div>1</div>
		<div>2</div>
	</div>
}
```
2. render函数里边的JSX的标签中可以插入js代码，但是需要将代码用{}包裹，js代码不仅可以插入再标签内的属性值。
3. 标签属性class和for都是js的关键字，在JSX中无法使用，替代方案class==>className，for==>htmlFor，其他属性照常使用。
4. JSX里边可以嵌套JSX
```
	{isLink?<button>取消</button>:<button>点赞</button>}
```
5. JSX元素变量
```
let cancle = <button>取消</button>;
let prise = <button>点赞</button>;
...
{isLink?cancle:prise}
```
6. 