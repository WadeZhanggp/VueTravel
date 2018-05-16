# VueTravel
## 项目描述：
### 1、项目基于Vue2.5.2
### 2、主要组件有axios0.18.0、vue-router3.0.1、webpack3.6.0
### 3、该项目适用于手机web页面，一个webApp，参考去哪儿网
### 4、网络接口为本地static文件夹下mock下的.json文件

**********************
## 环境安装
### 1、环境要求
node >= 6.0.0
npm >= 3.0.0

### 2、windows node及npm环境安装
  #### windows下的NodeJS安装是比较方便的（v0.6.0版本之后，支持windows native），只需要登陆官网 http://nodejs.org 便可以看到首页的“INSTALL”按钮，直接点击就会自动下载安装了
  #### 安装过程基本直接“NEXT”就可以了。（windows的安装msi文件在过程中会直接添加path的系统变量，变量值是你的安装路径，例如“C:\Program Files\nodejs”）。
  #### 安装完成后可以使用cmd（win+r然后输入cmd进入）测试下是否安装成功。方法：在cmd下输入node -v，出现版本提示就是完成了NodeJS的安装。
  #### npm的安装。由于新版的NodeJS已经集成了npm，所以之前npm也一并安装好了。同样可以使用cmd命令行输入"npm -v"来测试是否成功安装，出现版本提示便OK了。
  #### 然后我们要先配置npm的全局模块的存放路径以及cache的路径，例如我希望将以上两个文件夹放在NodeJS的主目录下，便在NodeJs下建立"node_global"及"node_cache"两个文件夹。
  #### 启动cmd，输入npm config set prefix "C:\Program Files\nodejs\node_global"以及npm config set cache "C:\Program Files\nodejs\node_cache"
  #### 现在我们来装个模块试试，选择express这个比较常用的模块。同样在cmd命令行里面，输入“npm install express -g”（“-g”这个参数意思是装到global目录下，也就是上面说设置的“C:\Program Files\nodejs\node_global”里面。）。待cmd里面的安装过程滚动完成后，会提示“express”装在了哪、版本还有它的目录结构是怎样。
  #### 关闭cmd，打开系统对话框，“我的电脑”右键“属性”-“高级系统设置”-“高级”-“环境变量”。
  #### 进入环境变量对话框，在系统变量下新建"NODE_PATH"，输入”C:\Program Files\nodejs\node_global\node_modules“。（ps：这一步相当关键。）2014.4.19新增：由于改变了module的默认地址，所以上面的用户变量都要跟着改变一下（用户变量"PATH"修改为“C:\Program Files\nodejs\node_global\”），要不使用module的时候会导致输入命令出现“xxx不是内部或外部命令，也不是可运行的程序或批处理文件”这个错误。
  #### 参考链接：https://blog.csdn.net/xxmeng2012/article/details/51492149

### 3、MacOS node及npm环境安装
  自行搜索

## 项目运行
### 1、项目下载
  使用git下载 git clone 或者直接下载文件包
### 2、项目依赖安装和运行
  npm install
  npm run start 或者 npm run dev

**********************
## 新建项目指南
1、vue安装
### 最新稳定版
$ npm install vue

2、命令行工具 (CLI)
### 全局安装 vue-cli
$ npm install --global vue-cli
### 创建一个基于 webpack 模板的新项目
$ vue init webpack my-project
### 创建项目并运行
$ cd my-project
$ npm run dev
