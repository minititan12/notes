## Flex布局

+ flex容器的属性

  + flex-direction

    + 决定主轴的方向（即项目排列方向）
    + row（默认值）：主轴为水平方向，起点在左端
    + row-reserve：主轴为水平方向，起点在右端
    + column：主轴为垂直方向，起点在上沿
    + column-reverse:主轴为垂直方向，起点在下沿

  + flex-wrap

    + 项目都在一条轴线上，flex-wrap定义如果一条轴线上排不下，如何换行
    + nowrap（默认）：不换行
    + wrap：换行
    + wrap-reverse：换行，第一行在下方

  + flex-flow

    + flex-direction和flex-wrap的简写形式
    + 默认为row nowrap

  + justify-content

    + 定义了项目在主轴上的对齐方式
    + flex-start（默认值）：左对齐
    + flex-end ：右对齐
    + center：居中
    + space-between：两端对齐，项目之间的间隔都相等
    + space-around：每个项目两侧的间隔相等，所以，项目之间的间隔比项目与边框的间隔大一倍

  + align-items

    + 定义项目在交叉轴上如何对齐
    + flex-start：交叉轴的起点对齐
    + flex-end：交叉轴的终点对齐
    + center：交叉轴的中点对齐
    + baseline：项目的第一行文字的基线对齐
    + stretch（默认值）：如果项目未设置高度或者设为auto，将占满整个容器的高度

  + align-content

    + 定义了多根轴线的对齐方式，如果项目只有一根轴线，该属性不起作用
    + flex-start：与交叉轴的起点对齐
    + flex-end：与交叉轴的终点对齐
    + center：与交叉轴的中点对齐
    + space-between：与交叉轴两端对齐，轴线之间的间隔平均分布
    + space-around：每根轴线两侧的间隔都相等。所以，轴线之间的间隔比轴线与边框的间隔大一倍。
    + stretch（默认值）：轴线占满整个交叉轴

+ flex项目（item）的属性

  + order
    + 定义项目的排列顺序
    + 默认为0
    + 数值越小，排列越靠前
  + flex-grow
    + flex项目的扩张系数
    + 默认值为0
    + 当同一根main轴线上项目flex-grow值的和超过1
      + 则通过各自项目系数的占比平分剩余空间
    + 当同一根main轴线上项目flex-grow值的和不超过1（如0.5）
      + 则通过各自项目系数的占比平分剩余空间的0.5
  + flex-shrink
    + flex项目的收缩系数
    + 默认值为1
    + 当同一根main轴线上项目flex-shrink值的和超过1
      + 则需要项目的宽度乘于自身的flex-shrink，得出项目间收缩的比值，最后按比值平分需要收缩的数值
    + 当同一根main轴线上项目flex-shrink值的和不超过1
      + 则项目需要收缩的数值只是超出部分乘于flex-shrink值的和，最后按各自宽度乘于flex-shrink值的比值平分
  + flex-basis
    + 定义了在分配多余空间之前，项目占据的主轴空间（main-size）
    + 浏览器根据这个属性，计算主轴是否有多余空间
    + 默认值为auto，项目本来大小
  + align-self
    + 允许单个项目和其他项目有不一样的对齐方式
    + 可以覆盖align-items属性
    + 默认为auto，即继承父元素的align-items属性，如果没有父元素，则等同于stretch
  + 匿名文本也能成为一个flex项目
  + margin都不会合并，为auto时会把项目顶开

