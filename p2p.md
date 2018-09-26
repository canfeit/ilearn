## 使用p2p协议，代替http+websocket，实现设备屏幕同步共享
* 用户直接与device client通信获取屏幕数据，免去服务器压力(网络和性能瓶颈)
* 去中心化，免去中心服务器二次转发，理论上可以显著提升同步流畅度和画面清晰度
* 解决方案(JS)：IPFS OR webtorrent(WebRTC)