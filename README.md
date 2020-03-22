# live-2d
>快捷，实用

>Fast , practical

[![作者](https://img.shields.io/badge/作者-Colorfulshadowty-blue.svg)](https://github.com/colorfulshadowty)
[![许可证](https://img.shields.io/badge/许可证-GPLv3-orange.svg)](LICENSE)
![版本](https://img.shields.io/badge/版本-1.0.0-green.svg)

[![author](https://img.shields.io/badge/Author-Colorfulshadowty-blue.svg)](https://github.com/colorfulshadowty)
[![license](https://img.shields.io/badge/License-GPLv3-orange.svg)](LICENSE)
![version](https://img.shields.io/badge/Version-1.0.0-green.svg)

## 目录 Table of Contents

- [简介 Introduction](#简介-Introduction)
- [分类 Classification](#分类-Classification)
- [食用方法 usage](#食用方法-usage)
- [演示 Demo](#演示-Demo)
- [贡献者 Contributing](#贡献者-contributing)
- [问题 problem](#问题-problem)
- [许可证 License](#许可证-license)

## 简介 Introduction

Live2D是一种应用于电子游戏的绘图渲染技术，技术由日本Cybernoids公司开发。通过一系列的连续图像和人物建模来生成一种类似三维模型的二维图像。live2d模型即适用于该技术的可供使用的模型，该模型适配于任何网站博客。</br>

Live2D is a graphic rendering technology used in video games developed by Cybernoids of Japan. A series of continuous images and character modeling are used to produce a two-dimensional image similar to a three-dimensional model. The live2d model is a usable model for the technology, and it is adapted to any website blog.</br>

## 分类 Classification

本模型按照1-8等级分类，其中1等级为最低，8等级为最高
评分规则：

- 1.基础打分：按照模型的样式及观赏程度进行基础打分</br>
- 2.动作打分：根据人物动作多少进行打分。较多+1，较少-1，极少-2</br>
- 3.内容打分：根据人物所含内容进行打分，含有暴力，色情等的-3，人物角色积极向上，阳光开朗的+1</br>
- 4.音乐打分：人物含有语音的+3，不含语音的不做调整（此规则建立在3中未扣分的任务上）</br>
- 5.后续内容将继续补充......</br>


The model is classified according to 1-8 grades, among which Grade 1 is the lowest and Grade 8 is the highest.</br>
Base Score:</br>

- 1.Basic rating: Base score based on model style and viewing level</br>
- 2.Action scoring: score according to how many actions the characters make. More +1, less -1, few -2</br>
- 3.Content rating: according to the content of the character scored, including violence, pornography, etc. -3, the character positive, sunny and cheerful +1</br>
- 4.Music rating: Characters with voice +3 (this rule is based on 3 undeducted tasks)</br>
- 5.The follow-up will continue to be supplemented ...</br>

### 具体分类 details

★：1-2</br>（1.0.0）
★★：3-6</br>（1.0.0）
★★★：7-18</br>（1.0.0）
★★★★：19-28</br>（1.0.1）
★★★★★：29-41</br>（1.0.1）
★★★★★★：42-49</br>（1.0.2）
★★★★★★★：50-54</br>（1.0.3）
★★★★★★★★：55</br>（1.0.3）

## 食用方法 usage

>详情见[Colorfulshadow-使用live2d模型](https://blog.oyi.me/live2d)，如果跑路，请联系 深海 （Colorfulshadow） colorfulshadowty@gmail.com

>For more information on [Colorfulshadow-使用live2d模型](https://blog.oyi.me/live2d), if it doesn't work ,please contact 深海 (Colorfulshadow) colorfulshadowty@gmail.com

## 演示 Demo

- [oyi 演示站(随时跑路)](https://sample.oyi.me)
- [oyi , sample website(anytime may be closed)](https://sample.oyi.me)

## 贡献者 Contributing

>[深海(Colorfulshadowty)](https://github.com/colorfulshadowty)

组织，整理，补充，修复</br>

organize ,sift , replenish , repair

>[Eikanya](https://github.com/Eikanya)

模型提供者</br>

Model provider

>[Thezqy](https://github.com/Thezqy )

整理，补充</br>

sift ,replenish

## 问题 problem
### 1 关于引用资源来加载 About referencing resources to load

事实上，我已经尝试过直接引用GitHub上的资源以减少live2d对我系统空间的占用，不幸的是，如果通过引用加载，浏览器会出现以下报错：</br>
```
Uncaught DOMException: Failed to execute 'texImage2D' on 'WebGLRenderingContext': The image element contains cross-origin data, and may not be loaded.
    at Image.n.onload (https://cdn.jsdelivr.net/gh/colorfulshadowty/live2d-model@test4/live2d/js/live2d.js:1:138590)
```
经我查询问题出现在:在一般情况下，禁止将跨域元素用作 WebGL 纹理的强制子句</br>

这个问题暂时我无力解决，但是将会摸索解决方法，也希望看到此live2d的朋友能够给出一些建议，共同修复此问题。</br>

In fact, I've tried to directly reference resources on GitHub to reduce live2d's use of my system space, and unfortunately, if you load by reference, the browser will make the following errors:</br>
```
Uncaught DOMException: Failed to 'texImage2D' on 'WebGLContextRendering': The image element contains cross-origin data, and may not be loaded.
    at Image.n.onload (https://cdn.jsdelivr.net/gh/colorfulshadowty/live2d-model@test4/live2d/js/live2d.js: 1:1:138590)
```
The question I've queried appears: In general, cross-domain elements are prohibited as mandatory clauses for WebGL textures</br>

This problem is not able to solve for the time being, but will explore solutions, but also want to see this live2d friends can give some advice to work together to fix this problem.</br>

### 2 关于更多的live2d模型 About more models

虽然我们已经从[Eikanya](https://github.com/Eikanya)处获得了部分模型，但是仍有部分因为格式不对所放弃的部分模型，后段时间我们将会对格式为.moc3的模型进行修改完善，及时发布在此Github上。</br>

Although we've already got some models from [Eikanya](https://github.com/Eikanya), there's still some of the models that are not discarded because the format isn't in place, and we'll be able to modify and refine the models for .moc3 later and release it on github in time.</br>

## 许可证 License

[![license](https://img.shields.io/badge/License-GPLv3-orange.svg)](LICENSE)</br>
[Live2d License © Colorfulshadow](LICENSE)
