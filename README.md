> 参考[仓库](https://github.com/DustinWin/clash-geosite)，配置自用

# 一、生成user.yaml

① 每天早上 3 点（北京时间）自动构建生成

② 添加[常用 fake-ip 地址过滤列表](https://github.com/juewuy/ShellClash/blob/master/public/fake_ip_filter.list)到 fake-ip-user.yaml 内的 `fake-ip-filter` 中，提高兼容性

③ 添加 [TrackersList](https://trackerslist.com) 到 fake-ip-user.yaml 内的 `fake-ip-filter` 中，防止 [BT 下载](https://github.com/c0re100/qBittorrent-Enhanced-Edition/releases)无法连接 TrackersList UDP 协议

<img src="https://user-images.githubusercontent.com/45238096/224113233-4d76dec2-495c-4790-a00e-538fc1469639.png" width="60%"/>

# 二、 导入 [ShellClash](https://github.com/juewuy/ShellClash)
## 1. DNS 模式为 fake-ip
连接 SSH 后执行如下命令：
- 注：以 geosite.dat 为例

```
curl -o $clashdir/yamls/user.yaml -L https://cdn.jsdelivr.net/gh/yaojia25/shellclash-user-config@release/fake-ip-user.yaml
$clashdir/start.sh restart
```
## 2. DNS 模式为 redir-host
使用 gist 生成的链接即可
