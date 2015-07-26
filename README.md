# developer-blog

- 下载文件
curl -o sqlalachemy.pdf https://media.readthedocs.org/pdf/sqlalchemy/rel_1_0/sqlalchemy.pdf

- 设置列默认值
alter table material_refinfos alter visible set default 1;

- 解压rar
unrar x xx-xxxx-xxx-xxx.rar

- emacs 批量注释
Alt + ;
- emacs 移动到上一个单词
M + b
- emacs 移动到下一个单词
M + f
- emacs 全选
C + x, h
- emacs 自动对齐
C + M + |

- git merge conflict
```git
<<<<<<< HEAD
我的修改
=======
别人的修改
>>>>>>> issue478
```

- 移除当前目录下所有1天前的文件
find . -mtime +1 -exec rm -rf {} \;

- unzip
unzip -d dir xxx.zip

- emacs 打开缓冲区
C-x C-b
- emacs 在两个窗口中切换
C-x o
- emacs query-replace
M-Shift-%,键入想要搜索的关键词，回车，输入想要替换的词，回车，空格继续下一个匹配

- 查找当前目录包括子目录下面所有文件中包含某个字符串的文件
grep "你想要查找的字符串" -R .

- git 恢复单个文件到最近commit
git checkout -- 文件路径
- git stash
- git stash apply

git push 应该先加ssh key，然后再clone
- git remote set-url origin git@github.com:dingguijin/cordova-plugin-mqtt.git
- git push origin master

- ./android avd : to open avd
- use `dd` to create specified size's file
dd if=/dev/zero of=test.data bs=1m count=500 -----> create a file which name is test.data and size is 500m.

- 《股票大作手回忆录》http://product.dangdang.com/20020271.html
- 《以交易为生》
- 《炒股的智慧》
- 《Advanced Programming in the UNIX Environment》
- 《深入理解计算机系统》
- 《Unix Internals》
- 《Understanding the Linux Kernel》

vi E37: No write since last change (add ! to override)
- 1. Hit 'Esc' key twice, to exit editing mode
- 2. Enter vi command mode by type in ':' and then type in 'q!' key and hit 'Enter' key to force quit vi without making any changes to the document.

- Mac Commands
Take a screenshot of part of your screen: command + shift + 4

------------------------SQLite---------------------

- .table
- .schema table_name
- .help
- .exit / .quit Exit this program
- .show Show the current values for various settings

- http://www.sqlite.org/pragma.html#pragma_index_info

-- PRAGMA table_info(your_table_name);
This pragma returns one row for each column in the named table. Columns in the result set include the column name, data type, whether or not the column can be NULL, and the default value for the column. The "pk" column in the result set is zero for columns that are not part of the primary key, and is the index of the column in the primary key for columns that are part of the primary key.

-- PRAGMA index_list(your_table_name);
This pragma returns one row for each index associated with the given table.

```sql

sequence number | index name | unique: 1, not unique: 0

0|index_messages_from_id|0

```

------------------------stackoverflow---------------------
- http://stackoverflow.com/questions/1108/how-does-database-indexing-work?rq=1

- https://engineering.purdue.edu/ECN/Support/KB/Docs/ViTextEditorTutorial/3.exiting

- http://stackoverflow.com/questions/221294/how-do-you-get-a-timestamp-in-javascript
-- new Date().getTime();

- Xiaomi MIUI6 set icon number
http://dev.xiaomi.com/doc/p=3904/index.html

- Emacs Commands
http://www.gnu.org/software/emacs/tour/

- keep processes running after ending ssh session
http://askubuntu.com/questions/8653/how-to-keep-processes-running-after-ending-ssh-session

- everything you never know about css floats
http://designshack.net/articles/css/everything-you-never-knew-about-css-floats/

- Introduction to tornado
http://demo.pythoner.com/itt2zh/ch8.html

- An introduction to Redis data types and abstractions
http://redis.io/topics/data-types-intro

------------------------english---------------------
frustrated

------------------------Job Requirement----------------

https://ie.linkedin.com/jobs2/view/56482765?trk=job_view_browse_map&trk=job_view_browse_map

You will work as part of a team developing new apps, and sometimes supporting existing apps, across a wide range of different industries.

 

There will be opportunities to work on different kinds of apps from project to project and often times the apps you work on will be for well known organisations and will have a large amount of users.




Duties and responsibilities

You will be expected to:

consistently ship high quality code on time

work with other senior developers, designers, QA specialists and our clients from project kickoff to delivery and beyond

provide input and feedback on design, platform specific best practices and usability

talk to our clients and their users and discuss and propose features

explore new technologies and tools through R&D initiatives from time to time

direct and mentor junior team members




Qualifications & Experience required

extensive experience shipping high quality code (ideally more than 5 years professional experience)

examples of completed Android apps

expertise with both Eclipse and Android studio

expertise with source control (we use git)

