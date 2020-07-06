# 常见问题（更新时间：2020年06月09日）

APK下载地址：[https://github.com/Lerist/fakelocation.github.io/releases](https://github.com/Lerist/fakelocation.github.io/releases/)     |    [http://apps.lerist.cc:81/fakelocation](http://apps.lerist.cc:81/fakelocation)

## 支付问题

### 1、订单码说明

订单码是在使用支付宝支付时临时生成的随机代码，该代码包含 FL(Fake Location) 账号以及您选择的专业版套餐等信息，是完成充值的重要依据，并且并非支付宝订单号；订单码仅可单次使用，完成充值后订单码会立即失效，因此请勿在下次充值时继续使用同一订单码。

### 2、点击支付宝支付方式，未能成功跳转到支付页面

请尝试升级支付宝客户端，或者采用手动转账方式，转账账号: lerist@163.com，转账时请记得备注上订单码。

### 3、支付宝支付完成，专业版长时间仍未开通

请先确认支付时，是否有在备注栏（下图1划红线处）里附带订单码

 * 若没有附带订单码，请在专业版开通页面的支付宝续期弹框里点击"忘记备注订单码"(下图2红框处)，重新提交一下。订单码会自动生成，您只需粘贴上支付宝订单号提交就行了（订单号是在支付宝账单详情里，年份开头那串数字）。记得提交前选择与支付金额一致的专业版套餐。

* 若有附带订单码，请将支付详情截图以邮件方式发给开发者处理，或者也可以直接采用前面没有附带订单码的方法，再次提交一下订单给开发者审查。
  开发者邮箱：lerist.5@gmail.com

<img src="https://raw.githubusercontent.com/Lerist/fakelocation.github.io/master/FAQ/zh/img/Screenshot_2019-04-27-05-54-30-945_com.eg.android.png" width="30%" height="30%" />       <img src="https://raw.githubusercontent.com/Lerist/fakelocation.github.io/master/FAQ/zh/img/IMG_20190427_041839.jpg" width="30%" height="30%" />

- - - -

## 使用问题 

### 1、使用 Magisk root 开启模拟时一直转圈

一直转圈是在等待 Root 授权，请先不要在 Magisk  Hide 里勾选 Fake Location，或者暂时先在Magisk设置中关闭“Magisk Hide”选项。有些手机还需保持 Magisk 在后台运行。

### 2、ROOT模式下开启模拟提示System分区不可写

可以先尝试使用 Syslock 解锁分区，若 Syslock 解不了的话，可以安装 Magisk 来解锁：先下载安装 Magisk Manager，然后取消 Magisk Manager 安装选项里的"保留 AVB 2.0/dm-verity"选项再点击Magisk 后面的"安装"，选择"直接安装"（需先授予 Magisk Manager Root权限才有此选项）。

若系统版本是 Android 9.0+ 的话，需将“ https://raw.githubusercontent.com/topjohnwu/magisk_files/master/canary_builds/release.json ”粘贴进 Magisk Manager 设置里的自定义更新通道里，然后重新打开 Magisk Manager ，这时会提示更新，点击 Magisk Manager 后面的更新按钮，更新完成后再执行前面的安装 Magisk 操作即可。

Syslock下载地址：[https://www.coolapk.com/apk/com.lerist.syslock](https://www.coolapk.com/apk/com.lerist.syslock)

Magisk Manager 下载地址：[https://www.coolapk.com/apk/com.topjohnwu.magisk](https://www.coolapk.com/apk/com.topjohnwu.magisk)

### 3、ROOT模式下开启模拟提示错误码103

103是系统分区空间不足了，使用RE管理器进到/system下删掉一些无用文件即可；小米可以删掉/system/data-app，魅族可以删掉/system/MzApp，一加可以删掉/system/reserve，其他机型可以将/system目录截图邮件发给开发者审查可删文件。开发者邮箱：lerist.5@gmail.com

### 4、ROOT模式下开启模拟提示错误码104

* 华为手机：华为近期发布的EMUI内核不支持ptrace操作，目前只有刷第三方解除了限制的内核才能使用ROOT模式，建议可以去xda论坛找找第三方内核

* 三星手机：三星部分机型的内核和KNOX服务限制，不能关闭SELinux，目前也只有刷解除限制了的第三方ROM和内核才能使用ROOT模式

* 其他机型：请打开FL设置里的"日志记录"功能，重启一下手机，再开启模拟，出现错误后，点击侧边栏里的"反馈"，选择邮件方式把日志文件发给开发者分析具体原因（若邮箱客户端附带不了日志文件，建议使用网易邮箱客户端发送）

### 5、ROOT模式下开启模拟提示“虚拟位置服务连接失败”

请先确保使用的是正版且最新版本的程序（最新版本下载地址见本页面顶部），然后不要在虚拟空间（例如一些多开软件）里安装运行，不要修改FL安装包，不要使用破解版本；若是在更新版本后出现的这个问题，请先重启手机，再进FL的设置里清理一下运行环境即可；若是问题依旧，请打开FL设置里的"日志记录"功能，重启一下手机，再开启模拟，出现上述错误后，点击侧边栏里的"反馈"，选择邮件方式把日志文件发给开发者分析具体原因（若邮箱客户端附带不了日志文件，建议使用网易邮箱客户端发送）

### 6、NOROOT模式下开启位置模拟后，部分APP依然显示真实位置

有些APP需要在ROOT模式下才有效，比如微信等；手机没有ROOT的话可以参考下面第 10 条。

### 7、ROOT模式下开启位置模拟后，被模拟软件提示 定位失败、获取位置信息失败 之类的提示

可能被模拟软件使用的是基站定位，请尝试在位置模拟页面点击"基站"开启基站模拟。

### 8、程序后台运行一段时间后自动关闭、跳回真实位置、摇杆退出或摇杆罗盘不随手机方向旋转

这种情况通常是程序被系统或其它某些应用清理掉了，请尝试允许FL后台运行，以及关闭省电优化之类的设置：

* 华为手机允许程序后台运行：
  [https://zhidao.baidu.com/question/521051452342852205.html](https://zhidao.baidu.com/question/521051452342852205.html)

* 华为手机忽略电池优化：
  [https://zhidao.baidu.com/question/652261302590163205.html](https://zhidao.baidu.com/question/652261302590163205.html)

* Oppo 手机允许程序后台运行：
  [https://zhidao.baidu.com/question/1545944666186333827.html](https://zhidao.baidu.com/question/1545944666186333827.html)

* Vivo 手机允许程序后台运行：
  [https://jingyan.baidu.com/article/046a7b3e9462f2f9c27fa9e9.html](https://jingyan.baidu.com/article/046a7b3e9462f2f9c27fa9e9.html)

* 小米手机：进入应用详情页，打开“自启动”开关，并把“省电策略”设为无限制，如下图所示

<img src="https://raw.githubusercontent.com/Lerist/fakelocation.github.io/master/FAQ/zh/img/Screenshot_2019-04-27-08-17-37-981_com.miui.secur.png" width="30%" height="30%" />

* 其他手机请自行百度允许程序后台运行的方法

### 9、关于反检测功能的使用

反检测功能需要手动设置“反检测应用”和“检测应用”

* 反检测应用：即需要隐藏的应用，或者不想被检测到的应用；如：Fake Location。点击页面内的“反检测应用”卡片进行设置。
* 检测应用：即会检测其他应用的应用；如：DD、一些游戏等。点击页面内的“+”按钮进行添加。

注：“反检测应用”和“检测应用”的关系是：“反检测应用”里勾选的应用不会被“检测应用”列表里的应用检测到，千万不要搞反了，并且两者里面不能同时包含同一应用。

### 10、手机没有ROOT权限，使用ROOT模式下的功能（不保证所有机型都适用）

手机没有ROOT权限的话，可以尝试在虚拟大师里使用ROOT模式，虚拟大师：https://www.coolapk.com/apk/com.vmos.app  ，安装虚拟大师后，把 Fake Location 和需要使用Fake Location功能的应用一并安装进虚拟大师，就可以使用ROOT模式下的功能了。(提示：有些APP可能不支持在虚拟大师里运行，还请自行测试)。

注：目前已知在虚拟大师里不能成功模拟GPS信号。

### 11、避免DD检测

* NOROOT模式（手机无ROOT权限）：使用FL设置里的"定制专属包"功能定制一个您自己的专属包来安装使用，就可以避免被DD检测到；安装专属包后记得卸载掉原版 Fake Location 然后重启一下手机。定制专属包时需要支付一定的定制费用。注：近期DD给部分账号推送了新的检测机制，NOROOT模式下可能无法使用部分功能; 或者可以尝试下载安装旧版本的DD（5.0之前的版本）。

* ROOT模式（手机有ROOT权限）：在反检测页面中点击"+"按钮添加DD到"检测应用"，然后开启反检测即可。

注：需确保手机上没有其它虚拟定位软件以及XP框架。

### 12、避免游戏检测

* NOROOT模式（手机无ROOT权限）：使用FL设置里的"定制专属包"功能定制一个您自己的专属包来安装使用，就可以避免被游戏检测到；安装专属包后记得卸载掉原版 Fake Location 然后重启一下手机。定制专属包时需要支付一定的定制费用。

* ROOT模式（手机有ROOT权限）：在反检测页面中点击"+"按钮将游戏添加到"检测应用"里，并且打开设置里的“增强反检测”选项，然后开启反检测即可；需确保Fake Location为最新版本并且手机上无其他虚拟定位软件及辅助软件。若开启“增强反检测”后导致应用无法正常运行，或提示"增强反检测未生效"，可以关闭增强反检测，然后用 存储重定向 为游戏“启用存储空间隔离”，存储重定向下载地址：https://www.coolapk.com/apk/moe.shizuku.redirectstorage

注：请合理使用模拟软件，速度不要超过10，也不要长时间保持同一速度，并且避免位置漂移。


### 未完待续...
