布局宽度自定义
模板宽度由网格定义，并划分为列数（默认为12列）。

若要更改模板宽度，请打开文件：variables.less in:templates/t3_bs3_blank/less，然后更改模板的定义宽度。
现在更改响应布局的大小。


这里是网格系统。可以更改网格数。

主题自定义
所有主题文件夹都位于：templates/t3_bs3_blank/less/themes/


在每个主题文件夹中，它有3个文件：

1。template.less此文件包含从默认主题自定义的样式。


创建新主题的最佳方法是克隆主题文件夹。


您可以手动创建新的主题文件夹，然后添加3个文件：template.less、variables.less和variables-custom.less。

自定义主题

在后端，您可以为所需样式选择新创建的主题，然后使用ThemeMagic自定义主题。


您可以在模板/t3_bs3_blank/less/themes/dark copy中使用较少的已创建主题文件自定义主题

少编译到css

自定义主题后，请少编译成css。新的主题CSS文件将位于templates/t3_bs3_blank/css/themes/dark copy中。


请不要使用css文件自定义主题，因为每次运行compile less to css时，它们都会覆盖。

添加的CSS文件包括：

引导程序
CSS
兆美
越南卡
窗体CSS
当站点在主题上运行时，所有添加的CSS文件都将被加载，这样，所有文件都将从1个文件夹中加载，只有这样才能提高站点性能。

使用CSS自定义模板
T3框架的开发使用较少，编译成CSS文件的文件较少。每次编译时，CSS文件都会被覆盖，因此我们建议您不要使用CSS进行自定义，开发您的站点，因为编译时，您的工作可能会丢失。

custom.css文件位于：templates/t3_blank/css中。如果看不到该文件，请创建新文件，然后打开该文件以将CSS添加到模板的样式中。


自定义.css文件的一些特性
默认情况下不包括该文件，您需要创建一个新文件。
该文件是要加载到站点中的最后一个文件。
该文件不是从less编译的文件，因此在编译时不会被重写或丢失。
使用文件

custom.css文件与任何其他css文件相同。输入要为模板设置样式的CSS。

让我们检查一下前端


主题魔术定制
t3框架的强大之处在于它基于主题魔术的简单主题定制。您可以为自定义添加无限参数。

您必须先启用ThemeMagic，然后单击ThemeMagic按钮打开ThemeMagic面板。


魔法工作面板


选择要自定义的主题
通过更改参数值自定义主题
单击预览查看更改
保存或另存为复制自定义主题
向ThemeMagic添加新参数


您可以为主题自定义添加无限参数和组。自定义参数在文件夹：templates/t3_bs3_blank中的thememagic.xml文件中设置。

注意：请注意，大写文本是语言键。
步骤1。定义新组



视频教程

标志定制
1。更改徽标图像

有两种方法可以更改使用T3框架开发的Joomla模板的徽标。

1：从模板管理器更改徽标

每种风格都可以搭配不同的标志。若要设置徽标样式，请在“模板样式设置”中打开“主题设置”。


2：从variable.less文件更改徽标

更改日志的另一种方法是在variables.less文件中更改徽标图像路径，该文件位于templates/t3_blank/less fodler中。

您还可以通过更改@t3LogoWidth:和@t3LogoHeight:变量的值来更改徽标块的大小。

2。标志造型

要自定义徽标样式，请打开位于templates/t3_blank/less文件夹中的文件style.less。搜索徽标文本，您可以在其中添加更多样式或按原样自定义样式。

页脚信息自定义
页脚信息
t3 blank的默认页脚信息包括三件事：

T3页脚标志
T3版权信息
引导程序版权信息
1。自定义T3页脚徽标

1：如何禁用页脚徽标？

要禁用页脚徽标，请打开T3模板管理器，在“全局”选项卡中，禁用T3徽标选项。

禁用T3页脚徽标
2:更改链接，类…T3页脚

打开位于templates/t3_bs3_blank/tpls/blocks/中的footer.php文件，更改footer徽标的链接，添加/更改类以设置徽标的样式…

定义页脚徽标
3：更改页脚徽标图像、大小和自定义样式

页脚徽标的样式在插件/system/t3/base-bs3/less中的t3.less文件中。打开文件并自定义徽标样式。

自定义页脚徽标样式
前端外观

前幅定制标志
2。自定义T3版权信息

T3版权信息位于templates/t3_bs3_blank/html/mod_footer中的default.php文件中。打开该文件并自定义T3版权信息。

自定义T3版权
三。自定义引导和字体Awesome版权信息

打开位于templates/t3_bs3_blank/tpls/blocks/中的footer.php文件，然后自定义引导和字体Awesome的版权信息。

自定义引导程序和字体太棒了版权所有
添加/安装新字体
步骤1:添加字体包

将字体包上载到templates/t3_bs3_blank/font s。


第2步：定义字体

现在打开位于template s/template_folder/etc文件夹中的file assets.xml来定义刚刚添加的字体



T3框架支持Google字体，您只需在assets.xml文件（位于templates/template_folder/etc文件夹）中定义要使用的Google字体。

嵌入样式表和javascripts
要向T3框架添加新的样式表和JavaScript，有两种方法可以做到这一点。您可以将新的样式表和javascripts声明为head.php文件或assets.xml文件。

1.使用head.php文件

