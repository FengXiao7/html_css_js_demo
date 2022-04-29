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

我做的效果：

<img src="C:\Users\FengXiao7\Pictures\GIF\134.gif" style="zoom: 100%"></img>

### HTML：

#### a标签href javascript:void(0)

我一般都写#

[a标签中href="javacript:;" href="javacript:void(0);" href="#"区别 - 掘金 (juejin.cn)](https://juejin.cn/post/6844903712289193991)

### CSS：

#### opacity: 0隐藏元素

传送门：

[(26条消息) opacity: 0、visibility: hidden、display: none 优劣和适用场景，以及隐藏元素的几种方法_青颜的天空的博客-CSDN博客_opacity:0;](https://blog.csdn.net/a1056244734/article/details/106758350)

博客中说display: none会引起回流和重绘，但我看有些文章又说display: none可以减少回流会重绘啊，有点懵

####    pointer-events: none;

传送门：[pointer-events - CSS（层叠样式表） | MDN (mozilla.org)](https://developer.mozilla.org/zh-CN/docs/Web/CSS/pointer-events)

span覆盖着复选框，鼠标放到span上是点不中复选框的，这个属性就可以解决这个问题，即便鼠标放到span上点击也能选中或取消选中复选框 

#### 多个transition

transition: transform 0.5s ease-in-out,top 0.5s ease-in-out 0.5s;

有执行顺序喔，第四个时间是延迟生效时间喔，不要忘了

#### nth-of-type

我这里用的是nth-of-type，不要忘了它和nth-child的区别喔。

## 动画思想：

![image-20220427015530144](https://picture-feng.oss-cn-chengdu.aliyuncs.com/img/image-20220427015530144.png)

把所有隐藏和过渡去掉的效果：

是不是清楚了很多？hhh

<img src="https://picture-feng.oss-cn-chengdu.aliyuncs.com/img/135.gif" style="zoom: 100%"></img>

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

### 效果：

<img src="https://picture-feng.oss-cn-chengdu.aliyuncs.com/img/132.gif" style="zoom: 100%"></img>

### CSS

#### backface-visibility: hidden;

传送门：[backface-visibility:hidden的作用是什么-php教程-PHP中文网](https://www.php.cn/php-weizijiaocheng-96397.html)

通过backface-visibility:hidden;样式，我们可以使一个元素在翻转之后消失，这时可以使用另一个元素放在它的背面，从而制作出一种元素翻转之后出现另一个元素的效果。

### 贝塞尔曲线

自定义运动轨迹，建议自己在控制台拖。以前图形学还学过，不过忘完了……

## 案例122：高光立体壁画式卡片悬停特效

### 效果：

<img src="C:\Users\FengXiao7\Pictures\GIF\138.gif" style="zoom: 100%"></img>

我做的效果：

<img src="https://picture-feng.oss-cn-chengdu.aliyuncs.com/img/141.gif" style="zoom: 100%"></img>

### CSS：

#### background-size

这个就是设置背景图片大小的喔，以前也记过，可以看看。重点记住cover和contain两种写法

### 动画思想：

#### 旋转：

图片有个小旋转，把旋转中心设为top center就行。hover的时候先往上挪一点，再往外转一点。



#### 白光掠过效果：

这个是真的秒！

```js
 /* 背景渐变(高光效果) */
                background: linear-gradient(300deg,rgba(255,255,255,0) 40%,rgba(255,255,255,0.3) 50%,rgba(255,255,255,0) 60%);
                /* 默认上移出可视范围 */
                transform: translateY(-100%);
                /* 设置过渡 */
                transition: transform 0.85s cubic-bezier(0.165, 0.84, 0.44, 1);
```

hover的时候

```css
transform: translateY(100%);
```

看这个动图就明白了吧~。我们用伪元素装这个渐变色就行，还可以调整角度

<img src="https://picture-feng.oss-cn-chengdu.aliyuncs.com/img/139.gif" style="zoom: 50%"></img>

还有个不容易注意到的动画效果

#### 阴影：

<img src="https://picture-feng.oss-cn-chengdu.aliyuncs.com/img/140.gif" style="zoom: 40%"></img>

有个hover阴影扩散的效果

这个也很简单，hover的时候跟着照片一起转，加上scale放大一点。自己调调还可以适配白光掠过的角度

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

# 搜索

## 案例92：全屏搜索栏

### 效果：

<img src="https://picture-feng.oss-cn-chengdu.aliyuncs.com/img/136.gif" style="zoom: 100%"></img>

### 我做的效果：

<img src="https://picture-feng.oss-cn-chengdu.aliyuncs.com/img/137.gif" style="zoom: 100%"></img>

### CSS

#### clip-path

东西有点多喔，很值得深究。

[觉得自己的页面不够花哨吗，试试clip-path吧 - 掘金 (juejin.cn)](https://juejin.cn/post/7076371912711995423)

### 动画思想：

两个字：隐藏！

这个案例大量使用了隐藏。先看html结构。有两个input框，其中一个是checkbox，另一个是text。

还有3个图标，其中两个搜索图标，一个关闭图标。

```html
<!-- input输入框，隐藏 -->
	<input type="checkbox" id="search_btn" hidden>

    <label for="search_btn" class="search-btn">
        <i class="fa fa-search" aria-hidden="true"></i>
    </label>
    <label for="search_btn" class="close-btn">
        <i class="fa fa-close" aria-hidden="true"></i>
    </label>
    <div class="container">
        <div class="search-box">
            <input type="text" placeholder="请输入..">
            <i class="fa fa-search" aria-hidden="true"></i>
        </div>
    </div>
```

整体来说，页面由两部分组成。

![image-20220428132508552](https://picture-feng.oss-cn-chengdu.aliyuncs.com/img/image-20220428132508552.png)

![image-20220428132535607](https://picture-feng.oss-cn-chengdu.aliyuncs.com/img/image-20220428132535607.png)

简单来说，search图标1(就是第一幅图里的，以下简称s1)和close图标(以下简称c)。通过label绑定了同一个checkbox。

我们点击checkbox会发生什么呢？

```less
// checkbox值改变后
#search_btn:checked {
    // 搜索图标1隐藏
    &+.search-btn {
        display: none;
    }
    // 关闭图标显示
    &~.close-btn {
        display: block;
    }
    //container占满全屏
    &~.container {
        clip-path: circle(100%);
        //搜索框盒子有了宽度
        .search-box {
            width: 500px;
        }
    }
}
```

然后就是两个页面的动画过渡效果。

是通过clip-path完成的。

最开始：

```css
clip-path: circle(40px at 50% 50%);
```

第二个页面：

```less
 //container占满全屏
    &~.container {
        clip-path: circle(100%);
```

