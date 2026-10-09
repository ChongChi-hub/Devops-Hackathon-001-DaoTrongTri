# DevOps Hackathon - Đề 001

Website tĩnh với HTML và cấu hình Nginx để triển khai trên máy chủ Ubuntu.

## Cấu trúc repository

```text
devops-hackathon-de001-DaoTrongTri/
├── src/
│   └── index.html
├── nginx/
│   └── devopsg5.conf
├── screenshots/
├── .gitignore
├── README.md
└── .gitignore
```

## 1. Cài đặt và chạy

```bash
sudo apt update
sudo apt install nginx
```

## 2. Copy website vào thư mục phục vụ

```bash
sudo mkdir -p /var/www/devops-hackathon-de001-DaoTrongTri
sudo cp -r src/* /var/www/devops-hackathon-de001-DaoTrongTri/
```

## 3. Kích hoạt cấu hình Nginx

```bash
sudo cp nginx/devopsg5.conf /etc/nginx/conf.d/devopsg5.conf
sudo nginx -t
sudo systemctl reload nginx
```

## 4. Kiểm tra website

Mở trình duyệt và truy cập địa chỉ IP của máy chủ, ví dụ:

```bash
http://<IP_MAY_CHU>/
```

Hoặc kiểm tra bằng cURL:

```bash
curl -I http://localhost/
```

## 5. Ghi chú

- Website được xây dựng theo hướng dẫn của đề bài và đặt ở thư mục `src/`.
- Cấu hình Nginx mục tiêu là phục vụ tĩnh file HTML trên cổng 80.
- Nên đặt tên file cấu hình server block theo tài khoản Linux hoặc tên repo của bạn để dễ quản lý.
