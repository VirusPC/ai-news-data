# ai-news-data

AI Coding 资讯周报（[VirusPC/edges-brain-viruspc](https://github.com/VirusPC/edges-brain-viruspc) 的 `ai-news/`）每期原始数据存档，便于事后核对、重写和分析。

## 目录约定

```
issues/YYYY-MM-DD/
  feeds.json
  feeds.index.json
  github-trending.json
  aa-language-models.json
  llm-arena-<榜单发布日>.json
  openrouter-rankings-daily.json
  openrouter-rankings-programming.json
  openrouter-app-rankings.json
  openrouter-app-rankings-coding.json
  openrouter-official-endpoints.json
  model-releases.json
  keywords.json
  manifest.json
  user-backfill.json          # 仅当用户给了补录清单
  products/                   # 新跑才写；现有期次没有，本次不回填
    selection.json
    summaries.json
    boards.json
    page.json
```

- 已有的原文、索引、trending、榜单、端点、model-releases、keywords、manifest 仍放在期次目录根上，不搬进 products/，也不在 products/ 里再复制一份。
- products/ 只放后续节点的表：选文 selection.json、总结 summaries.json、榜图说明 boards.json、最终页面 page.json。每张表记录上游文件的路径和 sha256，以及规则的 commit 与路径。字段以脑仓 `skills/managed/weekly-ai-blogs-digest/references/产物.md` 为准。
- 现有期次没有 products/。本次不生成、不从旧周报反推。
- user-backfill.json 只在用户给了补录时出现，不进 feeds、索引和 keywords。
- `feeds.json` 只存 feed 给出的正文。不足 280 字记为 `thin`，不另开文章页补全文。
- 每期一个目录，只增不改；更正放新提交并在 manifest 记录。
- 不存密钥；Artificial Analysis 只存公开字段。OpenRouter 快照是 Data API 导出（CC BY 4.0），同样不落密钥。
- 2026-10-23、2026-10-30、2026-11-06 是 2026-11-22 按现行订阅回补的快照。当时的榜、价格和速度补不回来的，写在各期 manifest，不拿抓取日的数字充数。再早的期次仍然没有原始抓取。
