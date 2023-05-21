1. isi Dockerfile https://pastebin.com/KVN1PkuL
2. membuild Dockerfile: `docker build -t image-nginx:v1.0 .`
3. mengerun docker image: `docker run -p 80:80 --name container-nginx image-nginx:v1.0`

---

1. buka browser lalu ketikkan localhost atau localhost:80.
2. ketikkan 'docker images', lalu cek apakah namanya 'image-nginx' dan tagnya v1.0.
3. ketikkan 'docker inspect image-nginx:v1.0', lalu cek obcject bernama ExposedPorts. Pastikan hasilnya seperti ini
   "ExposedPorts": {
   "80/tcp": {}
   },
4. ketikkan 'docker container ls' lalu cek namanya 'container-nginx'.

---

1. Buatlah sebuah konfigurasi dockerfile yang berisi image nginx
2. Copas kode html hello-world berikut https://pastebin.com/XG4wRSc1 pada file yang bernama index.html.
3. Letakkan file html tersebut pada direktori/folder yang sama dengan file dockerfile.
   visualisasi:
   ./
   ../
   Dockerfile
   index.html
4. Jadikan file html tersebut sebagai isi dari konten nginx (bisa suruh lihat dokumentasi image nginx di docker hub (https://hub.docker.com/_/nginx) atau jika asdos lagi berbaik hati, langsung suruh beri perintah copas file index.html ke direktori /usr/share/nginx/html ketika build atau jika sangat berbaik hati sekali suruh kasih perintah: COPY . /usr/share/nginx/html pada Dockerfile-nya).
5. Build image tersebut dengan nama image-nginx versi v2.0 dan lalu run dengan nama container nginx dan memforward port 80 container ke port 80 PC.
6. Terakhir, jalankan tiga container dengan image-nginx:v2.0 menggunakan docker compose dengan nama container-nginx1, container-nginx2, container-nginx3 serta masing-masing port forward 80, 8080, dan 8888

---

1. index.html: https://pastebin.com/XG4wRSc1
2. Dockerfile: https://pastebin.com/fkp5hz2q
3. docker compose: https://pastebin.com/ygJQFYJg , untuk mengerun docker compose memakai `docker compose up`
4. muncul hello world ketika dibuka:

- http://localhost
- http://localhost:8080
- http://localhost:8888

---

buka url berikut pada browser

- http://localhost
- http://localhost:8080
- http://localhost:8888

---

- berhasil menampilkan laman nginx di localhost
- nama image: image-nginx:v1.0
- nama container: container-nginx

---

1. buka browser lalu ketikkan localhost atau localhost:80.
2. ketikkan pada terminal 'docker images', lalu cek apakah namanya 'image-nginx' dan tagnya v1.0.
3. ketikkan pada terminal 'docker container ls' lalu cek namanya 'container-nginx'.
