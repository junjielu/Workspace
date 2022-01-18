# Xcode使用的小tips

Xcode是iOS日常开发都会用到的工具，下面介绍一些能提升日常开发效率的操作。

## 编译耗时统计

```sh
defaults write com.apple.dt.Xcode ShowBuildOperationDuration -bool YES
```

命令行中执行后重启Xcode就能看到整个编译阶段的耗时了。如果想要了解详细的编译耗时信息，可以通过`Product ->  Perform Action -> Build with Timing Summary`来触发统计时间的编译。或者通过xcodebuild，加上`buildWithTimingSummary`来获得耗时分析。

Swift编译提供了以下两个参数：

- `Xfrontend -warn-long-function-bodies=<millisecond>`
- `Xfrontend -warn-long-expression-type-checking=<millisecond>`

分别对应了长函数体编译耗时警告和长类型检查耗时警告。

一般这里输入 100 即可，表示对应类型耗时超过 100ms 将会提供警告。

## 快捷键

快速打开：**⇧ + ⌘ + O**

Clean build：**⇧ + ⌘ + K**

在当前行打断点：**⌘ +  \\**

打开文件跳转栏：**⌃ + 6**

调整缩进：**⌃ + I**

快速跳转到文件的目录：**⌘ + ⇧ + J**

打开关闭debug区域：**⌘ + ⇧ + Y**

多行编辑：**⌥ + Hold left mouse** 选中要编辑的行 **→ ⌘ + Arrows** 浏览行 **→ ⌥ + Arrows** 浏览词 → **Shift + Arrows** 选择 **→ Shift + ⌥ + Arrows** 选择词 **→ Shift + ⌘ + Arrows** 选择行

## 调试

改变对象

```sh
e saveButton.setTitle("Saved", for: .normal)
```

## 汇总

[Xcode-tips](https://xcode-tips.github.io/)