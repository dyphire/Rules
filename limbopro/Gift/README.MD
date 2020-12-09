库位置：https://github.com/limbopro/Profiles/tree/master/limbopro/Gift

# 主理人说


## 备份 iOS IPA 安装文件
- 备份 1.0.2/1.0.3 （有哪个就备份哪个）；
- 备份IPA参考 [仅需三步，使用iMazing 轻松下载（当前版本）/或安装IPA文件（旧版本）](  https://limbopro.xyz/archives/imazing.html)（需挂代理）

~~*针对未来的更新是否应该立即更新，暂保留意见；~~ 

# 预配置文件版本更新日志
## App更新
### 22:00 22.11.2019 1.0.3 版本更新
*此更新仅针对 Quantumult X app 1.0.3 版本；已经阉割远程调用脚本（Scripts）的功能回归；如果你仍在使用本地脚本，更新QuantumultX到1.0.3 则不会受任何影响；博主建议大家继续使用本地脚本；想折腾 Quantumult X app 1.0.3 版本远程调用脚本（Scripts）的可参考：https://github.com/limbopro/Script （依然需要配合`WorkingCopy`App食用，一次配置，再也不用担心脚本更新；）

## 预配置文件更新
### 13:00 29.10.2019 新增WC预配置文件

1. 新增 `Working Copy` 对应版本的预配置文件；
2. Working Copy丨将Github仓库内容同步到手机（iOS）并配置 Quantumult X 本地脚本，以应对 Quantumult X 1.0.2 版本更新 对远程脚本调用的限制
3. https://github.com/limbopro/Profiles/tree/master/limbopro/Gift/WC

### 22:00 28.10.2019 更新
1. 减少策略到8个，Twitter/Telegram/Google/Ins 默认走`健康检测`策略，可自行修改`策略偏好`；
0. 为应对 QuantumultX 商店版 1.0.2 更新；
1. 预配置文件内置了NobyDa 脚本；（预配置文件教程第6步有详细介绍）
1. 更新预配置文件内置 Tiktok 解锁配置
2. 更新内置 VSCO/Terimius/酷我音乐 解锁配置

*商店版已经更新到`1.0.2`版本，NobyDa `Rewrite`去广告脚本订阅失效（~~已直接内置到预配置文件~~）；如果你已更新到`1.0.2`版本，可进入`Rewrite`模块引用内，删除`NobyDa`脚本；

*如需解锁Tiktok，但不想下载预配置文件：可单独参考设置：[iOS 使用 Surge/Quantumult/Shadowrocket /QuantumultX 解锁 TikTok 区域限制（免拔卡）10.10.2019](https://limbopro.xyz/archives/3629.html)  ；

### 10:00 28.10.2019 更新
1. 增加 亚马逊/Hulu/HBO/Spotify等分流规则，默认走Proxy

### 23:00 21.10.2019 更新
1. 增加神机去广告规则订阅，右滑可使用；
2. 分流订阅排序改变，使得去广告订阅在最前；
3. 优化预配置文件注释说明，更方便自主修改；


# 教程步骤虽多，但足够清晰

本预配置文件，相当于提前为QuantumultX`预设策略`（~~10~~8个策略）及其`策略图标`，`去广告规则`，`主流站点`分流规则，以及无需拔卡看，`Tiktok`，解锁`VSCO`会员；务必遵循教程步骤前后顺序，以确保其可用性；



## 事前备份
*可备份配置文件，以防止后悔；

1. 进入`QuantumultX`，点击右下角`三菱`按钮；
2. 找到`配置文件`模块下`导出`，点击，选择`存储到文件`；
3. 备份完毕；

# 教程概要

1. 备份已有机场节点订阅 （该步随意
2. 下载本预配置文件 
3. 下载NobyDa JS脚本 到iPhone本地
4. 配置并信任证书
5. 开启 Rewrite +MitM
6. 完事

**最终效果图参考** https://t.me/limboprossr/863

# 预配置文件使用教程
*注意 本教程中的预配置文件特指 `https://raw.githubusercontent.com/limbopro/Profiles/master/limbopro/Gift/QuantumultX4limbopro.conf`；如果你会使用`WorkingCopy`App，可参考：https://github.com/limbopro/Profiles/tree/master/limbopro/Gift/WC ，更方便；

以下为教程详细步骤：

## 1.备份你的机场订阅链接
0. **针对有多个机场订阅链接的小伙伴，这会是一个快捷备份方法**
1. 进入`QuantumultX`，点击右下角`三菱`按钮；
2. 找到`配置文件`模块下`编辑`，点击；
3. 找到`[server-remote]`，下方就是你已经配置好的机场`订阅链接`；
4. 复制，粘贴到某处，留作备用（不然等下又要一个个添加（如果持有机场多的话））；
5. 如果你只订阅了一个机场，进入`QuantumultX`，点击右下角`三菱`按钮，找到`节点`模块，`引用（订阅）`处复制；


## 2.下载预设配置文件
0. 复制`https://raw.githubusercontent.com/limbopro/Profiles/master/limbopro/Gift/QuantumultX4limbopro.conf`预配置文件链接；
1. 进入`QuantumultX`，点击右下角`三菱`按钮；
2. 找到`配置文件`模块下的`下载`，点击；
3. 粘贴刚刚复制的配置链接，点击右上角`确定`按钮；
4. 保存完毕，回到`QuantumultX`主界面，就可以看到配置好的10个`策略`图标了；

## 3.配置你的节点，删除红色感叹号标注的节点（如有）
*操作步骤务必遵循先后顺序*

0. 订阅你的节点；
1. 复制之前备份的机场`订阅链接`粘贴到`[server-remote]`后或点击从`节点`模块>`订阅/引用`处添加订阅链接；
2. 务必`删除`策略图标下`被三角红色感叹号标注`的`节点`，并`配置自己的节点`；否则将会出现错误提示如“未知策略或节点`无用节点1`<-`负载均衡`”，其中`负载均衡`为`策略`名字，`无用节点1`为该策略下不可用的节点，需要长按相应`策略`图标并删除，并配置自己有效节点即可；

## 4.重新配置证书以使得Tiktok/Rewrite去广告/解锁VSCO实现
* 如无需看Tiktok（这个很重要）或Rewrite去广告（这个影响不大）以及解锁VSCO VIP会员可省略本配置证书步骤；

~~1. 如果之前有配置证书，可进入 iOS 系统`设置`-` 通用`-`描述文件`-`已下载的描述文件`-选中，`移除描述文件`，输入密码...完成描述文件安装；~~

2. 进入QuantumultX，点击页面右下角三菱`按钮`，找到`MinM`模块，点击`生成证书`，提示生成成功，点击`安装证书`此时会跳转至` Safari`，提示`此网站...下载一个配置描述文件。您要允许吗？`，点击`允许`，网页提示`已下载描述文件`；
3. 进入 iOS 系统`设置`-` 通用`-`描述文件`-`已下载的描述文件`-选中，并安装，输入密码...完成描述文件安装；
4. 进入 iOS 系统`设置`-` 通用`-`关于本机`-`证书信任设置`-`针对根证书启用完全信任`-选中刚刚安装的并启用即可；


* **VSCO解锁**： 测试解锁成功版本为 Version134.0 版本
* **Tiktok 如需换区**：进入`QuantumultX`，点击页面右下角三菱按钮，找到Rewrite模块，点击添加，复制
(?<=(carrier|account|sys)_region=)CN url 307 JP
将JP修改成其他地区英文缩写即可，其他国家或地区代码。例如改成 HK，KR，TW，KP；


## 5.下载并引用本地脚本

*为了应对Quantumlt X v1.0.1 及之后版本更新对远程脚本的限制；具体是指 v1.0.1-1.0.2  已不再支持远程下载JS脚本所以需要进行本地配置；（例如该Rewrite 脚本：https://raw.githubusercontent.com/NobyDa/Script/master/QuantumultX/Js.conf）

也就是说将NobyDa的脚本放到本地，以供`QuantumultX`进行引用；

0. 现在可以参考视频：https://t.me/limboprossr/921 并配合以下步骤食用；

1. 打开iOS 系统自带软件 `文件`，进入`我的iPhone`-找到`Quantumult X` 文件；
2. 进入`Quantumult X`文件夹-再进入`Scripts`子文件夹，长按空白处选择`新建文件夹`；
3. 命名为`NobyDa`;
4. 搞定；

5. 复制`https://github.com/NobyDa/Script/archive/master.zip`，并在手机浏览器打开，点击`下载`
6. 如何是Safari浏览器，页面右上角会有下载按钮，点击它，找到刚刚下载的文件，点击它；
7. 跳转到下载项，长按该文件，选择`移动`，移动到我们第2步新建的`NobyDa`文件夹里；
8. 返回`文件`app，进入`NobyDa`文件夹，解压`Script-master.zip`，得到 `Script-master` 文件夹；
9. 长按 `Script-master`，重命名为`Script` 即可；

* 预配置文件内已经进行了调用，完美；

## 6.Enjoy

1. 进入`QuantumultX`，点击右下角`三菱`按钮，找到并开启`Rewrite` & `MitM`按钮（如果第4步骤没有配置证书，这个按钮无需开），最后开启 QuantumultX；

2. 完事！
3. 享受无广告，带策略，带图标，带解锁！

# 玩法

## 试玩配置文件修改策略模式及模式说明
1. 进入`QuantumultX`，点击右下角`三菱`按钮；
2. 找到`配置文件`模块下`编辑`，点击；

3. 可以修改各个`策略`的`策略模式`；
## 策略模式说明及其用法
available 为`健康检查模式`（从该策略下的第一个节点往下检查，如第一个可用，则选第一个，不可用则向下检查，直到可用为止；如果你打开Telegram 无法连接，等几秒即可自动切换到可用节点，长时间不可以连接，则可能无可用节点）；round-robin 为`负载均衡模式`（依次从上向下使用该策略下的节点）；static 为`静态策略模式`（手动选择想用的节点）；另外，如何修改`策略模式`，进入`QuantumultX`，点击右下角`三菱`按钮，进入`配置文件`，点击编辑，找到相关策略名字，可以通过把 available 改为 static 的方式以切换至静态策略模式，其他同理；

# 小技巧
## 查看网络活动
**网络连不上？Twitter打不开？ins加载慢？**

1. 进入`QuantumultX`，找到`网络活动`模块（长得像记事本那个）；
2. 你就可以知道，最近打开某个APP例如ins/Twitter/在走哪个分流规则/走哪个策略了/哪个节点了，是直连还是代理还是拒绝连接服务器；
3. 日志可以详细到时间/节点/策略/；
4. 相应调整节点/策略/即可

## FAQ
### 如何删除无用/不想用的策略组
0. 以 `Instagram` 策略举例说明；
1. 进入`QuantumultX`，点击右下角`三菱`按钮；
2. 进入` 分流`-`订阅`，找到与之绑定的分流订阅，`..instagram.lis`，右滑选择禁用，或左滑`编辑`调整策略偏好为可用`策略`，例如`Proxy`；
2. 再找到`配置文件`模块下`编辑`，点击；
3. 找到`[policy]`，找到要删除的`策略`，在策略名前注释即可；
4. 以上步骤务必遵守前后顺序，否则QX将自动生成策略；
5. 因为分流规则跟策略的绑定关系，如果QX没有自带该策略，则系统会自动生成该策略；

```
[policy]

;static=Instagram, PROXY, 健康检测, DIRECT, img-url=https://raw.githubusercontent.com/limbopro/Zure/master/IconSet/Instagram-little.png
```
其中 `;` 符号为注释符号，也可以换成`#` 号

6. 玩法参考：QuantumultX 进阶教程：[组策略&分流规则&自定义图标的进阶玩法](https://limbopro.xyz/archives/3846.html)  

### 关于名叫CN策略
1. 进入`QuantumultX`，可以看到一个中国地图样式的策略，CN；
~~2. 该策略没有绑定分流规则；~~
~~3. 如果你在国内，可以在该策略下添加任意可用节点；~~
4. 本意是留作出国时用回国节点的，默认禁用；
5. 如果你在国外，如需开启：进入`QuantumultX`，点击右下角`三菱`按钮，找到`分流`模块，`引用（订阅）`
6. 找到`CN（回国）`分流的订阅链接，右滑开启；往上回到页面顶部，点击` 全部同步`即可；
7. 如需禁用，同理（第6步）；

### 是否还会更新
会的，或增加策略（概率很小），优化分流规则（只需更新分流订阅即可），~~优化图标~~；正常情况下，我个人认为，10个策略基本上已经足够；

### 想自定义图标或策略或新加去广告规则？
1. 参考：[QuantumultX 进阶教程：组策略&分流规则&自定义策略图标的进阶玩法参考（通俗规范教程）](https://t.me/limboprossr/843)
2. 参考：[iOS 使用 Surge/Quantumult/Shadowrocket /QuantumultX 解锁 TikTok 区域限制（免拔卡）10.10.2019](https://limbopro.xyz/archives/3629.html) 
3. 毒奶自用图标：https://github.com/limbopro/Zure Folk 自 Zure；
4. 毒奶自用分流规则：https://github.com/limbopro/Profiles/tree/master/Quantumult/X/Filter

*文章如若打不开，请挂代理访问！

## 参考以及鸣谢
1. NobyDa https://github.com/NobyDa/Script 脚本及去广告支持
2. ConnersHua https://github.com/ConnersHua/Profiles 主流网站分流规则支持
3. Zure https://github.com/zealson/Zure 图标支持

*如需额外脚本配置可以参考学习 NobyDa，分流规则配置可以参考学习 ConnersHua，图标学习找 Zure；



# 联系主理人

1. 关注频道 https://t.me/limboprossr 不失联；
2. `毒奶粉`们（我管我的Fans）可联系 [TG机器人](https://limbopro.xyz/usr/uploads/2019/10/3453243330.png) 或发送 [邮件](https://limbopro.xyz/usr/uploads/2019/10/3453243330.png) 获取帮助；

  [1]: https://raw.githubusercontent.com/limbopro/Profiles/master/limbopro/Gift/QX.jpg
