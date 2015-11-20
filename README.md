# SCCatWaitingHUD

This is a cute and simple loading HUD :-P Enjoy!  
这是一个可爱清新简单的加载HUD控件 :-P

[![CI Status](http://img.shields.io/travis/SergioChan/SCCatWaitingHUD.svg?style=flat)](https://travis-ci.org/SergioChan/SCCatWaitingHUD)
[![Version](https://img.shields.io/cocoapods/v/SCCatWaitingHUD.svg?style=flat)](http://cocoapods.org/pods/SCCatWaitingHUD)
[![License](https://img.shields.io/cocoapods/l/SCCatWaitingHUD.svg?style=flat)](http://cocoapods.org/pods/SCCatWaitingHUD)
[![Platform](https://img.shields.io/cocoapods/p/SCCatWaitingHUD.svg?style=flat)](http://cocoapods.org/pods/SCCatWaitingHUD)

## Preview 预览

![image](https://raw.githubusercontent.com/SergioChan/SCCatWaitingHUD/master/Preview/preview.png)

![image](https://raw.githubusercontent.com/SergioChan/SCCatWaitingHUD/master/Preview/preview.gif)

## Usage 用法

To run the example project, clone the repo, and run `pod install` from the Example directory first.  
想要运行示例工程，将这个仓库clone到本地，在`Example`目录下运行`pod install`。

Simply use as below :  
用法很简单：

```Objective-C
if(![SCCatWaitingHUD sharedInstance].isAnimating)
{
    [[SCCatWaitingHUD sharedInstance] animate];
}
else
{
    [[SCCatWaitingHUD sharedInstance] stop];
}
```

Here I provided you several complex way to call the `animate` method.  
这里我提供了两种更复杂一些的方式来调用`animate`方法。

```Objective-C
/**
 *  动画的时候是否允许和原始的View进行交互
 *  Whether you can interact with the original view while animating
 *
 *  @param enabled YES代表能响应原生View事件，NO代表block当前所有的手势操作
 */
- (void)animateWithInteractionEnabled:(BOOL)enabled;

/**
 *  You can attach your HUD title to the view using this animation method.
 *
 *  @param enabled YES代表能响应原生View事件，NO代表block当前所有的手势操作
 *  @param title   HUD title
 */
- (void)animateWithInteractionEnabled:(BOOL)enabled title:(NSString *)title;
```

## BackLog 更新日志
* v0.1.0 Basic Version
* v0.1.1 Add Landscape Orientation Support
* v0.1.4 Add eye cover and Loading contentLabel animation
* v0.1.5 Finish perfect timing function for eye cover movement and polish some of the codes

--

* v0.1.0 基本版本
* v0.1.1 支持横屏
* v0.1.4 添加眼皮运动和下方Loading字样的Label
* v0.1.5 优化代码结构，精确调整了眼皮和眼珠的运动时间曲线

## Requirements 版本需求
iOS 8.0 Above

## Installation 安装

SCCatWaitingHUD is available through [CocoaPods](http://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod 'SCCatWaitingHUD', '~> 0.1.5'
```

## License

SCCatWaitingHUD is available under the MIT license. See the LICENSE file for more info.
