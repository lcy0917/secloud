# SECloud 安全网盘

目前 Coding 的演示环境收费了，于是暂时关闭了演示

特点
---
- 专为注重隐私的`互联网强迫症患者`打造
- 文件云端加密存储，本地加解密
- 客户端与服务端分离，个人部署只需部署服务端，客户端通用跨平台
- 云存储商和服务端托管商可替换，选择自己信任的，甚至自己搭建
- Javascript全栈：前端为`AngularJS`，后端为`NodeJS`+`ExpressJS`

部署
---
需结合服务端[secloud-server][14]

`注：这里的演示部署仅仅是个参考，如果你愿意且有能力修改，怎么玩都可以`

目前存储用的是[七牛云存储][1]，服务端托管于[Coding][2]，客户端直接由Github Pages托管，接下来你需要：

  - 有七牛账号，最好通过实名认证（不然免费额度恐怕不够）
  - 有Coding账号，可能还需要知道git一点基本用法

客户端地址：http://secloud.xyz/ ，如个人不作修改则无需重新部署，
客户端认证的时候需要`认证域名`和`安全密码`，这里的`认证域名`即个人部署的服务端域名，服务端部署前需要：

七牛新建一个`BUCKET`，并且设为私有
![][3]

得到空间的域名`DOMAIN`

获得`ACCESS_KEY`和`SECRET_KEY`
![][5]

自己选一个足够安全的密钥，然后得到其MD5值`PASSWD`
如果是*nix，命令一般为：`echo -n "<your_password>" | md5sum`
也可以用[在线工具][6]得到

OK，此时记下：`BUCKET`、`DOMAIN`、`ACCESS_KEY`、`SECRET_KEY`、`PASSWD`

在Coding里新建一个项目，导入secloud-server仓库：`https://github.com/int64ago/secloud-server.git`
![][7]

开启演示

设置环境变量（之前让记下的）
![][9]

部署设置，设置完之后一键部署即可
![][10]

在 http://secloud.xyz/ 登录
![][11]

网盘主界面
![][12]


  [1]: http://www.qiniu.com/
  [2]: https://coding.net/
  [3]: https://dn-getlink.qbox.me/walco4scbx1or.png
  [5]: https://dn-getlink.qbox.me/43fwztyory66r.png
  [6]: http://tool.oschina.net/encrypt?type=2
  [7]: https://dn-getlink.qbox.me/95gxy2ry0hpvi.png
  [9]: https://dn-getlink.qbox.me/855fhcjhpk3xr.png
  [10]: https://dn-getlink.qbox.me/oriysmglgcik9.png
  [11]: https://dn-getlink.qbox.me/oriysmglgcik9.png
  [12]: https://dn-getlink.qbox.me/ku48e5k2fn7b9.png
  [13]: http://secloud.xyz/
  [14]: https://github.com/int64ago/secloud-server
