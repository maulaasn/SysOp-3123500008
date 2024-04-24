<div align="center">
  <h1 class="text-align: center;font-weight: bold">Praktikum 8<br>Sistem Operasi</h1>
  <h3 class="text-align: center;">Dosen Pengampu : Dr. Ferry Astika Saputra, S.T., M.Sc.</h3>
</div>
<br />
<div align="center">
  <img src="https://upload.wikimedia.org/wikipedia/id/4/44/Logo_PENS.png" alt="Logo PENS">
  <h3 style="text-align: center;">Disusun Oleh : <br>Kelompok 4</h3>
  <p style="text-align: center;">
    <strong>Muhammad Yafi Rifdah Zayyan (3123500001)</strong><br>
    <strong>Muhammad Daffa Erfiansyah (3123500006)</strong><br>
    <strong>Maula Shahihah Nur Sa'adah (3123500008)</strong>
  </p>

<h3 style="text-align: center;line-height: 1.5">Politeknik Elektronika Negeri Surabaya<br>Departemen Teknik Informatika Dan Komputer<br>Program Studi Teknik Informatika<br>2023/2024</h3>
  <hr><hr>
</div>

## Bash Programming 

### Pengertian Bash
Bash kependekan dari Bourne Again Shell, adalah open source command line interpreter dan scripting language. Ini menafsirkan perintah yang dimasukkan pengguna, baik secara interaktif atau dari file skrip.
Ini berfungsi sebagai interface untuk memanggil perintah, memungkinkan system function calls.
Ada 2 tipe dari mode bash
- **Interactive Mode**
    Juga disebut sebagai command intepreter, memungkinkan eksekusi perintah di terminal. Ini mengeksekusi perintah secara berurutan jika ada beberapa perintah.
- **Non-interactive Mode**
    Ini merujuk pada scrpts, memungkinkan Anda menulis Bash syntax yang berisi rangkaian beberapa perintah untuk eksekusi skrip.

### Perbedaan Bash dan Shell
Shell, alias Bourne Shell, adalah command-line interpreter untuk OS Unix dan Linux. Bash, alias Bourne Again Shell, adalah versi yang disempurnakan.

### Kegunaan Skrip Bash 

Skrip Bash memiliki banyak kasus penggunaan, termasuk:
- Menulis skrip untuk mengotomatiskan tugas pemrograman
- Menyinkronkan tugas untuk menyalin file
- Menjalankan tugas cron untuk penjadwalan

### Cara menulis kode di Bash
Untuk menulis kode dalam skrip Bash, ikuti langkah-langkah berikut:
- Di terminal, buat file menggunakan `vi test.sh`.
- Tambahkan `#!/bin/bash` di bagian atas file.
- Tambahkan beberapa cuplikan kode shell.
- Simpan file shell dengan `.sh` ekstensi.
- Jalankan skrip shell menggunakan `./test.sh` perintah di terminal.

### Apakah bash termasuk bahasa pengkodean?
Bash menjalankan perintah dari terminal atau file. Ini adalah bahasa pemrograman yang beroperasi pada sistem operasi kernel Unix/Linux, berisi semua fitur untuk menulis kode lengkap.
Bash adalah tipe shell khusus yang menerima masukan dari perintah, menjalankan kode, dan memproses masukan, serta mengembalikan hasilnya.
### Jenis Shell
Ada berbagai jenis shell di OS Unix.
<table>
<thead>
<tr>
  <th style="background-color: blue; color: white">Tipe Cangkang</th>
  <th style="background-color: blue; color: white">Alias</th>
  <th style="background-color: blue; color: white">Garis Pertama</th>
<tr>
</thead>
<tbody>
  <tr>
  <td>SH</td>
  <td>Bourne Shell</td>
  <td>#!/bin/sh</td>
  </tr>
   <tr>
  <td>bash</td>
  <td>Bourne Again Shell</td>
  <td>#!/bin/bash</td>
  </tr>
   <tr>
  <td>cshell</td>
  <td>C shel</td>
  <td>#!/bin/csh</td>
  </tr>
