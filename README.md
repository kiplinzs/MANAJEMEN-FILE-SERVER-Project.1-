# PROJECT-FILE-MANAGEMENT-SERVER-Project.1

### 1. Membuat Struktur Direktori Awal
```
mkdir -p Company/Marketing/Documents Marketing/Archives
mkdir -p Company/Engineering/Documents Engineering/Archives
mkdir -p Company/HR/Documents HR/Archives
```
### 2. Pindahkan dan salin file
***Pindahkan file yang salah tempat ke direktori yang benar***
```
mv marketing.pdf Marketing/Documents/


mv desain_bengkel.jpg Engineering/Documents/


mv data_perusahaan.txt HR/Documents/

```
***buat backup di
folder Archives***
```
cp  marketing.pdf Marketing/Archives/


cp desain_bengkel.jpg Engineering/Archives/

cp data_perusahaan.txt  HR/Archives/
```
### 3. Atur permission 
***Set permission yang tepat agar hanya departemen terkait yang bisa mengakses folder mereka***
tambah user departemen terkait terlrbih dahulu jika belum punya contoh:
```
sudo adduser admin-marketing
sudo adduser admin-engineering
sudo adduser admin-hr
```
```
sudo chown -R admin-marketing Marketing/
sudo chown -R admin-engineering Engineering/
sudo chown -R admin-hr Hr/
```
```
sudo chmod -R 700 Marketing/
sudo chmod -R 700 Engineering/
sudo chmod -R 700 HR/
```
### 4. Cari dan filter
***Temukan semua file PDF yang dibuat minggu lalu dan buat daftar
lengkapnya***
```
find -type f -name "*.pdf" -mtime -7 > daftarlengkap-pdf.jpg.txt
```
