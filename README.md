# TinyPNG CLI
方便的命令行工具，用于使用TinyPNG API缩小PNG图像

## 安装
`npm install -g tinypng-cli`

## 前言
要使用TinyPNG CLI，您需要一个TinyPNG的API密钥。您可以在 https://tinypng.com/developers 上获得一个.

## 用法
* TinyPNG CLI允许您以两种不同的方式提供API密钥。
1. 更为方便的方法是将API密钥保存到`home\.tinypng`目录中。
2. windows用户路径通常是`C:\Users\Administrator\.tinypng`创建方式`.tinypng.`or`echo YouApiTxt > .tinypng`

* 另一种方法是在运行CLI时将其作为选项提供。
例如: `tinypng demo.png -k E99a18c4f8cb3EL5f2l08u368_922e03`

> 缩小当前目录中的所有PNG图像。

`tinypng .`

> 要缩小当前目录和子目录中的所有PNG图片，请使用-r标记

`tinypng . -r`

> 要收缩特定目录中的所有PNG图像（assets/img在此示例中），可以运行以下命令。

`tinypng assets/img`

> 是否需要一次限制压缩次数？使用-m, --max标志：

`tinypng assets/img --max 100`

> 您还可以提供多个目录。

`tinypng assets/img1 assets/img2`

> 要收缩单个PNG图像（assets/img/demo.png在此示例中），您可以运行以下命令。

`tinypng assets/img/demo.png`

> 您还可以提供多个单个PNG图像。

`tinypng assets/img/demo1.png assets/img/demo2.png`

> 要调整图像大小，请使用--width和/或--height标志。

`tinypng assets/img/demo.png --width 123`

`tinypng assets/img/demo.png --height 123`

`tinypng assets/img/demo.png --width 123 --height 123`

> 默认情况下，此工具在中缓存发送到API的所有压缩图像的映射~/.tinypng.cache.json。要更改此目录，请使用-c, --cache标志：

`tinypng . -r --cache /path/to/myCache.json`

如果要强制重新压缩资产，请使用该--force标志。对于将发送到API的所有文件的空运行输出，请使用--dry-run标志。

> 很简单吧？
