# GreenBox Design System

> 建立日期：2026-05-07
> 類型：參考資料
> 適用對象：無毒農內部 + 老闆決策

無毒農（GreenBox）Design System v1 的方案決策樣本展示頁。

線上預覽：https://glenwen-soohoo.github.io/greenbox-design-system/

---

## 內容

| 路徑 | 內容 |
|---|---|
| `index.html` | 主展示頁，列出兩方案 + 6 個展示頁面 + 方案對照表 |
| `plan-a/preview.html` | 方案 A 規範總覽（色票/字級/版型...）|
| `plan-a/sample1.html` | 方案 A 範例 1：關於無毒農（純設計）|
| `plan-a/sample1-greenbox.html` | 方案 A 範例 1：套上 greenbox.tw 官網殼 |
| `plan-a/sample2.html` | 方案 A 範例 2：關於無毒農 變化版（純設計）|
| `plan-a/sample2-greenbox.html` | 方案 A 範例 2：套上官網殼 |
| `plan-c/preview.html` | 方案 C 規範總覽 |
| `plan-c/sample1.html` | 方案 C 範例 1：關於無毒農 |
| `plan-c/sample1-greenbox.html` | 方案 C 範例 1：套上官網殼 |
| `plan-c/sample2.html` | 方案 C 範例 2 |
| `plan-c/sample2-greenbox.html` | 方案 C 範例 2：套上官網殼 |
| `docs/plan-a-spec.md` | Plan A 完整規範文件 |
| `docs/plan-c-spec.md` | Plan C 完整規範文件 |

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

### 方案 C · 文青版

主色完全沿用無毒農品牌色，但字型、版型、間距、攝影風格大改，對齊主流 AI 在「無提示」時自然會產生的設計風格。

- 主色 `#4ba83b`（不變）+ 兩個延伸色（深森林綠 / 極淺綠）
- 字型 Noto Serif TC（標題）+ Noto Sans TC（內文）
- 圓角 0px
- Section padding 112~128px
- 容器 max-width 880px

視覺感最強、品牌升級感最高。但需要組織配套大改（攝影 brief、行銷文案、客服訓練）。

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
│   └── 方案C\
└── 簡報\              <- 對老闆的決策簡報
```

這份 repo 是「對外展示」的精選版；Obsidian 是「對內」完整工作版。
