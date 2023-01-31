# 基础项目模板

一个DOTS项目的基础模板

## 步骤

### 安装创建

1. 打开Unity Hub,选择`Installs -> Install Editor -> Official releases -> 2022.2.4f1 Install`(目前的版本，如果有更高就安装更高的版本，注意2023没有Entities包) ，安装以下模块：
    + Microsoft Visual Studio Community 2022
    + Windows Build Support (IL2CPP)

2. 打开Visual Studio Installer,选择`修改 -> 勾选使用C++的游戏开发 -> 点击右下修改`

3. 创建项目
    + 选择编辑器版本为2022
    + 选择3D(URP)模板
    + 创建项目(项目名不能用中文名，`Busrt`会导致项目崩溃报错)


## 安装包

2. `Editor\Project Setting\Package Manager` 勾选 `Enable Pre-release Packages `

`Window\Package Manager\+\add package by name` 输入一下包名安装，或者直接安装

+ com.unity.entities.graphics (会自动安装基础包)
+ com.unity.physics 

### 项目修改

1. 选择`Assets\Readme.asset`,在`Inspector`上点击`Remove Readme Assets`
2. `Editor\Project Setting\Editor` 勾选Enter Player Mode Options（运行不会重新编译脚本）
3. `Editor\Project Setting\Player\Other Settings` Scripting Backend 改为IL2CPP 
4. `Editor\Preferences\Entities` Scene View Mode 改为 Runtime Data

## 构建测试

选择File\Build Setting\Build

由于IL2CPP会出现一些问题，所以也可以选择Mono构建(但是据我观察，两者构造的项目运行效果可能会不一样)
