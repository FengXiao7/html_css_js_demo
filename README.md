# 说明：

学一下一些动画demo，我会重写作者的案例

欢迎支持原作者：https://gitee.com/wyanhui02/html_css_demo.git

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
