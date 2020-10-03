**小主机：Dell 9020M**

**CPU:i7 4770T**

**网卡：BCM94360CS 三天线**

-------
20201003更新
#### 1.升级OpenCore 0.6.1
#### 2.开启HiDpi：
项目地址：[One-Key-HiDPI](https://github.com/xzhih/one-key-hidpi)
#### 3.更换三码，开启变频正常
项目地址：[CPUFriend](https://github.com/acidanthera/CPUFriend)
1. 下载CPUFriernd.kext
2. 下载ResourceConverter.sh
3. 在ResourceConverter.sh所在目录运行以下命令：
`
./ResourceConverter.sh --kext /System/Library/Extensions/IOPlatformPluginFamily.kext/Contents/PlugIns/X86PlatformPlugin.kext/Contents/Resources/Mac-F60DEB81FF30ACF6.plist
`    
5. 其中后边的文件按目录找到对应SMBIOS机型`board-ID`对应的plist拖入终端即可，其中board-ID可以用OCC查看。
6. 完成后在ResourceConverter.sh同级目录下会生成一个`CPUFriendDataProvider.kext`文件，将其连同`CPUFriend.kext`放入clover的kext下即可
7. 用[CPU-S](https://github.com/lihaoyun6/CPU-S)重启查看变频效果
-------
