# 一.PHP课程介绍
## 1. 什么是PHP
### 1.1 官方解释
* PHP（“PHP: Hypertext Preprocessor”，超文本预处理器的字母缩写）是一种被广泛应用的开放源代码的多用途脚本语言，它可嵌入到 HTML中，尤其适合 web 开发。

### 1.2 我们的理解
* PHP是一门语言，服务器端的脚本语言，适合开发WEB，实现功能。

### 1.3 为什么要学习PHP
* 入门简单，即使没有编程经验也可以很容易上手
* 全国稀缺PHP的人才,PHP平均薪资比较高
* PHP是热门的编程语言
* PHP开源免费，运行于各种平台(`Windows,Linux,Unix,Mac OSX`),兼容几乎所有的服务器(`Apache,Nginx,IIS`等)，PHP几乎支持所有的数据库(`MySQL,SQL Server,Access`等)

### 1.4 学习完之后我们能做什么
* 开发动态网站，实现网站中看到的任何功能

### 1.5 未来发展
* 未来一片光明

### 1.6 如何学习一门编程语言
* 3W1H1P
	* What  
		是什么，在学习任何语言之前要搞清楚学习的是什么东西
	* Why  
		为什么要学习它
	* When  
		什么时候，学完这个只是之后我们什么时候来使用
	* How  
		怎么用，知识要学会举一反三，灵活运用
	* Practice  
		实践，光说不练嘴把式，把所学的内容实践起来

### 1.7 学习建议
* 态度
* 自信
* 不能懒惰
* 坚持
* 要多想，多问，多练
* 英语


# 二、工欲善其事，必先利其器
## 2. PHP环境搭建
* LAMP
	* Linux+Apache+MySQL+PHP
* LNMP
	* Linux+Nginx+MySQL+PHP
* LNMPA
	* Linux+Nginx+MySQL+PHP+Apache
* WAMP
	* Window+Apache+MySQL+PHP
* 独立安装
	* Apache 2.4 
	* MySQL5.7
	* PHP7.1
* 集成环境
	* wampserver
	* xampp
	* phpstudy

## 2.1 IDE安装及使用
* Atom , Sublime Text3 ,PHPStorm,ZendStudio
* https://atom.io/

# 3. PHP基础语法
## 3.1 PHP文档结构
* 文件扩展名.php
* 注意
	* 文件名不要使用中文，也不要包含特殊字符
## 3.2 PHP标记
* 标准风格
	* `<?php  代码段; ?>`
	* 注意
		* 如果文档中只有PHP代码，结束标记要省略掉
		* 如果文档中不只有PHP代码，一定要保证PHP的开始和结束标记成对出现，可以出现任意位置，任意多次都可以
* 短风格
	* `<? 代码段; ?>`
	* 注意
		* 需要配置PHP配置文件php.ini中short_open_tag=On,重启Apache服务器即可
* ASP风格
	* `<% 代码段; %>`
	* 注意
		* 需要配置PHP配置文件php.ini中asp_tags=On,重启Apache服务器即可
## 3.3 PHP文档的组成
* PHP代码
* HTML
* CSS
* JS/Jquery
## 3.4PHP语法规范
* PHP代码以英文的分号结束;
## 3.5 PHP中的注释
* 注释的作用
	* 注释可以理解成解释
	* 注释在源代码中看不到，只能在源文件中看到，因为PHP引擎不解析注释
* 注释的分类
	* 单行注释
		* // 注释内容
			* C++风格的注释
		* `#` 注释内容
			* shell风格
	* 多行注释
		* /*注释内容*/


# 4.PHP中的变量
## 4.1 什么是变量
* 在程序执行期间可以变化的量就是变量，通过变量保存值
## 4.2 声明变量
* 通过美元$变量名称来表示变量，可以声明变量在使用，也可以不声明，可以一次声明一个，也可以一次声明多个
* 注意
	* 变量名称以字母或者下划线开始，后面跟上数字、字母下划线，不能包含特殊字符
	* 变量名称最好含义明确
	* 变量命名最好遵循驼峰标记法或者是下划线法
		* 驼峰标记法
			* 小骆驼
				* firstName,lastName,zendControllerFront
			* 大骆驼
				* FirstName,LastName,ZendControllerFront
		* 下划线法
			* first_name,last_name,zend_controller_front
	* 变量名称严格区分大小写，$a和$A这是两个变量
	* 如果变量名称重复，后面的变量会覆盖之前变量的值
	* PHP是弱类型语言，变量可以不声明直接使用
## 4.3 使用变量
* 直接书写变量的名称即可
	* $变量名称
## 4.4 可变变量
* 等量代换  
`$i='j';$j='k';$k='hello world';echo $$$i;`


