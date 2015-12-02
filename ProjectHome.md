This project trying to generate a private p2p network.
To demo how to use this p2p pnet library, there is


Project requirment:
a) This network should be cost free
No server required for this network, no money required.

b) This network should be free of restraint
The node of this network should be hard to be blocked.

c) Safe
Not easy to sniffer.
Not very easy to hack into this network.
Try to confuse router which may sniffer the traffic by encrypt the traffic.
Using hash to identify the flow.

d) Support nodes behind NAT
Focus on customer located behind simple NAT like ADSL.
For nodes in net-bar, no plan currently, however in theory, it should also work.
Using upnp & punch hole & WAN node relay etc. So we need to have a stack for reliable  data flow.
Currently, in this project, we implemented a simple SCTP stack. Tunnel sctp traffic via UDP protocol.

Implement details:
1. implement KAD
> Choose KAD because it is  proven/simple algothrim.
2. integrate UDP punch hole function
> > Punch hole for clients which in LAN.
3. Broadcast in LAN
4. security related

For developers:
The freeddns is not stable/availabe, you have to configure a super seed if you are not LAN user. You can do it via API: p2p\_add\_seed(char **peer\_id, uint32 ip, uint16 port)**

For IM users:
You must add a seed via account->account setting for now.



---

目标是一个安全方便的网络联系平台。

无需注册，可以使用任意方式，包括汉字，字母，数字等来定义你的号码。
无需注册，永久免费的个人域名系统。
无需服务器，永远不用担心账号失效。
无需服务器，永远不用担心被人从服务器监听。
标签搜索功能，多种方式找到你失散的好友。
标签搜索功能，根据关键字找到新好友。
标签发布功能，灵活发布广告。
多人会议系统，快速组建自己的聊天室。
可配置端口，不怕封锁。
可设置聊天密码，不怕网络监听。
输出扩展接口，方便二次开发。

软件可和Netmeeting, 本地Web server集成使用，这样所有使用本软件的用户就形成一个综合性的网络平台。
注意： 必须至少有个一个正在使用本软件的用户有广域网地址， （不是192.168.x.x）。 目前我一般不在线，所以，如果你是想试一试，可以加种子地址在局域网使用，或者确定有一个人使用adsl可以获得公网地址的上网方式（非网吧）.