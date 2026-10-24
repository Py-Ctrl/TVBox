# TVBox / 影视仓 资源线路合集

<h3 align="center">精心收集的优质线路，由网页后台维护，改动自动提交到本仓库</h3>

## 订阅地址

| 应用 | 地址 | 说明 |
|---|---|---|
| TVBox | https://tvbox.zpd.dpdns.org/tvbox | 完整配置（sites / lives / parses）。TVBox 不支持单仓/多仓，只能直接吃整份配置 |
| 影视仓 | https://tvbox.zpd.dpdns.org/ysc | 线路清单 `{"urls":[...]}`。影视仓支持单仓/多仓，读这份列表 |

根路径 `https://tvbox.zpd.dpdns.org/` 等同 `/tvbox`。

## 使用说明

1. 复制上表对应地址
2. 在 TVBox / 影视仓的配置地址栏粘贴
3. 点「确定」等待加载

## 管理后台

https://tvbox.zpd.dpdns.org/admin

- 线路增删改，支持批量添加、批量修改、批量删除
- 按住最左侧 ⠿ 手柄拖拽排序（只在清单内生效）
- 「手动提交 Commit」草稿模式：改动先累积，点「提交」一次性写入，可自定义 commit 说明
- 一键检测：本机 + 服务器双通道，HTTP 200 记为可用；3xx 会显示跳转目标与最终状态
- 「不支持单/多仓专用」Tab：抓取所有线路并合并生成完整配置

后台密码由 Cloudflare Worker 的 `PASSWORD` 环境变量控制。

## 仓库文件

| 文件 | 内容 | 谁在用 |
|---|---|---|
| `tvbox.json` | 线路清单 `{"urls":[{name,url}]}` | 影视仓（`/ysc`） |
| `ysc.json` | 合并后的完整配置 `{spider,sites,lives,parses,flags}` | TVBox（`/tvbox`），由后台生成 |

## 更新维护

- 后台改完即提交，客户端约 1 分钟后拉到新配置
- 定期用「全部检测」清理失效线路
- 线路有增删后，到「不支持单/多仓专用」Tab 点一次「重建完整配置」

## 免责声明

本仓库仅收集公开可用资源，不保证所有线路的可用性和内容合法性。使用请遵守当地法律法规。
