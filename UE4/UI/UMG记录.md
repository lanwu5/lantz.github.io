

# WidgetSwitch //24.3.1
  - 所属层级的UI添加到ViewPort是，Switcher子项UI会进行Construct；且来回进行Switch时，不会触发子项UI的Construct


# ScrollBox //24.3.8
  - 不能滚动：需要Fill模式而不是Auto，其中Fill诺被Hor或Ver之类的包裹，则要求父为Fill模式

# Border //24.3.13
 
![image](https://github.com/lanwu5/lantz.github.io/assets/42904565/b3eae2de-4dfb-4bf9-b0df-f2dbcc1da32c)
对准Border去对其的，结果发现有偏移，原因是Border的DrawAsImage中应该设置为

![image](https://github.com/lanwu5/lantz.github.io/assets/42904565/378779d5-edf2-4a43-8671-88007620602d)



# Common-RenderScale //24.3.20
  - ![image](https://github.com/lanwu5/lantz.github.io/assets/42904565/24f44f0b-9f9b-4924-a451-0f6c7259cb20)

# Design RemoveFromparent //24.3.30
  -  抽象到父类并封装一个RemoveFromParent回调，默认UserWidget只提供了VisbilityChanged的回调


# 业务坑 //24.3.21 移除元素
![image](https://github.com/lanwu5/lantz.github.io/assets/42904565/64c4934a-c2a3-4339-864d-a2280339f38b)

# Common-成员函数比PreConstruct先执行//24.3.27 （执行流程）
![image](https://github.com/lanwu5/lantz.github.io/assets/42904565/8873bf3b-21b7-4e28-a349-95d41a214cca)
  - 原因是：外部CreateWidget后，先调用函数，后调用的AddChild（VerticalBox）

# 业务坑 //24.3.27 （执行流程）
![image](https://github.com/lanwu5/lantz.github.io/assets/42904565/c39dd7c4-524f-4e71-8690-44b2890b3617)
解决：先SetStyle

# UI坑 //24.5.11
  - 为什么UE4中 UI ScreenSize设定了Custom尺寸，但AddToViewPort后，仍然填充满整个屏幕
  - 原因：该UI根为SizeBox
  - 解决：根用Overlay再次包裹SizeBox，并调整SizeBox填充模式为居中


