# 案例1 用div+css重新布局首页
### div:块标签
### span:行标签
---
### css: 层叠样式表
- 作用:
    - 渲染页面
    - 提高工作效率
- 格式:
  - 选择器{属性:值; 属性1:值1}
- 后缀名:
  - .css
- 使用方式:
  - 内联样式表 通过标签style属性设置样式
  - 内部样式表 例如通过head标签的style字标签导入
    ```
    <style>
        #divId2{
                background-color: #0f0;
        }
    </style>
    ```
  - 外部样式表: ```<link rel="stylesheet" href="css/1.css" type="text/css">```

- 选择器:
    - id选择器
        - 要求 html元素必须有id属性且有值
        - css中通过"#"引入,后面加上id值
    - class选择器
        - 要求必须有class属性且有值
        - css通过"."引用,后面加上class值
    - 元素选择器
        - 直接用元素名即可
    - 派生的选择器
        - 属性选择器
        - 后代选择器
    - 锚伪类选择器   超链接的点击移动变色
        - 未访问的链接
        - 已访问的链接
        - 鼠标移到连接上
        - 选中的链接

  - 选择器使用小结:
    - id选择器:一个元素(标签)
    - class选择器:一个类元素
    - 元素选择器: 一种元素
    - 属性选择器:元素选择器的特殊用法
  - 使用的时候注意:
    - 多个样式用一个元素师,不同的样式会叠加,相同的样式就近原则
    - 多个选择器作用于一个元素的时候,越特殊,优先级越高 id优先级最高
- 属性
    - 字体
        - font-family: 设置字体(宋体) 设置字体家族
        - font-size: 设置字体大小
        - font-style:  斜体/粗体
    - 文本
        - color:
        - line-height: 行高
        - text-decoration: none underline
        - text-align: 对齐文本
    - 列表
        - list-style-type: 列表项类型 实心圆 空心圆
        - list-style-image: 设置图片为列表项类型
    - 背景
        - 
    - 尺寸
        - 
    - 浮动
     - 分类
