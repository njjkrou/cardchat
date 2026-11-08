<div align="center">

# 🌸 CardChat（蔵春閣）

**タバーン・エコシステム全体に対応した AI キャラクターチャット基盤**

[中文](README.md) · [English](README.en.md) · [日本語](README.ja.md)

デモ → **https://ccg.officechat.com.cn**

</div>

---

<p align="center">
  <img src="docs/images/chat.jpg" alt="チャット" width="49%">
  <img src="docs/images/discover.jpg" alt="発見" width="49%">
</p>

CardChat は、キャラクターカード・ワールドブック・プリセット・長期記憶・グループチャット・画像生成・
サブスクリプション・管理画面を備えた、そのまま運営できる AI キャラクターチャット基盤です。
チャットだけではありません。SillyTavern 的なエコシステムを Web に丸ごと持ち込み、しかも手間を減らしました。

---

## 1. タバーン・エコシステムに完全対応

**SillyTavern カード（v1 / v2）**、**Chub.ai**、**JanitorAI** 形式に対応。PNG も JSON もそのまま取り込め、
設定・第一声・会話例・埋め込みワールドブックが保持されます。

<p align="center">
  <img src="docs/images/characters.jpg" alt="キャラ管理" width="72%">
</p>

**カードはそのまま読めて、そのまま編集できます。** 形式変換も再入力も不要。開いて設定・第一声・
アバター・タグを変更するだけです。

<p align="center">
  <img src="docs/images/character.jpg" alt="キャラ詳細" width="72%">
</p>

## 2. ワンクリックでキャラクター生成

設定を書くのが面倒なときは、一言でキャラを説明するだけ。名前・紹介・性格・第一声・タグを AI が埋めます。
スタイル（恋愛 / ファンタジー / 学園 / 仕事 / ミステリー / 癒し…）を選び、後から調整もできます。

<p align="center">
  <img src="docs/images/create.jpg" alt="ワンクリック生成" width="72%">
</p>

## 3. 個人チャットとグループチャット

**個人チャット**：ストリーミング返信、複数分岐（スワイプ）、再生成、編集して再送、引用返信、エクスポート。

<p align="center">
  <img src="docs/images/chat.jpg" alt="個人チャット" width="72%">
</p>

**グループチャット**：1 つの会話に複数キャラを置き、`@` で話者を指定するとそのキャラだけが返信します。
キャラ同士の絡みもあり、群像劇は個人チャットでは出せません。

<p align="center">
  <img src="docs/images/chat-group.jpg" alt="グループチャット" width="72%">
</p>

## 4. 画像アップロードと Web 検索

- 画像を送信でき、マルチモーダルモデルが内容を理解します
- リアルタイム情報が必要なときは Web 検索結果を文脈に統合
- 画像 / 動画生成は接続済みで、**現在テスト中**

## 5. 破限（ジェイルブレイク）ファイルの一括インポート

これまで手作業でプロンプトを組み、パラメータを調整していた破限も、SillyTavern のプリセット JSON を
読み込むだけ。項目ごとに分割され、個別にオン・オフでき、会話ごとに紐付けられます。

<p align="center">
  <img src="docs/images/presets.jpg" alt="プリセット" width="72%">
</p>

プリセットでは **Temperature、Top P、Top K、Min P、Frequency / Presence / Repetition Penalty** などを直接調整でき、
**モデルパラメータは完全に自由**。コードを触る必要はありません。

## 6. ワールドブック

全体・キャラ内蔵・会話単位の三層構造。SillyTavern のワールドブックを取り込み、項目を手で編集し、
キーワードで発動できます。

<p align="center">
  <img src="docs/images/worldbook.jpg" alt="ワールドブック" width="72%">
</p>

## 7. ユーザーペルソナと設定

誰でも自分のペルソナを持てます：アバター、ニックネーム、性格、紹介。いつでも切り替え可能で、
キャラは「ユーザー」ではなくあなたのペルソナに向けて話します。

<p align="center">
  <img src="docs/images/profile.jpg" alt="マイページ" width="49%">
  <img src="docs/images/settings.jpg" alt="設定" width="49%">
</p>

設定では**プラットフォーム API**（公式価格でコイン消費）か、**自分の API キー**（コイン消費なし）を選択でき、
接続先 URL とモデルも指定できます。

## 8. 報酬システム

- **デイリーチェックイン** — 1 日 1 回、固定コイン
- **創作報酬** — カード公開で獲得、いいね・ダウンロードでも追加報酬
- **招待** — 招待コード登録で双方に報酬
- **初回チャージ特典 / サブスクプラン** — チャージと会員の 2 経路

<p align="center">
  <img src="docs/images/subscription.jpg" alt="サブスク" width="72%">
</p>

---

## その他の機能

