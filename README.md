SwiftMi-APP (Dev Share)
---

**Dev Share** 为 [www.swiftmi.com](http://www.swiftmi.com) 社区 App (已上线)，纯 Swift 实现，现开源。

Swift 开发 QQ 交流群：305170435

目前社区功能不全，欢迎贡献代码，相互学习。

## AppStore

[<img src="https://cloud.githubusercontent.com/assets/219689/5575342/963e0ee8-9013-11e4-8091-7ece67d64729.png" width="135" height="40" alt="AppStore"/>](https://appsto.re/cn/C3Hn7.i)

## 预览

![demo](swiftmi.gif)

## 构建
fork出来的项目，原始项目无法正常运行，需要按照以下方法操作，可能是添加子模块的时候使用的commit已经不存在，需要重新添加。
1. git clone https://github.com/duskalbatross/swiftmi-app.git swiftmi
2. 删除子模块
```
cd swiftmi
git rm --cached Alamofire
git rm --cached Kingfisher
git rm --cached SwiftyJSON
```
3. 编辑`.gitmodules`文件，删除以上三个的配置
4. 标记`.git/config`文件，删除文件中以上三个子模块的配置
5. 手动删除以上三个目录：`rm -rf Alamofire Kingfisher SwiftyJSON`
6. 重新添加子模块:
```
git submodule add https://github.com/Alamofire/Alamofire.git
git submodule add https://github.com/onevcat/Kingfisher.git
git submodule add https://github.com/SwiftyJSON/SwiftyJSON.git
```
7. cd swiftmi && pod install
8. 启动xcode，打开swiftmi.xcworkspace
9. 修改Target swiftmi的Signing信息为Automatically manage signing，并选择自己的Team
10. 修改Bundle Identifier，为自己的ID，因为swiftmi需要推送功能，所以该ID必须有推送的功能，需要登录 https://developer.apple.com 创建，并勾选Push Notifications。

## 更新

- 20150711  **增加 Handoff**：在内容(主题、源代码)详情界面阅读时增加 Handoff，支持 Mac 默认浏览器打开阅读详情
- 20150902  升级 Swift 2.0，XCode 7.0 编译下通过
- 20160918  Support Swift 3.0 / XCode 8

## 环境

- Xcode 8.0+
- Swift 3.0+

## 其他

网友 @sandyway 实现的对应 OC 版本 [https://github.com/sandyway/ocswiftmi](https://github.com/sandyway/ocswiftmi)

## 社区

Swift 迷社区 [http://www.swiftmi.com](http://www.swiftmi.com)
