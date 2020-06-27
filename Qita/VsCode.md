## VsCode常用软件配置
    主题颜色：Atom One Dark Theme
    图标选择：vscode-icon
    思维导图：vscode-mindmap
    SYNC同步：安装sync 输入下载GitHub Gist ID:d1da3472da3acf2979164df23f92f8ac
        注意：安装sync上传配置出现失败，在F1命令面板输入sync重置，重新输入
        Github tongken:b6cc741af49e7d2a8236ab5a7259ba7485091348
        github无法访问：hosts配置未见在文末
        
        sync下载同步：
        注意：第一步输入Github tongken;第二部输入下载GitHub Gist ID
    其他NetBeans IDE上传同步数据
        初始化-提取-添加-提交-推入


# GitHub仓库：
    00、git clone https://github.com/dawoy/php.git。//github存在仓库，首先克隆仓库。
    01、git init //克隆下来的仓库带git,不用使用初始化命令，如果没有就用命令初始化管理目录。
    02、git add . //添加所有文件包含修改文件。git add -A  添加到暂存区，如果后面接小数点“.”意为添加文件夹下的所有文件
    03、git commit -m "首次提交" //提交注释。
    04、git remote add origin https://自己的仓库url地址
    05、git push origin master //提交 会提示输入代码。
    

## 1、操作命令行模式
    1、同步仓库： git pull origin master  
        //保证代码一致性，每次操作前进行一次同步操作(origin远程仓库名，master分支)
    2、提交当前仓库的所有改动： git add .或git add -A  添加到暂存区，如果后面接小数点“.”，
        意为添加文件夹下的所有文件
    3、添加描述：git commit -m '简单修改'
    4、推送到远程仓库 git push origin master  // 强制推送加 -f  会覆盖别人的更新 
            仓库当前文件提交状态  git status -s
            提交的日志 git log
## 1、界面按钮点击模式
        点击'+'提交文件到暂存区
        点击'提交已暂存的文件' 输入好描述文件。
        点击'推送'

# 阿里云对象OSS自动上传
     扩展：名称: aliyun oss upload image   截图上传阿里云oss插件
     说明：阿里云创建RAM权限控制，创建用户设置管理OSS对象权限有写入权限。
         设置：Access Key ID；Access Key Secret；bucket名称；对外访问链接域名；/tmp缓存文件VSCODE根目录下创建
         设置地域节点：如：oss-cn-beijing；存放位置根目录下不用填写。
         然后在md文件格式中使用shift + P
    

# General
     Ctrl + Shift + P，F1    显示命令面板 安装插件 Show Command Palette
     Ctrl + P	            快速打开 Quick Open
     Ctrl + Shift + N	    新窗口/实例 New window/instance
     Ctrl + Shift + W	    关闭窗口/实例 Close window/instance

