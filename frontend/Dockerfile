# ベースイメージとして Node.js を使用
FROM node:22-slim

# 作業ディレクトリの設定
WORKDIR /app/frontend

RUN apt-get update && apt-get install -y git vim

RUN npm install -g pnpm@10.15.1

COPY . .

# node_modulesがあった場合削除
RUN if [ -d node_modules ]; then rm -rf node_modules; fi

RUN pnpm install