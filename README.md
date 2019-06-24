# Docsify

# 安装
!>推荐安装 docsify-cli 工具，可以方便创建及本地预览文档网站。

	!>npm i docsify-cli -g

# 初始化项目
>如果想在项目的 ./docs 目录里写文档，直接通过 init 初始化项目。

	docsify init ./docs

# 开始写文档
>初始化成功后，可以看到 ./docs 目录下创建的几个文件

	index.html 入口文件
	README.md 会做为主页内容渲染
	.nojekyll 用于阻止 GitHub Pages 会忽略掉下划线开头的文件
	直接编辑 docs/README.md 就能更新网站内容，当然也可以写多个页面。

# 本地预览网站
>运行一个本地服务器通过 docsify serve 可以方便的预览效果，而且提供 LiveReload 功能，可以让实时的预览。默认访问 http://localhost:3000 。

	docsify serve docs

# 配置中心

```php
<body>
<!--主框架-->
  <div id="app"></div>

<!--渲染 导航 显示目录-->
<script>
  window.$docsify = {
    name: '',
    repo: '',
    loadNavbar: true,
    loadSidebar: true,
    subMaxLevel: 6,
	auto2top: true,//当路线改变时，滚动到屏幕的顶部。
	mergeNavbar: false,//Navbar将在小屏幕上与侧边栏合并。
	formatUpdated: '{MM}/{DD} {HH}:{mm}',
  }
</script>

<!--搜索-->
<script>
  window.$docsify = {
    search: 'auto', // default

    search : [
      '/', 
    ],

    // complete configuration parameters
    search: {
      maxAge: 86400000, // Expiration time, the default one day
      paths: [auto], // or 'auto'
      placeholder: '搜索',

      // Localization
      placeholder: {
        '/zh-cn/': '搜索',
        '/': 'Type to search'
      },

      noData: 'No Results!',

      // Localization
      noData: {
        '/zh-cn/': '找不到结果',
        '/': 'No Results'
      },

      // Headline depth, 1 - 6
      depth: 2,

      hideOtherSidebarContent: false, // whether or not to hide other sidebar content

      // To avoid search index collision
      // between multiple websites under the same domain
      namespace: 'website-1',
    }
  }
</script>
<script src="//unpkg.com/docsify-copy-code"></script>
<script src="//unpkg.com/docsify/lib/plugins/search.js"></script>
<script src="//unpkg.com/docsify/lib/docsify.min.js"></script>
<script src="//unpkg.com/prismjs/components/prism-php.min.js"></script>
</body>
```
