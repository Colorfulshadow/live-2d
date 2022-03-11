# 弃坑
本库暂停更新(可能是很长很长一段时间）
感谢各位star

# live-2d
>快捷，实用

>Fast , practical

[![作者](https://img.shields.io/badge/作者-Colorfulshadow-blue.svg)](https://github.com/colorfulshadow)
[![许可证](https://img.shields.io/badge/许可证-GPLv3-orange.svg)](LICENSE)
![版本](https://img.shields.io/badge/版本-1.0.0-green.svg)

[![author](https://img.shields.io/badge/Author-Colorfulshadow-blue.svg)](https://github.com/colorfulshadow)
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
- [修改日志 Modifying logging](#修改日志-Modifying-logging)

## 简介 Introduction

Live2D是一种应用于电子游戏的绘图渲染技术，技术由日本Cybernoids公司开发。通过一系列的连续图像和人物建模来生成一种类似三维模型的二维图像。live2d模型即适用于该技术的可供使用的模型，该模型适配于任何网站博客。</br>
***
Live2D is a graphic rendering technology used in video games developed by Cybernoids of Japan. A series of continuous images and character modeling are used to produce a two-dimensional image similar to a three-dimensional model. The live2d model is a usable model for the technology, and it is adapted to any website blog.</br>

## 分类 Classification

本模型按照1-8等级分类，其中1等级为最低，8等级为最高
评分规则：

- 1.基础打分：按照模型的样式及观赏程度进行基础打分</br>
- 2.动作打分：根据人物动作多少进行打分。较多+1，较少-1，极少-2</br>
- 3.内容打分：根据人物所含内容进行打分，含有暴力，色情等的-3，人物角色积极向上，阳光开朗的+1</br>
- 4.音乐打分：人物含有语音的+3，不含语音的不做调整（此规则建立在3中未扣分的任务上）</br>
- 5.后续内容将继续补充......</br>
***
The model is classified according to 1-8 grades, among which Grade 1 is the lowest and Grade 8 is the highest.</br>
Base Score:</br>

- 1.Basic rating: Base score based on model style and viewing level</br>
- 2.Action scoring: score according to how many actions the characters make. More +1, less -1, few -2</br>
- 3.Content rating: according to the content of the character scored, including violence, pornography, etc. -3, the character positive, sunny and cheerful +1</br>
- 4.Music rating: Characters with voice +3 (this rule is based on 3 undeducted tasks)</br>
- 5.The follow-up will continue to be supplemented ...</br>

### 具体分类 details

★：1-2</br>
★★：3-6</br>
★★★：7-18</br>
★★★★：19-28</br>
★★★★★：29-41</br>
★★★★★★：42-49</br>
★★★★★★★：50-54</br>
★★★★★★★★：55</br>
各人物可在[model文件夹](model/readme)查阅(preview)

## 食用方法 usage

### 安装 Installation

- 下载live2d文件夹

- 在[model文件夹](model)中选出你喜欢的模型，将该模型下载到live2d文件夹中的model中

- 将该live2d文件夹上传到你的网站根目录中(/home/wwwroot/xxxx.com)
***
- Download live2d folder

- Select your favorite model in the model folder and download it to the model in the live2d folder

- Upload the live2d folder to the root of your website (/home/wwwroot/xxxx.com)

### 使用 usage

- 在你的网页的head标签内写入以下代码：(当然你也可以引用本地下载的)
***
- Write the following code in the head tab of your web page: (Of course you can also refer to locally downloaded)
```
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/colorfulshadow/live-2d/live2d/css/live2d.css" />
```

- 在你的body标签结束前写入以下代码：
***
- Write the code before the end of your body tag:

```
<div id="landlord" style="left:5px;bottom:0px;">
    <div class="message" style="opacity:0"></div>
    <canvas id="live2d" width="500" height="560" class="live2d"></canvas>;//部分模型不合适需要修改
    <div class="live_talk_input_body">
    	<div class="live_talk_input_name_body">
        	<input name="name" type="text" class="live_talk_name white_input" id="AIuserName" autocomplete="off" placeholder="你的名字" />
        </div>
        <div class="live_talk_input_text_body">
        	<input name="talk" type="text" class="live_talk_talk white_input" id="AIuserText" autocomplete="off" placeholder="要和我聊什么呀？"/>
            <button type="button" class="live_talk_send_btn" id="talk_send">发送</button>
        </div>
    </div>
    <input name="live_talk" id="live_talk" value="1" type="hidden" />
    <div class="live_ico_box">
    	<div class="live_ico_item type_info" id="showInfoBtn"></div>
        <div class="live_ico_item type_talk" id="showTalkBtn"></div>
        <!--<div class="live_ico_item type_huanzhuang" id="huanzhuangButton"></div> -->
        <div class="live_ico_item type_music" id="musicButton"></div>
        <div class="live_ico_item type_youdu" id="youduButton"></div>
        <div class="live_ico_item type_quit" id="hideButton"></div>
        <input name="live_statu_val" id="live_statu_val" value="0" type="hidden" />
        <audio src="" style="display:none;" id="live2d_bgm" data-bgm="0" preload="none"></audio>
        <input name="live2dBGM" value="https://cdn.jsdelivr.net/gh/colorfulshadowty1/music@1.0.0/3.mp3" type="hidden">
        <input name="live2dBGM" value="https://cdn.jsdelivr.net/gh/colorfulshadowty1/music@1.0.0/4.mp3" type="hidden">
        <input id="duType" value="douqilai,l2d_caihong" type="hidden">
    </div>
</div>
<div id="open_live2d">召唤看板娘</div>
<script type="text/javascript" src="https://apps.bdimg.com/libs/jquery/1.7.1/jquery.min.js"></script>
<script>
var message_Path = 'https://你的站点.com/live2d/';//资源目录，如果目录不对请更改
var talkAPI = "";//图灵机器人的聊天接口路径（下方有介绍）
</script>
<script type="text/javascript" src="https://你的站点.com/live2d/js/live2d.js"></script>
<script type="text/javascript" src="https://你的站点.com/live2d/js/message.js"></script>
```
### 修改 Modify

请注意！！此model需要很多地方自行修改（作者技术一般做不好一键，有大佬的话帮帮忙QWQ）

- live2d/message.json中，部分模型需修改第28行（可选，因为不太重要），Thezqy已经给出了详细的过程：[传送门](https://www.thezqy.top/archives/439)

- live2d/js/message.js中，第449，471行需修改，已给出注释，可直接ctrl+F查找：此处需修改

- body标签中[（即以上提到的）](#使用-usage)，给出注释的地方需要修改，可选是否使用换装按钮（前提是你的人物大多数都有换装）
***
Please note!! This model needs a lot of places to modify their own (the author's technology generally does not do a good one button, there are big guys to help QWQ)

- Live2d/message.json, part of the model needs to be modified in line 28 (optional, because it is not very important), Thezqy has given a detailed process: [Transfer door](https://www.thezqy.top/archives/439)

- Live2d/js/message.js, line 449,471 to be modified, commented, can be found directly ctrl-F: 此处需修改

- Body labels ,[The above mentioned](#使用-usage), where the comments need to be made, and whether to use the change button (provided that most of your characters have a change dress)

### 扩展 Extended

- 如何使用机器人聊天功能

- 为了让live2d能够聊天，我们可以借助图灵机器人，先去[图灵机器人官网](http://www.turingapi.com/)注册账号，新建机器人获取apikey

- 新建一个tlapi.php文件，加入如下代码，注意添加自己的apikey到里面
***
- How to use the bot chat feature

- In order to allow live2d to chat, we can use Turing Robot to first go to the website of [Turing Robotics](http://www.turingapi.com/) to register an account and create a new robot to get apikey

- Create a new tlapi.php file, add the following code, pay attention to adding your own apikey to it
```
<?php
//获得聊天
$appkey = ''; //你的appkey
$talkContent = ""; 
$info=addslashes($_POST['info']);
$userid=addslashes($_POST['userid']);
function send_post($url, $post_data) {  
  
  $postdata = http_build_query($post_data);  
  $options = array(  
    'http' => array(  
      'method' => 'POST',  
      'header' => 'Content-type:application/x-www-form-urlencoded',  
      'content' => $postdata,  
      'timeout' => 15 * 60 // 超时时间（单位:s）  
    )  
  );  
  $context = stream_context_create($options);  
  $result = file_get_contents($url, false, $context);  
  
  return $result;  
}  
  
//使用方法  
$post_data = array(  
  'key' => $appkey,  
  'info' => $info,
  'userid' => $userid,
);
if($appkey==""){
  $talkContent = '{"code":"500","text":"我还没学会聊天功能，快和站长联系吧！"}';
}
else{
  $talkContent = send_post('http://www.tuling123.com/openapi/api', $post_data);
}
header('Content-type:text/json');
echo $talkContent;
?>
```

## 演示 Demo

- [oyi 演示站(随时跑路)](https://sample.oyi.me)
- [oyi , sample website(anytime may be closed)](https://sample.oyi.me)

## 贡献者 Contributing

>[深海(Colorfulshadow)](https://github.com/colorfulshadow)

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
    at Image.n.onload (https://cdn.jsdelivr.net/gh/colorfulshadow/live2d-model@test4/live2d/js/live2d.js:1:138590)
```
经我查询问题出现在:在一般情况下，禁止将跨域元素用作 WebGL 纹理的强制子句</br>

这个问题暂时我无力解决，但是将会摸索解决方法，也希望看到此live2d的朋友能够给出一些建议，共同修复此问题。</br>
***
In fact, I've tried to directly reference resources on GitHub to reduce live2d's use of my system space, and unfortunately, if you load by reference, the browser will make the following errors:</br>
```
Uncaught DOMException: Failed to 'texImage2D' on 'WebGLContextRendering': The image element contains cross-origin data, and may not be loaded.
    at Image.n.onload (https://cdn.jsdelivr.net/gh/colorfulshadow/live2d-model@test4/live2d/js/live2d.js: 1:1:138590)
```
The question I've queried appears: In general, cross-domain elements are prohibited as mandatory clauses for WebGL textures</br>

This problem is not able to solve for the time being, but will explore solutions, but also want to see this live2d friends can give some advice to work together to fix this problem.</br>

### 2 关于更多的live2d模型 About more models

虽然我们已经从[Eikanya](https://github.com/Eikanya)处获得了部分模型，但是仍有部分因为格式不对所放弃的部分模型，后段时间我们将会对格式为.moc3的模型进行修改完善，及时发布在此Github上。</br>
***
Although we've already got some models from [Eikanya](https://github.com/Eikanya), there's still some of the models that are not discarded because the format isn't in place, and we'll be able to modify and refine the models for .moc3 later and release it on github in time.</br>

## 许可证 License

[![license](https://img.shields.io/badge/License-GPLv3-orange.svg)](LICENSE)</br>
[Live2d License © Colorfulshadow](LICENSE)

## 修改日志 Modifying logging
***
>1.0.3
- 2020.3.27 15:04</br>
修改live2d.js，改为完整版
***
>1.0.2
- 2020.3.27 8：45</br>
修补message.js</br>
检查所有model.json，修补3处漏洞
***
>1.0.1
- 2020.3.20 - 2020.3.26 22：46</br>
修改版本样式，使用手动安装的方式