# 5.PHP中的数据类型
## 5.1 8种主要数据类型
* 标量类型
	* 整型(int|integer)
		* 整数
			* 分类
				* 十进制(默认是十进制，打印变量：var_dump($变量))
				* 八进制（数字前面加加‘0’表示八进制；）
				* 十六进制（数字前面加‘0x’表示十六进制）
			* 范围
				* 带符号，-21亿~21亿之间，不带符号0~42亿
				* 超过整型存储范围，会产生溢出的现象
	* 浮点型(float|double|real)
		* 带小数点
		* 科学计数法的写法，e或者E
		* 注意
			* 浮点数比整型大
			* 浮点数是有误差，不要比较两个浮点数的大小
	* 布尔型(bool|boolean)
		* 要么是真，要么是假
			* true|TRUE：真
			* false|FALSE：假
			
	* 字符串型(string)
		* 定界符
			* 单引号
			* 双引号
			* heredoc 写大段文本用这个,和双引号效果一样。
				* 写法：<<<名称、代码段；名称;
				* 或这种写话：<<<"名称" 、代码段;、名称;
				* 例：`$str=<<<EOF` 换行结束开头`EOF;`
				* 注意
					* 在结束名称之前不能有任何输出
					* heredoc相当于双引号
			* nowdoc 相当于单引号
				* <<<'名称'、代码段;、名称;
				* 注意
					* nowdoc相当于单引号的作用
					*其他的和`heredoc`使用一样

			* 单引号和双引号的区别
				* 单引号不解析变量，双引号解析变量
				* 单引号只解析\'和\\,而双引号解析所有的转义符
			* 字符串替换操作
				* 字符串对应位置从0开始
				* 修改字符串只能一个字符串替换一个字符串
				* 不要对中字符串操作，一个中文占3个位数。
			* 字符串增加和删除操作
				* 删除用空字符串替换`$sting{0}='';`
				* 添加`$sting{5}='a';`
		* 转义符
			* \n  
				代表 换行
			* \r  
				代表 回车
			* \t  
				代表 水平制表符
					* 源代码中有效果，页面上只显示一个空格

			* `\\  `  
				代表 \
			* `\$  `  
				代表 $
			* `\'  `  
				代表 '
			* `\"  `  
				代表 "
				
		* 花括号{}
			* 可以将PHP中的变量括成一个整体来解析
				* {$变量名称}
				* ${变量名称}
			* 可以对字符串中的指定字符做增删改查的操作
				* 字符串的下标从0开始
				* 根据下标找到对应的字符做操作
	* 特点
		* 只能存储单一数据sss


* 复合类型
	* 数组(Array)
		```php
		$arr=array();//空数组
		var_dump($arr);
		```
	* 对象(Object)
		```php
		$obj=new StdClass();//空对象
		var_dump($obj);
		```


* 特殊类型
	* 资源(Resource) //如，软件、数据库、系统文件、通过API或函数访问
	* 空(null|NULL)
		* 变量未声明直接使用，它的值就是null  
			`var_dump($noteExistVar);//输出null`
		* 声明一个变量并且赋值为null  
			`$var=null; var_dump($var);//输出null`
		* 经过unset()注销过的变量值为null  
			`$var1=123; unset($var1)//输出null,销毁单个`
			`$a=$b=$c=123; unset($a,$b,$c)//输出null，销毁多个`
* 5种伪类型
	* number 参数可以是整型浮点型
	* mixed  混合的，可以接受不同的函数类型
	* callback 
	* void 没有返回值或不接受任何参数
	* ... 接受任意多个参数


# 6.PHP中的数据类型转换
* 自动转换(隐式转换)
	* 程序会根据上下文环境自动的进行转换
	* 其它类型转换成数值型
		* true->1; 
			* `echo 1+true;//结果2`
		* false->0；
			* `echo 1+false;//结果1`
		* null->0
		* 字符串如果以非法数值开始，直接转换成0；
			* `echo 1+'3abe';//结果4`
		* 如果字符串以合法数值开始，一直取到第一个非法数值结束
			* `echo 1+'true';//结果1,true不是合法数字开始即为0`

	* 其它类型转换成字符串型
		* 数值型直接转换成数值本身
		* true->1
		* false->空字符串 
			`echo '#',false,'#';//结果##`
		* null->空字符串 
			`echo '@',null,'@';//结果@@`
		* 数组->Array
		* 资源->Resource id #数字
		* 对象不能直接转换成字符串 
			`$obj=new StdClass();//致命错误终止程序`

	* 其它类型转换成布尔类型假的有（常用）
		* 除0外其他整型转换为真
		* 0->false
		* 0.0->false
		* 空字符串''或者""或者'0'或者"0"->false
		* null->false
		* 空数组array()->false
		
* 强制转换(显示转换)
	* 临时转换
		* (变量类型)$变量名称
			* 整型
				* (int)$变量名称|(integer)$变量名称
			* 浮点型
				* (float|double|real)$变量名称
			* 字符型
				* (string)$变量名称
			* 布尔型
				* (bool|boolean)$变量名称
			* 空
				* (unset)$变量名称
			* 数组
				* (array)$变量名称
			* 对象
				* (object)$变量名称
		* 通过系统函数实现
			* intval($var)
				* 返回变量转换成整型之后的值
			* floatval($var)|doubleval($var)
				* 返回变量转换成浮点型的值
			* strval($var)
				* 返回变量转换成字符串的值
			* boolval($var)
				* 返回变量转换成布尔类型的值
		* 注意
			* 临时转换不改变变量本身的类型
	* 永久转换
		* settype($var,$type)
			* 设置变量的类型
		* gettype($var)
			* 返回变量的类型
			* 注意
				* 不要使用gettype得到变量的类型，因为后续可能返回值会改变
	* 通过变量函数库检测变量的类型
		* is_*($var)
			* 检测的结果要么true，要么false
			* 整型
				* is_int()|is_integer()|is_long()
			* 浮点型
				* is_float()|is_double()|is_real()
			* 字符串型
				* is_string()
			* 布尔类型
				* is_bool()
			* 标量类型
				* is_scalar()
			* 空null
				* is_null()
			* 数组
				* is_array()
			* 对象
				* is_object()
			* 资源
				* is_resource()
			* 是否为数值型或者字符串形式的数值
				* is_numeric()