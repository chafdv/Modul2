# <h1 align="center">Laporan Praktikum Struktur Data<br> Modul 2 Pengenalan C++ Bagian 2 </h1>
<p align="center">Osha Alfida Valyana/ 103112430202</p>

## Dasar Teori
Bahasa C++ adalah bahasa pemrograman yang dikembangkan oleh Bjarne Stroustrup pada tahun 1985 sebagai pengembangan dari bahasa C.     Dengan performa tinggi serta kontrol penuh terhadap manajemen memori, C++ banyak digunakan untuk membangun aplikasi kompleks seperti game, perangkat lunak, dan sistem berkinerja tinggi memori, C++ banyak digunakan untuk membangun aplikasi kompleks seperti game, perangkat lunak, dan sistem berkinerja tinggi.


## Guided

### Soal 1 Call By Pointer

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

```

> output 
> ![output Soal 1](https://github.com/chafdv/Modul2/blob/main/Modul2/output/pointer.png)

Program ini membuktikan bahwa dengan menggunakan pointer, kita dapat mengubah nilai variabel asli yang ada di fungsi main() karena pointer mengakses langsung alamat memorinya. Hal ini menunjukkan konsep call by address (pemanggilan berdasarkan alamat), yaitu ketika sebuah fungsi menerima alamat variabel sebagai parameter, bukan salinan nilainya. Dengan menggunakan operator dereference (*) pada pointer, kita dapat mengambil dan memodifikasi nilai dari alamat yang ditunjuk tersebut.
---

### Soal 2 Call By Reference

```cpp
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

```

> output  
> ![output Soal 2](https://github.com/chafdv/Modul2/blob/main/Modul2/output/reference.png)

Program ini menunjukkan penggunaan call by reference, di mana fungsi menerima referensi langsung dari variabel, bukan salinannya. Parameter int &x dan int &y mereferensikan variabel a dan b, sehingga perubahan pada x dan y di dalam fungsi tukar() langsung mengubah nilai asli a dan b. Program ini menukar nilai kedua variabel tanpa menggunakan pointer.

## Unguided

### Soal 1

Buatlah sebuah program untuk melakukan transpose pada sebuah matriks persegi berukuran 3x3. Operasi transpose adalah mengubah baris menjadi kolom dan sebaliknya. Inisialisasi matriks awal di dalam kode, kemudian buat logika untuk melakukan transpose dan simpan hasilnya ke dalam matriks baru. Terakhir, tampilkan matriks awal dan matriks hasil transpose.

```cpp
#include <iostream>
using namespace std;

int main() {
    int matriks[3][3] = {
        {1, 2, 3},
        {4, 5, 6},
        {7, 8, 9}
    };

    int transpose[3][3];

    // Proses transpose
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 3; j++) {
            transpose[j][i] = matriks[i][j];
        }
    }

    cout << "Matriks Awal:" << endl;
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 3; j++) {
            cout << matriks[i][j] << " ";
        }
        cout << endl;
    }

    cout << "\nMatriks Hasil Transpose:" << endl;
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 3; j++) {
            cout << transpose[i][j] << " ";
        }
        cout << endl;
    }

    return 0;
}

```

> output  
> ![output Soal 1](https://github.com/chafdv/Modul2/blob/main/Modul2/output/unguided1.png)

Program ini membuat matriks 3x3 secara statis, lalu menukar posisi elemen baris dan kolom menggunakan dua perulangan for.
Setiap elemen [i][j] dipindahkan ke posisi [j][i] pada matriks baru.
Hasilnya, matriks yang semula baris menjadi kolom.
---

### Soal 2

Buatlah program yang menunjukkan penggunaan call by reference. Buat sebuah prosedur bernama kuadratkan yang menerima satu parameter integer secara referensi (&). Prosedur ini akan mengubah nilai asli variabel yang dilewatkan dengan nilai kuadratnya. Tampilkan nilai variabel di main() sebelum dan sesudah memanggil prosedur untuk membuktikan perubahannya.

```cpp
#include <iostream>
using namespace std;

void kuadratkan(int &angka) {
    angka = angka * angka;
}

int main() {
    int nilai = 5;
    cout << "Nilai awal: " << nilai << endl;

    kuadratkan(nilai);

    cout << "Nilai setelah dikuadratkan: " << nilai << endl;
    return 0;
}

```

> output 
> ![output Soal 2](https://github.com/chafdv/Modul2/blob/main/Modul2/output/unguided2.png)

Program ini menunjukkan penggunaan call by reference dengan operator &.
Parameter x pada fungsi kuadratkan() mengacu langsung ke variabel nilai di fungsi main().
Sehingga, perubahan nilai x di dalam fungsi juga mengubah nilai asli nilai tanpa perlu return value.

## Referensi

1. [https://www.dicoding.com/blog/memahami-esensi-bahasa-pemrograman-c/] 
