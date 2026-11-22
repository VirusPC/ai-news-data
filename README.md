# ai-news-data

AI Coding 资讯周报（[VirusPC/edges-brain-viruspc](https://github.com/VirusPC/edges-brain-viruspc) 的 `ai-news/`）每期原始数据存档，便于事后核对、重写和分析。

## 目录约定

一期是 `issues/YYYY-MM-DD/`，下面只有 `raw/`、`cleaned/`、`summary/`。契约和校验在 brain 仓 `skills/managed/weekly-ai-blogs-digest`。缺的文件写在对应阶段的 `gaps.json`，不留空文件。

```
issues/YYYY-MM-DD/
  raw/          # 抓取原文：window、articles、projects、models
  cleaned/      # 去重后的文章、项目、模型，一条一个文件
  summary/      # 页面数据：index.json、关键词、三路卡片和榜单绘图数据
```

- 2026-10-23、2026-10-30、2026-11-06、2026-11-13、2026-11-20 已从原来的平铺 JSON 和已发布正文转成这个结构。正文没有重写。转不出来的记在 `gaps.json`。原来的根目录文件和 `manifest.json` 已从树上删掉，Git 历史里还在。
- 不存密钥。OpenRouter 快照仍是 Data API 导出（CC BY 4.0）。
- 2026-10-23、2026-10-30、2026-11-06 当时补不回的榜、价格和速度仍在 `raw/gaps.json`，不拿后来的数字充数。
