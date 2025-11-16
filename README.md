# rese_ver_nextjs

## セットアップ
### githubからクローン
    git clone https://github.com/sakanadaketabetetai/rese_ver_nextjs.git

### laravelの設定ファイルをコピー
    ```
        cd src
        cp .env.exmple .env
    ```
### laravelのAPP_KEYを設定
    ```
        php artisan key:generate
    ```

### dockerビルド操作
    docker-compose up -d --build

### Nextjsとlaravelプロジェクトへアクセスできるか確認
    - Nextjs : http://localhost:3000
    - laravel : http://localhost:8000
# rese_ver_nextjs
