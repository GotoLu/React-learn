### React中的事件绑定

- 在JSX的标签内添加属性onClick，属性值为{this.bark}，例如
```
bark(){
	console.log("bark");
}
```
- 注意1：这里的onClock使用驼峰写法，事件方法调用记得加{}
- 注意2：在this.xxx调用的函数内，this为null或undefined
```
bark(){
	console.log(this); // onClick调用的不是对象方法，而是bark
}
```
- 针对第二点，此时应该修改onClick属性值为`{this.bark.bind(this)}`