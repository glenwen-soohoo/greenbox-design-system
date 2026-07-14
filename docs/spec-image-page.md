# DesignSystem 形象頁延伸

> 建立日期：2026-07-13
> 類型：參考資料
> 需求 Owner：glen.wen
> 適用對象：製作無毒農品牌形象類頁面（商品 / 訂單 / 會員 / Blog / 子品牌常態頁 / 介紹頁）的人與 AI agent
> 資料來源：由方案 A（形象頁現況規範）抽出、去除已進核心的骨幹後的 delta
> 前置：本檔為 [核心規範](4-DesignSystem-核心.md) 的延伸，只列「跟核心預設不同 / 核心交給延伸決定」的確切值。骨幹（色彩、字級、護欄、無障礙、SEO）一律見核心。

---

## 定位

**無毒農品牌門面的固定長相**，風格穩定、更新頻率低。這份是一組**鎖定值**——形象頁不需要每次外掛素材，直接照這裡做即可。

做形象頁 = **[核心](4-DesignSystem-核心.md)（全 MUST）＋ 本檔鎖定值**。本檔只寫 delta，不重抄核心。

---

## 一、按鈕

### 主 CTA

| 屬性 | 值 |
|---|---|
| 背景 / 文字 | `#4ba83b` 主綠 / `#ffffff` |
| 圓角 | 4px |
| Padding | 12px 28px（高度約 48px）|
| Font weight | 500 |
| Hover | 反白（背景變白、文字變綠、加 1px 綠邊）|

### 次要按鈕（文字底線型）

透明底、文字 `#008000`、無框、1px 底線始終顯示、padding 4px 0、hover 文字 + 底線變主綠。
→ 深色背景上的次要按鈕：文字與底線改白色（hover 降到 75% 透明）。

### 子品牌按鈕

粥寶寶 `#EE8D8D` / 綠拿鐵 `#FF755A` / 等家寶寶 `#FFA3A3` / 益菓保 `#4ba83b`，文字白、hover 反白（見核心 §1.3）。

---

## 二、圓角與間距（鎖定值）

| 項目 | 形象頁值 |
|---|---|
| 圓角 | **4px**（頭像 / 圓形圖示 50%）|
| Section padding | 桌機 **64px** / 手機 32px |
| 大 Section 之間 | 96px |

→ 級距與「同頁一致」紀律見核心 §3.2。

---

## 三、容器與版型參數

### 容器策略

| 頁面類型 | 容器 |
|---|---|
| 商品列表 / 詳情 | max-width 880px 置中 |
| Blog 列表 / 文章 | max-width 720px 置中 |
| 訂單 / 結帳 / 聯絡我們 | max-width 524px 置中 |
| 會員中心 / 後台型 | 全寬（放 sidebar + 主內容）|
| 首頁 / 子品牌 Landing | 全寬，內部區塊 880px |

### 常用版型參數

| 版型 | 形象頁參數 |
|---|---|
| 列表頁（商品）| 桌機 **2 欄**、卡片 **4:5 直立**、gap 32px、篩選器頂部 chip carousel |
| 列表頁（Blog / 訂單）| 桌機 2~3 欄、gap 32px |
| 詳情頁 | 桌機**左圖右資訊 50/50**、主 CTA inline（mobile sticky bottom）|
| 表單頁 | 524px 置中、單欄（姓名/電話可雙欄）、欄位 gap 16px |
| Landing Page | Hero 84~90vh、區塊間距桌機 128~160px、Hero 內不放 CTA（核心 §二）|
| Banner | 桌機 **16:9**、mobile 1:1、圓點在圖外、autoplay 7 秒、不放左右箭頭 |
| 圖文搭配 | 桌機**左圖右文 50/50**、圖 4:3 或 16:9、中間 gap 48px、左右交替；`<figure>` + alt 必填、預設不加 figcaption |
| 圖片段落 | 單張大圖全寬 21:9、雙/三/四圖網格、gap 48px |
| 圖片按鈕組 | 桌機 3~4 卡、圖 4:3、**兩種變體皆可**（A 圖下卡片式 / B 圖內 overlay）、hover zoom 5% + 陰影、整張 `<a>` |

#### 圖文搭配 sticky 圖片

右欄內容長時，桌機 `.split-image { position: sticky; top: 80px; }`；**mobile（`< 900px`）必須改 `static`**，否則單欄堆疊時圖會疊到文字上。

---

## 四、懸浮元素（形象頁保留）

| 元素 | 規格 |
|---|---|
| 主 FAB（電話 / LINE / 回頂）| 右下角、距邊 20px、圓形 48×48px、多顆垂直排 gap 12px |
| 錨點導航 | 桌機左側 sticky（寬 200px）/ 手機頂部 sticky 橫向滾動 |
| Sticky 底部 CTA（mobile）| 底部、高 64px、白底 + 上邊陰影（詳情頁「加入購物車」）|
| 主 nav | 頂部 sticky、下捲隱藏上捲顯示 |

---

## 五、表單（框線式）

| 元素 | 值 |
|---|---|
| Input / Textarea | 高 40~48px、padding 8px 12px、**1px solid `#999` 框**、圓角 4px、focus 邊框變 `#4ba83b`、字級 16px（避免 iOS zoom）|
| Select | 同 Input、下拉箭頭用瀏覽器原生 |
| Checkbox / Radio | 16×16px、checked `#4ba83b`、1px 邊框、label 14px、間距 8px |
| Label | 14px / weight 500 / `#1a1a1a`、必填紅 `*`（`#dc4e43`）|
| 錯誤狀態 | 1px solid `#dc4e43` 框、文字 `#dc4e43` 13px、欄位下方 4px |

---

## 六、Icon

Font Awesome（既有）、大小 16/20/24/32px、繼承父層 `color`、與文字間距 8px、`vertical-align: middle`。**允許 fill icon**。不引入新 library。

---

## 七、Toast / Loading / 空狀態 / Modal

| 元素 | 形象頁值 |
|---|---|
| Toast | 右上角（距邊 20px）/ mobile 頂部全寬、桌機 320px、成功 3 秒自動消失、錯誤手動關、滑入 300ms |
| Loading | 中央 spinner（`fa-spinner`）+「載入中...」；區塊用 skeleton；按鈕 loading 文字變「處理中...」+ disabled |
| 空狀態 | icon（`fa-inbox` 等 32px `#999`）+ 主文字 16px + 輔助 14px + 動作按鈕、上下 padding 64px |
| Modal | max-width 480px 置中、圓角 4px、padding 24px、右上 X + 點遮罩可關、遮罩 `rgba(0,0,0,0.5)` |

錯誤 / 警告 / 成功 / 提示四類：純文字 + 對應色底線（`#dc4e43` / `#eb6100` / `#4ba83b` / `#999`），無背景框、無 icon。

---

## 八、動畫

形象頁**沿用既有 slider 行為，不新增動態**。若未來要加，原則：150~300ms、`ease-out`、不用 bounce / 視差、必須可被 `prefers-reduced-motion` 關閉（核心 §五）。

---

## 九、攝影 / 素材風格

極簡背景、自然光、低飽和，呼應品牌的踏實質感。商品圖去背或乾淨背景、統一色溫。

---

## 十、與活動頁的關係

形象頁與活動頁**共用核心**，差別只在本檔這些鎖定值。若某個子品牌常態頁想做得比較活潑（接近活動頁），仍**不可違反核心護欄**；要偏離形象頁鎖定值時，比照活動頁流程外掛風格參考，見 [活動頁延伸](4-DesignSystem-活動頁.md)。
