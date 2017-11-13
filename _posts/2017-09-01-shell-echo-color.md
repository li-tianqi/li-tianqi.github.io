---
layout: post
title: shell输出彩色字符
categories: [Ubuntu, Shell]
tags: [shell]
excerpt_separator: <!--more-->
---

<!--categories: [Ubuntu, Database, Python, Github, Web, Tutorial, Test, Shell, ]-->
<!--tags: [jekyll, python3, github, Django, markdown, mysql, shell, ]-->

## shell打印输出彩色字符

shell中echo输出字符，设置字体颜色和背景颜色的方法：  
``` shell
echo -e "\033[背景颜色； 文字颜色m字符串\033[0m"
```  

<!--more-->

**说明：**  
`-e`: echo的选项参数，用于激活特殊字符解释器  
`\033`：引导非常规字符序列  
`m`: 设置属性并结束非常规字符序列  

**举例：**  
``` shell
echo -e "\033[44;37;5mME\033[0m COOL"  
```  
输出`ME COOL`,其中`ME`为蓝底白字，`COOL`为普通，光标闪烁。  


**可用编码及含义：**  

| 编码 |    颜色/动作                              |  
| ---- |:----------------------------------------- |  
|  0   |    重新设置属性到缺省设置                 |  
|  1   |    设置粗体                               |  
|  2   |    设置一半亮度（模拟彩色显示器的颜色）   |  
|  4   |    设置下划线（模拟彩色显示器的颜色）     |   
|  5   |    设置闪烁                               |  
|  7   |    设置反向图象                           |  
|  22  |    设置一般密度                           |  
|  24  |    关闭下划线                             |  
|  25  |    关闭闪烁                               |  
|  27  |    关闭反向图象                           |  
|  30  |    设置黑色前景                           |  
|  31  |    设置红色前景                           |  
|  32  |    设置绿色前景                           |  
|  33  |    设置棕色前景                           |  
|  34  |    设置蓝色前景                           |  
|  35  |    设置紫色前景                           |  
|  36  |    设置青色前景                           |  
|  37  |    设置白色前景                           |  
|  38  |    在缺省的前景颜色上设置下划线           |  
|  39  |    在缺省的前景颜色上关闭下划线           |  
|  40  |    设置黑色背景                           |  
|  41  |    设置红色背景                           |  
|  42  |    设置绿色背景                           |  
|  43  |    设置棕色背景                           |  
|  44  |    设置蓝色背景                           |  
|  45  |    设置紫色背景                           |  
|  46  |    设置青色背景                           |  
|  47  |    设置白色背景                           |  
|  49  |    设置缺省黑色背景                       |  


**常用组合：**  
``` shell
echo -e "\033[31m 红色字 \033[0m" 
echo -e "\033[34m 黄色字 \033[0m" 
echo -e "\033[41;33m 红底黄字 \033[0m" 
echo -e "\033[41;37m 红底白字 \033[0m"
echo -e "\033[30m 黑色字 \033[0m" 
echo -e "\033[31m 红色字 \033[0m" 
echo -e "\033[32m 绿色字 \033[0m" 
echo -e "\033[33m 黄色字 \033[0m" 
echo -e "\033[34m 蓝色字 \033[0m" 
echo -e "\033[35m 紫色字 \033[0m" 
echo -e "\033[36m 天蓝字 \033[0m" 
echo -e "\033[37m 白色字 \033[0m"
echo -e "\033[40;37m 黑底白字 \033[0m" 
echo -e "\033[41;37m 红底白字 \033[0m" 
echo -e "\033[42;37m 绿底白字 \033[0m" 
echo -e "\033[43;37m 黄底白字 \033[0m" 
echo -e "\033[44;37m 蓝底白字 \033[0m" 
echo -e "\033[45;37m 紫底白字 \033[0m" 
echo -e "\033[46;37m 天蓝底白字 \033[0m" 
echo -e "\033[47;30m 白底黑字 \033[0m"
echo -e "\033[42;30;5m wwww \033[0m" 
echo -e "\033[47;30;5m wwww \033[0m"
```