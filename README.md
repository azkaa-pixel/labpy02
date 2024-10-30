# modul praktikum 2 - struktur kondisi
Nama:ghefira azka fardani 

Kelas:TI.24.A5

NIM: 312410521

## 1. pernyataan if 
pada phyton di kenal penggunaan struktur kondisi menggunakan statement ```if```, di mana format/syntax penggunaan statement ```if``` 

ADALAH:

```if``` kondisi:

statement_true
### contoh program  menggunakan statement if
```phython
num = input("masukan angka: ")
if(int(num) > 0):
  print (num,"adalah bilangan positif")
print("ini diluar  pernyataan if")
```
## 2. pernyataan if ... else
syntax:

```if``` kondisi

statement_true

```else:``` 

statement_false
    
### contoh program statement if...else
```phython
num = input("masukan angka: ")
if int(num) > 0):
  print(num , "adalah bilangan positif ")
elif:
  print (num, "adalah  bilangan negatif")
print("ini di luar pernyataan if"
```
## 3. pernyataan if ... elif
syntax:

```if``` kondisi:

  statement_true
  
```elif``` kondisi2:

  statement_true
  
else:

  statement_false
### contoh program penggunaan statement if... elif
```phython
num=input("masukan angka: ")
if int(num ) > 0:
  print(num,"adalah bilangan positif")
elif int(num) == 0:
  print(num,"adalah angka nol"
else:
  print(num, "adalah bilangan negatif")
```
## 4. operator ternari
syntax:

condition_true ```if``` conditiom ```else``` condition false
### contoh
```phython
nilai input("Masukkan nilai: ")
keterangan "LULUS" if nilai 60 else "TIDAK LULUS"
print (keterangan)
```
syntax:

(condition_false, condition_true)[condition]
### contoh
```phython
nilai input("Masukkan nilai: ") 
keterangan ("TIDAK LULUS", "LULUS") (nilai > 60]
print(keterangan)
```
## latihan 

