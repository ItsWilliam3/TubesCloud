# TubesCloud

## Mohamad Farrel William Rosyadi (1101210306)
## Geva Almer Hariri (1101213144)
## Moch Firza Yudistira Meizia (1101210233)
## Reivanza Laksono (1101210320)
## Charlos Alvaredo Simanullang (1101213158)

### Sebelum menggunakan anda dapat menggunakan anda harus menginstal flask, docker engine serta docker compose terlebih dahulu

# Menginstal Docker Engine
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


# Menginstal Flask
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






















