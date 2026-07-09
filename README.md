# otomura-app-2019

**音村（otomura）** — 2019年に独学で Rails を学びながら作った、音楽系マッチング SNS です。

当時のコードを **そのまま** 公開しています。リファクタリングはしていません。  
これはメンテナンス対象のプロダクトではなく、**2019年の自分へのタイムカプセル** です。

## 紹介動画

当時のデモ・紹介動画: [YouTube](https://www.youtube.com/watch?v=ah80OINmokI)

コードだけじゃ伝わらない雰囲気は、こちらでどうぞ。

---

## タイムカプセルからのメッセージ

このリポジトリには、当時の自分の全部が詰まっています。

- 初めて Rails で作り切った SNS
- 投稿・フォロー・いいね・通知・メンバー検索
- Devise + OAuth（Twitter / Facebook）
- 画像・動画アップロード（CarrierWave）
- そして伝説の **`SerchController`**（1100行超の検索ロジック）

`SerchController` は、SQL の JOIN をよくわかっていなかった頃の自分が、  
「とにゃかく Ruby で動かす」と書き殴った痕跡です。  
今見ると笑える。でも、あのとき動かしたから今がある。

コードの美しさより **「制約の中で最後まで形にした」** ことの方が、このプロジェクトの価値だと思っています。

---

## 当時のスタック

| 項目 | バージョン |
|------|-----------|
| Ruby | 2.5.0 |
| Rails | 5.2.x |
| DB | MySQL |
| 認証 | Devise + OmniAuth |
| 画像 | CarrierWave + RMagick |

マイグレーションの期間: **2019年7月 〜 2020年2月**

---

## できること（当時）

- ミュージシャン・音楽好き向けのプロフィール登録
- ジャンル・楽器・エリアでのメンバー検索
- 投稿（テキスト / 画像 / 動画）
- フォロー / いいね / コメント / 通知

---

## 起動について

**当時の環境をそのまま再現するのは、今の macOS / Ruby バージョンでは難しい可能性があります。**  
（Ruby 2.5 / Rails 5.2 は EOL）

あくまでアーカイブとして公開しています。どうしても動かしたい場合の目安:

```bash
# Ruby 2.5 + MySQL が使える環境で
bundle install
# .env に DB 接続情報と OAuth キーを設定（dotenv-rails 使用）
rails db:create db:migrate
rails s
```

`.env` に必要な変数の例:

```
DB_USER=
DB_PASS=
DB_DEVELOPMENT_NAME=
TWITTER_KEY=
TWITTER_SECRET=
FACEBOOK_ID=
FACEBOOK_SECRET_KEY=
```

`.env` はコミットしないでください。

---

## 公開にあたって

- このリポジトリは **git 履歴を新規作成した public 版** です
- 秘密情報（API キー、`.env`）は含めていません
- `TableController` は当時のデバッグ用画面です。本番では使わない想定でした

---

## 2026年の自分より

6年後、フレームワークなし PHP で Twitter クローンを1週間で書けるようになった。  
この otomura があるから、そこには至っていないと思う。

読んでくれた人が、過去のコードを笑いながらも少し応援してくれたら嬉しいです。

---

*Archived as-is. No maintenance planned.*
