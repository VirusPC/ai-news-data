# ai-news-data

AI Coding 资讯周报（[VirusPC/edges-brain-viruspc](https://github.com/VirusPC/edges-brain-viruspc) 的 `ai-news/`）每期原始数据存档，便于事后核对、重写和分析。

## 目录约定

```
issues/YYYY-MM-DD/          # 生成日 D，与周报文件名同日
  feeds.json                # fetch_feeds.py --out 全文，不截断
  feeds.index.json          # 选文索引：标题、链接、来源、thin、开头约 400 字
  llm-arena.json            # fetch_llm_arena.py 当期快照
  aa-language-models.json   # Artificial Analysis（有密钥时）
  github-trending.json      # 从 feeds.json 抽出的 daily/all 全文；数组顺序不是榜上名次
  openrouter-rankings-daily.json       # OpenRouter 日用量（含上一周，CC BY 4.0）
  openrouter-rankings-programming.json # 编程分类，按周抽样
  openrouter-app-rankings.json         # 应用排行（周报正文用）
  openrouter-app-rankings-coding.json  # 编程类应用排行旁路快照
  manifest.json             # 覆盖窗口、生成时间、脚本 commit、各文件来源与条数
```

- `feeds.json` 只存 feed 给出的正文。不足 280 字记为 `thin`，不另开文章页补全文。
- 每期一个目录，只增不改；更正放新提交并在 manifest 记录。
- 不存密钥；Artificial Analysis 只存公开字段。OpenRouter 快照是 Data API 导出（CC BY 4.0），同样不落密钥。
- 2026-11-13 之前的各期没有留存抓取数据，不补。
