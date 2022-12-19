# Ujian Akhir Semester 
<br>Mata Kuliah 	:Dasar Pemrograman
<br> Nama		:Muhammad Fikri Zaelani
<br>NIM		:	1227050078
<br>Jurusan		:[Teknik Informatika](http://if.uinsgd.ac.id/) [UIN Sunan Gunung Djati Bandung](https://uinsgd.ac.id/) 

## Deskripsi Umum
Array dua dimensi adalah sebutan untuk array yang penomoran index-nya menggunakan 2 buah angka. Analogi lain adalah matriks. Matrixs Merupakan kumpulan-kumpulan bilangan yang disusun secara baris (vertikal) dan kolom (horizontal) bisa disebut juga array dua dimensi (multi-dimensional). Transpose Matriks adalah memperoleh sebuah matriks dengan cara menukar baris menjadi kolom dan kolom menjadi baris dari sebuah matriks. Dalam matematika, matriks terdiri dari kolom dan baris. Kembali, untuk menentukan nilai dari sebuah matriks, kita harus sebut secara berpasangan seperti baris 1 kolom 1, atau baris 2 kolom 3, dst. Konsep seperti inilah yang menjadi dasar dari array 2 dimensi. Untuk membuat array 2 dimensi di dalam bahasa C++, caranya tulis 2 kali tanda kurung siku setelah nama variabel, seperti contoh berikut: int arr[2][2]; Untuk UAS kali ini kami diminta membuat 2 buah program yaitu program pertama adalah membuat array 2 dimensi dengan baris , kolom dan nilai nya di input lalu ditukarkan antara kolom dan baris sedangkan program ke dua digunakan untuk mencari nilai yang dapat di bagi 3, 7, dan 5.

## Source Code 1
    #include <iostream>
    using namespace std;

    int main() {
     int arr[100][100], transpose[100][100], baris, kolom;

       cout << "Muhamad Fikri Zaelani" << endl;
      cout << "1227050078" << endl;
      cout << "IF-B" << endl;
      cout << "=======================================" << endl;
      cout << "^Program C++ Transpose Matrix Ordo 2^" << endl;
      cout << "=======================================" << endl;

     cout << "baris: "; cin >> baris;
     cout << "kolom: "; cin >> kolom;

     for(int i=0; i<baris; i++){
      for(int j=0; j<kolom; j++){
       cout << "arr ke["<<i <<"."<<j<<"]: "; cin >> arr[i][j];
      }
     }

     cout << endl;

     for(int i=0; i<baris; i++){
      for(int j=0; j<kolom; j++){
       cout << arr[i][j] << " ";
       if(j == kolom - 1);
      }
      cout << endl;
     }

     cout << endl;

     for(int i=0; i<baris; i++){
      for(int j=0; j<kolom; j++){
       transpose[j][i] = arr[i][j];
      }
     }

     for(int i=0; i<kolom; i++){
      for(int j=0; j<baris; j++){
       cout << transpose[i][j] << " ";
       if(j == baris - 1);
      }
      cout << endl;
     }
    }
## Source Code 2
    #include <iostream>

    using namespace std;

    int main() {
       int matrix[100][100], baris, kolom, num;

       cout << "Muhamad Fikri Zaelani" << endl;
      cout << "1227050078" << endl;
      cout << "IF-B" << endl;
      cout << "=======================================" << endl;
      cout << "^Program C++ Matrix Ordo 2 habis dibagi 3 5 7^" << endl;
      cout << "=======================================" << endl;
      // Membuat matriks dengan ukuran 


       cout << "baris: "; cin >> baris;
     cout << "kolom: "; cin >> kolom;

      // Menambahkan elemen ke dalam matriks
      for (int i = 0; i < baris; i++) {
        for (int j = 0; j < kolom; j++) {

        cout << "Matriks ke["<<i <<"."<<j<<"]: ";
          cin >> num;
          // Menambahkan elemen ke dalam matriks jika habis dibagi oleh 3, 5, atau 7
          if (num % 3 == 0 || num % 5 == 0 || num % 7 == 0) {
            matrix[i][j] = num;
          }
        }
      }

      // Mencetak matriks
      for (int i = 0; i < baris; i++) {
        for (int j = 0; j < kolom; j++) {
          cout << matrix[i][j] << " ";
        }
        cout << endl;
      }

      return 0;
    }

## Output 1
![Screenshot_2022-12-19-15-10-37-46](https://user-images.githubusercontent.com/118877849/208385190-76e636a5-b82e-41af-818d-da503d6da251.jpg)

## Output 2
![Screenshot_2022-12-19-15-09-37-41](https://user-images.githubusercontent.com/118877849/208385669-dfa8857f-4e68-4f8e-b371-1482ac28e08d.jpg)

