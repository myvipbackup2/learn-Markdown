# learn-Markdown

##### 最近对Markdown的常用语法总结

Markdown的简介
---
Markdown是一种轻量级标记语言，它用简洁的语法代替排版，使我们专心于码字。它的目标是实现易读易写，成为一种适用于网络的书写语言。同时，Markdown支持嵌入html标签。

注意：Markdown使用#、+、*等符号来标记， 符号后面必须跟上 至少1个 空格才有效！

Markdown的常用语法
---
### 标题

Markdown 标题支持两种形式：

##### 1、用#标记

在 标题开头 加上1~6个#，依次代表一级标题、二级标题....六级标题

``` markdown
<!-- more -->

# 一级标题
## 二级标题
### 三级标题
##### 四级标题
###### 五级标题
###### 六级标题

```

##### 2、用=和-标记
在 标题底下 加上任意个=代表一级标题，-代表二级标题

一级标题
======

二级标题
----------
效果如下：

一级标题
===

二级标题
---

### 三级标题

#### 四级标题

##### 五级标题

###### 六级标题 

### 列表

**Markdown 支持有序列表和无序列表。**

_无序列表使用-、+和*作为列表标记_：

``` markdown
- Red
- Green
- Blue

* Red
* Green
* Blue

+ Red
+ Green
+ Blue
```

**效果如下：**

- Red
- Green
- Blue

**有序列表则使用数字加英文句点.来表示：**

``` markdown
1. Red
2. Green
3. Blue
```

**效果如下：**

1. Red
2. Green
3. Blue

### 引用

引用以`>`来表示，引用中支持多级引用、标题、列表、代码块、分割线等常规语法。

**常见的引用写法：**
```markdown
    > 这是一段引用    //在`>`后面有 1 个空格
    > 
    >     这是引用的代码块形式    //在`>`后面有 5 个空格
    >     
    > 代码例子：
    >   
        protected void onCreate(Bundle savedInstanceState) {
            super.onCreate(savedInstanceState);
            setContentView(R.layout.activity_main);
        }
    
    > 一级引用
    > > 二级引用
    > > > 三级引用
    
    > #### 这是一个四级标题
    > 
    > 1. 这是第一行列表项
    > 2. 这是第二行列表项
```
**效果如下：**
> 这是一段引用    //在`>`后面有 1 个空格
> 
>     这是引用的代码块形式    //在`>`后面有 5 个空格
>     
> 代码例子：
>   
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
    }

> 一级引用
> > 二级引用
> > > 三级引用

> #### 这是一个四级标题
> 
> 1. 这是第一行列表项
> 2. 这是第二行列表项

### 强调

两个`*`或`-`代表加粗，一个`*`或`-`代表斜体，`~~`代表删除。

```markdown
    **加粗文本** 或者 __加粗文本__
    
    *斜体文本*  或者_斜体文本_
    
    ~~删除文本~~
```

**效果如下：**

**加粗文本** 或者 __加粗文本__

*斜体文本*  或者_斜体文本_

~~删除文本~~

### 图片与链接

图片与链接的语法很像，区别在一个 `!` 号。二者格式：

```markdown
    图片：![]()    ![图片文本(可忽略)](图片地址)
    
    链接：[]()     [链接文本](链接地址)
```

链接又分为行内式、参考式和 自动链接：

```markdown
这是行内式链接：[Fly.Lee's Blog](http://blog.lizixiang.cn)。

这是参考式链接：[Fly.Lee's Blog][url]，其中url为链接标记，可置于文中任意位置。

[url]: http://blog.lizixiang.cn/ "Fly.Lee's Blog"

链接标记格式为：[链接标记文本]:  链接地址  链接title(可忽略)

这是自动链接：直接使用`<>`括起来<http://www.lizixiang.cn>

这是图片：![][avatar]

[avatar]: https://avatars1.githubusercontent.com/u/19941690?v=3&s=460
```

**效果如下：**

这是行内式链接：[Fly.Lee's Blog](http://blog.lizixiang.cn)。

这是参考式链接：[Fly.Lee's Blog][url]，其中url为链接标记，可置于文中任意位置。

[url]: http://blog.lizixiang.cn/ "Fly.Lee's Blog"

链接标记格式为：[链接标记文本]:  链接地址  链接title(可忽略)

这是自动链接：直接使用`<>`括起来<http://www.lizixiang.cn>

这是图片：![][avatar]

[avatar]: https://avatars1.githubusercontent.com/u/19941690?v=3&s=460

### 代码

代码分为行内代码和代码块。

* 行内代码使用 `代码` 标识，可嵌入文字中
* 代码块使用4个空格或```标识

```
这里是代码
```

代码语法高亮在 ```后面加上空格和语言名称即可

``` 语言
//注意语言前面有空格
这里是代码
```

**例如：**

这是行内代码`export default Comment;`的例子。

这是代码块和语法高亮：

```markdown
    ``` javascript
    // 注意javascript前面有空格
    import React from 'react'
    import {Avatar, Timeline} from 'antd'
    
    class Comment extends React.Component {
        render() {
            return (
                <div style={{overflow: 'hidden'}}>
                    <Avatar style={{float: 'left', backgroundColor: this.props.color}}
                            size="large">{this.props.author}</Avatar>
                    <Timeline style={{float: 'left', marginLeft: '3%', width: '80%'}}>
                        <Timeline.Item>{this.props.date}</Timeline.Item>
                        <Timeline.Item>{this.props.children}</Timeline.Item>
                    </Timeline>
                </div>
            );
        }
    }
    
    export default Comment;
    ```
```
**效果如下：**
``` javascript
    // 注意javascript前面有空格
    import React from 'react'
    import {Avatar, Timeline} from 'antd'
    
    class Comment extends React.Component {
        render() {
            return (
                <div style={{overflow: 'hidden'}}>
                    <Avatar style={{float: 'left', backgroundColor: this.props.color}}
                            size="large">{this.props.author}</Avatar>
                    <Timeline style={{float: 'left', marginLeft: '3%', width: '80%'}}>
                        <Timeline.Item>{this.props.date}</Timeline.Item>
                        <Timeline.Item>{this.props.children}</Timeline.Item>
                    </Timeline>
                </div>
            );
        }
    }
    
    export default Comment;
```

### 表格

* 表格对齐格式

1. 居左：:----
2. 居中：:----:或-----
3. 居右：----:

例子：

