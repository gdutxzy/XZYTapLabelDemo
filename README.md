
# XYTapLabel

[![CI Status](https://img.shields.io/travis/gdutxzy/XYTapLabel.svg?style=flat)](https://travis-ci.org/gdutxzy/XYTapLabel)
[![Version](https://img.shields.io/cocoapods/v/XYTapLabel.svg?style=flat)](https://cocoapods.org/pods/XYTapLabel)
[![License](https://img.shields.io/cocoapods/l/XYTapLabel.svg?style=flat)](https://cocoapods.org/pods/XYTapLabel)
[![Platform](https://img.shields.io/cocoapods/p/XYTapLabel.svg?style=flat)](https://cocoapods.org/pods/XYTapLabel)

## Example

To run the example project, clone the repo, and run `pod install` from the Example directory first.

## Requirements

## Installation

XYTapLabel is available through [CocoaPods](https://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod 'XYTapLabel'
```

## Author

gdutxzy, xiezongyuan@xhg.com

## License

XYTapLabel is available under the MIT license. See the LICENSE file for more info.



# XZYTapLabelDemo
require :  >= ios7


 XZYTapLabel的功能只有一个，就是识别你点击的是哪一个字符或者没有点击到任何一个字符，通过回调返回这个信息。
 
这个类是为了实现微信的评论里的Label的功能，点击名字跳转，点击其它地方回复。

之前用了其他人写的富文本Label,他没有提供点击非响应区域的回调，自己再加一个Tapgesture就会与它内部已有的Tap冲突，很难完成识别点击整个label的需求。
     
用法是只需要调用这个方法，就可以增加你想响应的点击范围
- (void)addTapRange:(NSRange)range with:(NSObject *)information;

使用- (void)cleanTapRange; 来清除已有的点击范围设置，主要避免tableviewcell的复用机制。

此- (void)BYLabelDidtapWith:(NSObject *)information;回调会返回你设置的点击范围的信息.如果为空，说明他点击了整个label
