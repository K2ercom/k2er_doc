# 常见问题

## [激活相关FAQ](activation_zh.md)

## 怎么链接手柄、键鼠

K2er支持市面上绝对多数手柄、键鼠。包括支持自带手柄的安卓掌机。

* 蓝牙链接：如果手柄、键鼠支持蓝牙链接，请在手机设置的蓝牙界面中，直接使用蓝牙和这些设备配对。

* 扩展坞链接：如果手柄、键鼠是有线的，或者只有USB适配器，那么请使用扩展坞链接。需要对扩展坞供电，否则无法驱动多个设备。

```bash
[手机] ----线--- [扩展坞] ---线---- [手柄、键鼠]
```

> 注意：部分手柄默认链接方式是`模拟鼠标事件`，此时需要切换手柄的链接方式改成`原生安卓模式`、`PC模式(Xbox)`、`PS模式`、`NS模式(Switch)`
> K2er支持多个设备同时映射：如手柄+鼠标，键盘+鼠标+手柄，手柄+手柄

## 游戏中找不到`悬浮窗`

1. 检查是否已经把游戏添加到K2er中

2. 在手机`游戏模式`（有些叫`游戏空间`）的`游戏列表`中，把游戏移除

> 添加一个不是游戏的app到K2er中，看看是否有悬浮窗

## 按键点击无效，包括鼠标

1. `小米`/`红米`/`黑鲨`/`POCO`手机需要在`开发者选项` -> `USB调试(安全设置)`

> 注意：打开`USB调试(安全设置)`。这个选项打开了才能模拟手指点击。如果开了还不行,需要重启手机。

2. 电脑版K2er：请注意电脑的输入法要切换成英文。

3. 在手机K2er设置中【重启激活服务】。

4. 重启手机再试试。

5. 如果以上还不行，可能是手机中的`游戏模式`问题，把游戏移除出`游戏模式`。

## 射击类游戏如何鼠标控制任务视角（隐藏鼠标）

按键配置时需要添加一个`瞄准模式`，用来模拟手指按下后控制人物视角移动的手指。默认快捷键是`鼠标中键`。

> 注意：一般情况下，`瞄准模式`要放在屏幕的右边，并且不要放在有弹出框出现的地方。

## 使用手柄右摇杆瞄准时，镜头自动向一个方向移动

请在右摇杆的详细设置中，把`死区`调大。

## 组合键如何使用

K2er支持2种方式的组合键。

* Mod+Key：按住Mod键后，保持不放，再按下Key键，例如，`Ctl+1`，`L1+A`
   - 键盘Mod键：Ctl，Sht，Alt，Win，↑←↓→
   - 手柄Mod键：L1，L2，L3，R1，R2，R3，Select，Start，Mode
   
* Key1&Key2：同时按下任意2个键，例如，`A&B`，`L1&L2`

## `宏`如何使用

`宏`有最少1个`轮转状态`，每个`轮转状态`下都可以设置：`按键按下时`、`按键松开时`、`循环时`的`命令`。

* `轮转状态`: 每按一次`宏`的快捷键，就会自动切换到下一个`轮转状态`。到最后一个`状态`后，会返回第一个`状态`
    * `按键按下时`: 当`宏`的快捷键按下的一刹那发生执行的`命令`列表
    * `按键松开时`: 当`宏`的快捷键松开的一刹那发生执行的`命令`列表
    * `循环时`: 
        * `按下循环`: 当`按键按下时`的命令完结后，就执行循环执行`循环时`的命令，直到快捷键松开
        * `松开循环`：当`按键松开时`的命令完结后，就执行循环执行`循环时`的命令，直到`中断快捷键`按下或出现`中断命令`
* `命令`:
    * `点击命令`: 单击一下指定的位置，命令耗时30ms
    * `快捷键命令`: 触发其他快捷键，比如`鼠标右键`，`键盘A`，注意：有按下（↓），就要有松开（↑）。
        * `按下（↓）`: 触发快捷键按下，命令耗时0ms
        * `松开（↑）`: 触发快捷键松开，命令耗时0ms
        * `按下并松开（↓↑）`触发快捷键按下并松开，命令耗时30ms
    * `延迟命令`: 等待x毫秒
    * `瞄准模式命令`: 开启或者关闭`瞄准模式`
    * `切换场景命令`: 可以变更当前的`场景`
    * `中断命令`: 中断当前`宏`的所有命令，并且设置`轮转状态`为第一个

#### 使用例子
* 射击游戏打开和关闭背包

成品效果点击Tab键时，模拟点击背包（位置1），并且关闭瞄准模式，显示鼠标。
再按一次Tab键时，模拟点击关闭背包（位置2），并且开启瞄准模式，隐藏鼠标。

> `宏`快捷键: Tab
> * 轮转状态1
>   * 按键按下时
>       1. [点击命令] 点击位置1
>       2. [瞄准模式命令] 关闭
> * 轮转状态2
>   * 按键按下时
>       1. [点击命令] 点击位置2
>       2. [延迟命令] 300毫秒
>       3. [瞄准模式命令] 开启

* 临时释放鼠标指针

成品效果点击Alt键时，关闭瞄准模式，显示鼠标。松开Alt键时，开启瞄准模式，隐藏鼠标。

> `宏`快捷键: Alt
> * 轮转状态1
>   * 按键按下时
>       1. [瞄准模式命令] 关闭
>   * 按键松开时
>       1. [瞄准模式命令] 开启

* 用宏来实现蓄力长按

成品效果：按下宏快捷键C后，自动长按鼠标左键500毫米后释放。

> `宏`快捷键: C
> * 轮转状态1
>   * 按键按下时
>       1. [快捷键命令] 鼠标左键 ↓ 
>       2. [延迟命令] 300毫秒
>       3. [快捷键命令] 鼠标左键 ↑

* 射击游戏更换武器

成品效果：按下`宏`快捷键鼠标滚轮 ↓（滚轮向下） ，自动切换2把武器，每按（滚轮向下）一次，切换一把武器

> `宏`快捷键: 滚轮 ↓
> * 轮转状态1
>   * 按键按下时
>       1. [点击命令] 点击位置1 （武器1）
> * 轮转状态2
>   * 按键按下时
>       1. [点击命令] 点击位置2 （武器2）

* 手柄玩MOBA游戏，按住循环出招

已经配置了3个MOBA右摇杆键，分别是L1，L2，L1&L2，成品效果：按住`宏`快捷键Y ，循环触发这3个技能，松开快捷键Y，停止。

> `宏`快捷键: Y
> * 轮转状态1
>   * 循环时`按下循环`
>       1. [快捷键命令] L1 ↓↑
>       2. [延迟命令] 50毫秒
>       3. [快捷键命令] L2 ↓↑
>       4. [延迟命令] 50毫秒
>       5. [快捷键命令] L1&L2 ↓↑

* 手柄玩MOBA游戏，自动循环出招

已经配置了3个MOBA右摇杆键，分别是L1，L2，L1&L2，成品效果：单按`宏`快捷键Y ，循环触发这3个技能，再按快捷键Y停止。

> `宏`快捷键: Y
> * 轮转状态1
>   * 循环时`松开循环`
>       1. [快捷键命令] L1 ↓↑
>       2. [延迟命令] 50毫秒
>       3. [快捷键命令] L2 ↓↑
>       4. [延迟命令] 50毫秒
>       5. [快捷键命令] L1&L2 ↓↑
> * 轮转状态2
>   * 按键按下时
>       1. [中断命令]