[合集 \- manim(37\)](https://github.com)[1\.【manim动画教程】\-\- 安装2023\-03\-28](https://github.com/wang_yb/p/17264724.html)[2\.【manim动画教程】\-\- 基本图形2023\-03\-29](https://github.com/wang_yb/p/17269340.html)[3\.【manim动画教程】\-\- 坐标系2023\-04\-10](https://github.com/wang_yb/p/17301528.html)[4\.【manim动画教程】\-\- 文本样式2023\-04\-07](https://github.com/wang_yb/p/17294918.html)[5\.【manim动画教程】\-\- 文字和公式2023\-04\-04](https://github.com/wang_yb/p/17285467.html)[6\.【manim动画教程】\-\- 图形样式2023\-03\-31](https://github.com/wang_yb/p/17275154.html)[7\.【manim动画教程】\-\-相机2023\-04\-19](https://github.com/wang_yb/p/17334029.html)[8\.【manim动画教程】\-\-高级动画效果2023\-04\-14](https://github.com/wang_yb/p/17317576.html)[9\.【manim动画教程】\-\-常用动画效果2023\-04\-12](https://github.com/wang_yb/p/17309865.html)[10\.【manim】之滚动字幕2022\-12\-06](https://github.com/wang_yb/p/16955924.html)[11\.【manim】之圆规动画2023\-01\-31](https://github.com/wang_yb/p/17079903.html)[12\.【manim】之目录动画2023\-02\-28](https://github.com/wang_yb/p/17163051.html)[13\.manim边学边做\-\-DecimalNumber06\-12](https://github.com/wang_yb/p/18243662)[14\.manim边学边做\-\-Integer06\-13](https://github.com/wang_yb/p/18245670)[15\.manim边学边做\-\-Variable06\-14](https://github.com/wang_yb/p/18248823)[16\.manim边学边做\-\-Title06\-20](https://github.com/wang_yb/p/18258229)[17\.manim边学边做\-\-BulletedList06\-21](https://github.com/wang_yb/p/18261017)[18\.manim边学边做\-\-SingleStringMathTex06\-23](https://github.com/wang_yb/p/18264154)[19\.manim边学边做\-\-MathTex06\-28](https://github.com/wang_yb/p/18272507):[豆荚加速器](https://yirou.org)[20\.manim边学边做\-\-Tex07\-01](https://github.com/wang_yb/p/18278554)[21\.manim边学边做\-\-Text07\-04](https://github.com/wang_yb/p/18284013)[22\.manim边学边做\-\-Paragraph07\-09](https://github.com/wang_yb/p/18291657)[23\.manim边学边做\-\-MarkupText07\-10](https://github.com/wang_yb/p/18294000)[24\.manim边学边做\-\-Code07\-16](https://github.com/wang_yb/p/18304450)[25\.manim边学边做\-\-Matrix07\-17](https://github.com/wang_yb/p/18307871)[26\.manim边学边做\-\-Table07\-25](https://github.com/wang_yb/p/18322456)[27\.manim边学边做\-\-点08\-09](https://github.com/wang_yb/p/18351279)[28\.manim边学边做\-\-圆形类08\-15](https://github.com/wang_yb/p/18361469)[29\.manim边学边做\-\-圆弧形08\-20](https://github.com/wang_yb/p/18368851)[30\.manim边学边做\-\-直线类08\-22](https://github.com/wang_yb/p/18374417)[31\.manim边学边做\-\-带箭头直线09\-02](https://github.com/wang_yb/p/18392446)[32\.manim边学边做\-\-曲线类09\-04](https://github.com/wang_yb/p/18396028)[33\.manim边学边做\-\-角度标记09\-07](https://github.com/wang_yb/p/18401449)[34\.manim边学边做\-\-常用多边形09\-10](https://github.com/wang_yb/p/18406455)[35\.manim边学边做\-\-通用多边形09\-13](https://github.com/wang_yb/p/18411587)[36\.manim边学边做\-\-弧形多边形09\-15](https://github.com/wang_yb/p/18415355)37\.manim边学边做\-\-空心多边形09\-21收起
空心的多边形`Cutout`是一种比较特殊的多边形，主要用于解决与形状、大小、位置等相关的数学问题。


`Cutout`多边形可以定义物体表面的**空洞**或**凹陷**部分，从而更准确地模拟现实世界中的复杂形状。


比如，在`PCB`（印制电路板）设计中，通过放置`Cutout`空心的多边形，设计师可以精确地控制铜的覆盖区域，从而优化电路布局和信号完整性。


在机械加工时，`Cutout`多边形也可以用于指导切割工具的运动轨迹，以便于在材料上形成精确的空洞或凹槽。


其实，在我们上学期间学习几何时，也经常遇到`Cutout`多边形，只是它一般不以`Cutout`这个名称出现。


比如，计算复杂图形的面积时，经常将其分割成几个简单的多边形（如三角形、矩形等），然后分别计算；


在证明两个图形面积相等、两线段相等或两角相等时，有时需要构造辅助线或辅助图形，这实质上也是一种“cut out”操作。


`manim`中虽然也可以通过组合前面几篇文章中提及的几何图形对象来构造`Cutout`图形，


但是直接用其`manim`提供的`Cutout`对象则更简单方便。


# 1\. 主要参数


`Cutout`对象的主要参数就两个。




| **参数名称** | **类型** | **说明** |
| --- | --- | --- |
| main\_shape | VMobject | 被切割的主体形状 |
| mobjects | \*VMobject | 从main\_shape中切割出的一个或多个小形状 |


# 2\. 使用示例


`Cutout`使用起来比较简单，下面的通用示例中展示空心多边形的使用方式，


其余几个例子演示的是`Cutout`在一些常见几何题目中的应用。


## 2\.1\. 通用示例


通用示例中，演示`Cutout`的使用方式，在一个大的四边形中切出三角形，四边形，五边形和六边形。



```
main = Square()scale(2)
sub1 = Triangle().scale(0.5)
sub2 = Square().scale(0.5)
sub3 = RegularPolygon(5).scale(0.5)
sub4 = RegularPolygon(6).scale(0.5)

Cutout(
    main,
    sub1,
    sub2,
    sub3,
    sub4,
    fill_opacity=1,
    color=BLUE,
    stroke_color=YELLOW,
)

```

![](https://img2024.cnblogs.com/blog/83005/202409/83005-20240921112103894-462678215.gif)


## 2\.2\. 矩形中的三角形


求解矩形中的一个三角形的面积是常见的题型，利用`Cutout`，可以构造矩形中“切割”一个三角形的效果。



```
points = [A, B, C, D]
sub_points = [D, F, E]
main = Polygon(*points)
sub = Polygon(*sub_points)

Cutout(
    main,
    sub,
    fill_opacity=1,
    color=BLUE,
    stroke_color=GREEN,
)

```

![](https://img2024.cnblogs.com/blog/83005/202409/83005-20240921112103889-567629181.gif)


## 2\.3\. 圆的切线


圆的切线相关问题也一样，可以沿着切线进行“切割”。


下面的示例中，沿着小圆的切线切割了一个三角形。



```
main = Polygon(A, P, B, O)
sub = Polygon(A, P, O)
Cutout(
    main,
    sub,
    fill_opacity=1,
    color=BLUE,
    stroke_color=GREEN,
)

```

![](https://img2024.cnblogs.com/blog/83005/202409/83005-20240921112103872-281241641.gif)


## 2\.4\. 梯形的中位线


梯形的中位线定理证明中，关键就是两个全等三角形的全等，


下面的示例将梯形的其他部分“切割”掉，只保留两个全等三角形。



```
main = Polygon(A, B, F, G, D)
sub = Polygon(A, F, C, D)

Cutout(
    main,
    sub,
    fill_opacity=1,
    color=BLUE,
    stroke_color=GREEN,
)

```

![](https://img2024.cnblogs.com/blog/83005/202409/83005-20240921112103849-1645163241.gif)


# 3\. 附件


文中完整的代码放在网盘中了（`cutout.py`），


下载地址: [完整代码](https://github.com) (访问密码: 6872\)


