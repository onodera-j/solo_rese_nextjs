# rese_ver_nextjs

## セットアップ
### githubからクローン
    git clone https://github.com/sakanadaketabetetai/rese_ver_nextjs.git

### laravelの設定ファイルをコピー
    cd src
    cp .env.example .env

### dockerビルド操作
    cd ..
    docker-compose up -d --build

### laravelのAPP_KEYを設定
    docker-compose exec api bash
    php artisan key:generate

### Nextjsとlaravelプロジェクトへアクセスできるか確認
    - Nextjs : http://localhost:3000
    - laravel : http://localhost:8000