| 機能 | 説明 |
|---|---|
| 発見とレコメンド | タグを選んでカードをスワイプ。いいね／スキップで精度が上がる |
| 長期記憶 | 階層圧縮＋事実抽出＋ハイブリッド検索。数十ターン後も覚えている |
| 自動メッセージ | キャラが一定間隔で自分から連絡してくる |
| ランキング | 作品数・いいね・利用数でクリエイターをランキング |
| 通知 | いいね、コメント、審査結果、お知らせ |
| 正規表現 | 表示層の置換で AI っぽさを除去、書式を整える |
| エクスポート | テキスト／JSON |
| フォロー | 作者の新作を追える |
| 多言語 | 中文・English・日本語・한국어・Français・Español（メインメニューから切替） |
| ログイン | ID／パスワード、または Discord クイックログイン（登録停止中でも利用可） |
| 登録コンプライアンス | 18歳以上・成人向けコンテンツ同意が必須。中国本土からの登録は非対応 |
| モバイル | レスポンシブ対応、スマホブラウザでそのまま |

<p align="center">
  <img src="docs/images/discover-prefs.jpg" alt="タグ選択" width="24%">
  <img src="docs/images/discover-tags.jpg" alt="タグ選択済み" width="24%">
  <img src="docs/images/leaderboard.jpg" alt="ランキング" width="24%">
  <img src="docs/images/notifications.jpg" alt="通知" width="24%">
</p>

<p align="center">
  <img src="docs/images/chat-mobile.jpg" alt="モバイルチャット" width="26%">
  <img src="docs/images/discover-mobile.jpg" alt="モバイル発見" width="26%">
  <img src="docs/images/auto.jpg" alt="自動メッセージ" width="26%">
</p>

---

## 管理画面

運営のすべてをここで行います：審査、凍結、残高調整、注文確認、価格変更、お知らせ配信、モデル設定。

<p align="center">
  <img src="docs/images/admin-dashboard.jpg" alt="ダッシュボード" width="72%">
</p>

<p align="center">
  <img src="docs/images/admin-users.jpg" alt="ユーザー管理" width="49%">
  <img src="docs/images/admin-characters.jpg" alt="カード審査" width="49%">
</p>

<p align="center">
  <img src="docs/images/admin-orders.jpg" alt="注文管理" width="49%">
  <img src="docs/images/admin-ledger.jpg" alt="コイン履歴" width="49%">
</p>

<p align="center">
  <img src="docs/images/admin-platform.jpg" alt="プラットフォーム設定" width="72%">
</p>

<p align="center">
  <img src="docs/images/admin-subscriptions.jpg" alt="サブスクプラン" width="49%">
  <img src="docs/images/admin-comments.jpg" alt="コメント審査" width="49%">
</p>

---

## アーキテクチャ

<p align="center">
  <img src="docs/architecture.svg" alt="アーキテクチャ" width="100%">
</p>

| レイヤー | 採用技術 |
|---|---|
| フロントエンド | Vue 3 · TypeScript · Vite · SSE ストリーミング |
| バックエンド | Node.js（22/24）· Express · TypeScript |
| データベース | SQLite（WAL）· FTS5 全文検索 |
| モデル接続 | OpenAI 互換ゲートウェイ、ストリーミング／非ストリーミング自動フォールバック |
| デプロイ | Docker Compose · Nginx リバースプロキシ |

### 長期記憶の仕組み

会話が長いほどコンテキストは高コストになります。記憶を層に分け、固定トークン予算で最大限に記憶します。

| 層 | 役割 | コスト |
|---|---|---|
| **L1 作業記憶** | 予算に合わせて直近の原文を切り出す | 毎ターン固定 |
| **L2 区間要約** | 30 件または 6,000 字ごとに要約、以後再計算しない | 区間ごとに 1 回 |
| **L3 事実カード** | 身元／好み／関係／出来事を抽出し重複統合 | L2 と同時 |
| **検索注入** | 現在の入力で検索し、ヒット時のみ注入 | 毎ターン 1 クエリ |

実測：実際の長い会話で **prompt トークン約 35% 削減**、ウィンドウ外の事実も正しく想起。

---

## 構成

```
.
├── README.md                 # 中国語（既定）
├── README.en.md              # English
├── README.ja.md              # 日本語
├── docs/
│   ├── architecture.svg
│   └── images/
├── web/                      # フロントエンド（静的配信可能）
└── LICENSE
```

`web/` は SPA のビルド成果物です。Nginx では未知パスを `index.html` にフォールバックしてください
（`try_files $uri /index.html`）。

---

## ライセンス

**All Rights Reserved（無断転載・商用利用禁止）**。詳細は [LICENSE](LICENSE)。

<div align="center">
<sub>Made with 🌸</sub>
</div>
