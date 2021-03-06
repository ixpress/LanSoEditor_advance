# LanSoEditor_advance
android  video editor  advance sdk . filter, overlay,remark,mixer and so on安卓平台视频编辑高级版本，可以滤镜，叠加，标记等操作
## 当前版本是2.2.7
*  增加Gif图层 GifLayer, 您可以增加一些Gif动画.
*  优化MV图层.
*  后台可以在处理过程中,插入声音,比如一些搞笑的效果音等.
*  SDK的限制条件: SDK如果没有授权, 则APP名字一定要是我们demo的名字, 请注意.

## 视频编辑的高级版本
*  基本覆盖了秒拍,美拍,快手等视频编辑的大部分功能.
*  采用全新的[画板]+ [图层] 的编程思想.
*  新增短点录像功能,支持回删操作.
*  增加了78种滤镜,基本覆盖市面上大部分APP中的滤镜效果.
*  可以实现视频和视频, 视频和图片,视频和MV,视频和您的UI界面, 视频和Canvas, 独立Canvas形式的编辑工作.
*  在叠加的过程中:支持任意时间点的加入,隐藏,显示,退出.支持同时获取媒体来任意叠加,支持叠加过程中的各种调节,支持实时保存.
*  可以实现 图片和图片的叠加,来实现多张图片合并成影集的效果.
*  可以实现涂鸦, 浪漫情诗等效果.
*  我们完全以API的形式呈现,稳定可靠,简单易用,您可以根据项目的个性化而任意的发挥.


## 核心架构
*   一个工程是由多个线程组成, 又由各种类对象组成. 
*   我们把对视频处理的OpenGLGL技术处理后封装成 线程，命名为DrawPad(画板)
*   对视频处理用到的各种素材，封装成类，命名为Layer(图层)
*   这样视频处理的OpenGLGL线程中增加的各种类对象，就被抽象成 画板和图层的关系。和日常画画流程一致，方便您的使用。
*   画板：用来处理各种素材的线程，分为 [画板前台线程] 和 [画板后台线程], 您自由选择使用。
*   图层：编辑会用到的素材。包括：视频，图片，文字，音乐，麦克风，摄像头，裸数据，MV等。这些经过我们的核心技术处理，变成：视频图层， 		图片图层，UI图层，Canvas图层，音乐图层，麦克风图层，数据图层，摄像头图层，MV图层,Gif图层等。
*   抽象类Layer：继承它的有：视频图层， 图片图层，UI图层，数据图层，摄像头图层，MV图层；均有：平移/缩放/旋转/隐藏/显示/RGBA调节的功能。
		另外他们各自也有独立的方法。
*   滤镜功能：当前所有的图层均支持滤镜功能。


比如您的操作是：
1.	把给视频增加滤镜： 则你增加视频图层到画板上， 然后调节VideoLayer中的滤镜即可。

2.	再比如： 你要在视频中增加文字： 则你增加[视频图层]+[UI图层]到画板中，在处理过程中，实时的调节他们即可。

3.	再比如：你要拍照的同时增加滤镜，或增加图片或视频在四周环绕， 则您可以增加[摄像头图层]+[图片图层]或[视频图层]到画板上，图片设置到四周，视频用滤镜处理成中间透明，就实现您要的效果。

4.	再比如：你想生成一段文字或把炫酷的动画转换为视频，则可以直接增加[UI图层]到画板上。

5.	再比如：你想给视频实时增加说话声，则可以直接增加[Mic图层]，当然如果仅仅是剪切替换声音，则直接用VideoEditor类中的替换方法就可以。

											
*  此SDK采用为收费授权,公司性质的合作,为了您项目更好的进行,欢迎和我们联系.谢谢!

## 更仅一步说:
*	1，你用 【视频图层 VideoLayer】在 画板 DrawPad上作画， 就得到 调整后的视频

* 2，你用  【图片图层 BitmapLayer】在画板上作画， 就得到 动态的照片影集。

*	3，你用 【UI图层  ViewLayer】在画板上作画， 就是把精美的UI界面转换为视频， 当然我们的设计，也可以后台处理。

* 4， 你用 【视频图层】+ 【图片图层】 在画板上作画， 就得到动态的视频图片效果。

* 5， 你用  【视频图层】 + 【MV图层】 在画板上作画， 就是在视频中叠加MV的效果。

* 6， 当然： 画板 可以在前台工作， 也可以在后台处理。



## 下载地址: 
*  https://github.com/LanSoSdk/LanSoEditor_advance

## 我们有基本视频编辑,以方便您项目中基本需求：
*	https://github.com/LanSoSdk/LanSoEditor_common

## 我们的IOS版本， 欢迎您的使用：
*	https://github.com/LanSoSdk/LanSongEditor_IOS

## 直接下载获取APK:
   下载整个项目后, 在bin文件下有apk, 直接安装后即可演示.


## 联系方式:
*   QQ 1852600324 
*   Email:support@lansongtech.com
*   网址: www.lansongtech.com

*  如果您下载过慢, 可联系我们, 索取最新的工程包