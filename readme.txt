# 📊 Day 3：Steam 遊戲資料分析專案

本專案以 Steam 平台公開遊戲資料為分析對象，透過資料前處理、分類統計、數值分布與推薦排序，進行完整的探索性資料分析（EDA）。

---

## 📁 資料來源

- 資料檔案：`games.csv`
- 欄位包含：遊戲名稱、價格、好評率、評論數、支援平台、發行日期等

---

## 🔍 今日任務與成果（2025-05-23）

| 任務 | 技能 | 圖表/成果 |
|------|------|------------|
| A. 了解資料型態 | `.info()` / `.describe()` | 確認欄位與缺值 |
| B. 平台支援分析 | `.sum()` + `barplot()` | Windows / Mac / Linux 支援比例 |
| C. 免費 vs 收費分析 | `.value_counts()` + `pie()` + `histplot()` | 免費佔比、價格分布圖 |
| D. 評論與好評率關係 | `regplot()` + `.corr()` | 散佈圖與相關係數 |
| E. 發行年份趨勢 | `datetime` + `groupby()` | 發行數量年線圖 |
| F. 推薦系統雛型 | 多條件過濾 + 排序 | 高評價 + 低價 + 熱門 遊戲排行榜 |

---

## 🏆 精選排行榜展示

```python
print(top_games[['title', 'price_final', 'positive_ratio', 'user_reviews']])
```

---

## 📘 延伸建議

- 加入更多欄位如 genre / platform 做推薦
- 整合 tag 標籤轉換為 one-hot 後用 cosine similarity 比對相似遊戲
- 建立 Web UI 推薦器（例如用 Streamlit）