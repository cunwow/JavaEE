# javascript
JavaScript 是一种直译式脚本语言,是一种动态类型,弱类型,基于原型的语言,内置支持类型.他的解释器被称为JavaScript引擎,为浏览器的一部分.
### 组成部分
- ECMAScript: js基础语法(规定 关键字 运算符 语句 函数...)
- BOM:浏览器对象模型
- DOM:文档对象模型

### 作用
- 修改html页面内容
- 修改html样式
- 完成表单验证

### 注意
- js可以在页面上直接写,也可以单独出去
- js文件的后缀名 .js

### js和html 整合
- 方式1: 在页面上直接写 将js代码放在 script标签中
- 方式2: 独立的js文件 通过script标签的src属性导入

### js中变量的声明
- var 变量名 = 初始化值;
- 注意: 最后一个分号可以省略,最好不要省略;

### js的数据类型
- 原始类型(5种)
    - Null
    - String
    - Nubmer
    - Boolean
    - Undefined
- typeof 可以查看变量的类型

### js:事件驱动
- 函数定义格式:
    - 方式1:
    ``` function 函数名(){
            函数体;
         }
    ```
    - 方式2:
    ```
    var 函数名 = function(参数){
        函数体;
    }
    ```
    - 注意: 函数不用声明返回值类型 参数不需要加类型 函数调用的时候 直接
    函数名(参数)

- js中的事件:
    - 单击: onclick
    - 表单提交: onsubmit
    - 页面加载: onload

- js 事件的函数的绑定:
  - 方式1: 通过把标签的事件属性 <xxx onclick="函数名(参数)"></xxx>
  - 方式2: 给元素派发事件 document.getElementById(id
    ).onclick=function(参数){...}
  - 注意: 内存中应该存在该元素才可以派发事件


- js获取元素:
  - document.getElementById（"id值"）;
  - 获取元素的value值  obj.value;
  - 获取元素的标签体重的内容 obj.inerHTML

---
### 案例3 轮播图片
- 需求:
    - 每隔三秒图片更新一下
- 技术分析:
    - BOM中window对象的定时器方法
- 定时器:
    - var id = setInterVal(code,毫秒数): 每隔指定的毫秒数 执行一次函数
    - var id = setTimeout(code, 毫秒数): 延迟指定的毫秒数之后只执行一次
    - 清除定时器
        - clearInterval(id);
        - clearTimeout(id);
- String 对象
    - 原始类型的String 是一个伪对象 可以直接调用 String类的方法
- 步骤分析:
  1. 在首页上绑定一个onload事件
  2. 事件绑定的函数中编写一个定时器
  3. 定时器每隔三秒更换图片  imgobj.src="";
### 补充:
- 运算符
    - 比较运算符:
        - 两边都是数字 和 java一样
        - 若一边为数字,一边为字符串形式的数字,将字符串形式转换成数字再进行比较 3>"2"
        - 若一边为数字,另一边为字符串,返回一个false 3>"hello"
        - 两边都是字符串的事件,比较ascii
    - 等性运算符 ==  ===
        - ==:只判断值是否相等
        - ===: 不仅判断值是否相等, 还判断类型是否相当
- 语句:
    - if语句和java一样
    - for while语句和java一样
    - switch 和java一样(区别,switch可以跟字符串.还可以跟变量)