</tbody>
</table>
| tcsh | TENEX C shell | #!/bin/tcsh | | | | ksh | Korn shell | #!/bin/ksh |

### Perbedaan Command Line dan Script di Bash
Perbedaan antara baris perintah dan skrip
Opsi baris perintah
- Baris perintah memiliki prompt yang menerima masukan dari pengguna
- Perintah tidak disimpan ke file.
- Ini hanya mendukung satu perintah pada satu waktu.
File skrip
- Mendukung banyak perintah dalam satu file
- Prompt masih dapat ditulis dalam file skrip
- Hanya satu baris dalam sebuah file yang dijalankan secara berurutan

## Bash - Variables

### Bash Shell Variable
**Deklarasi Variable**: Untuk membuat variable, maka harus memberikan nilai padanya
``` 
variableName=VariableValue
```
Keterangan: 
- variableName: dapat berisi kombinasi huruf apa saja, angka, dan garis bawah
- variableValue: adalah nilai yang disimpan dalam variabel, dan dapat berupa angka, string atau boolean. Simbol `=` digunakan untuk memberikan nilai pada suatu variabel.
Misalnya
```
AGE=25
```
### How to Access Variables in Bash

![App Screenshot](img/variables/2.png)

Pertama adalah mendeklarasikan variable *AGE* dengan memberikan nilai 25. Kemudian menggunakan `echo` untuk menampilkan outputnya. Simbol dollar `$` sebelum nama variable sangat penting untuk mengakses nilainya.

![App Screenshot](img/variables/3.png)

### Bash Shell Readonly Variables

![App Screenshot](img/variables/4.png)

Setelah variabel diberi nilai, kita dapat mengubahnya ke nilai baru menggunakan operator penugasan =

![App Screenshot](img/variables/5.png)

**Membuat Variable tidak dapat diperbarui**

![App Screenshot](img/variables/6.png)

keyword `readonly` mencegah variable untuk diperbarui, secara efektif mengubahnya menjadi `constant`

![App Screenshot](img/variables/7.png)

#### Bash unset variable

Keyword `unset` membantu menghilangkan nilai dari variable yang ditentukan. Variable tetap dapat diakses tetapi mencetak nilai kosong.

![App Screenshot](img/variables/8.png)

Output:

![App Screenshot](img/variables/9.png)

### Bash Global Variables

![App Screenshot](img/variables/10.png)

Output:

![App Screenshot](img/variables/11.png)

### Bash Local variables

![App Screenshot](img/variables/13.png)

Output:

![App Screenshot](img/variables/14.png)

## Bash - Loop File

### Perulangan while

![App Screenshot](img/loop-file/1.png)

Output:

![App Screenshot](img/loop-file/3.png)

Output diatas merupakan isi dari file `filename.txt` 

![App Screenshot](img/loop-file/2.png)

## Bash - Comments

### Single line Comment in bash shell
![App Screenshot](img/comments/1.png)

Output:

![App Screenshot](img/comments/2.png)

### Multi-Line comments in a shell script
![App Screenshot](img/comments/3.png)

Output:

![App Screenshot](img/comments/4.png)

## Bash - Arrays

### How to declare and create an array?
- Declare an array
  ![App Screenshot](img/arrays/2.png)

  ![App Screenshot](img/arrays/3.png)

  ![App Screenshot](img/arrays/4.png)

- Assign the values without declaring an array
  ![App Screenshot](img/arrays/5.png)

### Access the array values
![App Screenshot](img/arrays/6.png)

### Declare an Array of numbers and loop through
![App Screenshot](img/arrays/7.jpeg)

Output:

![App Screenshot](img/arrays/8.png)

### Declare an Array of strings and loop through
![App Screenshot](img/arrays/9.png)

