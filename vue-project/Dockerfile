# ベースイメージを指定
FROM node:latest

# 作業ディレクトリを設定
WORKDIR /app

# ホストのpackage.jsonとpackage-lock.jsonをコピーして依存関係をインストール
COPY package*.json ./

# 依存関係のインストール
RUN npm install

# ソースコードをコピー
COPY . .

# アプリケーションのビルド
RUN npm run build

# ポートを公開
EXPOSE 8080

# アプリケーションを起動
CMD ["npm", "run", "serve"]
