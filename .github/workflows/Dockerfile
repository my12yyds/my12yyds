# 使用官方 PHP 镜像作为基础镜像
FROM php:7.4-apache

# 拷贝应用程序代码到 /var/www/html 目录中
COPY src/ /var/www/html/

# 安装 PHP 扩展
RUN docker-php-ext-install mysqli pdo pdo_mysql

# 设置时区为 Asia/Shanghai
RUN ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && echo "Asia/Shanghai" > /etc/timezone

# 暴露 Apache 80 端口
EXPOSE 80