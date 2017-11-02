### 输入框input／textarea／select等元素的value设置问题
- 当上述元素的value设置为state时，那么对于输入文本框内容是不可改的.
- 解决方法，当输入框改变时调用的方法里面执行setState改变state，并能重新渲染