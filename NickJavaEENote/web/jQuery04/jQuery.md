# jQuery 介绍
- 传统使用js获取对象的方法
```
    var obj=document.getElementById("id");
    
    funtion getId(id){
        return document.getElementById("id");
    }
```
- jQuery 获取对象

    ```
    $("选择器')===>获取元素
    ```

### js类库
- 对常用的方法和对象进行封装,方便我们使用.


---
### jQuery 和html 的整合
- jQuery 是单独的js对象, 通过script 标签的src属性导入即可
- 注意: 2.0版本 不支持 IE 6.7.8   所以使用 1.11.0
- 集成方法
```
<script src="jquery位置"></script>
```
- 获取方法
    - js原生  alert(document.getElementById("username").value)
    - jquery 获取     var $username = $("#username")
    - alert($username.val());
    - 注意!!!  jQuery对象 有其特有的方法, 不要和dom对象混用     val()/value 并不相同
    - jquery 与 dom 转换   $(dom对象)      $jquery对象.get(index)
- 页面加载
    - js:  window:onload=function(){}       //页面中只能出现一次
    - jquery:
        - 方式一   $(funciton(){...});   //一个页面中 可以使用多次
        - 方式二   $(document).ready(funciton(){...});

- 派发事件
    - $("选择器").click(function(){...})   等价于 原生  dom对象.onclick=function(){...}
- jquery 中效果:
    - 隐藏或展示  show(毫秒)  hide(毫秒)
    - 滑入滑出  slideDown(毫秒): 向下滑入  slideUp(毫秒): 想上滑入
    - 淡入淡出   fadeIn(int)  fadeOut(int)
---
### jQuery
- 案例1 弹出广告
- 技术
    - 定时器
    - jQuery
- 步骤分析
  1. 页面加载成功之后$(function(){...}) 开始一个定时器 setTimeout();
  2. 编写展示广告方法
    - 获取div,然后调用效果放阿飞
    - 设置另一个定时器 隐藏

  3. 编写隐藏广告的方法
    - 获取div 然后调用效果方法

---
### 选择器总结
- 基本选择器 $("#id值") $(".class值") $("标签名")
    - 了解 : $("*")  选择全部
    -  理解: 多个选择器 用逗号隔开  $("#id值,.class值")

- 层次选择器
    - a b   : a的所有b后代
    - a>b   : a的所有b孩子
    - a+b   : a的下一个兄弟(大弟弟)  "同级 下一个"
    - a~b   : a的所有弟弟
- 基本过滤选择器:
    - first 第一个  $("div:first").css("background-color","#0f0 ")
    - last 最后一个
    - odd 索引为奇数
    - even 索引为偶数
    - eq(index) 指定索引
    - gt(index) 大于指定索引
    - lt(index) 小于指定索引
- 内容过滤:
    - has("选择器"): 包含指定选择器的元素
- 可见过滤:
    - hidden 在页面不展示元素 一般指 input type="hidden"
    - visible 在页面中所有可见元素
- 属性过滤器:
    -      [属性名]
    -      [属性名=属性值 ]
- 表单过滤:
  	-	:input  所有的表单子标签  input select textarea button
  	-	//input
  	- :enabled   可用的
    - :disabled  不可用
    - :checked 	选中的(针对于单选框和复选框的)
    - ★:selected 	选中的(针对于下拉选)





























