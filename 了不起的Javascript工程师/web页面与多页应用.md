# 2.6 CSS布局

## 问题

1. 外边距合并规则
2. 问题2
3. 问题3

### 1. 外边距合并规则

```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <meta http-equiv="X-UA-Compatible" content="ie=edge">
        <title>Document</title>
        <style>
            div {
                background-color: pink;
                margin-bottom: 100px;
                width: 100px;
                height: 100px;
            }
            .box2 {
                margin-top: 100px;
            }
        </style>
    </head>
    <body>
        <div class="box1"></div>
        <div class="box2"></div>
    </body>
    </html>
```
> 上边这段代码创建了两个边长为100的正方形元素，每个元素的下边距均为100px，第二个元素上边距为100px，那么两个元素之间的距离是多少？100px + 100px = 200px ?  

 
##### 实际效果如下：
![实际效果如下：](https://github.com/Veramin/Image-Gallery/blob/master/images/01/1.png?raw=true)

##### 解释：
**外边距合并规则，这是从css的规则**
**如何让外边距不会被合并？修改其中的一个块级元素，让其变为内建元素或者浮动元素即可。**
