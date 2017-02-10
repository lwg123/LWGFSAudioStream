# LWGFSAudioStream
FreeStreamer 流媒体播放音乐
添加第三方库时注意事项
1.拷贝FreeStreamer中的Reachability.h、Reachability.m和Common、astreamer两个文件夹中的内容到项目中。

2.添加FreeStreamer使用的类库：CFNetwork.framework、AudioToolbox.framework、AVFoundation.framework
、libxml2.dylib、MediaPlayer.framework。

3.如果引用libxml2.dylib编译不通过，需要在Xcode的Targets-Build Settings-Header Build Path中添加$(SDKROOT)/usr/include/libxml2。

4.将FreeStreamer中的FreeStreamerMobile-Prefix.pch文件添加到项目中并将Targets-Build Settings-Precompile Prefix Header设置为YES，在Targets-Build Settings-Prefix Header设置为$(SRCROOT)/项目名称/FreeStreamerMobile-Prefix.pch
