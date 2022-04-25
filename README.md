# 说明：

学一下一些动画demo，我会重写作者的案例

欢迎支持原作者：https://gitee.com/wyanhui02/html_css_demo.git

# 疑问：

## 1.vh和vw使用场景

# 导航栏

## 案例3：伸缩式导航栏

这个东西看起来很难，但是用到的方法都特别巧妙。想到这方法的人真是天才！明天写写

### 效果：

<img src="https://picture-feng.oss-cn-chengdu.aliyuncs.com/img/133.gif" style="zoom: 100%"></img>

# 登录页

## 案例1：hover效果登录页

### 效果：

<img src="https://picture-feng.oss-cn-chengdu.aliyuncs.com/img/129.gif" style="zoom: 100%"></img>

### 静态：

#### 改变input默认样式

```
		   outline: none; //防拖拽
            background: none; 
            border: none;
```



### JS：

#### 移除元素

remove移除元素和removeChild的区别？



### 动画思想：

#### 1.生成新元素

mouseenter的时候生成一个大圆，leave的时候把圆高宽变为0就行

<img src="https://picture-feng.oss-cn-chengdu.aliyuncs.com/img/128.gif" style="zoom: 100%"></img>

#### 2.关门和开门

生成大圆和消除大圆一定要注意用bool变量控制，防止错乱



# 纯动画

## 案例2：翻转卡片

这个以前写过，还是很简单的喔。

## 效果：

<img src="https://picture-feng.oss-cn-chengdu.aliyuncs.com/img/132.gif" style="zoom: 100%"></img>

### CSS

#### backface-visibility: hidden;

传送门：[backface-visibility:hidden的作用是什么-php教程-PHP中文网](https://www.php.cn/php-weizijiaocheng-96397.html)

通过backface-visibility:hidden;样式，我们可以使一个元素在翻转之后消失，这时可以使用另一个元素放在它的背面，从而制作出一种元素翻转之后出现另一个元素的效果。

### 贝塞尔曲线

自定义运动轨迹

# 轮播图

## 案例61：纯CSS实现轮播图

### 效果：

<img src="https://picture-feng.oss-cn-chengdu.aliyuncs.com/img/130.gif" style="zoom: 100%"></img>

### CSS：

#### :checked选择器

传送门：

[CSS3 :checked 选择器 | 菜鸟教程 (runoob.com)](https://www.runoob.com/cssref/sel-checked.html)

#### ~选择器

兄弟选择器

‘~’选择器则表示某元素后所有同级的指定元素，强调所有的。

传送门：

[(26条消息) CSS选择器之兄弟选择器（~和+）_HainesFreeman的博客-CSDN博客_css兄弟选择器](https://blog.csdn.net/weixin_41829196/article/details/107024820)

[CSS3 element1~element2 选择器 | 菜鸟教程 (runoob.com)](https://www.runoob.com/cssref/sel-gen-sibling.html)

[input:checked ~ 代表什么意思？_百度知道 (baidu.com)](https://zhidao.baidu.com/question/1926791439354298827.html)

### HTML：

#### label

<label> 标签的 for 属性应当与相关元素的 id 属性相同。

#### radio

name属性一样，即为同一个单选列表

```html
<input type="radio" name="indicator" id="indicator1" checked >
      
<input type="radio" name="indicator" id="indicator2" >
        
<input type="radio" name="indicator" id="indicator3" >

```

#### hidden

传送门：

[“hidden” 属性](https://zh.javascript.info/basic-dom-node-properties#hidden-shu-xing)

用hidden属性可以把标签隐藏起来

### 动画思想：

<img src="https://picture-feng.oss-cn-chengdu.aliyuncs.com/img/131.gif" style="zoom: 100%"></img>

![image-20220425143624291](https://picture-feng.oss-cn-chengdu.aliyuncs.com/img/image-20220425143624291.png)
