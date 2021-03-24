#HTML的常用标签
## a标签的用法
1. a标签的作用是表示一个超链接：跳转到外部页面，内部锚点或者跳转到邮箱电话等
   ```
   <a href="https://google.com" >超链接</a>
   ```
2. a标签的属性有
   * href 链接地址
   * target 指定超链接在那个页面打开
3. a标签href的取值
   * 网址 https://baidu.com http://baidu.com //baidu.com
   * 路径 绝对路径与相对路径都可以 
   * 伪协议 可以执行里面代码当javascript执行
   ```
   <a href="javascript:代码;">伪协议</a>
   ```
   还有其他的伪协议
    ```
   <a href="mailto:邮箱地址">发邮件</a>
   <a href="tel:手机号">打电话</a>
   ```
   * id #xxx 可以跳转指定标签
   ```
   <a href="#xxx">10</a>
   ```
4. target的取值 指定在那打开超链接
   * _blank 在新的网页打开
   * _top 在顶层页面打开
   * _parent 在当前页面的父级窗口打开
   * _self 默认值，在本身窗口打开
   * xxx 如果没有xxx窗口就创建一个新的窗口打开，有就在原xxx窗口打开
   ```
   <a href="//baidu.com" target="xxx">百度</a>
    ```
## img标签的用法
1. img标签的作用是发出get请求展示一张图片
  ```html
  <img src="t.jpg" alt="一棵树">
  ```
     
2. img标签的属性
   * alt 在加载失败时显示
   * src 图片的地址
   * width 调整图片的宽度
   * height 调整图片的高度
3. 事件
   * onload 图片加载成功时触发
   * onerror 图片加载失败时出发
  ```html
      <img id="xxx"  src="t.jpg" alt="一只树">
    <script>
        xxx.onload = function(){
            console.log('图片加载成功')
        }
            xxx.onerror = function(){
                console.log("图片加载失败")
                xxx.src = "/404.png"
            }
    </script>
  ```   
  4. 响应式 添加 img{max-width: 100%;} 是图片可以适应不同的屏幕
   ```html
   <style>
        *{margin: 0; padding: 0;box-sizing: border-box;}
        img{max-width: 100%;}
    </style>
   ```
## table 标签的用法
table标签是表格在table内只能有三个标签
 ```html
<table>
    <thead></thead>
    <tbody></tbody>
    <tfoot></tfoot>
</table>
```   
* thead 表示这一行是列表表头
* th 表头
* tbody 表示表的主题
* tr 表的一行
* td 表的内容
* tfoot 表的结尾汇总，可以省略
* table_layout: auto 根据表的内容预测表的宽度
                fixed 根据表的内容定制宽度
* border -collapse 控制body是否合并
         -spacing 控制body的距离   
```html
<style>
        table{
            table-layout: fixed ;
            border-spacing: 0;
            border-collapse: collapse;
        }      
    </style>
```
## 其他标签
### form标签 表单标签
* 作用发出get或者post请求然后刷新页面
* 属性：action 发出请求的目标是那个页面
        method 指定是用get或post发出请求
        autocomplete 在输入框输入时自动给出一些建议
        target 告诉游览器将请求提交到那个页面刷新
* 事件 onsubmit 点击提交时触发
* 注意form内必须有一个type = “submit”的标签才可以提交
  ```html
   <form action="/yyy" method="post" 
    autocapitalize="on" target="_blank">
        <input name=username type="text">
        <button type="submit">提交</button>
    </form>
  ```
### input标签 文本输入标签
  * 作用:让用户输入内容
  * 属性：type= button 按钮 color指定颜色 password密码
                checkbox多选框 radio单选框 将name设为一样就可以完成多选或单选
                file 选择文件 textarea 多行文本输入编辑
                hidden 隐形的，但他的值还是会提交
          其他： name 表示标签的名字
                autofocus 加载时自动聚焦这个标签
                vule 这个标签的值可以一起提交
    ```html
    <input type="button"  />
    <input type="color"  />
    <input type="password"  />
    <input type="file" multiple />
    <input type="hidden"  />看不见的input
    ```
* 事件：onchange：鼠标点击 onfocus 焦点聚集 onblur 鼠标移出
* 验证器：required 提交验证，未完成表单无法提交
  ```html
    <input type="text" required> 
    <button type="submit">提交</button>
   ```
* 注意所有form里的input都要有name
  
### select选择框
* select + option 下拉选择框
  ```html
  <select>
        <option value="1">星期一</option>
        <option value="2">星期二</option>
    </select>
  ```

## 关于标签的兼容性一定要查看文档