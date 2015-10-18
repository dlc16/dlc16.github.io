---
layout: post
title: Jekyll安装教程
description: Jekyll • 简单的博客、静态网站工具
keywords: 程序,博客,安装
categories : [jekyll,install]
tags : [博客, 程序,安装]
---

* 目录
{:toc}

---

#### 1. 安装 Ruby
**官网：**[http://rubyinstaller.org/downloads/](http://rubyinstaller.org/downloads/)<br>
**测试：**Ruby是否安装成功，执行命令`ruby -v`<br>
注意：勾选 “Add Ruby executables to your PATH”，安装路径不能包含空格<br>

---

#### 2. 安装 DevKit
**官网：**[http://rubyinstaller.org/downloads/](http://http://rubyinstaller.org/downloads/)<br>
**步骤：**在命令窗口下切换到安装目录，并执行以下命令

        ruby dk.rb init
        ruby dk.rb install


**测试：**gem是否安装成功，执行命令`gem -v`<br>
注意：Ruby与DevKit版本要对应<br>

---

#### 3. 安装 Jekyll
**步骤：**在命令窗口下执行以下命令<br>


        //更换gem源
        gem sources --remove https://rubygems.org/
        gem sources -a https://ruby.taobao.org/

        //查看gem源
        gem sources -l

        //更新gem
        gem update --system

        //安装jekyll
        gem install jekyll

---

#### 4. 安装 Python 相关环境

##### a. 安装 Python
**官网：**[http://www.python.org/download/](http://http://www.python.org/download/)<br>
**测试：**python是否安装成功，执行命令`python -V`<br>
注意：下载Python 2安装，如果安装Python 3 可能不会正常工作。安装后添加环境变量。<br>

##### b. 安装 Easy Install
**提示：**需要下载[ez_setup.py](http://pan.baidu.com/s/1jG2bYbs)<br>
**安装：**`python "D:\software\Jekyll\ez_setup.py"`<br>
**测试：**Easy Install 是否安装成功，执行命令`easy_install --version`<br>
**注意：**添加 Python Scripts 路径到环境变量<br>

##### c. 安装 Pygments
**安装：**`easy_install Pygments`<br>

---

#### 5. Jekyll启动与调试
**步骤：**打开命令行窗口，执行以下命令

        //创建jekyll工程目录
        jekyll new myblog

        //切换到工程目录，并开启服务
        cd myblog
        jekyll serve


**测试：**Jekyll是否正常开启，访问[localhost:4000](http://localhost:4000)<br>

---