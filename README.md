Griddy
======

使用同一个标签结构，可以变成40+中不同的分栏布局，这就是__Griddy__。


#### html 结构


```html
<div class="row">
    <div class="main">
        <div class="wrap">
            <!-- 主栏 -->
        </div>
    </div>
    <div class="sub">
            <!-- 侧栏 -->
    </div>
    <div class="extra">
            <!-- 附件 -->
    </div>
</div>
```

__Griddy__主要是针对我们常见的二分栏和三分栏，利用浮动和负margin技术，来达到不同布局。无论哪一种布局，使用的标签结构都是一样的。


#### css

__Griddy__中包含的分栏布局主要有三类

1. 百分比布局
2. 流式布局
3. 固定宽度布局
3. 混合类型布局

```css
.main,
.sub,
.extra {
    float: left;
}

.main {
    width: z;
}

.main .wrap {
    padding-left: x;
    padding-right : y;
}

.sub {
    margin-left: -100%;
    width: x;
}

.extra {
    margin-left: -y;
    width: y;
}
```

根据不同类型的布局，设计css中的_{z}_, _{x}_, _{y}_，如：

* 百分比布局：100%, 30%, 40%
* 流式布局：100%, 200px, 300px
* 固定宽度布局：990px, 200px, 300px
* 混合类型布局：...
