# Wechat-Lottery-number-generator
彩票号码生成器  
&nbsp;&nbsp;&nbsp;&nbsp;本小程序首先进行界面设计，分为两栏一按钮，一栏显示随机产生的红球号码，一栏显示随机产生的蓝球号码，按钮为点击生成新的彩票号码。界面设计代码index.wxml中，在view组件中用class属性约束文本的样式以及显示的样式，在botton组件中用type约束颜色，再绑定生成新的彩票号码的事件函数，实现点击生成新的彩票号码。

&nbsp;&nbsp;&nbsp;&nbsp;接着是逻辑层的编写，根据彩票规则，红球为6个，每个数取1~31，蓝球为1个，每个数取1~13， 首先定义了onLoad 函数，newRand函数，全局数组变量rand用来存储产生的红球数列，全局数组变量rand1用来存储产生的蓝球。
&nbsp;&nbsp;&nbsp;&nbsp;但是有一个在设计上需要注意到的问题，就是红球不能重复，但random产生随机数会重复，为了解决这个问题，定义一个存放生成随机数的数组rand2，通过for循环生成6个随机数，在for循环中调用一个方法generateRandom用于生成随机数，放在rand数组中，然后再定义一个for循环遍历一下数组rand，接下来就是方法体部分，用Math.random( )生成后用parselnt转成数字后存入数组rand2，用for循环与rand比较，相同返回false，再把rand2写入rand数组。蓝球只有一个数，就直接调用Math.random生成。createRand( )函数用于产生随机数列，最后再显示出来。

&nbsp;&nbsp;&nbsp;&nbsp;以上为本小程序开发设计总结。

This applet first carries out the interface design, which is divided into two columns, one button, one column displays the randomly generated red ball number, the other column displays the randomly generated blue ball number, and the button is to click to generate a new lottery number. In the interface design code index.wxml, use the class attribute to constrain the text style and display style in the view component, use the type to constrain the color in the botton component, and then bind the event function to generate a new lottery number to generate a new lottery number by clicking.

Then the logic layer is written. According to the lottery rules, there are 6 red balls, 1 ~ 31 for each number, 1 ~ 13 for each number. First, the onload function and newrand function are defined. The global array variable Rand is used to store the generated red ball sequence, and the global array variable rand1 is used to store the generated blue ball.

But there is a problem that needs to be noticed in design, that is, the red ball can not be repeated. However, the number of random numbers generated by random will be repeated. In order to solve this problem, we define an array rand2 that generates random numbers, generate 6 random numbers through the for loop, and call a method generateRandom in the for loop to generate random numbers and put them in the RAND array. Then define a for loop to traverse the array Rand. The next step is the method body. After generating it with math. Random(), convert it into a number with parselnt and store it in the array rand2. Compare it with Rand with the for loop, return false, and then write rand2 into the RAND array. If the blue ball has only one number, it is generated directly by calling math.random. The createrand() function is used to generate a random sequence of numbers, which is then displayed.

The above is the summary of this applet development and design.