Output:

![App Screenshot](img/arrays/10.png)

### Access the first elements of an array
![App Screenshot](img/arrays/11.png)

Output:

![App Screenshot](img/arrays/12.png)

### Get the last element of an array
Dalam skrip bash, dapat menggunakan indeks=-1 untuk mendapatkan elemen array terakhir.

![App Screenshot](img/arrays/13.png)

Dengan versi bash 4.0 terbaru, dapat menggunakan sintaks di bawah ini untuk membaca elemen terakhir.

![App Screenshot](img/arrays/15.png)

Output:

![App Screenshot](img/arrays/14.png)

### Iterate or loop array elements
For loop digunakan untuk mengulangi elemen.

Berikut adalah contoh contoh loop array untuk mencetak semua elemen

![App Screenshot](img/arrays/9.png)

Output:

![App Screenshot](img/arrays/18.png)

Cara lain untuk mencetak indeks dan elemen array menggunakan for loop.

![App Screenshot](img/arrays/19.png)

Output:

![App Screenshot](img/arrays/20.png)

### Print all array elements
Gunakan [@] atau [*] untuk mencetak semua elemen array.

![App Screenshot](img/arrays/21.png)

Output:

![App Screenshot](img/arrays/22.png)

### Remove an element from an array
Menghapus elemen dari array menggunakan `unset` indeks tertentu.

![App Screenshot](img/arrays/23.png)

Output:

![App Screenshot](img/arrays/24.png)

### Adding an element to an array
Contoh penambahan elemen awal dan akhir serta tengah

![App Screenshot](img/arrays/25.png)

Output:

![App Screenshot](img/arrays/26.png)

### Length of an array
![App Screenshot](img/arrays/27.png)

Output:

![App Screenshot](img/arrays/28.png)

## Bash - Expansion
![App Screenshot](img/expansion/1.png)

Output:

![App Screenshot](img/expansion/2.png)

## Bash - Conditional Expression
Ekspresi kondisional dievaluasi pada waktu eksekusi skrip, berdasarkan hasil, Ia mengeksekusi blok perintah tertentu.

Ada berbagai jenis ekspresi kondisional di Bash

- Operator Perbandingan String
- Operator Perbandingan Numerik
- Operator File
- Operator Logis

### Operator File
Bash menyediakan operator logika pada FIle dan direktori untuk menguji ekspresi kondisional. Ini memungkinkan Anda untuk memeriksa berbagai operasi seperti keberadaan, dan izin, ukuran. Ini digunakan ekspresi kondisional dalam pernyataan kondisional seperti if else dan case.

Syntax:

![App Screenshot](img/condional-expression/1.png)

## Bash - Case Statements
Pernyataan case mirip dengan switch case dalam bahasa pemrograman lain.
Ini digunakan untuk membandingkan masukan yang diberikan dengan beberapa pola, dan perintah di dalam pola yang cocok dijalankan.

Syntax:
![App Screenshot](img/case-statements/1.png)

- expression adalah variabel atau expression yang valid untuk dievaluasi
- Ini berisi pola defiend di dalam case yang dievaluasi dengan membandingkan expression, mencocokkan case fuound, mengeksekusi perintah di dalamnya.
- case default ( `*)`) untuk dijalankan jika tidak ada pola yang cocok
- Setiap blok pola diakhiri dengan `;;`
`case` adalah kata awal dan `esac` merupakan kata yang mengakhiri pernyataan kasus

Contohnya sebagai berikut:

![App Screenshot](img/case-statements/2.png)

Output:

![App Screenshot](img/case-statements/3.png)

## Bash - Special Characters
### Blankspace(" “):
![App Screenshot](img/special-characters/1.png)

Output:

![App Screenshot](img/special-characters/2.png)

### Expansion($)
### Ambersand (&)
### Pipe (|)
### Semicolon(;)
### Single quotes
![App Screenshot](img/special-characters/5.png)

