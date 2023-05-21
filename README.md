# xray for Render

## 项目特点

* 本项目用于在 [Render](https://render.com/) 免费服务上部署 vmess / vless / trojan / shadowsocks 节点
* 集成哪吒探针，可以自由选择是否安装
* 部署完成如发现不能上网，请检查域名是否被墙，可使用 Cloudflare CDN 或者 worker 解决。

## 部署

* 注册 [Render](https://render.com/)
* config.json 中的第 14、52、69、100、128 和 157 行，修改自己的UUID（UUID生成器：https://www.uuidgenerator.net/ ）。在第 28 和 108 行修改 vmess 路径，在第 14 和 80 行修改 vless 路径，在第 32 和 136 行修改 trojan 路径，在第 36 和 165 行修改shadowsocks路径。
* app.js 的 5 行修改哪吒参数
* 部署成功后 vmess / vless / trojan / shadowsocks ws 的路径为: `/协议名` (例如：vmess 的路径为 `/vmess`)，如要修改，可以在 `config.json` 文件中寻找并替换相对应的路径

* 需要应用的 URL 参数
  | 命令 | 是否必须 | 说明 |
  | ------------ | ------ | ------ |
  | <URL>/start | 是 | 运行 xray |
  | <URL>/nezha | 否 | 运行哪吒 | 以 / 开头 |
  | <URL>/status | 否 | 查看后台进程  |

