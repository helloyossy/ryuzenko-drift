# 龍涎香ドリフト（Ryuzenko Drift）

龍涎香4部作の**第二弾「海を漂って育つ」**。海をさまよう龍涎香を操り、月光・海藻・塩などを吸い込んで育ち、汚染を避けて漂着するローグライト。単一HTML・外部依存ゼロ（`index.html` をブラウザで開くだけ。音も鳴る／進行は localStorage 保存）。

- 仕様書（正本）：Obsidian `02_仕事/企画/龍涎香ドリフト_ゲーム仕様_v0.2_ローグライト漂流_2026-06-16.md`
- 確認用URL（GitHub Pages・push後に有効）：**https://helloyossy.github.io/ryuzenko-drift/**

## 遊ぶ
`index.html` をダブルクリック。または上の確認用URL。

## 開発メモ
- 全部 `index.html` に収まっている（HTML/CSS/Canvas/WebAudio）。
- 現行 v0.4：高級感（ベル音＋リバーブ＋ペンタトニック＋明朝体＋金の差し色）、メタ進行（熟成エキスで永続強化）、香り図鑑、6海域、シェア画像生成。

## 公開手順（よっしー実行・このAIシェルはネット遮断のため）

### A. gh CLI が入っているなら一発
```sh
cd ~/Documents/ryuzenko-drift
gh repo create helloyossy/ryuzenko-drift --public --source=. --push
gh api -X POST repos/helloyossy/ryuzenko-drift/pages -f "source[branch]=main" -f "source[path]=/"
```

### B. 手動
1. GitHub で空のリポジトリ `ryuzenko-drift`（Public）を作成
2. push（remote は設定済み）：
   ```sh
   cd ~/Documents/ryuzenko-drift
   git push -u origin main
   ```
3. GitHub → Settings → Pages → Source: **Deploy from a branch** → Branch: **main** / **/(root)** → Save
4. 数分後に **https://helloyossy.github.io/ryuzenko-drift/** が有効化

以降は `git add -A && git commit -m "..." && git push` で更新→自動再公開。
別PCでは `git clone https://github.com/helloyossy/ryuzenko-drift.git` で続きができる。