Output:

![App Screenshot](img/special-characters/6.png)

Jika kutipan tunggal berisi quoe tunggal bersarang, Anda harus menghindarinya menggunakan ```.

![App Screenshot](img/special-characters/7.png)

Output:

![App Screenshot](img/special-characters/8.png)
Contoh berisi ``` adalah karakter kutipan tunggal di dalam kutipan tunggal

### Double quotes
![App Screenshot](img/special-characters/9.png)

Output:

![App Screenshot](img/special-characters/10.png)

### Backslash Character (\\)
![App Screenshot](img/special-characters/11.png)

Output:

![App Screenshot](img/special-characters/12.png)

### Comment (#)
![App Screenshot](img/special-characters/13.png)

Output:

![App Screenshot](img/special-characters/14.png)

## Bash - if elif else

### Bash Shell Conditional Statements
![App Screenshot](img/if-elif-else/1.png)
- Pernyataan tersebut `if` digunakan untuk mengeksekusi blok kode jika suatu kondisi benar, dengan sintaksis `if then fi`.
- Pernyataan `else` digunakan untuk mengeksekusi kode jika suatu kondisi salah, mengikuti sintaksis `if then else fi`.
- Pernyataan `if..elif..else` berguna ketika Anda perlu mengeksekusi kode jika tidak ada kondisi sebelumnya yang benar.

### If Conditional Statements
Pernyataan `if` di Bash digunakan untuk mengeksekusi blok kode ketika kondisi tertentu adalah `true`.

![App Screenshot](img/if-elif-else/2.png)

Contoh:

![App Screenshot](img/if-elif-else/3.png)

Output:

![App Screenshot](img/if-elif-else/4.png)

