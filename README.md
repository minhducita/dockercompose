<article class="markdown-body entry-content container-lg" itemprop="text">
  <h1>Ví dụ Docker compose cơ bản</h1>
  <p>Pull code</p>
  <pre><code>git clone https://github.com/minhducita/dockercompose.git</code></pre> 
  <p>Sau khi Pull code về bạn vào thư mục chứa Docker Compose bằng lệnh sau</p>
  <pre><code>cd dockercompose</code></pre> 
  <p>Tiếp theo tạo file .env từ file .env.example<p>
  <pre><code>
  cd app
  cp .env.example .env/
  </code></pre>
  <p>Change value params in .env:</p>
  <pre><code>
  DB_HOST=database
  DB_PASSWORD=secret
  </code></pre>
  
  
  <p>Và chúng ta sẽ chạy lên thử với câu lệnh</p>
  <pre><code>
  cd ../
  sudo docker-compose up -d
  </code></pre>
  
  <p>ssh vào docker app</p>
  <pre><code>sudo docker-compose exec app bash</code></pre>
  
  <h2>Tiến hành cài đặt composer</h2  
  <p>Trước tiên, hãy cập nhật bộ đệm ẩn của trình quản lý gói bằng cách chạy:</p>
  <pre><code>apt-get update && apt-get install zip -y</code></pre>
  <p>Tiếp theo, chạy lệnh sau để cài đặt các gói cần thiết:</p>
  <pre><code>apt install php-cli unzip</code></pre>
  <p>Tải xuống và cài đặt Composer</p>
  <pre><code>cd ~</code></pre>
  <pre><code>curl -sS https://getcomposer.org/installer -o composer-setup.php</code></pre>
  <p>Để tạo thuận lợi cho bước xác minh, bạn có thể sử dụng lệnh sau để lấy mã băm mới nhất theo chương trình từ trang Composer và lưu trữ nó trong một biến shell</p>
  <pre><code>HASH=`curl -sS https://composer.github.io/installer.sig`</code></pre>
  <p>Bây giờ hãy thực thi mã PHP sau, như được cung cấp trong trang tải xuống Trình soạn nhạc, để xác minh rằng tập lệnh cài đặt có an toàn để chạy:</p>
  <pre><code>php -r "if (hash_file('SHA384', 'composer-setup.php') === '$HASH') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"</code></pre>
  <p>Để cài composer globally , hãy sử dụng lệnh sau sẽ tải xuống và cài đặt Composer  dưới dạng system-wide  có tên là composer, trong / usr / local / bin:</p>
  <pre><code>
  php composer-setup.php --install-dir=/usr/local/bin --filename=composer
  composer install
</code></pre>
<p><i>Tài liệu tham khảo cài đặt composer https://www.digitalocean.com/community/tutorials/how-to-install-and-use-composer-on-ubuntu-20-04</i></p>
  
  

<p>Thiết lập quyền lưu trữ cho storage</p>
<pre><code>chown -R root:www-data storage/</code></pre>
<p> generate laravel key</p>
<pre><code>php artisan key:generate</code></pre>

<p>run migrate create database</p>
<pre><code>php artisan migrat</code></pre>
  
<p>Tiếp đến, truy cập vào địa chỉ http://http://0.0.0.0:8080, để tận hưởng thành quả nào.</p>
<hr>
<p>Bạn có thể tham khảo cách tạo Docker compose tại <a href="https://kipalog.com/posts/Cai-dat-moi-truong-Docker-cho-Laravel-2019" rel="nofollow">https://kipalog.com/posts/Cai-dat-moi-truong-Docker-cho-Laravel-2019</a></p>
</article>
