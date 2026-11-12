# ai-news-data

AI Coding 资讯周报（[VirusPC/edges-brain-viruspc](https://github.com/VirusPC/edges-brain-viruspc) 的 `ai-news/`）每期原始数据存档，便于事后核对、重写和分析。

## 目录约定

```
issues/YYYY-MM-DD/          # 生成日 D，与周报文件名同日
  feeds.json                # fetch_feeds.py 精简输出（正文截 1200 字，写周报用）
  feeds-full.json           # 同一批条目的全文版（不截断，仅存档）
  llm-arena.json            # fetch_llm_arena.py 当期快照
  aa-language-models.json   # Artificial Analysis（有密钥时）
  github-trending.json      # GitHub Trending daily/all 快照（拿得到时）
  manifest.json             # 覆盖窗口、生成时间、脚本 commit、各文件来源与条数
```

- 每期一个目录，只增不改；更正放新提交并在 manifest 记录。
- 不存密钥；Artificial Analysis 只存公开字段。
- 2026-11-13 之前的各期没有留存抓取数据，不补。
