# <h1 align="center">Laporan Praktikum Struktur Data<br> Modul 1 Pengenalan C++ </h1>
<p align="center">Osha Alfida Valyana - 103112430202</p>

## Dasar Teori

Bahasa C++ adalah bahasa pemrograman yang dikembangkan oleh Bjarne Stroustrup pada tahun 1985 sebagai pengembangan dari bahasa C.     Dengan performa tinggi serta kontrol penuh terhadap manajemen memori, C++ banyak digunakan untuk membangun aplikasi kompleks seperti game, perangkat lunak, dan sistem berkinerja tinggi memori, C++ banyak digunakan untuk membangun aplikasi kompleks seperti game, perangkat lunak, dan sistem berkinerja tinggi.


## Guided

### Soal 1

Sruct

⁠ cpp
#include <iostream>
#include <string>
using namespace std;

struct Mahasiswa {
    string nama;
    string nim;
    float ipk;
};

int main() {

    Mahasiswa mhs1;

    cout << "Masukkan Nama Mahasiswa: ";
    getline(cin, mhs1.nama);
   
    cout << "Masukkan NIM Mahasiswa : ";
    cin >> mhs1.nim;
    cout << "Masukkan IPK Mahasiswa : ";
    cin >> mhs1.ipk;

    cout << "\n=== Data Mahasiswa ===" << endl;
 ⁠

	⁠outputpengerjaan
	⁠![output pengerjaan struct](https://github.com/chafdv/Modul1-/blob/main/Modul1/outputpengerjaan/struct%20cpp.png)

Program diminta membuat program untuk menyimpan data mahasiswa (nama, NIM, IPK), lalu minta input dari user dan tampilkan kembali datanya.
---

### Soal 2

Aritmatika

⁠ cpp
#include <iostream>
using namespace std;

int main() {
    int X, Y;
    float Z;
    X = 2; Y = 3; 
    Z = (X + Y) / (X * Y);
    cout << "Nilai Z = " << Z << endl; 
    return 0;
}
 ⁠


	⁠outputpengerjaan
	⁠![output pengerjaan aritmatika](https://github.com/chafdv/Modul1-/blob/main/Modul1/outputpengerjaan/aritmatika%20cpp.png)

Membuat program aritmatika sederhana: menghitung nilai Z = (X + Y) / (X * Y) dengan X = 2 dan Y = 3, lalu menampilkan hasilnya.

### Soal 3

Kondisi

⁠ cpp
#include <iostream>
using namespace std;
// int main()
// {
//     double tot_pembelian, diskon;
//     cout << "total pembelian: Rp";
//     cin >> tot_pembelian;
//     diskon = 0;
//     if (tot_pembelian >= 100000)
//         diskon = 0.05 * tot_pembelian;
//     cout << "besar diskon = Rp" << diskon;
// }



// int main()
// {
//     double tot_pembelian, diskon;
//     cout << "total pembelian: Rp";
//     cin >> tot_pembelian;
//     diskon = 0;
//     if (tot_pembelian >= 100000)
//         diskon = 0.05 * tot_pembelian;
//     else
//         diskon = 0;
//     cout << "besar diskon = Rp" << diskon;
// }



int main()
{
    int kode_hari;
    cout << "Menentukan hari kerja/libur\n"<<endl;
    cout << "1=Senin 3=Rabu 5=Jumat 7=Minggu "<<endl;
    cout << "2=Selasa 4=Kamis 6=Sabtu "<<endl;
    cin >> kode_hari;
    switch (kode_hari)
    {
    case 1:
    case 2:
    case 3:
    case 4:
    case 5:
        cout<<"Hari Kerja";
        break;
    case 6:
    case 7:
        cout<<"Hari Libur";
        break;
    default:
        cout<<"Kode masukan salah!!!";
    }
    return 0;
}
 ⁠

	⁠outputpengerjaan
	⁠![output pengerjaan kondisi](https://github.com/chafdv/Modul1-/blob/main/Modul1/outputpengerjaan/kondisi%20cpp.png)

Pertama menghitung diskon 5% jika total belanja lebih dari Rp100.000, jika kurang maka tidak ada diskon. Kedua sama, hanya lebih jelas dengan if–else. Program ketiga memakai switch case untuk menentukan hari kerja (kode 1–5), hari libur (kode 6–7), atau menampilkan pesan salah jika kode tidak valid.

### Soal 4

Perulangan

⁠ cpp
#include <iostream>
using namespace std;
// int main()
// {
//     int jum;
//     cout << "jumlah perulangan: ";
//     cin >> jum;
//     for (int i = 0; i < jum; i++)
//     {
//         cout << "saya sahroni\n";
//     }
//     return 1;
// }


// while
int main()
{
    int i = 1;
    int jum;
    cin >> jum;
    do
    {
        cout << "bahlil ke-" << (i + 1) << endl;
        i++;
    } while (i < jum);
    return 0;
}
 ⁠

	⁠outputpengerjaan
	⁠![output pengerjaan perulangan](https://github.com/chafdv/Modul1-/blob/main/Modul1/outputpengerjaan/perulangan%20cpp.png
)

Program pertama menampilkan kalimat *“saya sahroni”* berulang sesuai angka yang kita masukkan. Program kedua menampilkan kalimat *“bahlil ke-…”* berulang mulai dari 1 sampai sebelum jumlah yang kita masukkan.


### Soal 5

Fungsi

⁠ cpp
#include <iostream>
using namespace std;

// Prosedur: hanya menampilkan hasil, tidak mengembalikan nilai
void tampilkanHasil(double p, double l)
{
    cout << "\n=== Hasil Perhitungan ===" << endl;
    cout << "Panjang : " << p << endl;
    cout << "Lebar   : " << l << endl;
    cout << "Luas    : " << p * l << endl;
    cout << "Keliling: " << 2 * (p + l) << endl;
}

// Fungsi: mengembalikan nilai luas
double hitungLuas(double p, double l)
{
    return p * l;
}

// Fungsi: mengembalikan nilai keliling
double hitungKeliling(double p, double l)
{
    return 2 * (p + l);
}

int main()
{
    double panjang, lebar;

    cout << "Masukkan panjang: ";
    cin >> panjang;
    cout << "Masukkan lebar  : ";
    cin >> lebar;

    // Panggil fungsi
    double luas = hitungLuas(panjang, lebar);
    double keliling = hitungKeliling(panjang, lebar);

    cout << "\nDihitung dengan fungsi:" << endl;
    cout << "Luas      = " << luas << endl;
    cout << "Keliling  = " << keliling << endl;

    // Panggil prosedur
    tampilkanHasil(panjang, lebar);

    return 0;
}

 ⁠
	⁠outputpengerjaan
	⁠![output pengerjaan fungsi](https://github.com/chafdv/Modul1-/blob/main/Modul1/outputpengerjaan/fungsi%20cpp.png)

Program ini menghitung luas dan keliling persegi panjang. Bedanya, fungsi mengembalikan nilai hasil hitung, sedangkan prosedur langsung menampilkan hasilnya. 

### Soal 6

Test

⁠ cpp
#include <iostream>
using namespace std;
int main()
{
    string ch;
    cout << "Masukkan sebuah karakter: ";
    // cin >> ch;
    ch = getchar();  //Menggunakan getchar() untuk membaca satu karakter
    cout << "Karakter yang Anda masukkan adalah: " << ch << endl;
    return 0;
}

 ⁠

	⁠outputpengerjaan
	⁠![output pengerjaan test](https://github.com/chafdv/Modul1-/blob/main/Modul1/outputpengerjaan/test%20cpp.png)

Program ini dipakai untuk meminta kita mengetik satu huruf/karakter, lalu program akan menampilkan kembali huruf yang kita ketik.

## Unguided

### Soal 1

Buatlah program yang menerima input-an dua buah bilangan bertipe float, kemudian memberikan output-an hasil penjumlahan, pengurangan, perkalian, dan pembagian dari dua bilangan tersebut.

⁠ cpp
#include <iostream>
using namespace std;

int main() {
    float a, b;
    cout << "Masukkan bilangan pertama: ";
    cin >> a;
    cout << "Masukkan bilangan kedua: ";
    cin >> b;

    cout << "Hasil Penjumlahan: " << a + b << endl;
    cout << "Hasil Pengurangan: " << a - b << endl;
    cout << "Hasil Perkalian: " << a * b << endl;
    if (b != 0)
        cout << "Hasil Pembagian: " << a / b << endl;
    else
        cout << "Pembagian tidak dapat dilakukan (b = 0)" << endl;

    return 0;
}
 ⁠

	⁠outputpengerjaan
	⁠![output pengerjaan soal1](https://github.com/chafdv/Modul1-/blob/main/Modul1/outputpengerjaan/soal1.png)

Program ini seperti kalkulator sederhana. Kita memasukkan dua angka, lalu program akan menampilkan hasil tambah, kurang, kali, dan bagi. Kalau angka kedua yang dimasukkan nol, program memberi tahu bahwa pembagian tidak bisa dilakukan. 

---

### Soal 2

Buatlah sebuah program yang menerima masukan angka dan mengeluarkan output nilai angka tersebut dalam bentuk tulisan. Angka yang akan di-input-kan user adalah bilangan bulat positif mulai dari 0 s.d 100.  
Contoh: 79 → tujuh puluh sembilan

⁠ cpp
#include <iostream>
#include <string>
using namespace std;

string angkaSatuan[] = {"nol", "satu", "dua", "tiga", "empat", "lima", 
                        "enam", "tujuh", "delapan", "sembilan"};
string angkaBelasan[] = {"sepuluh", "sebelas", "dua belas", "tiga belas", 
                         "empat belas", "lima belas", "enam belas", 
                         "tujuh belas", "delapan belas", "sembilan belas"};
string angkaPuluhan[] = {"", "", "dua puluh", "tiga puluh", "empat puluh", 
                         "lima puluh", "enam puluh", "tujuh puluh", 
                         "delapan puluh", "sembilan puluh"};

string terbilang(int n) {
    if (n < 10) return angkaSatuan[n];
    else if (n < 20) return angkaBelasan[n - 10];
    else if (n < 100) {
        int puluh = n / 10;
        int satuan = n % 10;
        if (satuan == 0) return angkaPuluhan[puluh];
        else return angkaPuluhan[puluh] + " " + angkaSatuan[satuan];
    } else if (n == 100) {
        return "seratus";
    }
    return "";
}

int main() {
    int n;
    cout << "Masukkan angka (0-100): ";
    cin >> n;
    if (n >= 0 && n <= 100) {
        cout << n << " : " << terbilang(n) << endl;
    } else {
        cout << "Angka di luar jangkauan!" << endl;
    }
    return 0;
}
 ⁠

	⁠outputpengerjaan
	⁠![output pengerjaan soal2](https://github.com/chafdv/Modul1-/blob/main/Modul1/outputpengerjaan/soal2.png
)

Program ini mengubah angka 0 sampai 100 menjadi tulisan. Misalnya kalau kita masukkan *15* maka keluar *“lima belas”, kalau **42* keluar *“empat puluh dua”, dan kalau **100* keluar *“seratus”*. Kalau angkanya di luar 0–100, program akan bilang angkanya tidak bisa diproses. 

---

### Soal 3

Buatlah program yang dapat memberikan input dan output sebagai berikut.  
Input: 3  
Output:  

321 * 123
21 * 12
1 * 1
   *


⁠ cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    cout << "input: ";
    cin >> n;
    cout << "output:\n";

    for (int i = n; i >= 1; i--) {
        for (int j = i; j >= 1; j--) {
            cout << j;
        }
        cout << " * ";
        for (int j = 1; j <= i; j++) {
            cout << j;
        }
        cout << endl;
    }

    for (int spasi = 1; spasi <= n; spasi++) {
        cout << " ";
    }
    cout << "*" << endl;

    return 0;
}
 ⁠

	⁠outputpengerjaan
	⁠![output pengerjaan soal3](https://github.com/chafdv/Modul1-/blob/main/Modul1/outputpengerjaan/soal3.png)

Program ini menampilkan pola angka simetris dengan tanda ⁠ * ⁠ di tengah. Angka input jadi batas pola, tiap baris berisi angka menurun, ⁠ * ⁠, lalu angka menaik, dan di akhir ada satu ⁠ * ⁠ di bawah.

---


## Referensi

1.⁠ ⁠[https://www.dicoding.com/blog/memahami-esensi-bahasa-pemrograman-c/]
