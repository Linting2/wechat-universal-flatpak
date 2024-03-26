# wechat-universal-flatpak

基于微信 Linux Universal 版打包，无发行版限制。

## 安装

从 Release 下载安装包，使用以下命令安装即可。

```shell
flatpak install com.tencent.WeChat.flatpak
```

## 无法正常使用的功能

 - Wayland 环境若如果无法使用输入法，请添加环境变量：QT_IM_MODULE 及 GTK_IM_MODULE。

## 截图

![aa](.assets/sc.png)

## flatpak的runtime问题
如果在安装过程中遇到如下问题
error: The application com.tencent.WeChat/x86_64/master requires the runtime org.freedesktop.Platform/x86_64/23.08 which was not found
可以利用下面的命令进行修复，之后再重新安装
```shell
sudo flatpak remote-add --if-not-exists --system flathub \
  https://flathub.org/repo/flathub.flatpakrepo
```
