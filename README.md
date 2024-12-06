# TubesCloud

## Mohamad Farrel William Rosyadi (1101210306)
## Geva Almer Hariri (1101213144)
## Moch Firza Yudistira Meizia (1101210233)
## Reivanza Laksono (1101210320)
## Charlos Alvaredo Simanullang (1101213158)

Sebelum menggunakan docker anda dapat menggunakan anda harus menginstal flask, docker engine serta docker compose terlebih dahulu

# Menginstal aplikasi yang ingin digunakan

## Menginstal Docker Engine
Untuk menginstal docker anda perlu mengetik perintah ini di terminal :
```
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc
```
Jika di berikan prompt y/n anda masukan y untuk melanjutkan
Kemudian tambahkan repository-nya ke Apt source
```
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
```
Setelah menambahkan repository anda tinggal menginstal Package Docker-nya
```
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```
Untuk mengverifikasi apakah docker sudah terinstal bisa jalankan perintah
```
sudo docker run hello-world
```
Akan muncul gambar seperti ini

![image](https://github.com/user-attachments/assets/73bddc29-6254-42ca-9b2d-443b2e9de442)


## Menginstal Flask
Flask adalah framework WSGI yang ringan. Flask digunakan untuk membuat aplikasi web sederhana.
Instal dahulu virtual environment menggunakan modul venv
```
sudo apt install python3-venv
```
Buat direktori baru dan pindah ke direktori tersebut menggunakan perintah :
```
mkdir flask_app && cd flask_app
```
Kemudian jalankan perintah ini di dalam direktori tersebut untuk membuat virtual environment
```
python3 -m venv venv
```
Aktifkan virtual environment menggunakan perintah ini
```
source venv/bin/activate
```
Ketika sudah diaktifkan bin virtual environment akan muncul di awal variable $PATH seperti di gambar
![image](https://github.com/user-attachments/assets/edc93e27-527a-462f-a4c3-fc1f7ab78a6a)

Ketika virtual environment sudah aktif, gunakan Python package manager `pip` untuk menginstal Flask
```
pip install Flask
```
untuk mengverifikasi apakah Flask sudah terinstal bisa jalankan perintah :
```
python -m flask --version
```
yang akan menampilkan versi Flask seperti pada gambar

![image](https://github.com/user-attachments/assets/7a4ea93f-926d-4768-ae87-40ed8054e5c0)

Ketika virtual environment sudah aktif, gunakan Python package manager `pip` untuk menginstal Flask
```
pip install Flask
```
untuk mengverifikasi apakah Flask sudah terinstal bisa jalankan perintah :
```
python -m flask --version
```
yang akan menampilkan versi Flask seperti pada gambar

![image](https://github.com/user-attachments/assets/7a4ea93f-926d-4768-ae87-40ed8054e5c0)

## Menginstal Docker Compose
Menginstal docker compose dapat menggunakan perintah:
```
sudo apt install docker-compose
```


# Membuat Web App untuk di docker-kan

Buka terminal baru, kemudian buat direktori baru untuk meletakan file web app, untuk web app akan saya buat menggunakan python
saya menggunakan TubesCC sebagai nama folder
```
mkdir TubesCC && cd TubesCC
```
Buat file berformat `.py` untuk membuat web app. Saya menggunakan calculator sebagai web app
```
nano calculator.py
```
Masukan script web app flask python ke dalam `calculator.py` sehingga tampilannya seperti ini


![image](https://github.com/user-attachments/assets/6e698c45-215c-4a8f-b6d0-605532a8a998)

untuk script ini bisa di download di atas

Karena script ini memperlukan `html` agar dapat bekerja maka kita perlu membuat folder baru lagi bernama `templates`
```
mkdir templates && cd templates
```
Buat file `.html` yang diberi nama sama seperti file script python
```
nano calculator.html
```
Masukan file `.html` seperti di bawah ini

![image](https://github.com/user-attachments/assets/16eaf2d1-1893-4157-a114-0ad09322503d)

file `.html` juga bisa di dapatkan di folder html di atas

# Membuat Dockerfile dan docker-compose.yml
Sebelum membuat Dockerfile dan docker-compose.yml kembali ke folder TubesCC menggunakan `cd ..`
Kemudian buat file Dockerfile dengan menggunakan
```
nano Dockerfile
```
masukan ini ke dalam Dockerfile untuk containerization

![image](https://github.com/user-attachments/assets/98d493e7-5516-4692-b95a-ee1a949ced40)

Dockerfile ini juga tersedia di atas

Kemudian kita buat juga docker-compose.yml yang berisikan

![image](https://github.com/user-attachments/assets/1a9037de-2352-4865-8245-a430736762e5)

yang juga tersedia di atas

sebelum menjalankan docker kita perlu membuat file requirements untuk menjalankan docker compose dengan menggunakan
```
nano requirements.txt
```
kemudian masukan saja satu kalimat `flask` kemudian close dan save

# Menjalankan Docker
untuk menjalankan docker kita dapat menggunakan 
```
docker compose up 
```
sehingga tampilan muncul seperti ini

![image](https://github.com/user-attachments/assets/53c0a18b-06da-4439-87f3-be14895a7739)

coba buka browser dan masukan salah satu IP dibawah ini 

![image](https://github.com/user-attachments/assets/94c2cae4-84ad-472a-98a5-a0b43f31bd90)

di coba saja IP nya satu-satu

Ketika berhasil maka anda dapat membuka Web App yang sudah di Docker-kan

![image](https://github.com/user-attachments/assets/e792ce2d-77d5-4891-b26c-c700058d0a43)

Untuk mematikan docker-compose maka anda hanya perlu menekan `CTRL + C`