expertise building UIs using the latest design guidelines

experience using testing frameworks

knowledge of design patterns such as MVP and dependency injection

experience in other languages and environments

experience consuming web services in a mobile app

experience creating novel user interfaces

ability to work on your own initiative

Java certification desirable

https://nl.linkedin.com/jobs2/view/49881806?trk=job_view_browse_map&trk=job_view_browse_map
- A/B testing

------------------ebook-------------------

- [Packtpub](https://www.packtpub.com)

- [CSS Ebook Download](http://ebook.jiani.info/category/programming_language/CSS)

------------------css---------------------

http://zh.learnlayout.com/

## display
display:block #块级元素
display:inline #行级元素
display:none #不会保留元素本来应该显示的空间, 但是visibility:hidden还会保留

块级元素:div, p, form... 开始新的一行,尽可能的撑满容器
行级元素:span, a

## margin
设置块级元素的`width`可以阻止它撑满容器,然后就可以设置左右外边距`auto`来使其水平居中

```
#main {
	width:600px;
	margin:0 auto;
}
```

## max-width
使用max-width代替width能够很好的处理小窗口的情况,这点在移动设备上尤其重要,窗口水平缩小的时候不会出现滚动条了
```
#main {
	max-width:600px;
	margin:0 auto;
}
```

## 盒模型
在我们讨论宽度的时候，我们应该讲下与它相关的一个重点知识：盒模型。当你设置了元素的宽度，实际展现的元素却能够超出你的设置：因为元素的边框和内边距会撑开元素。看下面的例子，两个相同宽度的元素显示的实际宽度却不一样。
```
.simple {
  width: 500px;
  margin: 20px auto;
}

.fancy {
  width: 500px;
  margin: 20px auto;
  padding: 50px;
  border-width: 10px;
}
```

## box-sizing
经过了一代又一代人们意识到数学不好玩，所以他们新增了一个叫做 box-sizing 的CSS属性。当你设置一个元素为 box-sizing: border-box; 时，此元素的内边距和边框不再会增加它的宽度。这里有一个与前一页相同的例子，唯一的区别是两个元素都设置了 box-sizing: border-box;
```
.simple {
  width: 500px;
  margin: 20px auto;
  -webkit-box-sizing: border-box;
     -moz-box-sizing: border-box;
          box-sizing: border-box;
}

.fancy {
  width: 500px;
  margin: 20px auto;
  padding: 50px;
  border: solid blue 10px;
  -webkit-box-sizing: border-box;
     -moz-box-sizing: border-box;
          box-sizing: border-box;
}
```
既然没有比这更好的方法，一些CSS开发者想要页面上所有的元素都有如此表现。
```
* {
  -webkit-box-sizing: border-box;
     -moz-box-sizing: border-box;
          box-sizing: border-box;
}
```

## position
relative 表现的和 static 一样，除非你添加了一些额外的属性。

在一个相对定位（position属性的值为relative）的元素上设置 top 、 right 、 bottom 和 left 属性会使其偏离其正常位置。其他的元素则不会调整位置来弥补它偏离后剩下的空隙。
```
.relative1 {
  position: relative;
}
.relative2 {
  position: relative;
  top: -20px;
  left: 20px;
  background-color: white;
  width: 500px;
}
```

一个固定定位（position属性的值为fixed）元素会相对于视窗来定位，这意味着即便页面滚动，它还是会停留在相同的位置。和 relative 一样， top 、 right 、 bottom 和 left 属性都可用。

一个固定定位元素不会保留它原本在页面应有的空隙。


```
.fixed {
  position: fixed;
  bottom: 0;
  right: 0;
  width: 200px;
  background-color: white;
}
```

absolute 是最棘手的position值。 absolute 与 fixed 的表现类似，除了它不是相对于视窗而是相对于最近的“positioned”祖先元素。如果绝对定位（position属性的值为absolute）的元素没有“positioned”祖先元素，那么它是相对于文档的 body 元素，并且它会随着页面滚动而移动。记住一个“positioned”元素是指p osition 值不是 static 的元素。

```
.relative {
  position: relative;
  width: 600px;
  height: 400px;
}
.absolute {
  position: absolute;
  top: 120px;
  right: 0;
  width: 300px;
  height: 200px;
}
```

## position例子
使用margin-xx来确保一些元素有空间来显示它们
[Example](http://zh.learnlayout.com/position-example.html)

## float
另一个布局中常用的CSS属性是 float 。Float 可用于实现文字环绕图片
```
img {
  float: right;
  margin: 0 0 1em 1em;
}
```

## clear
clear 属性被用于控制浮动。

使用 clear 我们就可以将这个段落移动到浮动元素 div 下面。你需要用 left 值才能清除元素的向左浮动。你还可以用 right 或 both 来清除向右浮动或同时清除向左向右浮动。

```
.box {
  float: left;
  width: 200px;
  height: 100px;
  margin: 1em;
}
.after-box {
  clear: left;
}
```

## 清除浮动（clearfix hack）

这个图片比包含它的元素还高， 而且它是浮动的，于是它就溢出到了容器外面！

见证奇迹的时刻到了！有一种比较丑陋的方法可以解决这个问题，它叫做清除浮动（clearfix hack）.

让我们加入一些新的CSS样式：

```
.clearfix {
  overflow: auto;
}

<div class="clearfix">
```

这个可以在现代浏览器上工作。如果你想要支持IE6，你就需要再加入如下样式：

```
.clearfix {
  overflow: auto;
  zoom: 1;
}
```

有些独特的浏览器需要“额外的关照”。[清除浮动这谭水很深很深](http://stackoverflow.com/questions/211383/which-method-of-clearfix-is-best)，但是这个简单的解决方案已经可以在今天所有的主要浏览器上工作。

## 浮动布局例子
完全使用 float 来实现页面的布局是很常见的。
```
nav {
  float: left;
  width: 200px;
}
section {
  margin-left: 200px;
}
```

## 百分比宽度
百分比是一种相对于包含块的计量单位。

你甚至还能同时使用 min-width 和 max-width 来限制图片的最大或最小宽度！

当布局很窄时， nav 就会被挤扁。更糟糕的是，你不能在 nav 上使用 min-width 来修复这个问题，因为右边的那列是不会遵守它的。

## 媒体查询
“响应式设计（Responsive Design）”是一种让网站针对不同的浏览器和设备“响应”不同显示效果的策略，这样可以让网站在任何情况下显示的很棒！

媒体查询是做此事所需的最强大的工具。让我们使用百分比宽度来布局，然后在浏览器变窄到无法容纳侧边栏中的菜单时，把布局显示成一列：

```
@media screen and (min-width:600px) {
  nav {
    float: left;
    width: 25%;
  }
  section {
    margin-left: 25%;
  }
}
@media screen and (max-width:599px) {
  nav li {
    display: inline;
  }
}

使用 meta viewport 之后可以让你的布局在移动浏览器上显示的更好
```

## inline-block
你可以创建很多网格来铺满浏览器。在过去很长的一段时间内使用 float 是一种选择，但是使用 inline-block 会更简单。

使用 after-box的div 不会浮动到上面那堆盒子的旁边。

```
.box {
  float: left;
  width: 200px;
  height: 100px;
  margin: 1em;
}
.after-box {
  clear: left;
}
```

你可以用 display 属性的值 inline-block 来实现相同效果

```
.box2 {
  display: inline-block;
  width: 200px;
  height: 100px;
  margin: 1em;
}
```

也不用使用clear了

## inline-block 布局
你可以使用 inline-block 来布局。有一些事情需要你牢记：

- vertical-align 属性会影响到 inline-block 元素，你可能会把它的值设置为 top 。
- 你需要设置每一列的宽度
- 如果HTML源代码中元素之间有空格，那么列与列之间会产生空隙

```
nav {
  display: inline-block;
  vertical-align: top;
  width: 25%;
}
.column {
  display: inline-block;
  vertical-align: top;
  width: 75%;
}
```

## column

这里有一系列新的CSS属性，可以帮助你很轻松的实现文字的多列布局。

```
.three-column {
  padding: 1em;
  -moz-column-count: 3;
  -moz-column-gap: 1em;
  -webkit-column-count: 3;
  -webkit-column-gap: 1em;
  column-count: 3;
  column-gap: 1em;
}
```

## flexbox

新的 flexbox 布局模式被用来重新定义CSS中的布局方式。很遗憾的是最近规范变动过多，导致各个浏览器对它的实现也有所不同。不过我仍旧想要分享一些例子，来让你知道即将发生的改变。这些例子目前只能在支持 flexbox 的 Chrome 浏览器中运行，基于最新的标准。

```
.container {
  display: -webkit-flex;
  display: flex;
}
nav {
  width: 200px;
}
.flex-column {
  -webkit-flex: 1;
          flex: 1;
}
```

flex 看样子描述的是一种比例

```
.container {
  display: -webkit-flex;
  display: flex;
}
.initial {
  -webkit-flex: initial;
          flex: initial;
  width: 200px;
  min-width: 100px;
}
.none {
  -webkit-flex: none;
          flex: none;
  width: 200px;
}
.flex1 {
  -webkit-flex: 1;
          flex: 1;
}
.flex2 {
  -webkit-flex: 2;
          flex: 2;
}
```

使用 Flexbox 的居中布局

```
.vertical-container {
  height: 300px;
  display: -webkit-flex;
  display:         flex;
  -webkit-align-items: center;
          align-items: center;
  -webkit-justify-content: center;
          justify-content: center;
}
```

## css框架

[框架](https://github.com/anxiaoyi/developer-blog/blog/master/image/css-frame.png)
