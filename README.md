# Daily
对2023秋季OS训练营的学习记录

## 第一周
### (2023-10-9 周一)
- 从github获取了第一阶段的学习任务，并clone到本地
- 按照教程安装好了rust环境，准备开始做题
- 由于是rust初学者，打算从头开始看《Rust语言圣经》，边学边做题

### (2023-10-14 周六)
- 周一至今一直边学习rust语法边做练习，今天终于通关了
- 于是继续寻找学习资料，发现Rust Quizes一题都不会...，于是决定等到第二阶段再边做项目边巩固
  
## 第二周
### (2023-10-16 周一)
- 开始学习RISC-V相关知识，发现原来OS的很多设计被ISA给限定了(比如页表和中断处理)，猜想rCore有些内容应该和xv6类似，于是打算做完两个6.S081剩下的2个lab来顺便复习一下

### (2023-10-17 周二)
- 做完了一个fslab，开始做mmaplab

### (2023-10-19 周四)
- 做完了所有lab，开始配置rCore的环境

## 第三周
### (2023-10-23 周一)
- (千辛万苦终于)等到了新的阶段与新的任务
- 可能是由于之前配环境看的是往届的文档，今天上手clone内核跑不通，于是按照新文档重新配了一遍环境
- ~~感觉是我太笨了，找了好一会才弄懂要学什么，怎么做lab~~
- 开始跟着文档学习，第一章看完了，println使用的宏和内嵌汇编语法不太懂，最后一节的汇编也不太理解，去补相关知识了

### (2023-10-24 周二)
- 看完了第二章和第三章，开始做ch3实验了

### (2023-10-24 周三)
- ch3实验做完了，开始ch4实验

### (2023-10-24 周四)
- 在文档中发现了081许多没有提到的点，两个课程的内容串起来了
- 接着做ch4实验
  
### (2023-10-25 周五)
- ch4实验做完了，踩了挺多坑，主要是不知道原来可以在本地Grading，然后本地多次测试才发现原来reports要带上之前全部的report

### (2023-10-26 周六)
- ch5实验做完了
- 感觉自己做ch5实验过程踩了非常多坑，于是稍微整理形成了`trap.md`