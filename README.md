# 西安电子科技大学(杭州研究院)晨检自动填报工具（只进行晨检）

本代码更改自[HANYIIK/Auto-dailyup](https://github.com/HANYIIK/Auto-dailyup)，在此基础上完善`杭州研究院`并增加了`Qmsg推送`，因目前只要求进行晨检，并对晨午晚检相关逻辑进行了更改，只进行晨检，但并未删除午晚检相关程序，方便后续进行晨午晚检。


##### 感谢大佬们的无私奉献，本代码仅供学术交流，侵删
##### 使用本程序即默认同意使用者承诺未感染新冠肺炎，
##### 使用本程序造成的任何后果由用户自行负责。



### 使用方法如下：
Windows系统：
```
pip install requests -i https://pypi.tuna.tsinghua.edu.cn/simple
```
```
python index.py
```
Linux系统：
```
pip3 install requests -i https://pypi.tuna.tsinghua.edu.cn/simple
```
```
python3 index.py
```
然后根据提示输入学号、位置、密码，在后台挂着不管它就行了。<br>
第一次登录成功后无需再次输入密码，如果后期更改了密码，建议删除`data/cookie.inf`文件，重新运行即可。<br>
##### 特别提醒 1：Mac系统第一次登录后无法实现清屏功能，为防止明文密码暴露，建议`Ctrl+C`停止一下，再重新`python index.py`即可隐藏密码。
##### 特别提醒 2：位置信息建议选`6：美国加利福尼亚州洛杉矶`，可以感受一下被校领导关心的感觉。
##### 特别提醒 3：脚本记录的cookie数据每隔一段时间会失效，若是无法上报可通过删除`data`文件夹下的`cookie.inf`后重新登录来刷新。

### 运行截图：
![image](https://github.com/bcmy/AutoDailyup-XDU-HZ/blob/master/images/1.png)

![image](https://github.com/bcmy/AutoDailyup-XDU-HZ/blob/master/images/2.jpg)
#### 终端每天正常的输出结果：
![image](https://github.com/bcmy/AutoDailyup-XDU-HZ/blob/master/images/3.png)
* ### 关于Linux和Mac用户如何实现眼不见心不烦：
如果觉得终端一直挂在那里很烦的话，建议安装一个后台分屏软件`screen`:
```
sudo apt-get install screen
```
安装好后进入screen模式：
```
screen
```
按回车确认，进入该`screen`后运行程序:
```
python index.py
```
按住`Ctrl`+`A`键后，再按一个`D`键，即可将该窗口`detach`掉，然后你就看不见它了。<br>
<br>关于如何唤醒这个`screen`:
```
screen -ls
```
找到该`screen`的`id`号 `xxxxx`后：
```
screen -r xxxxx
```
即可。

### Qmsg机器人搭建

自行查看并搭建[Qmsg酱](https://qmsg.zendee.cn/)  

### 获取位置
预留了自己家的位置，请根据自身位置情况自行更改  
在[这个页面](https://geoinfo.hawa130.com/)获取位置信息。
手机复制[这个网址](https://geoinfo.hawa130.com/)到微信聊天框，该网址由[Health Card Checkin](https://github.com/hawa130/health-card-checkin)提供
1. 点击「获取定位信息」。
2. 若提示需要权限，请允许。
3. 获取成功后，点击「复制打卡用数据」，此时位置信息已存储至剪贴板。
4. 将得到的位置自行更改到`UPLOAD.py`的`HOME_UPLOAD_MSG`中即可

### 手动打卡
请至少在所在城市[手动打卡](https://xxcapp.xidian.edu.cn/ncov/wap/default/index)过一次再使用本脚本

### 用户协议

#### 再次申明

1. 本脚本默认使用者承诺未感染新冠肺炎以及未出现有疑似新冠肺炎症状的情况，如果身体有任何疑似新冠肺炎症状的情况，请立即停止使用该脚本，并根据实际情况[手动填报](https://xxcapp.xidian.edu.cn/ncov/wap/default/index)。（一定要如实填报哦）
2. 该脚本开源，免费提供，无任何收费服务~~（这简陋脚本总不会有人倒卖吧）~~，你可以自行搭建部署、修改、分发该脚本
3. 若发生因使用本脚本而导致的任何意外，作者概不负责。~~（免责声明）~~
4. 感谢大佬们的无私奉献，本代码仅供学术交流，侵删

如果你使用本脚本，将默认视为你同意上述协议。


## 鸣谢
[西安电子科技大学(包含广州/杭州研究院)晨午晚检自动填报工具](https://github.com/HANYIIK/Auto-dailyup )  
[Qmsg酱](https://qmsg.zendee.cn/)  
[Xddailyup](https://github.com/Pairman)  
[Health Card Checkin](https://github.com/hawa130/health-card-checkin)  
[jiang-du/Auto-dailyup.git](https://github.com/jiang-du/Auto-dailyup.git)  
[使用Github Aciton自动填写疫情通](https://cnblogs.com/soowin/p/13461451.html)  
[西安电子科技大学疫情通、晨午晚检自动填报工具 ](https://github.com/jiang-du/Auto-dailyup )  
[西安电子科技大学晨午晚检自动填报工具](https://github.com/cunzao/ncov)  
