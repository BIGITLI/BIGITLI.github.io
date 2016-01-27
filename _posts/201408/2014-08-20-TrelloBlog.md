---
layout: post
title: Trello的使用
description: Trello的简介优缺点以及使用
categories:
- Hadoop
tags:
- vagrant
---



###任务管理与协作平台Trello介绍


1. __Trello简介__

	+ Trello 是由国外的软件公司Fog Greek开发上线的项目跟踪与团队协作的工具平台。Trello使用目前非常流行的看板（Board，之后会有介绍）来跟踪管理项目。看板可以清楚的看到项目进度和卡住的地方。

2. __Trello的优点__
	+ 没有使用人数的限制。

	+ 简洁易用。不会因为纠结于使用工具的复杂性，而忽视了使用的目的。对于企业提供了团队协作，任务跟踪的功能，对于个人，也是时间管理的工具。

	+ 运营和管理的一个困难是跟踪团队的工作内容，Trello 主要解决这个问题。而强调团队协作是可以让同一地域和不同地域的人协同工作，任何人只要能连上公网就可以基于Trello工作。没有时间地域限制。

	+ Trello支持各种终端，比如PC, Ios和Android应用，各主要应用市场都提供了免费的Trello App下载，实现移动互联。

	+ Trello完全免费。节省了开发以及购买软硬件的成本。

	+ 与同类的项目管理工具相比 ，Trello是稳定并且用户众多的。横向比较的另一个特点是Trello可以按照需求定制任务列表流(一个Board可以定义多个List以构成列表流，之后会有介绍)，通常最简单也最好用的是Trello默认的任务列表流: To Do-> Doing->Done这样的流向，任务（Card）是流动的元素。定义任务是在To do列表，任务开始可以将任务拖动到Doing列表，任务完成可以将任务再拖动到Done列表。不同的列表表示任务处于不同阶段。 任务可以直接在页面上从所在List拖动到目标List，这是看板管理的特点。又比如Trello的帮助Board定义的任务列表流：Basis->Intermediate->Advanced，如下图
	![](/image/20140820/welcome.jpg)

	+ 对于开发团队，可以创建任务列表流如下：新需求收集->需要分析-需求排期->开始研发->测试->发布->培训
3. __Trello的缺点__
	+ Trello通过公网访问，存在被墙的可能性，但是微乎其乎。

	+ 帮助和主要元素是英文（仅需要理解），日常工作中定义的任务，列表都可以是中文。英文几乎不是问题。

	+ 机密敏感信息最好不要通过附件上传。尽量只使用Trello做任务管理。因为数据不在本地。

