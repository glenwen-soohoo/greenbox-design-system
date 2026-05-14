# GreenBox Design System

> 建立日期：2026-05-07
> 最後更新：2026-05-14
> 類型：參考資料
> 適用對象：無毒農內部 + 老闆決策

無毒農（GreenBox）Design System v1 的方案決策樣本展示頁。

線上預覽：https://glenwen-soohoo.github.io/greenbox-design-system/

---

## 內容

| 路徑 | 內容 |
|---|---|
| `index.html` | 主展示頁，列出兩方案 + 6 個展示頁面 |
| `plan-a/preview.html` | 方案 A 規範總覽（色票/字級/版型...）|
| `plan-a/sample1.html` | 方案 A 範例 1：關於無毒農（套上官網殼） |
| `plan-a/sample2.html` | 方案 A 範例 2：關於無毒農 變化版（套上官網殼） |
| `plan-d/preview.html` | 方案 D 規範總覽 |
| `plan-d/sample1.html` | 方案 D 範例 1：關於無毒農（套上官網殼） |
| `plan-d/sample2.html` | 方案 D 範例 2：關於無毒農（套上官網殼） |
| `tools/font-weight.html` | 字體測試工具（設計可自行調字級／字重）|
| `docs/plan-a-spec.md` | Plan A 完整規範文件 |
| `docs/plan-d-spec.md` | Plan D 完整規範文件 |

---

## 兩個方案

### 方案 A · 踏實版

把現有官網「不動的頁面」（商品 / 訂單 / 子品牌 / Blog）的視覺規則整理成一份規則書。

- 主色 `#4ba83b`（不變）
- 字型 Noto Sans TC
- 圓角 4px
- Section padding 64px
- 容器 max-width 1140px

最低風險、最快上線。AI 改版時可以從這份規則開始疊加。

### 方案 D · 精煉版

主色完全沿用無毒農品牌色，字型統一 Noto Sans TC、字重整體偏細，視覺克制、不誤導點擊。

- 主色 `#4ba83b`（不變）+ 極淺綠延伸色
- 字型 Noto Sans TC（中文唯一字型）
- 字級 39 / 30 / 24 / 19 / 16 / 14 / 13
- 字重 h1=500 / h2-h4=400 / body=300
- 圓角 0px
- Section padding 112~128px
- 容器 max-width 880px / 同區塊內對齊一致

整體比 A 更克制：Hero 不放 CTA、標題不做按鈕樣、無連結卡片不加 hover、避免空洞金句與 Statement Section。

---

## GitHub Pages 部署

倉庫已啟用 GitHub Pages。Push 到 `main` 分支後，幾分鐘內可在以下網址看到：

https://glenwen-soohoo.github.io/greenbox-design-system/

如果還沒啟用，到 GitHub repo → Settings → Pages → Source 選 `Deploy from a branch` → Branch `main` / `/ (root)`。

---

## 在地預覽

```bash
cd greenbox-design-system
python -m http.server 8000
# 瀏覽器開 http://localhost:8000
```

或直接雙擊 `index.html`（greenbox 殼版本是自包含的，圖片 base64 內嵌、可離線開）。

---

## 內部規範文件

跟這份 repo 並行的完整規範文件在 Obsidian：

```
D:\Obsidian\projects\Gb-Design System\
├── 製作規劃\          <- 三方案策略、簡報結構、執行清單
├── Design System\
│   ├── 方案A\         <- 規範文件 + 預覽 + 範例 HTML
│   ├── 方案D\         <- 規範文件 + 預覽 + 範例 HTML
│   ├── 留存\          <- 已淘汰的方案 C 等
│   └── 整合到 fruit_web 的踩雷筆記.md
└── 簡報\              <- 對老闆的決策簡報
```

這份 repo 是「對外展示」的精選版；Obsidian 是「對內」完整工作版。