# 基础编辑 Basic editing
    Ctrl+X	            剪切行（空选定） Cut line (empty selection)
    Ctrl+C	            复制行（空选定）Copy line (empty selection)
    Alt+ ↑ / ↓	        向上/向下移动行 Move line up/down
    Shift+Alt + ↓ / ↑	向上/向下复制行 Copy line up/down
    Ctrl+Shift+K	    删除行 Delete line
    Ctrl+Enter	        在下面插入行 Insert line below
    Ctrl+Shift+Enter	在上面插入行 Insert line above
    Ctrl+Shift+\	    跳到匹配的括号 Jump to matching bracket
    Ctrl+] / [	        缩进/缩进行 Indent/outdent line
    Home	            转到行首 Go to beginning of line
    End	                转到行尾 Go to end of line
    Ctrl+Home	        转到文件开头 Go to beginning of file
    Ctrl+End	        转到文件末尾 Go to end of file
    Ctrl+↑ / ↓	        向上/向下滚动行 Scroll line up/down
    Alt+PgUp / PgDown	向上/向下滚动页面 Scroll page up/down
    Ctrl+Shift+[	    折叠（折叠）区域 Fold (collapse) region
    Ctrl+Shift+]	    展开（未折叠）区域 Unfold (uncollapse) region
    Ctrl+K Ctrl+[	    折叠（未折叠）所有子区域 Fold (collapse) all subregions
    Ctrl+K Ctrl+]	    展开（未折叠）所有子区域 Unfold (uncollapse) all subregions
    Ctrl+K Ctrl+0	    折叠（折叠）所有区域 Fold (collapse) all regions
    Ctrl+K Ctrl+J	    展开（未折叠）所有区域 Unfold (uncollapse) all regions
    Ctrl+K Ctrl+C	    添加行注释 Add line comment
    Ctrl+K Ctrl+U	    删除行注释 Remove line comment
    Ctrl+/	            切换行注释 Toggle line comment
    Shift+Alt+A	        切换块注释 Toggle block comment
    Alt+Z	            切换换行 Toggle word wrap


# 导航 Navigation
    Ctrl + T	        显示所有符号 Show all Symbols
    Ctrl + G	        转到行... Go to Line...
    Ctrl + P	        转到文件... Go to File...
    Ctrl + Shift + O	转到符号... Go to Symbol...
    Ctrl + Shift + M	显示问题面板 Show Problems panel
    F8	                转到下一个错误或警告 Go to next error or warning
    Shift + F8	        转到上一个错误或警告 Go to previous error or warning
    Ctrl + Shift + Tab	导航编辑器组历史记录 Navigate editor group history
    Alt + ←/→	        返回/前进 Go back / forward
    Ctrl + M	        切换选项卡移动焦点 Toggle Tab moves focus


# 搜索和替换 Search and replace
    Ctrl + F	          查找 Find
    Ctrl + H	          替换 Replace
    F3 / Shift + F3	      查找下一个/上一个 Find next/previous
    Alt + Enter	          选择查找匹配的所有出现 Select all occurences of Find match
    Ctrl + D	          将选择添加到下一个查找匹配 Add selection to next Find match
    Ctrl + K Ctrl + D	  将最后一个选择移至下一个查找匹配项 Move last selection to next Find match
    Alt + C / R / W	      切换区分大小写/正则表达式/整个词 Toggle case-sensitive / regex / whole word


# 多光标和选择 Multi-cursor and selection
    Alt +单击	        插入光标 Insert cursor
    Ctrl + Alt +↑/↓	    在上/下插入光标 Insert cursor above / below
    Ctrl + U	        撤消上一个光标操作 Undo last cursor operation
    Shift + Alt + I	    在选定的每一行的末尾插入光标 Insert cursor at end of each line selected
    Ctrl + I	        选择当前行 Select current line
    Ctrl + Shift + L	选择当前选择的所有出现 Select all occurrences of current selection
    Ctrl + F2	        选择当前字的所有出现 Select all occurrences of current word
    Shift + Alt + →	    展开选择 Expand selection
    Shift + Alt + ←	    缩小选择 Shrink selection
    Shift + Alt + （拖动鼠标）	            列（框）选择 Column (box) selection
    Ctrl + Shift + Alt +（箭头键）	        列（框）选择 Column (box) selection
    Ctrl + Shift + Alt + PgUp / PgDown	   列（框）选择页上/下 Column (box) selection page up/down


# 丰富的语言编辑 Rich languages editing
    Ctrl + 空格	             触发建议 Trigger suggestion
    Ctrl + Shift + Space	触发器参数提示 Trigger parameter hints
    Tab	Emmet               展开缩写 Emmet expand abbreviation
    Shift + Alt + F	        格式化文档 Format document
    Ctrl + K Ctrl + F	    格式选定区域 Format selection
    F12	                    转到定义 Go to Definition
    Alt + F12	            Peek定义 Peek Definition
    Ctrl + K F12	        打开定义到边 Open Definition to the side
    Ctrl + .	            快速解决 Quick Fix
    Shift + F12	            显示引用 Show References
    F2	                    重命名符号 Rename Symbol
    Ctrl + Shift + . /，	替换为下一个/上一个值 Replace with next/previous value
    Ctrl + K Ctrl + X	    修剪尾随空格 Trim trailing whitespace
    Ctrl + K M	            更改文件语言 Change file language


# 编辑器管理 Editor management
    Ctrl+F4, Ctrl+W	    关闭编辑器 Close editor
    Ctrl+K F	        关闭文件夹 Close folder
    Ctrl+\	            拆分编辑器 Split editor
    Ctrl+ 1 / 2 / 3	    聚焦到第1，第2或第3编辑器组 Focus into 1st, 2nd or 3rd editor group
    Ctrl+K Ctrl+ ←/→	聚焦到上一个/下一个编辑器组 Focus into previous/next editor group
    Ctrl+Shift+PgUp / PgDown	向左/向右移动编辑器 Move editor left/right
    Ctrl+K ← / →	    移动活动编辑器组 Move active editor group


# 文件管理 File management
    Ctrl+N	        新文件 New File
    Ctrl+O	        打开文件... Open File...
    Ctrl+S	        保存 Save
    Ctrl+Shift+S	另存为... Save As...
    Ctrl+K S	    全部保存 Save All
    Ctrl+F4	        关闭 Close
    Ctrl+K Ctrl+W	关闭所有 Close All
    Ctrl+Shift+T	重新打开关闭的编辑器 Reopen closed editor
    Ctrl+K	        输入保持打开 Enter Keep Open
    Ctrl+Tab	    打开下一个 Open next
    Ctrl+Shift+Tab	打开上一个 Open previous
    Ctrl+K P	    复制活动文件的路径 Copy path of active file
    Ctrl+K R	    显示资源管理器中的活动文件 Reveal active file in Explorer
    Ctrl+K O	    显示新窗口/实例中的活动文件 Show active file in new window/instance


# 显示 Display
    F11	            切换全屏 Toggle full screen
    Shift+Alt+1	    切换编辑器布局 Toggle editor layout
    Ctrl+ = / -	    放大/缩小 Zoom in/out
    Ctrl+B	        切换侧栏可见性 Toggle Sidebar visibility
    Ctrl+Shift+E	显示浏览器/切换焦点 Show Explorer / Toggle focus
    Ctrl+Shift+F	显示搜索 Show Search
    Ctrl+Shift+G	显示Git Show Git
    Ctrl+Shift+D	显示调试 Show Debug
    Ctrl+Shift+X	显示扩展 Show Extensions
    Ctrl+Shift+H	替换文件 Replace in files
    Ctrl+Shift+J	切换搜索详细信息 Toggle Search details
    Ctrl+Shift+C	打开新命令提示符/终端 Open new command prompt/terminal
    Ctrl+Shift+U	显示输出面板 Show Output panel
    Ctrl+Shift+V	切换Markdown预览 Toggle Markdown preview
    Ctrl+K V	    从旁边打开Markdown预览 Open Markdown preview to the side


# 调试 Debug
    F9	            切换断点 Toggle breakpoint
    F5	            开始/继续 Start/Continue
    Shift+F5	    停止 Stop
    F11 / Shift+F11	    下一步/上一步 Step into/out
    F10	            跳过 Step over
    Ctrl+K Ctrl+I	显示悬停 Show hover


# 集成终端 Integrated terminal
    Ctrl+`	        显示集成终端 Show integrated terminal
    Ctrl+Shift+`	创建新终端 Create new terminal
    Ctrl+Shift+C	复制选定 Copy selection
    Ctrl+Shift+V	粘贴到活动端子 Paste into active terminal
    Ctrl+↑ / ↓	    向上/向下滚动 Scroll up/down
    Shift+PgUp / PgDown	    向上/向下滚动页面 Scroll page up/down
    Ctrl+Home / End	        滚动到顶部/底部 Scroll to top/bottom

# GITHUB无法访问HOStS文件
#Github
151.101.73.194 github.global.ssl.fastly.net
151.101.108.133 assets-cdn.github.com
185.199.111.153 documentcloud.github.com
185.199.110.153 documentcloud.github.com
185.199.109.153 documentcloud.github.com
185.199.108.153 documentcloud.github.com
192.30.253.113 github.com
192.30.253.112 github.com
192.30.253.119 gist.github.com
192.30.253.118 gist.github.com
185.199.111.153 help.github.com
185.199.110.153 help.github.com
185.199.109.153 help.github.com
185.199.108.153 help.github.com
192.30.253.121 nodeload.github.com
192.30.253.120 nodeload.github.com
151.101.108.133 raw.github.com
18.204.240.114 status.github.com
18.211.136.12 status.github.com
18.211.136.12 status.github.com
192.30.253.166 training.github.com
151.101.109.194 github.global.ssl.fastly.net
151.101.108.133 avatars0.githubusercontent.com
151.101.72.133 avatars1.githubusercontent.com