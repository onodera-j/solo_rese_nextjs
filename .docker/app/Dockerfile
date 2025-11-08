# php側 Dockerfile
FROM php:8.2-fpm

ENV TZ=Asia/Tokyo

# composer を追加
COPY --from=composer:2.5.5 /usr/bin/composer /usr/bin/composer

# 必要パッケージ & PHP拡張
RUN set -eux; \
    apt-get update; \
    apt-get install -y --no-install-recommends \
      ca-certificates curl git unzip zlib1g-dev libzip-dev vim; \
    rm -rf /var/lib/apt/lists/*; \
    docker-php-ext-install pdo_mysql bcmath zip

# タイムゾーンを反映（ログ時刻ズレ防止）
RUN ln -snf /usr/share/zoneinfo/${TZ} /etc/localtime && echo ${TZ} > /etc/timezone

# PHP設定
COPY ./.docker/app/php.ini /usr/local/etc/php/php.ini

WORKDIR /var/www/src