4. __Trello的主要元素__

	_Trello的元素就是在操作的过程中，使用到的一些对象_

	+ 比如看板（Board），任务列表（List），任务（或者项目，Card），可执行可检查步骤（Checklist），活动（Activity）等。每个元素都有对应的操作。比如将鼠标移动到List和Card上会显示下拉钮，里面是当前元素对应的操作菜单。Board的对应操作是点击右上角的Show sidebar，然后点击Menu会出现对应的菜单。通常Board，List操作是由相应的管理员负责。项目执行人需要熟悉Card, Checklist等操作。项目跟踪人往往只需要通过看板了解项目的进度以及添加评论（Activity会提到）。

	_看板（Board，管理员需要熟悉）_
	+ 浏览和管理任务时，希望能够在一块看板上按顺序将各个列表排列出来。Board元素支持这样的功能。下图左上角的Boards可以将个人能看到的所有Board列出来。Board默认就是蓝色背景。示例的Board名称为”信息技术部“，个人理解Board对于一个企业来讲，可以对应到部门或者对应到部门中团队，如果项目是跨部门协作，也可以定义跨部门Board,比如“零售信息技术协作”。
	![](/image/20140820/liststream.jpg)

	+ Trello默认新建Board会包含三个列表，分别是To Do,Doing,Done。默认的列表名称可以修改，比如修改为待办，办理中，办结。
	+ 通常有这三个列表就可以应付日常管理的工作。如果需要添加List, 可以通过看板上的“Add a list”添加定制的list，比如添加新的列表“总结”。或者按照需要重新定义整个列表流。

	+ Board对应的操作菜单是Show sidebar显示的菜单列表。Board的主要操作是添加成员。将来Board成员主要有二种：执行者、跟踪者。执行者就可以指定任务。跟踪者主要是跟踪Board中任务的执行情况。添加Board成员直接点击Add Members即可。因为Board个人理解对应一个团队或机构或跨机构。所以Board成员通常也是该团队或机构的成员。通常每个部门指定一个Board管理员。由该管理员添加部门的所有成员和跟踪者。

	_Label设置_
	+ Label是用来划分任务。每个Label有一个对应的颜色来标志任务属于哪种类型。Board通过Show sidebar->Menu->Settings->Edit label names设置Label。常见的Label的设置比如按照时间管理划分为紧急，重要，普通三种类型。还可以根据业为如下类型：
    某公司DBA团队按任务的状态分类:
    ![](/image/20140820/status.jpg)
    + 某开发团队按照任务的性质或类型分类:
    ![](/image/20140820/xinzhi.jpg)
 	+ 按照协作的小组:
    ![](/image/20140820/groupspai.jpg)
	+ 按照优先级划分：
    ![](/image/20140820/youxianji.jpg)
    _列表（List，管理员需要熟悉）_
	+ 列表是指任务列表，可以把列表理解为放置任务的容器。任务定义和拖动都是在列表中进行。列表如图默认是横向排列。

	+ 人为将List划分为不同阶段是方便管理和跟踪项目。项目跟踪人员可能查看待办的任务有哪些，正在办理的任务有哪些，办结的任务又有哪些。某个任务执行进度是多少（进入对应任务查看任务完成百分比，以及通过查看任务的Checklist观察任务被卡在哪里）。

	+ List新建后需要通过List下拉菜单先做归档（Archive），然后再Delete。
	![](/image/20140820/listaction.jpg)
	+ 归档List,List会从Board上消失，如果Archive之后，还想复原List到Board,可以Show sidebar->Menu->Achived Items->选中已经归档的List,Send to Board
	![](/image/20140820/menu.jpg)

	_任务（Card，每个项目成员都需要熟悉）_

	+ 任务列表List中的每个Card表示一个任务，任务具体指项目或者比项目粒度更小的一些事情。具体到信息技术，比如开发某个功能点，提数，培训，写文档都可以。只要需要花时间完成的工作都是任务。如果任务是一个项目，项目的完成周期很长，完全可以把”项目“拆分成多个Card。

	+ 任务的发起可以是任何人。任务需要定义在待办列表（To do）中。假设2014年信息技术部的主要任务是：机房搬迁、网点建设、ODS集中、全年保障等。

	+ 那么可以在To Do列表中新建任务, 新建任务是点击To do列表中的Add a card添加。
	![](/image/20140820/addcard.jpg)
	+ 当有资源可以保证开始任务时，就可以将任务拖动到办理中列表（Doing）, 指定任务的执行者（点开任务后，Assign给指定的人，可以同时指定给多人）。任务的执行者点击任务，可以通过Add checklist添加任务的可执行步骤（先点击Add checklist添加Checklist，使用默认的Title即可，添加之后光标会自动定位到Add Item，每个Item就是一个具体的步骤，输入所有的步骤之后，Checklist创建完成）以及任务的结束时间（Due date，通过右侧Due Date菜单项添加任务的完成时间，在接近完成时间以及超过完成时间，会有不同的提示）。

	+ 任务的执行者完成任务之后，可以将任务从Doing拖动到Done表示办结。

	+ 办结的任务可以归档。归档的目的是保持面板上任务列表中的任务保持当前任务。任务在被移动到办结列表中后，就可以归档，将任务变成历史任务。可以象恢复归档的列表一样，恢复已经归档的历史任务，将其变为当前任务，只有当前任务会在面板的列表中显示。

	+ Card中还可以上传附件，附件的内容可以是任务的需求文档也可以是表示任务完成的结果内容，比如报表，状态值。附件的类型可以是视频，声音，文档等格式。

	+ Card可以设置Label来标记该Card属于哪种类型。点击Edit Labels从Board中已经定义好的Label来标记任务。比如“紧急”。

	_任务在不同列表中流动_
	+ 介绍了Card的主要设置之后，Card做为元素在任务列表中流动是常用操作，一个完整的示例如下：

	+ 假设Card“ODS集中“的执行者可以开始该项任务，那么任务的执行者可以将任务从To Do拖到Doing。添加任务的Checklist，Due Date，上传任务需求文档。
	![](/image/20140820/cundang.jpg)
	+ 如果任务完成（执行者将Checklist项全部勾选），那么可以将任务从Doing拖到Done表示完结

	+ 在完成列表中，可以将任务归档。归档操作之后，Done列表不再会显示已归档的历史任务：

	_可执行步骤（Checklist，每个成员需要熟悉）_

	+ 可执行步骤是观察任务完成情况的指标，跟踪人员可以跟踪任务进度或者卡在哪里。 Checklist本身是在Card中添加。如果任务比较小，可以不设置Checklist。如果任务比较大，需要由任务的执行者细化为若干步骤。如果任务是跨部门合作的，每个部门的执行者可以添加自己的Checklist。总之，Checklist只有执行者最清楚怎么去细化。多个执行者可以分别定义多个Checklist。假设任务“ODS集中”可以分为以下几个步骤：了解现有ODS系统并熟悉ODS集中的背景和原因、ODS集中总行培训、ODS集中分行实施、ODS集中后问题修复，那么新建Checklist并Add Item如下：
	![](/image/20140820/checklist.jpg)
	+ 任务的执行者每完成一个步骤，就可以勾选相应的步骤。Checlist的进度条会显示相应的百分比。比如完成了步骤“了解现有ODS系统并熟悉ODS集中的背景和原因”并勾选后，进度条显示25%。

	_Activity（跟踪者和执行者等人需要熟悉）_

	+ Activity与Checklist一样，也是在Card的设置面板中显示。Activity表示与当前任务相关的动作。默认会记录Card的移动，归档等操作。Activity还有一个重要的功能是可以写评论。达到与相关人员沟通协作的目的。下图是Card "ODS集中"的Activity列表。里面记录了该Card相关的动作。
	![](/image/20140820/activity.jpg)

