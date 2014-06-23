Platform
========

## 介绍

由于国内手机浏览器平台的多样性，官方 polymer 项目并不能很好的支持国内主流的手机浏览器（包括最新版QQ、UC），且 polymer 还处在 pre-alpha 状态，相关标准和规范都在变化中，过早的指望 polymer 提升其兼容性也不现实。因此为了让国内开发者能够用上稳定兼容的 polymer 项目，我们提出了 polymer-cn 分支，旨在于提升 polymer 在各个手机浏览器（尤其是国产主流浏览器）上的兼容性，并不提供任何新功能。

polymer-cn 将同官方 polymer 保持同步更新，由于兼容性修复都存在于 polymer 的 platform 部分（不了解 platform，请访问 polymer-project.org 先行了解）,我们只发布独立版本的 platform.js，并不发布 polymer.js。

## 版本

polymer-cn 的版本号将同官方 polymer 版本号保持**第二位**版本号的同步，如：

* 官方发布 0.2.0，polymer-cn 将发布 0.2.1；
* polymer-cn 进行了新的修复后将发布 0.2.2；
* 官方发布 0.2.1，polymer-cn 将同步后发布 0.2.3；
* 官方发布 0.3.0，polymer-cn 将发布 0.3.1。

我们并不会修改代码中的版本号，polymer-cn 基于的官方版本号，可以在 platform.js 中的注释中看到。

## 安装

我们只发布 platform 至 bower：

	bower install polymer-cn/platform
	
polymer 的安装请参考[官方文档](http://www.polymer-project.org/docs/start/getting-the-code.html#installing-polymer)。

## 提交问题

可以在 https://github.com/polymer-cn/platform/issues 提交兼容性问题，请详细描述以下信息：

* 操作系统与浏览器版本，包括各种 ROM 版本，如 MIUI 4.2.21 Android 4.1.1 UC 9.6.0.378；
* 详细问题描述，包括触发场景、操作步骤等。

## 贡献

请查看 https://github.com/polymer-cn/platform/blob/master/CONTRIBUTING.md

Aggregated polyfills the Polymer platform. 

[![Analytics](https://ga-beacon.appspot.com/UA-39334307-2/Polymer/platform/README)](https://github.com/igrigorik/ga-beacon)
