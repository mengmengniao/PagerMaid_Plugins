# PagerMaid_Plugins

这个 repo 用于存储 PagerMaid-Modify 的插件。

## 如何上传插件？

欢迎加入 [讨论群](https://t.me/joinchat/FLV4ZFXq9nUFLLe0HDxfQQ) 探讨你的疑问。

> 开始编写 PagerMaid 插件前请确认 repo 没有对应功能的插件。

### pypi 包引入须知

额外不在 PagerMaid-Modify `requirements.txt` 下的包，请通过 `try` 来进行引入，在用户运行命令时判断包是否引入，如未引入则编辑消息提醒用户安装相应的 pypi 包。

代码参照：https://github.com/xtaodada/PagerMaid_Plugins/blob/master/sendat.py

### 调试

使用 `-apt install` 回复你的插件即可进行本地安装，请在本地测试基本无报错后进行下一步。

### 添加文件

您可以使用的文件目录为：
 - `/` 根目录放置 插件的 python 源文件
 - `/插件名/` 子目录放置 插件的资源文件（可选）

### 添加插件到库

您需要参照 `list.json` 的相关格式，在 `list` (`object`) 下 创建一个 `list`

下面是对应参数的介绍：
 - `name` : 插件名
 - `version` : 版本号
 - `section` : 分类
 - `maintainer` : 作者
 - `size` : 插件大小
 - `supported` : 插件是否允许 issue
 - `des-short` : 短介绍（用于 `-apt search`）
 - `des` : 详细介绍（用于 `-apt show`）

## Plugins 文件结构介绍

- 插件名
    - `*.*` : 插件对应的资源文件
- `插件名.py` : 插件源文件
- `version.json` : 通过 `-apt install` 命令安装的插件版本记录文件

## 目前已有的插件

- chat （聊天类）
    - `autorespond` : 自动回复。
    - `dme` : 反 TG desktop 防撤回插件。
    - `autorm` : 在指定的时间后删除自己的消息。
    - `sendat` : 定时发送消息。
    - `atadmins_atall` : 一键 AT 本群管理员、群员。
    - `denyu` : 在某群中强制禁言某用户。
    - `nthmsg` : 获取你发送的第 n 条消息。
    - `portball` : 回复你要临时禁言的人的消息来实现XX秒的禁言。
- profile （资料类）
    - `autochangename` : 自动更新 last_name 为时间等。
    - `throwit` : 生成一张 扔头像 图片。
- daily （便民类）
    - `weather` : 查询天气。
    - `xtao-some` : 一大堆便民功能。
    - `yb-dl` : 上传 Youtube、Bilibili 视频到 telegram。
    - `rate` : 汇率转换。
    - `netease` : 网易云热评。
    - `hyperlink` : 生成隐藏链接。
    - `whois` : 查询域名信息
    - `resou` : 知乎，抖音，微博实时热搜