### If-Else Conditional Statements
Pernyataan `if-else` kondisional di Bash memungkinkan Anda untuk mengeksekusi blok kode yang berbeda tergantung pada apakah suatu kondisi `true`` atau `false`.

![App Screenshot](img/if-elif-else/5.png)

Contoh:

![App Screenshot](img/if-elif-else/6.png)

Output:

![App Screenshot](img/if-elif-else/7.png)

### If..Elif..Else Statements
Gunakan `if..elif..else` pernyataan kondisional di Bash untuk mengeksekusi blok kode berbeda berdasarkan beberapa kondisi.

![App Screenshot](img/if-elif-else/8.png)

Contoh:

![App Screenshot](img/if-elif-else/9.png)

Output:

![App Screenshot](img/if-elif-else/10.png)

## Bash - Loops

### For loop
For loop digunakan untuk mengeksekusi kode beberapa kali.

![App Screenshot](img/loops/1.png)

Contoh:

![App Screenshot](img/loops/2.png)

Output:

![App Screenshot](img/loops/3.png)

### For index loop
Untuk loop indeks mirip dengan bahasa C. Ini mengeksekusi kode beberapa kali berdasarkan kondisi benar, dimulai dengan nilai awal dan iterasi berisi nilai yang akan bertambah 1.

![App Screenshot](img/loops/4.png)

Contoh:

![App Screenshot](img/loops/5.png)

Output:

![App Screenshot](img/loops/6.png)
Ini mencetak angka dari 0 hingga 5

### While loop in bash
Perulangan `while` di Bash memungkinkan eksekusi kode berulang selama kondisi yang ditentukan adalah `true`. Jika kondisinya menjadi `false`, perulangan akan keluar.

![App Screenshot](img/loops/7.png)

Contoh:

![App Screenshot](img/loops/8.png)

Output:

![App Screenshot](img/loops/9.png)
while loop mengeksekusi kode selama kondisi yang ditentukan ( `[[ i -lt 100 ]]`) benar. Blok kode menambah nilai sebesar 1 dan mencetak nilainya. Jika kondisi salah, loop keluar.

### Until loop in bash
Kata `until` kunci di Bash digunakan untuk mengeksekusi kode berulang kali hingga kondisi tertentu menjadi `true`, di mana loop keluar.

![App Screenshot](img/loops/10.png)

Contoh:

![App Screenshot](img/loops/11.png)

Output:

![App Screenshot](img/loops/12.png)
Dalam contoh ini, blok kode dijalankan selama `[[ i -eq 100 ]]` bernilai salah. Ini menambah nilai sebesar 1 dan mencetak nilainya. Output mencetak angka dari 0 hingga 99 angka.

## Bash - Append String

### Bash Athematic expressions
![App Screenshot](img/append-string/1.png)
Output:

![App Screenshot](img/append-string/2.png)
Ekspresi artema dibuat menggunakan operator di bawah ini

- Operator Artmatik
- Operator Perbandingan

Operator perbandingan digunakan untuk mengecek satu sama lain dengan membandingkan nilai Operator ( `<, <=, >, >=, ==, !=` )

![App Screenshot](img/append-string/3.png)
Output:

![App Screenshot](img/append-string/4.png)

### Bash Athematic Expansion
`Expansion` sama dengan ekspresi, menghitung nilai ekspresi dan hasilnya diganti dengan nilai. Dan selalu diawali dengan tanda dolar.

![App Screenshot](img/append-string/5.png)
Output:

![App Screenshot](img/append-string/6.png)

### Bash - Functions

### How to declare a Function and call it
Definisi fungsi berisi beberapa baris kode yang akan dieksekusi.
Fungsi berisi nama fungsi yang diapit `{}`.

![App Screenshot](img/functions/1.png)

### How to pass a parameters to an function
![App Screenshot](img/functions/2.png)

Parameter dapat diakses menggunakan $1 $2 $3.. $n

![App Screenshot](img/functions/3.png)

## Bash - Append String

### Simple variable append
Mendeklarasikan dua variabel string dalam skrip bash, yang dapat dicetak ke konsol menggunakan echo dengan mengapit variabel dalam tanda kutip ganda.

![App Screenshot](img/append-string-2/1.png)

Dapat juga menambahkan tanpa tanda kutip ganda.

![App Screenshot](img/append-string-2/3.png)

Output:

![App Screenshot](img/append-string-2/2.png)
![App Screenshot](img/append-string-2/4.png)

Contoh lain melibatkan penggabungan string ke variabel yang sama dan mencetaknya ke konsol:

![App Screenshot](img/append-string-2/5.png)

Output:

![App Screenshot](img/append-string-2/6.png)

### Use Shorthand Arithmetic Operator
Operator aritmatika singkat ( `+=` ) biasanya digunakan dalam aritmatika untuk menambahkan nilai ke suatu variabel. Ini juga dapat digunakan untuk menambahkan string ke variabel.

Misalnya.

`a+=1` setara dengan `a=a+1` dalam hal angka.
`str+="test"` akan menjadi `str=str+"test"` dalam kasus string.

![App Screenshot](img/append-string-2/7.png)

Output:

![App Screenshot](img/append-string-2/8.png)

### Use printf command
`printf` digunakan untuk memformat string dengan berbagai opsi pemformatan yang kompleks. Kita dapat menggunakan `printf` perintah untuk menggabungkan string. Formatnya adalah `%s%s` , menambahkan dua variabel string.

![App Screenshot](img/append-string-2/9.png)

Output:

![App Screenshot](img/append-string-2/10.png)

### Using here string
`Here strings` adalah sintaks khusus untuk meneruskan string ke perintah dalam skrip bash. Digunakan untuk meneruskan string input tanpa menggunakan sumber lain, seperti file. Ini memungkinkan meneruskan string ke perintah bash apapun dari file atau baris perintah.

command: valid command `<<<` : is a `here string operator`

![App Screenshot](img/append-string-2/11.png)

Output:

![App Screenshot](img/append-string-2/12.png)