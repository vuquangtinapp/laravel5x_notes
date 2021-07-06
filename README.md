# Tìm hiểu cấu trúc của Laravel 5.x

## Tìm hiểu cấu trúc của Laravel
Ở bài trước chúng ta đã cài đặt thành công laravel trong chuyên mục basic-laravel, chúng ta tiến hành mở chúng sẽ thấy có cấu trúc như sau:

```
basic-laravel/
├── app/
│   ├── Console
│   ├── Exceptions
│   ├── Http
│   │   ├── Controllers
│   │   ├── Middleware
│   │   └──  Kernel.php
│   └── Providers
├── bootstrap/
├── config/
├── database/
├── public/
├── resources/
├── storage/
├── routes/
├── tests/
├── vendor/
├── .env
├── .env.example
├── composer.json
├── composer.lock
├── package.json
├── gulpfile.js
├── server.php
└── artisan
```

Và bây giờ mình sẽ giải thích mục đích, vai trò của từng thư mục tập tin trong đây nhé, chúng ta sẽ có như sau:

*   **app** là thư mục chứa tất cả các thư mục, các tập tin php, các class php, thư viện, models để xây dựng project của bạn.
    *   **Console** thư mục chứa các tập tin định nghĩa các lệnh thực thi trên Artisan.
    *   **Excerption** thư mục chứa các tập tin quản lý, điều hướng lỗi.
    *   **Http**
        *   **Controllers** là thư mục chứa các tập tin controllers
        *   **Middleware** là thư mục chứa các tập tin lọc và ngăn chặn các requests.
        *   **Kernel.php** là tập tin cấu hình, định nghĩa Middleware hoặc nhóm Middleware.
    *   **Providers** chứa các providers mình sẽ nói rõ về nó trong các bài nâng cao.
*   **bootstrap** thư mục chứa tập tin điều hướng khởi động hệ thống, thường thì chúng ta sẽ không làm gì đến nó.
*   **config** chứa mọi tập tin cấu hình của Laravel
*   **database** chứa các thư mục tập tin về CSDL
    *   **migrations** chứa các tập tin định nghĩa khởi tạo và sử bảng.
    *   **seeds** chứa các tập tin định nghĩa dữ liệu insert vào database.
    *   **factories** chứa các tập tin định nghĩa các cột bảng dữ liệu để tạo ra các dữ liệu ảo phục vụ cho tests.
*   **public** chính là webroot người dùng sẽ truy cập vào đây, đây cũng là nơi chứa các tập tin css, js, image.
*   **resources** chứa các tập tin giao diện (js, css, less, sass, coffeescript,...), views, ngôn ngữ.
*   **storage** chứa các tập tin hệ thống như upload, cache, session, cookie, log...
*   **routes** là thư mục chứa các tập tin định nghĩa <span style="line-height: 20.8px;">các router, xử lý router hoặc điều hướng router (tức là URL, laravel không tự đặt url theo kiểu example.com/controller/action/value mà chúng ta phải tự định nghĩa chúng) bao gồm 3 loại là web, api và console.</span>
*   **tests** chứa các tập tin định nghĩa tests.
*   **vendor** thư mục của composer.
*   **.env** và **.env.example** là 2 tập tin cấu hình chính của laravel như key app, tên app, url app, email, env mode, CSDL hay bật tắt debug.
*   **composer.json**, **composer.lock** tập tin của composer.
*   **package.js** tập tin cấu hình của nodejs chứa các package cần thiết cho projects.
*   **gulpfile.js** là tập tin gulp builder.
*   **phpunit.xml** là tập tin xml của phpunit dùng để testing project.
*   **server.php** là tập tin để artisan trỏ đến tạo server khi gõ lệnh `php artisan serve`
*   **artisan** tập tin thực thi lệnh của Laravel, cũng là tập tin mà chúng ta tương tác nhiều nhất.

Ngoài ra còn có các thư mục và tập tin khác nữa, nhưng mình sẽ nói rõ hơn ở các bài sau. Có một số thư mục mình còn giải thích quá trừu tượng, nhưng các bạn hãy tạm hiểu như thế ở các bài học riêng từng cái mình sẽ nói rõ hơn về Laravel.

http://esbenp.github.io/2016/04/11/modern-rest-api-laravel-part-1/

http://esbenp.github.io/2016/04/15/modern-rest-api-laravel-part-2/
