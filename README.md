# tool-emoji ➢ emoji.rec.ooo

全 emoji、點一下就複製的單頁工具。最近用過的 20 個存在瀏覽器本機（localStorage，不上雲、不跨裝置）。

## 用法

- 雙擊 `rituals/自動localhost.command` 本機預覽（port 2222），或直接用瀏覽器開 `index.html`。
- 上線：雙擊 `rituals/自動push.command`（git push → GitHub Pages）。

## 操作

- 上方 emoji 列＝分類切換；下方滿版牆點任一顆即複製，並進「最近」條。
- 左上角 ❓ 說明「為什麼」（隱私、本機儲存），不講怎麼用。
- 顯示不出的表情（該裝置字型缺字形）會用 canvas 偵測後自動隱藏，不留豆腐框。

## 結構

- 目前 `index.html` 自足（HTML＋CSS＋emoji 資料＋邏輯同檔）。
- TODO（待 rec-kit/design-modules 同步到本機後）：
  - 配色換成 `rec-kit` 通用色卡的系統色／主題色（現為暫定中性 token，集中在 `:root`，一次可換）。
  - 視需要照 `machine/specs/08-single-page-tool` 拆成 `index.html` + `styles.css` + `data.js`（emoji 資料為 SoT）+ `cyc/specs/data-model.md`。

## 部署 / DNS

- Hosting：GitHub Pages（`recdnd/tool-emoji`，Public）。`CNAME` = `emoji.rec.ooo`。
- ⚠️ DNS 要在有 `OrinthRoot/porkbread`（Porkbun API key）的機器上跑：
  `CNAME emoji → recdnd.github.io`（見 `machine/lib/rec-dns.sh` 的 `rec_dns_for_gh_pages emoji.rec.ooo`）。
  本機（sus）沒有 porkbread，所以 emoji.rec.ooo 在 DNS 做好前不會解析；期間可用 `recdnd.github.io/tool-emoji/` 測。
