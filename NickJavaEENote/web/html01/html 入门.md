#  网站信息展示
- 需求
    - 在页面展示文字
- 技术分析
    - html 超文本标签语言
- - -
- html
  - 作用: 展示
  - 超文本: 超越了一般文本,描述文字的字体 颜色 图片
  - 标签: 标记
  - 书写规则:
    - 文本的后缀 .html
    - 标签必须用<> 引起来
    - 属性 格式 key="value" 建议属性的值用引用引起来.不徐芬大小写
  - 注意:
    - 最好将所有内容放到一个```<html></html>```中
    - 有开始标签和结束标签称为围堵标签
    - 没有结束的标签称为空标签```<br/>```
    - 开始标签和结束标签之间的内容称为标签体
    - ```<!--注释内容-->``` 注释
    - 标签必须正常嵌套
    - 标签最好关闭
```
        html标签:
                声明
                字标签:
                    <head></head>
                    <body></body>
                head: 用来存放当前页面的重要信息，一般不展示在html页面上
                    常见的字标签：
                    <title></title> 网页的标题
                    <mete></meta> 源  
                    编码,关键词,描述(搜索相关)
                body: 用来存放展示的数据
                    
```

#### 标签介绍
- ```<h1> - <h6>```标题  从大到小 自动换行 留白 默认加粗
    - 常用属性: align:对齐方式   left左  center中  right右
    - 格式  ```<h2 align="center"></h2>```
- 字体标签 ```<font></font>```
    -常用属性 face 字体  size  尺寸  color 颜色
- 颜色取值
    - #xxxxxx  x为16进制
    - 英文单词
- 段落标签
    ```<p></p>```
- 其他标签
    - ```<b></b><strong></strong>``` 加粗
    - ```<i></i>```斜体
- 水平线 ```<hr/>```

- 换行 ```<br/>```

- 图片: ```<img/>```
    - 常用属性: src: 图片路径  alt 代替文字  title 移上去显示的文字  width 宽 height 高
    -  大小的写法: 像素:123px 百分比: 20%
    -  路径的写法:
        - 相对路径 ./ 或者  什么都不写  当前目录    ../ 上级目录
        - 绝对路径 带协议的绝对路径:  http://www.itheima.com
- 列表
    -  ```<ol></ol>```有序列表
    -  ```<ul></ul>```无序列表 ```<li></li>```
        -  type 图标类型  disc square
- 超链接标记 ```<a>```
    - 常用属性 href 超链接地址
        - target 在哪里打开 _blank 空白的页面  (新建页面)
        - target # 当前页面
        - 默认 _self 自身打开
- 表格标签  ```<table></table>```   子标签 ```<tr>```
    - ```<tr>``` 常用子标签 ```<td>```列
    - 注意 : 一行必须只有一个单元格或者列
    - table 的常用属性
        - border 边框 像素值
        - bgcolor 背景色
        - align  表格位置   left right center
    - tr 的常用属性
        - align
    - td 的常用属性
        - align
        - colspan 跨列合并
        - rowspan   跨行合并
- 表单标签 ☆☆☆
    - 常见属性
        - action 信息提交的路径 默认是当前页面
        - method 表单提交的方式 get/post  默认是get
        - get 和 post 的区别
            1. get会把所有请求追加在地址栏上, post 请求不会
            2. get 请求参数大小有限制,post 请求大小参数大小没有限制
            3. post 相当于 get更加安全


    - input
        - 常见标签
        - type
            - text 文本框
            - password 密码框
            - radio 单选
            - checkbox 多选
            - file
            - submit 提交
                - 点击提交时地址栏会发生变化 产生提交到服务器的内容  格式: key=value&
                - 对于文本框 密码框 文本域 手写的内容传递过去了
                - 对于单选框和多选框来说,却没有把值传递过去,想要把值传递过去,必须设置value属性
            - reset 重置
            - button 普通按钮
            - hidden 隐藏域  在页面上不显示 但是提交的时候可以提交上去
            - image 图片提交
        - name
            - 可以将几个单选框或者复选框 设置成一组
            - 信息要保存到服务器上必须要有name属性
        - readonly  只读,无法修改
        - disabled  无法使用
    - select
        - 子标签 option
        - 下拉选择要把选择的内容传递上去,则需要给每个option加上value
    - textarea


### 后台页面入门
- 页面分析  开发一个后台管理页面需要通过 frameset 实现
    - frameset 框架集  **注意:** body 与 framest 最好不共存  谁在上面谁显示
        - 常见属性
            - cols 垂直切割
            - rows 水平切割
        - 常见的子标签   frame
    - frame 具体实现 在frameset 中展示
        - 常见属性 src 类似于item布局
    - 例子:
    ```
    <frameset cols = "40%",*,10%>
        <frame/>
        <frame/>
        <frame/>
    </frameset>
    ```
    - 在frame 中点击 超链接 如何 更换另一个frame 的内容
    - 在目标frame 中 设置name属性  源frame 设置target 为 目标 name属性

---
#### 转义字符
- 转义字符分三部分  &实体;
    - &gt great then   >
    - &lt <
    - &amp &
    - &nbsp
#### 元信息
- ```<meta charset="UTF-8">``` 制定浏览器用什么编码打开此页面






















