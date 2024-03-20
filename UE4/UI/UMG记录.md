

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

