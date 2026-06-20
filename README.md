# HelloWorldLP

[**研究室 在室・勤怠・日誌管理システム（LabBoard）**](https://github.com/akakirishima/HelloWorld) のランディングページです。

`https://hack.nikkei.com/` のエディトリアルなデザインを参考に、白基調・1px ヘアライン区切り・英ラベル＋日本語見出し・二言語フォント分割で構成しています。プロダクトの中心である「在室ボード」を、グロッシーなスクリーンショットではなくヘアライン罫のエディトリアルな表として表現しているのが特徴です。

## 公開URL

GitHub Pages で公開しています。

- **https://akakirishima.github.io/HelloWorldLP/**

## 構成

ビルド不要の静的サイトです。

| ファイル | 役割 |
| --- | --- |
| `index.html` | ページ本体（セマンティックHTML） |
| `styles.css` | デザインシステム（トークン・レイアウト・モーション） |
| `script.js` | スクロールリビール・モバイルナビ・ライブ時計（`prefers-reduced-motion` 対応） |

## ローカルで確認する

```sh
# 任意の静的サーバーで開くだけ
python3 -m http.server 8080
# → http://localhost:8080
```

## デザイン

- フォント: Noto Sans JP（日本語）/ Roboto（英ラベル）/ JetBrains Mono（数値・時刻・ポート等の「計器」表現）
- アクセント: スレートブルー `#14467a` を全体の約1割だけに限定して使用
- アクセシビリティ: WCAG AA コントラスト、本文は `#4a4a4a`、ステータスは色だけに依存せず必ずテキスト併記、スキップリンク・`:focus-visible`・`lang` 属性、`prefers-reduced-motion` でアニメーション停止

## 対象プロダクト

- リポジトリ: https://github.com/akakirishima/HelloWorld
- 概要: Raspberry Pi 上で動かし、研究室LAN内の端末から在室状況・勤怠・日誌をまとめて管理する、タッチ操作前提の Web アプリ（React 19 + FastAPI）
