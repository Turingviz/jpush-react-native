如果iOS项目是Swift代码。

可以根据以下操作来完成 AppDelegate.swift 文件里的配置。

1. 新建Swift调用OC代码的桥接文件。

  XCode - File from Template - Header File, 键入桥接文件名, 一般为 iOS项目名-Bridging-Header.h ,创建桥接文件。并在Xcode 的 Build Settings 中找到 Swift Compiler - General>> -> Objective-C Bridging Header 选项，将新建的桥接头文件路径填入其中。并将 "JPUSHService.h" 和 "RCTJPushModule.h" 文件通过 #import 方式引入。
  
  桥文件的代码示例：也可以参考ios-swift/HelloWord-Bridging-Header.h 文件。
  
```
#ifndef HelloWord_Bridging_Header_h
#define HelloWord_Bridging_Header_h

//JPush Need
#import "JPUSHService.h"
#import "RCTJPushModule.h"

#endif /* HelloWord_Bridging_Header_h */
```


2. AppDelegate.h 文件的配置可以参考ios-swift/AppDelegate.swift中的配置，请关注标注 JPush Need 的代码。

