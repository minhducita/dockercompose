<article class="markdown-body entry-content container-lg" itemprop="text">
  <h1>Ví dụ Docker compose cơ bản</h1>
  <p>Bước 1. Bạn vào thư mục chứa Dockerfile bằng lệnh sau</p>
  <pre><code>cd dockerfile</code></pre>
  <p>Bước 2. Build Docker image và tạo container mới trên image vừa tạo</p>
  <pre><code>sudo docker build -t nginx_image .</code></pre>
  <p>Bước 3. Chạy lệnh sau để tạo container mới từ nginx_image ở trên:</p>
  <pre><code>sudo docker run -it -v /webroot:/var/www/html -p 9000:80 --name demo_dockerfile nginx_image</code></pre>
  <p>Tiếp đến, truy cập vào địa chỉ http://http://192.168.33.10:9000, để tận hưởng thành quả nào.</p>
  <hr>
  <p>Bạn có thể tham khảo cách tạo Dockerfile tại <a href="https://viblo.asia/p/docker-tao-docker-images-tu-dockerfile-3P0lPORvZox" rel="nofollow">https://viblo.asia/p/docker-tao-docker-images-tu-dockerfile-3P0lPORvZox</a></p>
</article>
