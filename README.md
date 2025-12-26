# 株式会社Precious ウェブサイト

このリポジトリは、株式会社Preciousの公式ウェブサイトのソースコードを管理しています。

## 自動デプロイについて

このリポジトリは、GitHub Actionsを使用してLolipop FTPサーバーへ自動デプロイされます。

### デプロイの仕組み

- `main`ブランチにプッシュすると、自動的にLolipopサーバーへデプロイされます
- デプロイ先: http://precious-2020.jp/
- FTPサーバー: ftp-1.lolipop.jp

### ウェブサイトの更新方法

1. ファイルを編集する
2. 変更をコミットする
   ```bash
   git add .
   git commit -m "更新内容の説明"
   ```
3. GitHubにプッシュする
   ```bash
   git push origin main
   ```
4. 自動的にLolipopサーバーへデプロイされます（数分かかります）

### ファイル構成

- `index.html` - メインページ
- `assets/` - CSS、JavaScriptファイル
- `*.png`, `*.jpg`, `*.jpeg` - 画像ファイル
- `.github/workflows/deploy.yml` - 自動デプロイ設定

## 注意事項

- FTPパスワードはGitHub Secretsに安全に保管されています
- ファイルを直接FTPでアップロードすると、次回のGitプッシュ時に上書きされる可能性があります
- 必ずGitを通じて更新を行ってください

## 最終更新

2025年12月26日 10:48:14
