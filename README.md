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
  
  <p>Để cài composer globally , hãy sử dụng lệnh sau sẽ tải xuống và cài đặt Composer  dưới dạng system-wide  có tên là composer, trong / usr / local / bin:</p>
  <pre><code>
  php composer-setup.php --install-dir=/usr/local/bin --filename=composer
  composer install
</code></pre>
<p><i>Tài liệu tham khảo cài đặt composer https://www.digitalocean.com/community/tutorials/how-to-install-and-use-composer-on-ubuntu-20-04</i></p>
  
  

<p>Thiết lập quyền lưu trữ cho storage</p>
<pre><code>chown -R root:www-data storage/</code></pre>
<p>Tạo khóa laravel</p>
<pre><code>php artisan key:generate</code></pre>

<p>Tạo cơ sở dữ liệu</p>
<pre><code>php artisan migrate --seed</code></pre>
  
<p>Tiếp đến, truy cập vào địa chỉ http://http://0.0.0.0:8080, để tận hưởng thành quả nào.</p>
<hr>
<p>Bạn có thể tham khảo cách tạo Docker compose tại <a href="https://kipalog.com/posts/Cai-dat-moi-truong-Docker-cho-Laravel-2019" rel="nofollow">https://kipalog.com/posts/Cai-dat-moi-truong-Docker-cho-Laravel-2019</a></p>
</article>
