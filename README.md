# Process Manager

## 简介

这是基于PHP和swoole实现的一个进程管理工具，个人撸的一个小demo，功能持续更新中。。。

暂时还不能实现开箱即用，仅仅供PHPer交流学习

## 需求

该项目运行于 php-cli 下，需要swoole扩展，及 pcntl 扩展，如没有，请使用 pecl 安装

## 功能

- 进程创建及守护，创建及守护 **config/task.php** 中的配置的任务及数量
- 信号量控制，暂时支持 **kill** **kill -USR1** 两种信号量处理
- Manager退出，主动回收所有子进程

## To-do

- 根据业务自动进行增减任务的子进程数量
- 子进程处理一定数量任务后自动重启，避免内存泄漏造成内存溢出
- 子进程启动失败，自动预警