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

- Download Google App Apk
http://apps.evozi.com/apk-downloader/

- Real time user presence (the technical explanation)
http://docs.intercom.io/FAQs/real-time-user-presence-the-technical-explanation

- hasattr
http://stackoverflow.com/questions/610883/how-to-know-if-an-object-has-an-attribute-in-python

- comm
https://blog.tallan.com/2014/11/03/bidirectional-communication-between-directives-and-controllers-in-angular/

- emoji code
http://apps.timwhitlock.info/emoji/tables/unicode

- HTTP assess control (CORS)
https://developer.mozilla.org/en-US/docs/Web/HTTP/Access_control_CORS

- js object oriented introduction
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Introduction_to_Object-Oriented_JavaScript

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


## Css learn

### Why use css

- Helps avoid duplication
- Makes maintenance easier
- Allows you to make a site-wide change in one place

### Tag Selector

```css
p {
  color:blue;
  text-decoration:underline
}

strong {
  color:red
}
```

### Class Selectors And ID Selectors

```css
<p class="key" id="principal">

.key {
  color: green;
}

#principal {
  font-weight: bolder;
}

p.key {
  color: green;
}
``

specific: tag selector < class selector < id selector

### Pseudo-classes selectors

A CSS pseudo-class is a keyword added to selectors that specifies a special state of the element to be selected.

```css
selector:pseudo-class {
  property: value;
}
```

- :link
- :visited
- :active
- :hover
- :focus
- :first-child
- :last-child
- :nth-child
- :nth-last-child
- :nth-of-type
- :first-of-type
- :last-of-type
- :empty
- :target
- :checked
- :enabled
- :disabled

```css
a.homepage:hover, a.homepage:focus, a.homepage:active {
  background-color: #666;
}
```

### Information: Selectors based on relationships

Selector | Selects
A E | Any E element that is a descendant of an A element (that is: a child, or a child of a child, etc.)
A > E | Any E element that is a child (i.e. direct descendant) of an A element
E:first-child | Any E element that is the first child of its parent
B + E | Any E element that is the next sibling of a B element (that is: the next child of the same parent)

You can also use the symbol * (asterisk) to mean "any element".

```css
div.menu-bar ul ul {
  display: none;
}

div.menu-bar li:hover > ul {
  display: block;
}
```

### Readable css

Comments

```
/* style for initial letter C in first paragraph */
.carrot {
  color:            orange;
  text-decoration:  underline;
  font-style:       italic;
  }
```

Grouped selectors

```
/* color for headings */
h1, h2, h3 {color: navy;}
```

## Web technology for developers

https://developer.mozilla.org/en-US/docs/Web

## JavaScript

### Prototype-based programming

Prototype-based programming is an OOP model that doesn't use classes, but rather accomplishes behavior reuse (equivalent to inheritance in class-based languages) by decorating (or expanding upon) existing prototype objects. (Also called classless, prototype-oriented, or instance-based programming.)