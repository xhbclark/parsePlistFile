# parsePlistFile
Package a method about how to get and parse the local plist file
如果你的项目中有较多的本地plist文件需要解析（这里暂时只针对数组套字典类型的plist文件，后续会继续添加）,我提供了一个工具类，它封装了两个方法用来解析本地的plist文件，比如本地有一个plist文件叫local.plist,你有一个模型类model，你只需要导入这个工具类的头文件,然后执行如下代码即可
static NSArray *_localArray = nil;
+ (NSArray *)getLocalArray {
    if (!_localArray) {
        _localArray = [[self alloc] getAndParseWithPlistFile:@"local.plist" withClass:[model class]];
    }
    return _localArray;
}
