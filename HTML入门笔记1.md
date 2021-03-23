# HTML是谁建立的
    HTML是Tim Berners-Lee 称做李爵士的人在1990年左右建立的
# HTML的起手式
    创建html文件输入 "!"然后按tab键可以自动生成
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```
# 常用的表章节的标签有
1. 标题 h1~h6 ```<h1>文章大标题</h2>```
2. 章节 ```<section>表示文件的一节为一整块章节</section>```
3. 文章 ```<article>文章</article>```  段落 ```<p>划出文章的一个段落</p>```
5. 头部```<header>在顶部内容</header>``` 脚部```<footer>在底部内容</footer>```
6. 主要内容```<main>文章主要内容<main>``` 旁支内容```<aside>主要的分支内容<aside>```
7. 划分模块```<div>把上面的几个标签化成一整块</div>```

# 全局属性有
* class
* contenteditable
* hidden
* id
* style
* tabindex
* title
# 常用的内容标签有
* a 表示一个链接<a href="http://www.bilibili.com">B站</a>
* em 更多是语气的强调
* strong 表示本身内容的强调
* code 让游览器显示输出的内容与你写入的内容格式一样
* pre 让多的空格回车保留显示
* ol 有顺序的列表，里只能有li
  ```html
    <ol>
        <li></li>
    </ol>
    ```
* ul 无顺序的列表
    ```html
    <ul>
        <li></li>
    </ul>
    ```
* dl列表 dt表示列表里的项目 dd描述列表中的项目
    ```html
    <dl>
        <dt></dt>
        <dd></dd>
    </dl>
    ```