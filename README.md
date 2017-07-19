# swift

在自己项目中使用到或者日常接触到的的swift类库，收录最简单，易用，稳定的，方便快速，高效开发

[Swift 第一章节工具库篇]</br>
[时间](https://github.com/wangwu59105/swift#%E4%B8%80时间)、[音频](https://github.com/wangwu59105/swift#%e4%ba%8c音频)、
[摄像头](https://github.com/wangwu59105/swift#%e4%b8%89摄像头)、[网络请求](https://github.com/wangwu59105/swift#%e5%9b%9b网络请求)、
[图片处理](https://github.com/wangwu59105/swift#%e4%ba%94图片处理)、[文本](https://github.com/wangwu59105/swift#%e5%85%ad文本)、
[数据解析](https://github.com/wangwu59105/swift#%e4%b8%83数据解析)、
[UI界面布局](https://github.com/wangwu59105/swift#%e5%85%ab界面布局)、
[加载框，弹窗](https://github.com/wangwu59105/swift#%e4%b9%9d加载框弹窗)、
[其它扩展](https://github.com/wangwu59105/swift#%e5%8d%81其它扩展)
</br>
[Swift 第二章节完整APP]</br>
[高仿系列](https://github.com/wangwu59105/swift#%E4%B8%80高仿)

## 工具类
### 一、时间
1,SwiftyTimer
Swift里面的时间控制器，使用方便</br>
```swift
Timer.every(0.7.seconds) {
    statusItem.blink()
}

Timer.after(1.minute) {
    println("Are you still here?")
}
......
```
项目地址:https://github.com/radex/SwiftyTimer

### 二、音频
1.SwiftySound
播放音频的工具类，简单易用,稳定</br>
```swift
Sound.play(file: "dog.wav")
```

```swift
Sound.play(url: fileURL)
```
项目地址：https://github.com/adamcichy/SwiftySound

###  三、摄像头
1.swiftScan
二维码 各种码识别，生成，界面效果</br>
![image](https://github.com/MxABC/swiftScan/blob/master/ScreenShots/page1.jpg)
![image](https://github.com/MxABC/swiftScan/blob/master/ScreenShots/page2.jpg)
</br>
项目地址：https://github.com/MxABC/swiftScan

### 四、网络请求
1.Alamofire
强大的网络请求类库，可以结合swiftJson使用，方便易用，支持各种请求方式</br>
```swift
public enum HTTPMethod: String {
    case options = "OPTIONS"
    case get     = "GET"
    case head    = "HEAD"
    case post    = "POST"
    case put     = "PUT"
    case patch   = "PATCH"
    case delete  = "DELETE"
    case trace   = "TRACE"
    case connect = "CONNECT"
}
```
项目地址：https://github.com/Alamofire/Alamofire


### 五、图片处理
1.Kingfisher
网络图片加载神器，轻量级继承，改写UIimageView，使用简单，功能强大
```swift
let url = URL(string: "url_of_your_image")
imageView.kf.setImage(with: url)
```
项目地址：https://github.com/onevcat/Kingfisher

2.BSImagePicker
别人写的图片选择器工具，继承方便，使用简洁，如果没有太多页面要求，可以
直接使用
```swift
let vc = BSImagePickerViewController()
bs_presentImagePickerController(vc, animated: true,
    select: { (asset: PHAsset) -> Void in
      // User selected an asset.
      // Do something with it, start upload perhaps?
    }, deselect: { (asset: PHAsset) -> Void in
      // User deselected an assets.
      // Do something, cancel upload?
    }, cancel: { (assets: [PHAsset]) -> Void in
      // User cancelled. And this where the assets currently selected.
    }, finish: { (assets: [PHAsset]) -> Void in
      // User finished with these assets
}, completion: nil)
```
![alt text](https://cloud.githubusercontent.com/assets/4034956/15001931/254805de-119c-11e6-9f68-d815ccc712cd.gif "Demo gif")
</br>
项目地址：https://github.com/mikaoj/BSImagePicker

### 六、文本
1.YYText
功能强大的 iOS 富文本编辑与显示框架。
(该项目是 YYKit 组件之一)
</br>
oc库，swift直接引用使用
<table>
  <thead>
    <tr>
      <th>Demo</th>
      <th>Attribute Name</th>
      <th>Class</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><img src="https://raw.github.com/ibireme/YYText/master/Attributes/YYText Extended/YYTextAttachment.gif" width="200"></td>
      <td>TextAttachment</td>
      <td>YYTextAttachment</td>
    </tr>
    <tr>
      <td><img src="https://raw.github.com/ibireme/YYText/master/Attributes/YYText Extended/YYTextHighlight.gif" width="200"></td>
      <td>TextHighlight</td>
      <td>YYTextHighlight</td>
    </tr>
    <tr>
      <td><img src="https://raw.github.com/ibireme/YYText/master/Attributes/YYText Extended/YYTextBinding.gif" width="200"></td>
      <td>TextBinding</td>
      <td>YYTextBinding</td>
    </tr>
    <tr>
      <td><img src="https://raw.github.com/ibireme/YYText/master/Attributes/YYText Extended/YYTextShadow.png" width="200"></td>
      <td>TextShadow<br/>TextInnerShadow</td>
      <td>YYTextShadow</td>
    </tr>
    <tr>
      <td><img src="https://raw.github.com/ibireme/YYText/master/Attributes/YYText Extended/YYTextBorder.png" width="200"></td>
      <td>TextBorder</td>
      <td>YYTextBorder</td>
    </tr>
    <tr>
      <td><img src="https://raw.github.com/ibireme/YYText/master/Attributes/YYText Extended/YYTextBackgroundBorder.png" width="200"></td>
      <td>TextBackgroundBorder</td>
      <td>YYTextBorder</td>
    </tr>
    <tr>
      <td><img src="https://raw.github.com/ibireme/YYText/master/Attributes/YYText Extended/YYTextBlockBorder.png" width="200"></td>
      <td>TextBlockBorder</td>
      <td>YYTextBorder</td>
    </tr>
    <tr>
      <td><img src="https://raw.github.com/ibireme/YYText/master/Attributes/CoreText and TextKit/Obliqueness.png" width="200"></td>
      <td>TextGlyphTransform</td>
      <td> NSValue(CGAffineTransform)</td>
    </tr>
    <tr>
      <td><img src="https://raw.github.com/ibireme/YYText/master/Attributes/CoreText and TextKit/Underline.png" width="200"></td>
      <td>TextUnderline</td>
      <td>YYTextDecoration</td>
    </tr>
    <tr>
      <td><img src="https://raw.github.com/ibireme/YYText/master/Attributes/CoreText and TextKit/Strikethrough.png" width="200"></td>
      <td>TextStrickthrough</td>
      <td>YYTextDecoration</td>
    </tr>
    <tr>
      <td><img src="https://raw.github.com/ibireme/YYText/master/Attributes/YYText Extended/YYTextBackedString.png" width="200"></td>
      <td>TextBackedString</td>
      <td>YYTextBackedString</td>
    </tr>
  </tbody>
</table>

</br>
项目地址：https://github.com/ibireme/YYText

### 七、数据解析
1.SwiftyJSON
让json的解析变得更加简单,快捷
```swift
let json = JSON(data: dataFromNetworking)
if let userName = json[0]["user"]["name"].string {
  //Now you got your value
}
```
项目地址：https://github.com/SwiftyJSON/SwiftyJSON

### 八、界面布局
1.SnapKit
简化页面ui组件布局，适用喜欢代码写布局的开发人员，前期我也喜欢用storybroad写页面，
后来发现代码写页面来的直接，快捷。cell文件还是喜欢用xib写。强烈推荐代码布局开发人员，
减去了很多系统排版步骤
```swift
import SnapKit

class MyViewController: UIViewController {

    lazy var box = UIView()

    override func viewDidLoad() {
        super.viewDidLoad()

        self.view.addSubview(box)
        box.snp.makeConstraints { (make) -> Void in
           make.width.height.equalTo(50)
           make.center.equalTo(self.view)
        }
    }

}
```
项目地址：https://github.com/SnapKit/SnapKit

### 九、加载框弹窗
1.SVProgressHUD
数据加载框，使用很宽泛的oc类库</br>
![SVProgressHUD](http://f.cl.ly/items/2G1F1Z0M0k0h2U3V1p39/SVProgressHUD.gif)
</br>
方便Swift开发使用请引入https://github.com/wangwu59105/swift/blob/master/SVProgressHUD.swift
这个类配套使用
项目地址：https://github.com/SVProgressHUD/SVProgressHUD



### 十、其它扩展
1.TimedSilver
这个工具类，没有多少人用到，个人开发上传上去的，对应的开源完整的项目
TSWeChat中使用到的，对很多组件进行的扩展，很强大，个人喜欢使用tabView
和collectionView的对应扩展。如果想了解的可以参考TSWeChat

```
├── Foundation
│   ├── Bundle+TSExtension.swift
│   ├── Data+TSExtension.swift
│   ......
├── Struct
│   ├── Array+TSExtension.swift
│   ├── CGSize+TSExtension.swift
│   ......
├── TimedSilverHeader.h
└── UIKit
    ├── UIAlertController+TSExtension.swift
    ├── UIApplication+TSExtension.swift
    ├── UIButton+TSExtension.swift
    ......
```
项目地址：https://github.com/hilen/TimedSilver

2.CommonExtension.swift
自己项目中使用频率较高的扩展，系统设备的view的一些常量
```swift
extension UIView {
    /// X值
    var x: CGFloat {
        return self.frame.origin.x
    }
    /// Y值
    var y: CGFloat {
        return self.frame.origin.y
    }
    /// 宽度
    var width: CGFloat {
        return self.frame.size.width
    }
    ///高度
    var height: CGFloat {
        return self.frame.size.height
    }
    var size: CGSize {
        return self.frame.size
    }
    var point: CGPoint {
        return self.frame.origin
    }
}
```
项目地址：https://github.com/wangwu59105/swift/blob/master/CommonExtension.swift

## 完整的APP
### 一、高仿
1.高仿爱鲜蜂 - Swift2.0
</br>
</br>
![image](https://camo.githubusercontent.com/37f325f585f91a4fe01efad595c7d1ea795632a9/687474703a2f2f7777322e73696e61696d672e636e2f6d773639302f303036387552753167773166306e376974696f676f67333037753064786e70672e676966)
</br>
- 使用Swift2.0
- 编译器为Xcode7.0.1正式版,请用7.0以上的Xcode打开工程
- 直接打开xcworkspace运行工程即可
```
使用系统原生布局，代码编写，对初学很有帮助
```
项目地址：https://github.com/ZhongTaoTian/LoveFreshBeen
</br>


2.TSWeChat Swift3.0 高仿微信
</br>
</br>
![image](https://github.com/hilen/TSWeChat/blob/master/images/preview1.gif)
</br>
- 使用Swift3.0
- Xcode 8.1+正式版,iOS 8.0+ / Mac OS X 10.9+ Cocoapods 1.1.1 +
```
代码编写布局，可以熟悉很多第三方model的使用，SnapKit的布局，熟悉功能组件编写
```
项目地址：https://github.com/hilen/TSWeChat