在templates/t3_bs3_blank/tpls/blocks文件夹中打开file head.php，然后根据需要声明新的样式表和javascripts，格式如下。

添加CSS样式表
只需复制并更正css和javascripts文件的路径。

Joomla提供了addStyleSheet、addScript、addScriptScriptDeclaration函数，您应该使用这些函数。

2.使用assets.xml文件

另一种添加新CSS的方法是javascripts将它们嵌入assets.xml，该文件位于templates/t3_bs3_blank/etc文件夹中。

CSS样式表和字体

添加要嵌入网站的样式表和字体的路径。使用以下格式：


添加要嵌入到站点中的javascripts文件的路径。使用以下格式：

覆盖404页和脱机页
1.覆盖404页

通常，每个JA模板都有自己的404页面样式。如果您想定制它，这将指导您快速操作：


步骤1:添加文件error.php

添加此文件的最佳方法是在templates/system中复制默认joomla error.php文件，然后复制到templates/t3_bs3_blank/


第二步：自定义404页

打开此文件并根据需要对其进行自定义。

您可以定义页面将使用的CSS文件。

<link rel=“stylesheet”href=“/>？php echo$this->baseurl？>/templates/<？php echo$this->template？>/css/error.css“type=”text/css“/>
您可以为404页创建新的CSS文件，但我们建议在templates/system/css中复制默认的joomla error.css文件，然后粘贴到templates/t3_bs3_blank/css/文件夹。打开文件并开始自定义。


还有一件事是，每个主题可以使用不同的CSS文件，这样它将具有不同的样式。

每个主题404页的CSS文件位于templates/t3_bs3_blank/css/themes/theme_name/

注：

当您将更少的代码编译为CSS时，不会覆盖CSS文件。

2.第2条。覆盖脱机页

要自定义脱机页，只需执行与404页自定义相同的过程。


步骤1:添加新的offline.php文件。

在文件夹templates/system中复制文件offline.php，然后粘贴到templates/t3_bs3_blank


步骤2:自定义脱机页

打开此文件并根据需要自定义脱机页。

您可以定义页面将使用的CSS文件。

<link rel=“stylesheet”href=“/>？php echo$this->baseurl？>/templates/<？php echo$this->template？>/css/offline.css“type=”text/css“/>
您可以为脱机页创建新的css文件，但我们建议在templates/system/css中复制默认的joomla offline.css文件，然后粘贴到templates/t3_bs3_blank/css/文件夹。


您可以定义每个主题以使用一个CSS文件，以便每个主题对于脱机页具有不同的样式。

每个主题中脱机页的css文件位于templates/t3_bs3_blank/css/themes/theme_name/

注：

当您将更少的代码编译为CSS时，不会覆盖CSS文件。

添加“返回顶部”按钮
“返回顶部”按钮允许您快速导航到网站顶部。


步骤1：启用“返回顶部”按钮

要在站点中添加此按钮，请打开文件模板/t3bs3_blank/tpls/blocks/footer.php，然后将以下代码添加到文件中。

<！--返回顶部按钮-->
第2步：样式“返回顶部”按钮

打开文件模板/t3_bs3_blank/less/style.less，然后添加样式规则：


Megamenu多语言
T3框架支持Megamenu，运行多语言站点时，必须为Megamenu配置多语言。按照本指南操作。


请确保设置多语言站点的所有步骤都已完成。如果还没有完成这些步骤，有两种方法可以构建多语言站点：手动设置或使用JA多语言组件自动设置。不管走哪条路，都由你决定。

手动设置指南JA多语言指南

为语言创建菜单

步骤1:创建语言菜单
对于每种语言，您需要基于默认语言菜单系统创建菜单系统。例如，您的网站有两种语言：英语和阿拉伯语。然后，您应该根据英语的现有菜单为阿拉伯语创建菜单。


实际上，您不需要翻译所有菜单，只需要翻译所有正在使用的菜单。
步骤2:复制默认模板样式

转到“扩展”>>“模板管理器”，然后复制默认模板样式。


步骤3:重命名并为复制的模板样式指定语言

接下来，打开复制的模板样式将其重命名。然后分配到所需的语言。


步骤4:为Megamenu分配菜单

现在打开导航选项卡，启用Megamenu，然后在菜单字段中分配创建的菜单。


第5步：保存蒙加门努设置

现在您只需保存Megamenu设置，请记住，即使您没有更改任何内容，也需要执行此步骤，因为它旨在检测您的Megamenu。

打开Megamenu设置面板，然后确保选择了右菜单-阿拉伯语主菜单。


多实例Megamenu
t3框架允许您为Megamenu创建多个实例。在本文中，我们将为一个站点的主菜单和顶部菜单创建megamenu。


步骤1:创建主菜单和顶部菜单


步骤2：为主菜单和顶部菜单创建菜单项


步骤3:创建topnav.php文件

在templates/t3_bs3_blank/tpls/blocks中复制文件mainnav.php，然后重命名为topnav.php。


步骤4:自定义mainnav.php文件

打开mainnav.php文件，然后更改：


查找代码

数据目标=“t3导航栏折叠”
替换为：

数据目标=“t3导航栏主菜单”
“主菜单”是主菜单的菜单类型名称。

添加T3级导航栏主菜单


查找代码


步骤6：调用TopMenu的LoadBlock