## latihan 1 membuat program  menentukan nilai akhir 
### - flowchart
![foto](https://github.com/azkaa-pixel/labpy02/blob/8eece5e39380c96cc439fb51313fa1c187dbb8c8/Blank%20diagram.png)
### - code program
```phython
nama = input("Masukkan nama: ")
uts = input("Masukkan nilai UTS: ")
uas = input("Masukkan nilai UAS: ")
tugas = input("Masukkan nilai Tugas: ")
```
Program meminta pengguna untuk memasukkan nama dan nilai dari UTS (Ujian Tengah Semester), UAS (Ujian Akhir Semester), dan Tugas. Semua input ini akan disimpan dalam variabel yang sesuai.

```phython
akhir = (int(tugas)*2 + int(uts)*4 + int(uas)*4) / 10
```
Nilai akhir dihitung dengan rumus tertentu:
Nilai tugas memiliki bobot 2, sedangkan nilai UTS dan UAS masing-masing memiliki bobot 4.
Semua nilai dikonversi ke integer sebelum dihitung.
Total bobot adalah 10.

```phython
keterangan = "LULUS" if akhir > 60.0 else "TIDAK LULUS"
```
Jika nilai akhir lebih dari 60, maka keterangan adalah "LULUS", jika tidak, "TIDAK LULUS".

```phython
if akhir >= 88:
    huruf = "A"
elif akhir >= 70:
    huruf = "B"
elif akhir >= 50:
    huruf = "C"
elif akhir >= 40:
    huruf = "D"
else:
    huruf = "E"
```
Program menggunakan serangkaian pernyataan if untuk menentukan nilai huruf berdasarkan nilai akhir:
A untuk akhir >= 88
B untuk akhir >= 70
C untuk akhir >= 50
D untuk akhir >= 40
E untuk akhir < 40

```phython
print("\nNama: ", nama)
print("Nilai UTS: ", uts)
print("Nilai UAS: ", uas)
print("Nilai Tugas: ", tugas)
print("Nilai Akhir: ", akhir)
print("\nNilai Huruf: ", huruf)
print("Keterangan:",keterangan)
```
Akhirnya, program mencetak semua informasi yang telah dimasukkan dan hasil perhitungan, termasuk nama, nilai UTS, UAS, Tugas, nilai akhir, nilai huruf, dan keterangan lulus atau tidak lulus.
### - hasil
![foto](https://github.com/azkaa-pixel/labpy02/blob/517a988aadb72851013d28f142aff03ba7c865d9/latihan%201.jpg)
## latihan 2 membuat program menampilkan status gaji karyawan 
### - flowchart
![foto]
### - code program 
```phython
# Meminta input gaji dari pengguna
gaji = int(input("Masukkan gaji: "))
```
Kode ini meminta pengguna untuk memasukkan gaji dan mengonversi input tersebut menjadi tipe data integer. Input ini disimpan dalam variabel gaji.

```phython
# Meminta input apakah sudah berkeluarga
berkeluarga_input = input("Sudah berkeluarga? (Y/T): ")
berkeluarga = berkeluarga_input.upper() == "Y"
```
Pengguna diminta untuk menginput apakah sudah berkeluarga atau tidak. Input ini disimpan dalam berkeluarga_input.
Kemudian, berkeluarga_input diubah menjadi huruf kapital menggunakan .upper() dan dibandingkan dengan "Y". Hasil perbandingan (True atau False) disimpan dalam variabel berkeluarga.
```phython
# Meminta input apakah punya rumah
punya_rumah_input = input("Punya rumah? (Y/T): ")
punya_rumah = punya_rumah_input.upper() == "Y"
```
Proses ini mirip dengan sebelumnya, tetapi kali ini untuk menanyakan apakah pengguna memiliki rumah. Hasilnya disimpan dalam variabel punya_rumah.
```phython
# Memeriksa status gaji
if gaji >= 3000000:  # UMR contoh, sesuaikan dengan nilai UMR yang berlaku
    print("Gaji sudah di atas UMR")
```
Kode ini memeriksa apakah gaji yang dimasukkan lebih besar atau sama dengan 3.000.000 (misalnya, Upah Minimum Regional/UMR). Jika ya, program melanjutkan untuk menampilkan pesan dan pemeriksaan lebih lanjut.

```phython
    if berkeluarga:
        print("Wajib ikutan asuransi dan menabung untuk pensiun")
    else:
        print("Tidak perlu ikutan asuransi")
```
Jika pengguna sudah berkeluarga, program menyarankan untuk ikut asuransi dan menabung untuk pensiun. Jika tidak, diberitahukan bahwa tidak perlu ikut asuransi.
```phython
    if punya_rumah:
        print("Wajib bayar pajak rumah")
    else:
        print("Tidak wajib bayar pajak rumah")
else:
    print("Gaji belum UMR")
```
Program memeriksa apakah pengguna memiliki rumah. Jika iya, maka mereka diwajibkan untuk membayar pajak rumah. Jika tidak, mereka tidak perlu membayar pajak rumah.
### - hasil
![foto](https://github.com/azkaa-pixel/labpy02/blob/be923871e081edb111f8e8a4349b62d2d60bd2a3/latihan%202%20.jpg)
## latihan 3
### - flowchart
![foto]
### - code program
```phython
# Mengambil input dari pengguna
a = int(input("Masukkan bilangan A: "))
b = int(input("Masukkan bilangan B: "))
c = int(input("Masukkan bilangan C: "))
```
Kode ini meminta pengguna untuk memasukkan tiga bilangan: A, B, dan C.
Fungsi input() digunakan untuk mengambil input, dan int() mengonversi input tersebut menjadi tipe data integer.
```phython
# Memeriksa apakah penjumlahan dua bilangan sama dengan bilangan lainnya
if a + b == c or b + c == a or a + c == b:
```
Kondisi ini memeriksa apakah jumlah dari dua bilangan sama dengan bilangan yang ketiga.
Ada tiga kemungkinan yang diperiksa:
Apakah A + B sama dengan C.
Apakah B + C sama dengan A.
Apakah A + C sama dengan B.
Jika salah satu dari kondisi tersebut benar, maka bagian ```if``` akan dijalankan.
```phython
    print("BENAR")
```
Jika salah satu kondisi di atas terpenuhi, program akan mencetak "BENAR".
```phython
else:
    print("SALAH")
```
Jika tidak ada kondisi yang terpenuhi, program akan mencetak "SALAH".

### - hasil
![foto](https://github.com/azkaa-pixel/labpy02/blob/be923871e081edb111f8e8a4349b62d2d60bd2a3/latihan%203.jpg)
## kasus
## kasus 1
### - flowchart
![foto]
### - code program 
```phython
# Meminta input dari pengguna
tipe_tiket = input("Masukkan tipe tiket (reguler/VIP): ").strip().lower()
status_member = input("Apakah Anda memiliki kartu member? (ya/tidak): ").strip().lower()
```
input(): Meminta pengguna untuk memasukkan tipe tiket dan status member.
strip(): Menghapus spasi di awal dan akhir input.
lower(): Mengubah input menjadi huruf kecil agar lebih mudah dibandingkan.
```phython
# Menentukan harga tiket
harga_reguler = 50000
harga_vip = 100000
```
Menentukan harga tiket reguler dan VIP.
```phython
# Menghitung total harga berdasarkan tipe tiket dan status member
if tipe_tiket == 'reguler':
    total_harga = harga_reguler
elif tipe_tiket == 'vip':
    total_harga = harga_vip
else:
    print("Tipe tiket tidak valid.")
    total_harga = 0
```
Jika pengguna memasukkan reguler, harga tiket di-set ke harga_reguler.
Jika vip, harga tiket di-set ke harga_vip.
Jika input tidak valid, mencetak pesan dan mengatur total_harga menjadi 0.
```phython
# Menghitung diskon jika pengguna memiliki kartu member
total_harga = total_harga * 0.8 if status_member == 'ya' else total_harga
```
Jika pengguna memiliki kartu member (status_member adalah ya), total harga dikalikan 0.8 (diskon 20%).
Jika tidak, harga tetap sama.
```phython
# Menampilkan total harga yang harus dibayar
if total_harga > 0:
    print(f"Total harga yang harus dibayar: Rp{total_harga:.2f}")
```
Jika total_harga lebih dari 0, program mencetak total harga yang harus dibayar, diformat dengan dua angka di belakang koma.
### - hasil
![foto](https://github.com/azkaa-pixel/labpy02/blob/be923871e081edb111f8e8a4349b62d2d60bd2a3/kasus%201.jpg)
## kasus 2
### - flowchart
![foto]
### - code program
```phython
# Fungsi kalkulator
def kalkulator():
```
```phython
    # Menerima input dari pengguna
    angka1 = float(input("Masukkan angka pertama: "))
    angka2 = float(input("Masukkan angka kedua: "))
    operator = input("Masukkan operator (+, -, *, /): ")
```
Kode ini meminta pengguna untuk memasukkan dua angka dan sebuah operator.
float() digunakan untuk mengkonversi input menjadi angka desimal.
```phython
    # Menghitung hasil berdasarkan operator yang dipilih
    if operator == '+':
        hasil = angka1 + angka2
    elif operator == '-':
        hasil = angka1 - angka2
    elif operator == '*':
        hasil = angka1 * angka2
    elif operator == '/':
        # Menangani pembagian dengan nol
        if angka2 != 0:
            hasil = angka1 / angka2
        else:
            return "Error: Pembagian dengan nol tidak diizinkan."
    else:
        return "Error: Operator tidak valid."
```
Di sini, kita memeriksa operator yang dimasukkan pengguna.
Berdasarkan operator tersebut, kita melakukan operasi aritmatika yang sesuai.
Jika operator adalah pembagian (/), kode ini juga memeriksa apakah angka2 tidak nol untuk menghindari pembagian dengan nol.
```phython
    return f"Hasil: {hasil}"
```
Jika operasi berhasil, fungsi akan mengembalikan string yang menunjukkan hasil perhitungan.
```phython
# Menjalankan kalkulator
print(kalkulator())
```
Kode ini memanggil fungsi kalkulator() dan mencetak hasilnya ke layar.
### - hasil 
![foto](https://github.com/azkaa-pixel/labpy02/blob/be923871e081edb111f8e8a4349b62d2d60bd2a3/kasus%202.jpg)







