# <h1 align="center">Laporan Praktikum Struktur Data<br>Modul 2 Pengenalan Bahasa C++</h1>
<p align="center">Osha Alfida Valyana - 103112430202</p>

---

## Dasar Teori
Bahasa C++ adalah bahasa pemrograman yang dikembangkan oleh Bjarne Stroustrup pada tahun 1985 sebagai pengembangan dari bahasa C.     Dengan performa tinggi serta kontrol penuh terhadap manajemen memori, C++ banyak digunakan untuk membangun aplikasi kompleks seperti game, perangkat lunak, dan sistem berkinerja tinggi memori, C++ banyak digunakan untuk membangun aplikasi kompleks seperti game, perangkat lunak, dan sistem berkinerja tinggi.


---

## Guided

### Soal 1 — Call by Pointer

```cpp
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
}


	⁠output
	⁠![output]((https://github.com/chafdv/Modul2/blob/main/Modul2/output/pointer.png))

Program diminta membuat program untuk menyimpan data mahasiswa (nama, NIM, IPK), lalu minta input dari user dan tampilkan kembali datanya.
---

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


	⁠output
	⁠![output]
)

Program pertama menampilkan kalimat *“saya sahroni”* berulang sesuai angka yang kita masukkan. Program kedua menampilkan kalimat *“bahlil ke-…”* berulang mulai dari 1 sampai sebelum jumlah yang kita masukkan.



## Unguided

### Soal 1

Buatlah program yang menerima input-an dua buah bilangan bertipe float, kemudian memberikan output-an hasil penjumlahan, pengurangan, perkalian, dan pembagian dari dua bilangan tersebut.

⁠ ```cpp
#include <iostream>
using namespace std;

int main() {
    int matriks[3][3] = {
        {1, 2, 3},
        {4, 5, 6},
        {7, 8, 9}
    };
    int transpose[3][3];

    cout << "Matriks Awal:\n";
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 3; j++) {
            cout << matriks[i][j] << " ";
        }
        cout << endl;
    }

    // Proses transpose
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 3; j++) {
            transpose[j][i] = matriks[i][j];
        }
    }

    cout << "\nMatriks Hasil Transpose:\n";
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 3; j++) {
            cout << transpose[i][j] << " ";
        }
        cout << endl;
    }

    return 0;
}

	⁠output
	⁠![output](https://github.com/chafdv/Modul1-/blob/main/Modul1/outputpengerjaan/soal1.png)

Program ini seperti kalkulator sederhana. Kita memasukkan dua angka, lalu program akan menampilkan hasil tambah, kurang, kali, dan bagi. Kalau angka kedua yang dimasukkan nol, program memberi tahu bahwa pembagian tidak bisa dilakukan. 

---

### Soal 2

Buatlah sebuah program yang menerima masukan angka dan mengeluarkan output nilai angka tersebut dalam bentuk tulisan. Angka yang akan di-input-kan user adalah bilangan bulat positif mulai dari 0 s.d 100.  
Contoh: 79 → tujuh puluh sembilan

⁠ ``cpp
#include <iostream>
using namespace std;

void kuadratkan(int &x) {
    x = x * x;
}

int main() {
    int nilai = 5;
    cout << "Nilai awal: " << nilai << endl;
    kuadratkan(nilai);
    cout << "Nilai setelah dikuadratkan: " << nilai << endl;
    return 0;
}


	⁠output
	⁠![output(https://github.com/chafdv/Modul1-/blob/main/Modul1/outputpengerjaan/soal2.png
)

Program ini mengubah angka 0 sampai 100 menjadi tulisan. Misalnya kalau kita masukkan *15* maka keluar *“lima belas”, kalau **42* keluar *“empat puluh dua”, dan kalau **100* keluar *“seratus”*. Kalau angkanya di luar 0–100, program akan bilang angkanya tidak bisa diproses. 

---


## Referensi

1.⁠ ⁠[https://www.dicoding.com/blog/memahami-esensi-bahasa-pemrograman-c/]

