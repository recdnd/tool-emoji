# journal - tool-emoji

## 2026-10-08 起站（sus 機）
- 主筆：做一個超簡單 emoji 工具，全 emoji 點擊即複製，本機存最近 20 個；完成推 emoji.rec.ooo。
- 做法：單頁靜態工具，10 類分頁（Unicode 官方分組），canvas 偵測濾掉該裝置顯示不出的表情，`Intl.Segmenter` 正確切合體 emoji。最近 20 存 localStorage（`emoji-recent-v1`）。
- 契約：照前端契約介面八條重寫（無標題塊／無旁白／`border:0`／按鈕無框用 emoji／❓放為什麼／無陰影漸進動畫／hover）。
- ⚠️ rec-kit/design-modules 本機不在 → 配色用暫定中性 token，主筆說「一會再做」；待同步後對齊通用色卡。
- 部署：GitHub Pages，`recdnd/tool-emoji` Public，CNAME emoji.rec.ooo。DNS 本機無 porkbread，待他機跑。
