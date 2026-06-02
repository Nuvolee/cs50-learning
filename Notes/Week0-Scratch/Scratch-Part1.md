---
Labels: CS50x, Lecture0
Keywords: Algorithm, Binary, Bit, Byte, ASCII, Unicode, RGB
Date: 2026-05-28
---

what ultimately matters in this course is not so much where you end up relative to your classmates <br>
but where you end up relative to yourself when you began


# 今日收获
- 理解二进制的作用。
- 学会 Bit 与 Byte。
- 了解*数字、字符、颜色、视频和声音*的数字化表示方式。



# Problem Solving

计算机解决问题的基本模型：
Input → ________ → Output





# Bit
Bit（Binary Digit，二进制数字）

bi表示二，意味着只有两种可能：0或1.  
bi+t=bit，比特。 比特其实就是二进制数字，也就是0或1，是计算机最小的信息单位。

可理解为：

| Bit | 状态  |
| --- | --- |
| 0   | Off |
| 1   | On  |




# Byte
1字节=8位（8比特）。可表示数字。

0000 0000  0+0+0+0 +0+0+0+0 = 0 
1111 1111  1+2+4+8+  16+32+64+128 = 15+80+160= 240+15= 255




# ASCII
使用数字表示字符。


0100 0001 =65 代表字母A
B = 66
a = 97




# Unicode
用于表示人类所有语言，可表示Emoji。
向后兼容ASCII。增加了超级表示法，可能用16、24或32位。


# emoji
表示表情。
4036991106，笑哭表情，😂，是目前全球最流行的emoji。



# RGB
表示颜色。
代表红绿蓝三原色。计算机常用三个字节来表示*像素*。3*8=24比特。 
72 73 33 <br>
中等红+中等绿+少量蓝 --->黄色




# 表示动态画面、视频、电影
大量图片快速播放。



# 表示声音



# 小结：
计算机只认识 0 和 1。
数字、文字、表情、图片、视频和声音最终都会转换为二进制进行处理。

计算机解决问题的基本模型：
Input → algorithm → Output
Algorithm：算法，即解决某个问题的一系列步骤说明。




# 易错点

* Bit ≠ Byte
* ASCII ≠ Unicode
* Unicode 包含 Emoji
* 视频本质是连续图片
* RGB 是颜色数值组合



