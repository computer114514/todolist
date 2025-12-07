### 删除模块（demo理解）：

1，肯定是在header组件----input上做文章，显示现输入和script的数据双向绑定。

2，摁下回车，监听事件，执行enterName函数，在这里边，（首先要definedemit函数定义要触发的app组件的自定义事件，这是为了组件之间通信），执行emit函数（"addToDo",value.name作为参数），（也会让input里面置空）触发addToDo自定义事件

3，app组件内需要@addToDo监听自定义事件，一旦触发，直接调用app里的addToDo函数，这个函数就在往list里面压入输入的东西了，list函数又被main渲染，完成添加

