# 龍涎香ドリフト OGP画像 制作プロンプト（他AI用）

Webゲーム「龍涎香ドリフト」のOGP（SNSシェア画像）を作るためのプロンプト集。
**仕様：1200×630px・横長・PNG。** SNS（X/Facebook/LINE/Slack等）でリンクを貼ったときに表示されるカード画像。

---

## 背景情報（どのAIにも共有する前提）

- **ブランド**：Ambergris Japan（龍涎香＝アンバーグリスの天然香料・天然香水。高級・静謐・海・スピリチュアルウェルネス）
- **ゲーム**：海を漂う一粒の龍涎香を操り、月光・海藻・塩などを吸い込んで育て、汚染を避け、浜へ漂着させると「あなただけの香り」が生まれるローグライト。
- **世界観のキーワード**：深い海、漂流、熟成、月光、生物発光、光のシャフト、静けさ、神秘、上質。
- **龍涎香の見た目**：象牙色〜飴色の、真珠／琥珀のような艶のある塊（年輪状の層がうっすら）。決して魚やキャラクターにしない。

---

## A. 画像生成AI向けプロンプト（Midjourney / DALL·E / Ideogram 等）

> ⚠️ 日本語の文字は画像生成AIだと崩れやすい。**文字なしの背景アート**として生成し、文字は後から重ねるのが安全。Ideogramなど文字に強いものだけ英字を試す。

**英語プロンプト（背景アート用・文字なし）：**
```
A luxury fragrance-brand key visual, 1200x630 landscape banner. A single luminous pearl-like sphere of ambergris (ivory to warm amber, soft pearlescent sheen, faint concentric growth rings, gentle specular highlight) glowing on the left third, surrounded by a soft golden halo. Deep ink-navy underwater background fading to near-black, subtle volumetric light shafts from above, sparse drifting marine-snow particles, faint bioluminescent specks. Calm, mysterious, editorial, premium, minimal, lots of negative space on the right for text. Cinematic soft lighting, fine grain, elegant, restrained color palette of deep navy and antique gold. No text, no characters, no fish, no whale photo. --ar 1200:630 --style raw
```

**日本語で渡す場合の指示文：**
```
香水ブランドの広告ビジュアル（1200×630の横長バナー）。
左3分の1に、象牙色〜飴色の真珠／琥珀のように艶めく龍涎香の球体を、淡い金色のハローと共に発光させる。
背景は深い藍色〜ほぼ黒の海中で、上から差す淡い光のシャフト、まばらに漂うマリンスノー、微かな生物発光。
静謐・神秘的・上質・ミニマル。右側は文字を載せるため大きく余白を空ける。
色は深い藍と金（アンティークゴールド）に抑える。文字・キャラ・魚・クジラ写真は入れない。
```

**重ねる文字（後工程・明朝体推奨）：**
- 見出し（小・金・字間広め）：`AMBERGRIS JAPAN`
- タイトル（大・明朝・白）：`龍涎香ドリフト`
- タグライン：`海を漂い、育ち、香りになる。`
- 小見出し：`月光や海藻を吸って育て、あなただけの龍涎香を浜へ。`
- 下部（小・金）：`RYUZENKO DRIFT`

---

## B. コード/SVGで作るAI向けブリーフ

```
1200×630のOGP画像をSVG（またはCanvas）で作って。テーマ＝香水ブランドのエディトリアル広告。
構図：左に龍涎香（象牙→飴色のradial gradient球体＋金のリム＋淡い年輪＋左上にスペキュラハイライト＋外側に金のハロー）。
背景：藍→黒の縦グラデ、淡い光のシャフト2本、まばらなマリンスノーの点。
右側にテキスト階層（明朝体）：
  ・小さな金の英字見出し AMBERGRIS JAPAN ＋細い金の区切り線
  ・大きな白のタイトル 龍涎香ドリフト
  ・タグライン 海を漂い、育ち、香りになる。
  ・小さめの補足 月光や海藻を吸って育て、あなただけの龍涎香を浜へ。
  ・下部に小さな金の英字 RYUZENKO DRIFT
全体に細い金のヘアライン枠。余白を多めに、上品でミニマルに。
制約：テキストは枠内に必ず収め、見切れさせない。色は深い藍＋アンティークゴールド＋象牙に限定。
納品：1200×630 PNG（文字が小サイズでも読めること）。
```

---

## 評価の観点（出てきた候補を選ぶとき）
1. 高級感・静謐さ（香水ブランドとして恥ずかしくないか）
2. 龍涎香が「真珠／琥珀の塊」に見えるか（魚・キャラに見えない）
3. タイトルが読めて見切れていないか
4. 小さいサムネイルでも何の画像か伝わるか
5. ブランド色（深い藍＋金＋象牙）に収まっているか

参考：現行版は同フォルダの `ogp.svg` / `ogp.png`。
