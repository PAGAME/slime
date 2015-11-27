# 1 chapter
## 1.1 scenario1 场景1
此处是注释部分
不带“\*”的部分不会被解析，只有"\*"列表会被翻译成可执行的部分。

* 某个人！： Hello world！
上一句会被翻译为一个对话（这一句仍然是注释）

其他形式则会被当做普通语句（特殊形式，或函数）
特殊形式：if when choice text seq
* if [flag_a]
  * A?： hi, I'm fine.
  * B?： en, let me see.
* if [flag_3]
  * 阿什顿发的说法
  * asdfasdf
不是对话，也不是特殊形式的会被当做函数调用，如果调用不成功则跳过
函数调用直接根据名称和参数调用，例如
* music music1

## 1.2 scenario2 场景2
实例1：
* 娜谢塔尼娅？：逮到了吗？
* 亚德雷~：……想得美。要想一击夺命，你就应该放安静点
* 亚德雷！：加点油吧！地表最强的男人，是不会被这点雕虫小技逮到的！
* text 亚德雷此刻正伸手捂着右臂。从容的口吻也不过是装腔作势，藉此隐瞒自己负伤的事实罢了。
text 亚德雷一边跑，一边看着自己手背上头的奇特纹章。
* 亚德雷！：我岂能死在这儿……身为六花勇者，我岂能在这种地方丧命。
* choice
  * 选项1，左转
  * 执行选项1，（可以在此处写多条对话，或跳转到其他部分）
  * 选项2，右转
  * 执行选项2

## 1.3 特殊形式
顺序执行
* seq
  * ...
  * ...
  * ...

按条件执行
* if 条件（字符串，或者数组）
  * 如果为真，执行此行
  * 如果为假，执行此行

判断条件，同if，为真时执行多行，为假时跳过
* when 条件（字符串，或者数组）
  * ...
  * ...
  * ...

基本和when相同，特殊处理条件判断
* flag 字符串条件
  * ...
  * ...
  * ...
