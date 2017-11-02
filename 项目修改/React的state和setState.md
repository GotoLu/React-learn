### React的state和setState

```
class Button extends Component{
	constructor(...args){
		super(...args);
		state: {
			isLike: false
		}
	}
	
	handleOfClick(){
	}
	
	render(){
		return (
			<div>
				<button onClick={this.handleOfClick}>{islike ? '取消': '点赞'}👍</button>
			</div>
		)
	}
}
```
- setState接受对象参数，运行setState后会执行render进行渲染。
```
handleOfState(){
		console.log(this.state.isLike);
		setState({
			isLike: !this.state.isLike;
		})
		console.log(this.state.isLike);
}
```
<br />this.state.isLike两次都是false，React.js 的 setState 把你的传进来的状态缓存起来，稍后才会帮你更新到 state 上，所以你获取到的还是原来的 isLiked。
- setState还可以接收函数，例如
```
setState((preState)=>{
	return {
		isLike: !this.state.isLike
	}
})
```