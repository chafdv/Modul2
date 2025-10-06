# <h1 align="center">Laporan Praktikum Struktur Data<br> Modul 2 Pengenalan Bahasa C++ </h1>
<p align="center">Osha Alfida Valyana - 103112430202</p>

## Dasar Teori

Bahasa C++ adalah bahasa pemrograman yang dikembangkan oleh Bjarne Stroustrup pada tahun 1985 sebagai pengembangan dari bahasa C.     Dengan performa tinggi serta kontrol penuh terhadap manajemen memori, C++ banyak digunakan untuk membangun aplikasi kompleks seperti game, perangkat lunak, dan sistem berkinerja tinggi memori, C++ banyak digunakan untuk membangun aplikasi kompleks seperti game, perangkat lunak, dan sistem berkinerja tinggi.


## Guided

### Soal 1

Sruct

⁠ cpp
#include <iostream>
using namespace std;

void tukar(int *px, int *py);

int main()
{
    int a = 10, b = 20;
    cout << "Sebelum ditukar: a = " << a << ", b = " << b << endl;
    tukar(&a, &b);
    cout << "Setelah ditukar: a = " << a << ", b = " << b << endl;
    return 0;
}

void tukar(int *px, int *py)
{
    int temp = *px;
    *px = *py;
    *py = temp;
} ⁠

	⁠outputpengerjaan
	⁠![output pengerjaan struct](https://github.com/chafdv/Modul1-/blob/main/Modul1/outputpengerjaan/struct%20cpp.png)

Program diminta membuat program untuk menyimpan data mahasiswa (nama, NIM, IPK), lalu minta input dari user dan tampilkan kembali datanya.
---

### Soal 2

#include <iostream>
using namespace std;

void tukar(int &x, int &y);

int main()
{
    int a = 10, b = 20;
    cout << "Sebelum ditukar: a = " << a << ", b = " << b << endl;
    tukar(a, b);
    cout << "Setelah ditukar: a = " << a << ", b = " << b << endl;
    return 0;
}

void tukar(int &x, int &y)
{
    int temp = x;
    x = y;
    y = temp;
}

	⁠outputpengerjaan
	⁠![output pengerjaan aritmatika](https://github.com/chafdv/Modul1-/blob/main/Modul1/outputpengerjaan/aritmatika%20cpp.png)


	⁠outputpengerjaan
	⁠![output pengerjaan perulangan](https://github.com/chafdv/Modul1-/blob/main/Modul1/outputpengerjaan/perulangan%20cpp.png
)

Program pertama menampilkan kalimat *“saya sahroni”* berulang sesuai angka yang kita masukkan. Program kedua menampilkan kalimat *“bahlil ke-…”* berulang mulai dari 1 sampai sebelum jumlah yang kita masukkan.



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


## Referensi

1.⁠ ⁠[https://www.dicoding.com/blog/memahami-esensi-bahasa-pemrograman-c/]

