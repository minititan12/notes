## background

+ background-size: width height;

  + 控制背景的宽度和高度

+ background-position

  + 指定背景图像的位置，有两个值

  + 值可以是 left top或者right center以及其他 left right top bottom的组合

    + 如果只指定了一个关键字，其他值为center

  + 百分比数值

    + 一个是水平位置，一个是垂直位置
    + 左上角是0% 0%
    + 默认值是0% 0%

  + 像素值

    + 和百分比效用相差不多，可以和百分比混合使用

+ background-origin

  + 控制背景图像的定位区域

  + border-box

    + 从边框盒开始绘制

  + content-box

    + 从内容盒开始绘制

  + padding-box

    + 从padding（内边距）盒开始绘制

+ background-clip

  + 指定背景图像的绘制区域

  + 有content-box，paading-box，border-box

  + 例如值为content-box，即切除内容盒子外的背景

+ background-attachment

  + 指定背景图像是否固定或者随页面的其余部分滚动
  + fixed
    + 背景图像是固定的
  + scroll
    + 背景随页面其余部分滚动