
[http://jinlong.github.io/2013/08/29/devtoolsecrets/#persistent](http://jinlong.github.io/2013/08/29/devtoolsecrets/#persistent)

### 快捷键

快捷键列表在调试窗口的右上角，点击“齿轮”图标，再点击“Shortcuts”标签。

##### 常用如下

Sources:

+ Ctrl+o：打开文件，弹出窗口后还可以输入":行数:列数"
+ Alt+左键：展开所有子节点
+ Alt+左键拖拽：选中多列

运行代码片段：
Sources-Snippets

目前在chrome里，箭头函数=>中的this(ts文件)打断点后看到的不是真实的this,往往会显示为window;在js文件里可以显示出真实this指向对象

给chrome添加启动参数：--allow-file-access-from-files
chrome是不允许读取本地文件的，所以如果你要进行测试，可以在本地搭一个测试环境，可以使用wamp套件进行安装，或者换IE测试

--disable-web-security