5. __如何跟踪任务进度（Board管理员和跟踪者需要熟悉）__
	+ 任务跟踪者如果单纯跟踪任务进度，只需要Board的管理员将跟踪者添加为Board的成员即可。只要成为任何一个Board的成员，登陆Trello就会显示该用户的所有可见的Board，进而可以进入想要跟踪的Board跟踪该Board中的任何任务。下图中用户登陆后可见的所有Board。 注意，Starred Boards中的Board是用星号标记过，表示经常使用的Board。
	![](/image/20140820/High.jpg)
    + 下面是“信息技术部”管理员将跟踪人员加入为Board成员的过程：

		- 点击进入“信息技术部”Board, 点击Show sidebar->Add Members将任务跟踪者加入到当前Board, 添加Board成员时可以使用跟踪人员的名称，但是最好使用可以唯一标志的邮箱（需要任务跟踪人员将Trello的注册邮箱提供给Board管理员添加）。
		- 在部门管理员邀请任务跟踪者加入部门的Board后，任务跟踪者登陆Trello，就可以在首页看到该部门的Board。
	![](/image/20140820/lookBoards.jpg)
 	+ 类似操作将任务跟踪者添加到他想要查看的任意Board里。跟踪者的首页就会列出可查看的所有Board，进而查看Board中的任务。

6. __机构（补充介绍，只需要管理员了解）__
	+ 如果某人被指定为Board管理员之后，除了可以通过右上角的“+”新建团队的Board外，还可以新建Organization。机构的目的个人理解是做一些有限的权限控制。比如将Board设置为机构可见。Board默认创建之后是私有的。只有Board成员可见。通过机构可以扩大Board的可见范围，即使某人没有添加为Board成员，但是如果添加为机构的成员，并且该Board是机构可见。那么该人员登陆Trello后，可以通过某些路径跟踪到该Board。下图显示创建机构之后，如何添加机构的成员以及设置机构的可见性。
	![](/image/20140820/Setc.jpg)
	+ 查看创建的机构不仅可以通过左上角的“Boards”查看到，还可以通过个人的Profile中查看，如下图Organizations所列机构：
	![](/image/20140820/allOrganizations.jpg)
	+ 机构的visible分为Public、Private，Public表示机构是公开的，可以被任何人访问到，一般公共的机构这样设置，企业设置为Private。

	+ Board的可见设置分为三种：Private、Organization、Public。默认为Private表示加入Board成员可见并且可编辑。Organization表示加入机构的成员可见。Public表示公网上的任何人可见。一般企业设置为Private或Organization。
	![](/image/20140820/visibility.jpg)
	+ Organization还有一个好处是避免被动重复添加Board成员的工作，而将这个工作交给Organization中的成员主动完成。

	+ 假设某个部门包含了多个团队，Board管理员需要为每个团队都新建一个Board，但是每个Board都可能需要全部门的成员加入。此时Board管理员没必要为每个Board添加重复的人员。而是将主动权交给Organization中的成员。前提是将Board设置为Organization可见并且通过Board的Show sidebar | Menu | Settings | Allow Org Members To Join设置为Organization的成员可主动加入Board。这样设置一次Organization可以服务多个Board，同时将Board添加成员的工作量分散到了机构的每个成员身上。这与Board管理员直接往Board里Add Member效果一样。只是一个主动申请，一个被动分配。
	![](/image/20140820/joinBoards.jpg)
	+ 类似的设置还有Menu | Settings | Commenting Permissions,可以设置Organization的成员即使没有加入Board，也可以发表评论。
	![](/image/20140820/comment.jpg)

7. __Trello的注册方式__
	+ 使用外网可以访问的邮箱，登陆https://trello.com，点击页面右上角的Sign Up, 输入Name(可以是姓名)，Email（外网访问邮箱），Password（Trello登陆密码）。注意，注册之后，一定要使用邮箱将帐户激活才可以有效使用Trello。 在激活之后，可以将注册邮箱提供给Board管理员用来将注册用户添加到Board成员。

	+ Board的创建根据具体情况建立。比如任务跟踪者需要了解哪个部门的计划和任务执行情况，就需要为该部门新建Board。并将执行者和跟踪者都加入到该Board里。


