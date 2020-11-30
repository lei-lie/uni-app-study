## uni-app

![image-20201130162600585](C:\Users\admin\AppData\Roaming\Typora\typora-user-images\image-20201130162600585.png)

## 安装&运行

### 通过vue-cli命令行

1.全局安装vue-cli

```js
npm install -g @vue/cli
```

2.创建uni-app(创建基础脚手架)

```js
vue create -p dcloudio/uni-preset-vue my-project
```

3.选择模板

![uni-app选择模板](D:\00_workspace\00_mine\uni-app-study\doc\uni-app选择模板.png)

选择默认模板

4.在vscode中配置uni-app

* 安装组件语法提示

  ```js
  npm i @dcloudio/uni-helper-json
  ```

* 导入HBuilderX自带的代码块

  从 github 下载 [uni-app 代码块](https://github.com/zhetengbiji/uniapp-snippets-vscode)，放到项目目录下的 .vscode 目录即可拥有和 HBuilderX 一样的代码块

  ![ui-app代码块](D:\00_workspace\00_mine\uni-app-study\doc\ui-app代码块.png)

5.运行&发布`uni-app`

```js
npm run dev:%PLATFORM%
npm run build:%PLATFORM%
```



`%PLATFORM%` 可取值如下:

![%PLATFORM%](D:\00_workspace\00_mine\uni-app-study\doc\%PLATFORM%.png)

执行对应的命令：

```json
"scripts": {
    "serve": "npm run dev:h5",
    "build": "npm run build:h5",
    "build:app-plus": "cross-env NODE_ENV=production UNI_PLATFORM=app-plus vue-cli-service uni-build",
    "build:custom": "cross-env NODE_ENV=production uniapp-cli custom",
    "build:h5": "cross-env NODE_ENV=production UNI_PLATFORM=h5 vue-cli-service uni-build",
    "build:mp-360": "cross-env NODE_ENV=production UNI_PLATFORM=mp-360 vue-cli-service uni-build",
    "build:mp-alipay": "cross-env NODE_ENV=production UNI_PLATFORM=mp-alipay vue-cli-service uni-build",
    "build:mp-baidu": "cross-env NODE_ENV=production UNI_PLATFORM=mp-baidu vue-cli-service uni-build",
    "build:mp-kuaishou": "cross-env NODE_ENV=production UNI_PLATFORM=mp-kuaishou vue-cli-service uni-build",
    "build:mp-qq": "cross-env NODE_ENV=production UNI_PLATFORM=mp-qq vue-cli-service uni-build",
    "build:mp-toutiao": "cross-env NODE_ENV=production UNI_PLATFORM=mp-toutiao vue-cli-service uni-build",
    "build:mp-weixin": "cross-env NODE_ENV=production UNI_PLATFORM=mp-weixin vue-cli-service uni-build",
    "build:quickapp-native": "cross-env NODE_ENV=production UNI_PLATFORM=quickapp-native vue-cli-service uni-build",
    "build:quickapp-webview": "cross-env NODE_ENV=production UNI_PLATFORM=quickapp-webview vue-cli-service uni-build",
    "build:quickapp-webview-huawei": "cross-env NODE_ENV=production UNI_PLATFORM=quickapp-webview-huawei vue-cli-service uni-build",
    "build:quickapp-webview-union": "cross-env NODE_ENV=production UNI_PLATFORM=quickapp-webview-union vue-cli-service uni-build",
    "dev:app-plus": "cross-env NODE_ENV=development UNI_PLATFORM=app-plus vue-cli-service uni-build --watch",
    "dev:custom": "cross-env NODE_ENV=development uniapp-cli custom",
    "dev:h5": "cross-env NODE_ENV=development UNI_PLATFORM=h5 vue-cli-service uni-serve",
    "dev:mp-360": "cross-env NODE_ENV=development UNI_PLATFORM=mp-360 vue-cli-service uni-build --watch",
    "dev:mp-alipay": "cross-env NODE_ENV=development UNI_PLATFORM=mp-alipay vue-cli-service uni-build --watch",
    "dev:mp-baidu": "cross-env NODE_ENV=development UNI_PLATFORM=mp-baidu vue-cli-service uni-build --watch",
    "dev:mp-kuaishou": "cross-env NODE_ENV=development UNI_PLATFORM=mp-kuaishou vue-cli-service uni-build --watch",
    "dev:mp-qq": "cross-env NODE_ENV=development UNI_PLATFORM=mp-qq vue-cli-service uni-build --watch",
    "dev:mp-toutiao": "cross-env NODE_ENV=development UNI_PLATFORM=mp-toutiao vue-cli-service uni-build --watch",
    "dev:mp-weixin": "cross-env NODE_ENV=development UNI_PLATFORM=mp-weixin vue-cli-service uni-build --watch",
    "dev:quickapp-native": "cross-env NODE_ENV=development UNI_PLATFORM=quickapp-native vue-cli-service uni-build --watch",
    "dev:quickapp-webview": "cross-env NODE_ENV=development UNI_PLATFORM=quickapp-webview vue-cli-service uni-build --watch",
    "dev:quickapp-webview-huawei": "cross-env NODE_ENV=development UNI_PLATFORM=quickapp-webview-huawei vue-cli-service uni-build --watch",
    "dev:quickapp-webview-union": "cross-env NODE_ENV=development UNI_PLATFORM=quickapp-webview-union vue-cli-service uni-build --watch",
    "info": "node node_modules/@dcloudio/vue-cli-plugin-uni/commands/info.js",
    "serve:quickapp-native": "node node_modules/@dcloudio/uni-quickapp-native/bin/serve.js",
    "test:android": "cross-env UNI_PLATFORM=app-plus UNI_OS_NAME=android jest -i",
    "test:h5": "cross-env UNI_PLATFORM=h5 jest -i",
    "test:ios": "cross-env UNI_PLATFORM=app-plus UNI_OS_NAME=ios jest -i",
    "test:mp-baidu": "cross-env UNI_PLATFORM=mp-baidu jest -i",
    "test:mp-weixin": "cross-env UNI_PLATFORM=mp-weixin jest -i"
  },
```



### HbuilderX构建

1.新建项目

文件》新建》项目

![HBuilder中运行微信小程序报错](D:\00_workspace\00_mine\uni-app-study\doc\HBuilder中运行微信小程序报错.png)



2.设置微信小程序密钥

打开项目中的`mainifest.json`文件，选择微信小程序配置》将填写小程序的`AppId`



![设置小程序秘钥](D:\00_workspace\00_mine\uni-app-study\doc\设置小程序秘钥.png)

3.关联微信小程序开发者工具（运行后在小程序开发者工具上看效果）

在HbuilderX中选择工具》设置》运行配置，维护小程序开发工具的安装位置

![关联微信开发者工具](D:\00_workspace\00_mine\uni-app-study\doc\关联微信开发者工具.png)

4.登录微信开发者工具,开启安全设置（ 获取小程序端口号关联HBuilder）

选择设置》安全设置，开启安全设置



![开启安全设置](D:\00_workspace\00_mine\uni-app-study\doc\开启安全设置.png)

5.填写外部web服务器调用url

![外部web服务器调用Url](D:\00_workspace\00_mine\uni-app-study\doc\外部web服务器调用Url.png)

6.运行

运行》运行到小程序模拟器》微信开发者工具

##  开发规范

> 为了实现多端兼容，综合考虑编译速度、运行性能等因素，`uni-app` 约定了如下开发规范：
>
> - 页面文件遵循 [Vue 单文件组件 (SFC) 规范](https://vue-loader.vuejs.org/zh/spec.html)
> - 组件标签靠近小程序规范，详见[uni-app 组件规范](https://uniapp.dcloud.io/component/README)
> - 接口能力（JS API）靠近微信小程序规范，但需将前缀 `wx` 替换为 `uni`，详见[uni-app接口规范](https://uniapp.dcloud.io/api/README)
> - 数据绑定及事件处理同 `Vue.js` 规范，同时补充了App及页面的生命周期
> - 为兼容多端运行，建议使用flex布局进行开发

## 生命周期

![生命周期](D:\00_workspace\00_mine\uni-app-study\doc\生命周期.jpg)

## 路由

> `uni-app`页面路由为框架统一管理，开发者需要在[pages.json](https://uniapp.dcloud.io/collocation/pages?id=pages)里配置每个路由页面的路径及页面样式。类似小程序在app.json中配置页面路由一样。所以 `uni-app` 的路由用法与 `Vue Router` 不同，如仍希望采用 `Vue Router` 方式管理路由，可在插件市场搜索 [Vue-Router](https://ext.dcloud.net.cn/search?q=vue-router)

### 路由跳转

* [navigator组件](https://uniapp.dcloud.io/component/navigator)跳转
* 调用[API](https://uniapp.dcloud.io/api/router)跳转

## 运行环境判断

[开发环境和生产环境](https://uniapp.dcloud.io/frame?id=开发环境和生产环境)

`uni-app` 可通过 `process.env.NODE_ENV` 判断当前环境是开发环境还是生产环境。一般用于连接测试服务器或生产服务器的动态切换。

[判断平台](https://uniapp.dcloud.io/frame?id=%e5%88%a4%e6%96%ad%e5%b9%b3%e5%8f%b0)：

* 编译期判断
* 运行期判断

## 页面样式与布局

https://uniapp.dcloud.io/frame?id=%e9%a1%b5%e9%9d%a2%e6%a0%b7%e5%bc%8f%e4%b8%8e%e5%b8%83%e5%b1%80

### 尺寸单位

https://uniapp.dcloud.io/frame?id=%e5%b0%ba%e5%af%b8%e5%8d%95%e4%bd%8d

uni-app支持通用的css单位：

* px 屏幕像素

* rpx 响应式px,

  > 一种根据屏幕宽度自适应的动态单位。以750宽的屏幕为基准，750rpx恰好为屏幕宽度。屏幕变宽，rpx 实际显示效果会等比放大，但在 App 端和 H5 端屏幕宽度达到 960px 时，默认将按照 375px 的屏幕宽度进行计算，具体配置参考：[rpx计算配置](https://uniapp.dcloud.io/collocation/pages?id=globalstyle) 。

### 样式导入

https://uniapp.dcloud.io/frame?id=%e6%a0%b7%e5%bc%8f%e5%af%bc%e5%85%a5

使用`@import`语句可以导入外联样式表，`@import`后跟需要导入的外联样式表的相对路径，用`;`表示语句结束

### 内联样式

https://uniapp.dcloud.io/frame?id=%e5%86%85%e8%81%94%e6%a0%b7%e5%bc%8f

- style：静态的样式统一写到 class 中。style 接收动态的样式，在运行时会进行解析，请尽量避免将静态的样式写进 style 中，以免影响渲染速度。

  ```html
  <view :style="{color:color}" />
  ```

- class：用于指定样式规则，其属性值是样式规则中类选择器名(样式类名)的集合，样式类名不需要带上.，样式类名之间用空格分隔。

  ```html
  <view class="normal_view" />
  ```

### 选择器

https://uniapp.dcloud.io/frame?id=%e9%80%89%e6%8b%a9%e5%99%a8

![image-20201130171919689](C:\Users\admin\AppData\Roaming\Typora\typora-user-images\image-20201130171919689.png)

### 全局样式&局部样式

https://uniapp.dcloud.io/frame?id=%e5%85%a8%e5%b1%80%e6%a0%b7%e5%bc%8f%e4%b8%8e%e5%b1%80%e9%83%a8%e6%a0%b7%e5%bc%8f



定义在 App.vue 中的样式为全局样式，作用于每一个页面。在 pages 目录下 的 vue 文件中定义的样式为局部样式，只作用在对应的页面，并会覆盖 App.vue 中相同的选择器。

**注意：**

- App.vue 中通过 `@import` 语句可以导入外联样式，一样作用于每一个页面。
- nvue页面暂不支持全局样式

### CSS变量

https://uniapp.dcloud.io/frame?id=css%e5%8f%98%e9%87%8f

### 固定值

https://uniapp.dcloud.io/frame?id=%e5%9b%ba%e5%ae%9a%e5%80%bc

![image-20201130172405369](C:\Users\admin\AppData\Roaming\Typora\typora-user-images\image-20201130172405369.png)

## template& block

`uni-app` 支持在 template 模板中嵌套 `<template/>` 和 `<block/>`，用来进行 [列表渲染](https://uniapp.dcloud.io/use?id=列表渲染) 和 [条件渲染](https://uniapp.dcloud.io/use?id=条件渲染)。

`<template/>` 和 `<block/>` 并不是一个组件，它们仅仅是一个包装元素，不会在页面中做任何渲染，只接受控制属性。

`<block/>` 在不同的平台表现存在一定差异，推荐统一使用 `<template/>`。

## 参考

[uni-app](https://uniapp.dcloud.io/frame)

[uni-app/HBuilderX 搭建并启动微信小程序项目](https://blog.csdn.net/qq_41988143/article/details/106122566)

[HBuilderX Uniapp 微信小程序 环境及调试配置步骤](https://developers.weixin.qq.com/community/develop/article/doc/000e0c81704208647e3a9828256013)

[uni-app接口规范](https://uniapp.dcloud.io/api/README)

[uni-app组件规范](https://uniapp.dcloud.io/component/README)