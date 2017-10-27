## 对新建项目进行修改
### 一个hello world
* 删除App.js中原来的代码
```
<div className="App">
<header className="App-header">
  <img src={logo} className="App-logo" alt="logo" />
  <h1 className="App-title">Welcome to React</h1>
</header>
<div class="container">Hello React</div>
</div>
```

#### 了解React的渲染过程
- 从App.js第一行开始
  `import React, { Component } from 'react';`</br>
引入React和Component，React的页面都是一个个组件构成的
- 再从index.js第二行开始
 `import ReactDOM from 'react-dom';`</br>
 ReactDOM也是不可或缺的，组件最终渲染到浏览器页面就是靠的他。
- 了解App.js的核心代码--组件
```
class App extends Component {
  render() {
    return (
      <h1>Hello World</h1>
    );
  }
}
```
- 了解React是怎么把组件渲染到浏览器的
`ReactDOM.render(<App />, document.getElementById('root'));`</br>
通过ReactDOM的render方法将App组件渲染到页面的id为root处。

- 注意1，在组件中的render函数返回值看似html代码，其实是JSX代码，React.js和babel会将其编译为js对象，然后再对js对象进行渲染。
- 注意2，JSX代码中可以使用组件内的变量和组件间传递的变量，组件内的变量使用方法: {var},组件间通信：{this.props.xxx}