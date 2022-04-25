# 说明：

学一下一些动画demo，我会重写作者的案例

欢迎支持原作者：https://gitee.com/wyanhui02/html_css_demo.git

# 疑问：

## 1.vh和vw使用场景

# 案例1：hover效果登录页

## 效果：

<img src="https://picture-feng.oss-cn-chengdu.aliyuncs.com/img/129.gif" style="zoom: 100%"></img>

## 静态：

### 改变input默认样式

```
		   outline: none; //防拖拽
            background: none; 
            border: none;
```



## JS：

### 移除元素

remove移除元素和removeChild的区别？



## 动画思想：

### 1.生成新元素

mouseenter的时候生成一个大圆，leave的时候把圆高宽变为0就行

<img src="https://picture-feng.oss-cn-chengdu.aliyuncs.com/img/128.gif" style="zoom: 100%"></img>

### 2.关门和开门

生成大圆和消除大圆一定要注意用bool变量控制，防止错乱

# 案例61：纯CSS实现轮播图

## 效果：

<img src="https://picture-feng.oss-cn-chengdu.aliyuncs.com/img/130.gif" style="zoom: 100%"></img>

## CSS：

### :checked选择器

[CSS3 :checked 选择器 | 菜鸟教程 (runoob.com)](https://www.runoob.com/cssref/sel-checked.html)

### ~选择器

兄弟选择器

‘~’选择器则表示某元素后所有同级的指定元素，强调所有的。

[(26条消息) CSS选择器之兄弟选择器（~和+）_HainesFreeman的博客-CSDN博客_css兄弟选择器](https://blog.csdn.net/weixin_41829196/article/details/107024820)

[CSS3 element1~element2 选择器 | 菜鸟教程 (runoob.com)](https://www.runoob.com/cssref/sel-gen-sibling.html)

[input:checked ~ 代表什么意思？_百度知道 (baidu.com)](https://zhidao.baidu.com/question/1926791439354298827.html)

## HTML：

### label

<label> 标签的 for 属性应当与相关元素的 id 属性相同。

### radio

name属性一样，即为同一个单选列表

```html
<input type="radio" name="indicator" id="indicator1" checked >
      
<input type="radio" name="indicator" id="indicator2" >
        
<input type="radio" name="indicator" id="indicator3" >

```

## 动画思想：

<img src="https://picture-feng.oss-cn-chengdu.aliyuncs.com/img/131.gif" style="zoom: 100%"></img>

![image-20220425143624291](https://picture-feng.oss-cn-chengdu.aliyuncs.com/img/image-20220425143624291.png)
