# 编码规范
默认参考Apple[Coding Guidelines for Cocoa](https://developer.apple.com/library/content/documentation/Cocoa/Conceptual/CodingGuidelines/CodingGuidelines.html)以及[Github](https://github.com/github/objective-c-style-guide)的补充，除非以下特别声明。

# 常量
k+Pascal命名

# 文件、类
* 顶层模块以EFB前缀。
* 其他模块以模块名称作为前缀。
* 模块内部分为Models、Views、Controllers、Submodules、Constants、Utils、Storyboard。

# 资源文件
* 图片资源放在xcassets，每个子模块分别管理各自的xcassets，命名方式为所有单词首字母小写，模块名称作为前缀，下划线分割，图片名驼峰命名。如： setting_moreBright。

# 分类规范
头文件命名为原类名+项目名+功能/用途。
方法规范：项目名小写+下划线+方法名。
例如：
```
@interface NSDate (ZOCTimeExtensions)
- (NSString *)zoc_timeAgoShort;
@end
```
# 注释
* 注释是 [Tomdoc-style](http://tomdoc.org/)风格
* 所有的方法声明应加文档说明
* 方法注明是否允许nil作为参数
* 注释还包括对每个类的用途进行描述
# 使用#pragma mark进行分组，一般规则如下
```
#pragma mark - **************** Properties
#pragma mark - **************** Lifecycle

- (instancetype)init {}
- (void)dealloc {}
- (void)viewDidLoad {}
- (void)viewWillAppear:(BOOL)animated {}
- (void)didReceiveMemoryWarning {}

#pragma mark - **************** Custom Accessors

- (void)setCustomProperty:(id)value {}
- (id)customProperty {}

#pragma mark - **************** IBActions

- (IBAction)submitData:(id)sender {}

#pragma mark - **************** Public

- (void)publicMethod {}

#pragma mark - **************** Private

- (void)privateMethod {}

#pragma mark - **************** Protocol conformance
#pragma mark - **************** UITextFieldDelegate
#pragma mark - **************** UITableViewDataSource
#pragma mark - **************** UITableViewDelegate

#pragma mark - **************** NSCopying

- (id)copyWithZone:(NSZone *)zone {}

#pragma mark - **************** NSObject

- (NSString *)description {}
```
# 参考
[Appple 官方指南](https://developer.apple.com/library/content/documentation/Cocoa/Conceptual/CodingGuidelines/CodingGuidelines.html)
[中文翻译参考](http://blog.csdn.net/houseq/article/details/27369043)
[Github](https://github.com/github/objective-c-style-guide)
[raywenderlich](https://github.com/raywenderlich/objective-c-style-guide)
[Google 开源项目ojbc规范](https://github.com/zh-google-styleguide/zh-google-styleguide/blob/master/google-objc-styleguide/naming.rst)

