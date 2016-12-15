# 编码规范
默认参考Apple[Coding Guidelines for Cocoa](https://developer.apple.com/library/content/documentation/Cocoa/Conceptual/CodingGuidelines/CodingGuidelines.html)以及[Github](https://github.com/github/objective-c-style-guide)的补充，除非以下特别声明。

# 文件、类
* 顶层模块以EFB前缀。
* 其他模块以模块名称作为前缀。
* 模块内部分为Models、Views、Controllers、Submodules、Contants、Utils。

# 资源文件
* 图片资源统一放在xcasset，命名方式为所有单词首字母小写，模块名称作为前缀，下划线分割。如： more_setting。

# 分类规范
头文件命名为原类名+项目名+功能/用途。
方法规范：项目名小写+下划线+方法名。
例如：
```
@interface NSDate (ZOCTimeExtensions)
- (NSString *)zoc_timeAgoShort;
@end
```

# 参考
[Appple 官方指南](https://developer.apple.com/library/content/documentation/Cocoa/Conceptual/CodingGuidelines/CodingGuidelines.html)
[中文翻译参考](http://blog.csdn.net/houseq/article/details/27369043)
[Github](https://github.com/github/objective-c-style-guide)
[raywenderlich](https://github.com/raywenderlich/objective-c-style-guide)
[Google 开源项目ojbc规范](https://github.com/zh-google-styleguide/zh-google-styleguide/blob/master/google-objc-styleguide/naming.rst)

