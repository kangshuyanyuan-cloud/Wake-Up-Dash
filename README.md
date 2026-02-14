# 🌅 Wake Up Dash - Minimalist

「物理的に動く」を強制する、**二度寝防止QRコードアラーム Webアプリケーション**です。
GoogleのAI開発環境「Antigravity」を活用し、アイデア出しと実装を並行して行う「アジャイル・ハック」により、**約8時間**で完遂したプロトタイプです。

## 🚀 Live Demo
[https://lucent-seahorse-7af703.netlify.app/](https://lucent-seahorse-7af703.netlify.app/)
*(スマホで開き「ホーム画面に追加」することでアプリとして動作します)*

## 🛠 開発の動機 (Motivation)
これまでの目覚まし時計やアラームアプリには、以下の**「起床プロセスにおける構造的な欠陥」**がありました。

1.  **停止の容易さ (Unconscious Stopping)**: 
    枕元でタップするだけで止まるため、無意識のうちに二度寝してしまう。
2.  **覚醒後の行動遅延 (Lazing Around)**: 
    目は覚めていても、「あと5分だけ…」と布団の中でSNSや動画を見続けてしまい、結果として活動開始時間が大幅に遅れる。
3.  **物理的強制力の欠如**: 
    「起きる意思」のみに依存しており、ベッドから強制的に離脱させる仕組みが存在しなかった。

これらの課題を解決するため、**「寝室から離れた場所へ移動しないと止まらない」**仕組みと、**「ゲーム要素（スコア・継続記録）」**を組み合わせたアプリを開発しました。

## ✨ 主な機能 (Features)

### 🏃‍♂️ 1. QRコード強制解除 (Physical Action)
- **ロジック**: 事前に設定したQRコードを洗面所やリビングに設置。設定時刻から5分以内にそれをスキャンしない限り、起床完了とみなされません。
- **UX**: 「布団から出る」という最もハードルの高い行動をシステム側で強制し、ダラダラ過ごす時間を物理的にカットします。

### 🎮 2. ランク評価・ポイントシステム (Gamification)
- 起床までのスピード（0〜30秒、〜5分）に応じて、Sランク・Aランクといった評価とポイント（PT）を付与。
- 「ただ起きる」作業を、「高スコアを狙う」ゲーム体験に変換しました。

### 🔥 3. Streak（継続日数）の可視化
- 連続成功日数をトップ画面に大きく表示し、「記録を途切れさせたくない」という心理を利用して継続を促します。
- 貯めたポイントで「休日チケット」を購入できる救済措置も実装。

### 📱 4. PWA (Progressive Web App) 対応
- **ネイティブアプリ体験**: インストール不要でホーム画面に追加でき、全画面表示で起動します。
- **オフライン動作**: Service Workerを実装し、通信環境が不安定な朝でも確実に動作します。

## 💻 技術スタック (Tech Stack)

本プロジェクトは**AI駆動開発 (AI-Driven Development)** の実践として、コード記述の大部分を生成AIで効率化しています。
「何を作るか（要件定義）」と「どう動くべきか（体験設計）」を並行して行い、爆速でのプロトタイプ開発を実現しました。

- **Development Tool**: Google Antigravity (AI-Integrated IDE)
- **Frontend**: HTML5, Vanilla JavaScript, Tailwind CSS (CDN)
- **Libraries**:
    - `zxing-js/library`: QR Code Reader
    - `qrious`: QR Code Generator
- **PWA**: Service Worker, Web Manifest
- **Deployment**: Netlify

## 📅 開発期間 (Timeline)
**2026/02/14 - 2026/02/15 (Overnight Agile Hack)**
- **総開発時間**: 約8時間
- **プロセス**: アイデア出し・実装・UI調整(並行作業 7h) -> PWA化・デプロイ(1h)

## 🔮 Future Roadmap (今後の展望)
現在はオフライン版のプロトタイプですが、今後は以下の機能拡張を予定しています。

* **☁️ サーバーサイド連携 & フレンド機能**
    * Firebase等を導入し、Streakやスコアをクラウドで管理。
    * 友人同士で起床記録を競い合うランキング機能の実装。
* **⏰ ネイティブアラーム機能の統合**
    * 現在は別途アラーム設定が必要ですが、アプリ内完結でアラーム音を制御する機能の実装。
* **🔔 ソーシャル通知 (Wake-up Call)**
    * 寝坊している友人に「起こす」通知を送れる機能。

## 👤 Author
**Kouki Iwamoto**
Information & Electrical Engineering Student / Kumamoto Univ.
- Focus: AI-Driven Development, Product Management (PdM)
- Status: **Looking for Summer Internship (2028 Grad)**
