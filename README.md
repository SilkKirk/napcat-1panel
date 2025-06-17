## 使用方式

github代理地址
- 自建 : https://gh.spoli.cn/ 
- 网络 : https://ghproxy.link/

*注意:* 失效请自行寻找代理
docker镜像已添加自建代理

### 1 使用 git 命令获取应用

`1Panel`计划任务类型`Shell 脚本`的计划任务框里，添加并执行以下命令，或者保存为sh然后在终端运行。
#### 国内
```bash
#!/bin/sh

install_dir=$(which 1pctl | xargs grep '^BASE_DIR=' | cut -d'=' -f2)

rm -rf $install_dir/1panel/resource/apps/local/napcat-1panel-napcat

git clone -b main https://gh.spoli.cn/https://github.com/SilkKirk/napcat-1panel.git "$install_dir/1panel/resource/apps/local/napcat-1panel-napcat"

if [ $? -eq 0 ]; then
    rm -rf $install_dir/1panel/resource/apps/local/napcat
    mv $install_dir/1panel/resource/apps/local/napcat-1panel-napcat $install_dir/1panel/resource/apps/local/napcat
    echo "success"
else
    echo "error"
    exit 1
fi
```
然后应用商店刷新本地应用即可。

<div align="center">
  <img src="https://socialify.git.ci/NapNeko/NapCatQQ/image?font=Jost&logo=https%3A%2F%2Fnapneko.github.io%2Fassets%2Flogo.png&name=1&owner=1&pattern=Diagonal%20Stripes&stargazers=1&theme=Auto" alt="NapCatQQ" width="640" height="320" />
</div>

---
## 欢迎回来
NapCatQQ (aka 猫猫框架) 是现代化的基于 NTQQ 的 Bot 协议端实现

## 猫猫技能
- [x] **超高性能**：轻松数千群聊 独创消息队列
- [x] **启动方式**：支持以无头、LiteLoader 插件、仅 QQ GUI 三种方式启动
- [x] **覆盖平台**: 覆盖 Windows / Linux (可选 Docker) / Android Termux / MacOS
- [x] **安装简单**: 支持一键脚本/程序自动部署/镜像部署等多种覆盖范围
- [x] **超低占用**：无头模式占用资源极低，适合在服务器上运行
- [x] **超多接口**：实现大部分 OneBot 和 go-cqhttp 接口，超多扩展 API
- [x] **远程管理**：自带 WebUI 支持，远程管理更加便捷
- [x] **扩展支持**：基于 MoeHoo 的Native 可实现发包与收包

## 使用猫猫

可前往 [Release](https://github.com/NapNeko/NapCatQQ/releases/) 页面下载最新版本

**首次使用**请务必查看如下文档看使用教程

### 文档地址
[Github.IO](https://napneko.github.io/)

[Cloudflare.Worker](https://doc.napneko.icu/)

[Cloudflare.HKServer](https://napcat.napneko.icu/)

[Cloudflare.Pages](https://napneko.pages.dev/)

## 回家旅途
[QQ Group](https://qm.qq.com/q/VfjAq5HIMS)

[Telegram Link](https://t.me/+nLZEnpne-pQ1OWFl)

## 猫猫朋友
感谢 [LLOneBot](https://github.com/LLOneBot/LLOneBot)

感谢 [Lagrange](https://github.com/LagrangeDev/Lagrange.Core) 对本项目的大力支持

不过最最重要的 还是需要感谢屏幕前的你哦~

---

## 约法三章
> [!CAUTION]\
> **请不要在 QQ 官方群聊和任何影响力较大的简中互联网平台（包括但不限于: 哔哩哔哩，微博，知乎，抖音等）发布和讨论*任何*与本项目存在相关性的信息**

任何使用本仓库代码的地方，都应当严格遵守[本仓库开源许可](./LICENSE)。**此外，禁止任何项目未经授权二次分发或基于 NapCat 代码开发。**
