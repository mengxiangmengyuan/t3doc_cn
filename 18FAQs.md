新建T3模板
当基于基于T3的模板创建模板时，不能升级新版本，因为它们是不同的模板。

本指南帮助您根据t3 blank或t3 bs3 blank模板重命名或创建新模板。步骤如下：

步骤1：下载基于T3的模板

有2个基于t3的模板：t3 blank和t3 bs3 blank。这两个模板的区别在于：t3空白模板集成了bootrap 2和font-awesome 3，而t3 bs3空白模板集成了bootstrap 3和font-awesome 4。

要下载基于T3的模板，请遵循>>此链接。

步骤2:重命名模板文件夹和语言文件

解压下载的基于T3的模板并重命名模板文件夹。

重命名T3模板文件夹

接下来，打开您的_template_文件夹/language/en-gb文件夹并重命名语言文件：

en-GB.tpl_t3_bs3_blank.ini>>en-GB.tpl_joomlart_template.ini
en-GB.tpl_t3_bs3_blank.sys.ini>>en-GB.tpl_joomlart_template.sys.ini
步骤3:编辑templatedetails.xml文件

打开templatedetails.xml文件，按照说明编辑该文件：

更改模板名称：

步骤4：压缩模板文件夹并安装到joomla系统中

压缩模板文件夹，访问站点后端设置，转到：扩展名>>扩展名管理器，然后浏览模板zip文件，然后安装。

将模板安装到Joomla系统中

转到“扩展”>>“模板管理器”检查已安装的模板。

已安装模板

安装谷歌分析
在由T3框架开发的Joomla模板中安装Google Analytics可以通过多种方式完成。以下是我们如何做到这一点，最多需要5分钟。

以下是两个步骤：

第1步：获取你的谷歌分析代码


第2步：将谷歌分析代码添加到您的网站

从站点的后端，转到“扩展”>>“模板管理器”。


打开模板的模板样式设置面板，在本例中，我们使用t3 blank作为模板。所以我们要打开ja_v3-home的模板样式设置面板


导航到“注入”选项卡，然后将Google分析代码添加到之前的字段中。

现在，请打开标签注入，然后将谷歌分析代码添加到之前的字段中。


“注射”选项卡中的这些设置被设置为全局设置。这意味着您可以将谷歌分析代码添加到任何样式中，而不必返回每个样式并手动添加它。

如果在“管理面板”中找不到这些设置，则意味着您使用的是旧版本的T3框架，该版本低于1.3.0版。您可以升级到最新版本的t3框架（在进行任何更新之前请始终备份，强烈建议），也可以手动安装谷歌分析代码（通过向可在所有页面中使用的文件添加代码）。有关手动安装的更深入信息，请查看视频教程了解更多信息。

添加实时聊天脚本
说到在线聊天服务，它实际上取决于您使用的是哪种在线聊天服务。每个脚本都有自己的添加要求。但不用担心，我们在“注入”选项卡中列出了这些常见的位置，因此您可以继续相应地复制和粘贴它们。


这些设置也应用于网站的全局设置，因此您只需添加一次脚本。
首页无内容
问题

如果你觉得在主页上显示COM内容有困难，不管菜单类型是什么，这个线程都会对你有用。


这个问题的解释是，在一些模板中，主布局没有组件位置，并且您为主页分配了主布局。



在主布局中没有组件位置的模板列表。

日本商店
JA福比克斯
茉莉酸
JA主页
如何修复？

每个模板可以有一个或多个布局，但所有模板始终具有默认布局，在默认布局中，始终加载组件。

有两种方法可以解决此问题

1。将位置“组件”添加到“主”布局


步骤1：打开位于templates/ja_template/tpls/blocks中的主布局文件（应该是home.php）。


第二步：打开要添加组件的块文件，建议添加到主体主块。所以打开位于templates/ja_template/tpls/blocks/中的文件mainbody-home.php。

添加以下代码。

<jdoc:include type=“component”/>
里面<！——主要内容——……<！--//主要内容-->


2。更改主样式的布局

打开主模板样式并选择具有组件位置的默认布局。


注意：通过选择不同的布局，它将更改主页的现有布局/结构。

响应第三方扩展
T3框架是一个响应式框架模板，这意味着用T3框架开发的所有模板都是核心响应式的。

那么t3如何处理第三方扩展，如k2、virtuemart…在响应方面？



It does not intervene the 3rd extensions, hence if the 3rd extensions are not responsive by itself, then it's a huge chance they won't be responsive when you install in any of the templates developed with T3 Framework. Now it's up to you to consider if you want them in your site or not. If you still decide to go with it, you probably have to do the customization to make it responsive, and it sure does take a lot of time and effort. Please be wise here.

Template and Template styles

What is Joomla Template

The Template controls the overall look and layout of your site. It provides the framework that brings together common elements, modules and components as well as providing the cascading style sheet for your site.

What is Joomla Template Style

Template style feature (version 2.5 and above) is to assign different template styles to individual menu items. The default template style can be partially or completely overridden by assigning different template styles to the desired menu items in order to obtain a different look for their respective pages.

Template Hook
What is it used for

Template Hook allows you to track what component, menu item that you are working on when you debug.


When debug any item, please scroll up to the HTML section, you will see what component that the item you are debugging belongs to.

The templateHook.php file is located in templates/t3_bs3_blank. The file is the same in all JA Templates that are developed with T3 Framework.
它不会干扰第三个扩展，因此，如果第三个扩展本身没有响应，那么当您安装在用T3框架开发的任何模板中时，它们很可能不会响应。现在由你来决定你是否希望他们出现在你的网站上。如果您仍然决定使用它，那么您可能需要进行定制以使其具有响应性，而且这确实需要花费大量的时间和精力。请你在这里聪明点。

模板和模板样式

什么是Joomla模板

模板控制网站的整体外观和布局。它提供了将公共元素、模块和组件结合在一起的框架，并为您的站点提供级联样式表。

Joomla模板样式是什么

模板样式功能（2.5及以上版本）是为单个菜单项分配不同的模板样式。通过将不同的模板样式分配给所需的菜单项，可以部分或完全覆盖默认模板样式，以获得其各自页面的不同外观。

模板钩
它是做什么用的

模板挂钩允许您跟踪调试时正在处理的组件、菜单项。


调试任何项目时，请向上滚动到HTML部分，您将看到正在调试的项目属于哪个组件。

templatehook.php文件位于templates/t3_bs3_blank中。在所有使用T3框架开发的JA模板中，该文件都是相同的。