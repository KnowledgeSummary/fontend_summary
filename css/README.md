# css优化方案和技巧
* 1.双边距问题
    * 问题描述：`嵌套div`或`上下排列div`时，上下的margin会以两者较大的margin确定，左右则叠加
    * 问题原理：[BFC](http://web.jobbole.com/84808/)
    * 解决方案：
        * 1.使用padding,代替margin
        * 2.给div添加border
        * 3.再创建一个bfc环境，原理文档里面有解决方案
    * demo地址：double_margin.html
    
# CSS实现垂直居中的5种方法
 * [实现垂直居中的5种方法](https://www.qianduan.net/css-to-achieve-the-vertical-center-of-the-five-kinds-of-methods/)
