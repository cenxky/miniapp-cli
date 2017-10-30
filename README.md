# miniapp-cli
微信小程序脚手架工具

miniapp-cli支持你使用jade，sass/scss/stylus/coffee来编写[微信小程序](https://mp.weixin.qq.com/cgi-bin/wx)，并编译成小程序原生的wxml，wxss，js。这听起来就非常酷对吧！除此之外，miniapp-cli还提供了生成小程序page模板的功能，帮助你快速开发微信小程序。

## 安装
```
    $ npm install miniapp-cli -g
```
查看帮助
```
    $ miniapp-cli -h
```

## 创建项目
```
    $ miniapp-cli new your_app_name
```

`new`命令可以为你快速生成一个初始化的小程序项目，并为你自动安装其中的默认npm package依赖。
执行此命令后，你需要选择`wxml`和`wxss`及`wxs`的预编译方式。

`wxml` 支持的预编译方式
- wxml (不使用预编译)
- pug(即jade)

`wxss` 支持的预编译方式
- wxss (不使用预编译)
- sass
- scss
- stylus

`wxs` 支持的预编译方式
- babel(ES6->ES5)
- coffeescript


在`your_app_name`文件夹中，有两个主要目录，`src`和`dist`，前者是你的工作目录，后者是通过`miniapp-cli`编译生成的小程序，你可以通过微信小程序官网提供的开发者工具链接本地开发目录至`dist`，就可以实现实时预览了。

## 编译
通过`build`来编译小程序项目
```
    $ cd your_app_name
    $ miniapp-cli build
```
同时你还可以加上 `-w` 参数，以监测文件改动从而自动编译
```
    $ miniapp-cli build -w
```

## Page模板生成
通过`g` 来快速生成page，执行
```
    $ miniapp-cli g page_name folder
```
其中`folder`默认和`page_name`同名，当然也可以是路径, 将会自动在 `src/pages` 和 `dist/pages` 目录中生成 `folder` 文件路径，并生成基本的文件结构
- page_name.js
- page_name.wxml
- page_name.wxss

除此之外，还会自动将page添加到app.json中的pages定义。


## 其它
本项目是在 miniapps 基础上开发，以满足个性化需求，对此表示感谢！

### License

[MIT](http://opensource.org/licenses/MIT)
