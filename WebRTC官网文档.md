#WebRTC官网文档

[WebRTC官网](https://webrtc.org)

iOS源码路径：
Home > Native code > iOS

###1.Development Environment
```
开发环境
```

A macOS machine is required for iOS development. While it’s possible to develop purely from the command line with text editors, it’s easiest to use Xcode. Both methods will be illustrated here.

```
iOS开发需要一个macOS机器。虽然可以用文本编辑器开发命令行，但是用Xcode开发最简单。这两种方法都将在这里说明。
```

###2.Getting the Code
```
获取代码
```

####<1>Install prerequisite software
```
安装必备软件
```

####<2>Create a working directory, enter it, and run:

`fetch --nohooks webrtc_ios
 gclient sync`

This will fetch a regular WebRTC checkout with the iOS-specific parts added. The same checkout can be used for both Mac and iOS development, since you can generate your Ninja project files in multiple directories (see below).

```
创建一个工作目录，进入它，然后运行以下命令：

fetch --nohooks webrtc_ios
gclient sync

这将会使用常规的 WebRTC 来检测 iOS 的特定增加部分。同样的检测可用于 Mac 和 iOS 开发，因为你可以生成多个目录中你的 Ninja 项目文件(见下文)。
```

####<3>You may want to disable Spotlight indexing for the checkout to speed up file operations
```
您可能希望禁用“检查”的索引，以加快文件操作
```


See Development for generic instructions on how to update the code in your checkout
```
参见 Development 如何在检验中更新您的代码的通用指令
```

### 3.Generating project files
```
生成工程文件
```

GN is used to generate Ninja project files. In order to configure GN to generate build files for iOS certain variables need to be set. Those variables can be edited for the various build configurations as needed.
The component build is the default for Debug builds, which are also enabled by default unless `is_debug=false` is specified. iOS needs static builds, which is why `is_component_build=false` is specified for all the examples above.

```
GN 被用于生成 Ninja 工程文件。为了
```




