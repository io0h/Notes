# jade的语法总结

[jade](https://www.npmjs.com/package/jade) 是一个类python风格的html的模版引擎。
依赖node环境。

这里有jade的常见的使用的[example](http://naltatis.github.io/jade-syntax-docs/#basics)。

## jade的基本用法

```
doctype html
html
  head
    title my jade template
  body
    h1 Hello #{name}
```

第一行定义了html的doctype
下面采用缩进的方式定义了基本的html结构
输出html标签包裹的文字，只需要文字与html标签间隔一个空格
定义变量的话 采用 `#{ }` 的形式即可，这里`{"name": "Bob"}`


**html的输出**

```
<!DOCTYPE html>
<html>
  <head>
    <title>my jade template</title>
  </head>
  <body>
    <h1>Hello Bob</h1>
  </body>
</html>
```

## id和类


```
#content
  .block
    input#bar.foo1.foo2
```

id采用`＃`的方式
类采用`.`的方式


**html的输出**

```
<div id="content">
  <div class="block">
    <input id="bar" class="foo1 foo2"/>
  </div>
</div>
```

## 嵌套









