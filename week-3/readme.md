<div align="center">
  <h1 style="text-align: center;font-weight: bold">Pratikum 3<br>Sistem Operasi</h1>
  <h4 style="text-align: center;">Dosen Pengampu : Dr. Ferry Astika Saputra, S.T., M.Sc.</h4>
</div>
<br/>
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

<div>
<h2 align="center">Iops Dan Flops</h2>
<h2>Definisi</h2>
<h3>IOPS</h3>
<p>Input/output operations per second(IOPS) adalah pengukuran kinerja input/output yang digunakan untuk mengkarakterisasi perangkat penyimpanan komputer seperti hard disk drive (HDD), solid state drive (SSD), dan jaringan area penyimpanan (SAN). Seperti tolak ukur, angka IOPS yang diterbitkan oleh produsen perangkat penyimpanan tidak secara langsung berhubungan dengan kinerja aplikasi dunia nyata.</p>
<h3>FLOPS</h3>
<p>Dalam komputasi, floating point operations per second (FLOPS, flops or flop/s) adalah ukuran kinerja komputer, berguna dalam bidang perhitungan ilmiah yang memerlukan perhitungan floating-point. Untuk kasus seperti itu, ini adalah ukuran yang lebih akurat daripada mengukur instruksi per detik.</p>
<br>
<h2 align="center">Melakukan Benchmarking pada PC</h2>
<p>1. Melakukan Instalasi Package GCC,Make dan Git pada Debian 12 yang sudah terinstall</p>
<div align="center">
![App Screenshot](img/sudo%20apt%20update.png)
<p>Lakukan perintah "$ sudo apt update" pada terminal kemudian ketik "$ sudo apt install gcc" untuk menginstall compile dan "$ sudo apt install git" untuk menginstall git pada debian</p>
</div>
<p>2. Melakukan Git clone pada Debian 12</p>
<div align="center">
![App Screenshot](img/git%20clone.png)
<p>Arahkan direktori pada terminal yang ingin dituju lalu ketik "$ git init" kemudian "$ git clone (paste link github) lalu tekan enter</p>
</div>
<p>3. Melakukan Build Binaries,Cleaning, dan Install Binaries</p>
<div align="center">
![App Screenshot](img/make.png)
<p>Arahkan direktori pada folder flops/iops yang telah dilakukan git clone pada langkah sebelumnya kemudian buka terminal dan ketik "$ make"</p>
![App Screenshot](img/make%20clean.png)
<p>Kemudian lakukan perintah "$ make clean" lalu ketik "$ sudo make install" untuk menginstall binaries pada debian.</p>
</div>
<p>4. Melakukan Proses Benchmarking menggunakan Iops dan Flops</p>
<div align="center">
![App Screenshot](img/iops64.png)
<p>Untuk benchmarking menggunakan iops ketik pada terminal "$ iops32 $(nproc)" atau iops64 sesuaikan dengan spesifikasi laptop yang dipakai</p>
![App Screenshot](img/flops64.png)
<p>Untuk benchmarking pada flops sama seperti iops hanya saja mengganti dari iops menjadi flops "$ flops32 $(nproc)" atau $ flops64 $(nproc)</p>
</div>
<br>
<h2 align="center">Analisa Hasil Benchmarking</h2>

<p align-items="center">
<p justify-content="center">

|                      | IOPS (Integer)         | FLOPS (Floating Point)    |
|                      | IOPS64 (Integer)         | FLOPS64 (Floating Point)    |
|----------------------|------------------------|---------------------------|
| Total Throughput     | 6.339286 Gigaiops     | 5.637343 Gigaflops       |
| Single Core Throughput | 3.185454 Gigaiops   | 2.821573 Gigaflops       |
</p>
<p>Dengan melihat tabel di atas, dapat dilihat bahwa IOPS memiliki total throughput dan throughput single core yang lebih tinggi dibandingkan dengan FLOPS. Namun demikian, perbedaan antara total throughput dan throughput single core juga penting untuk diperhatikan karena menunjukkan seberapa baik CPU dapat mengalokasikan dan memanfaatkan sumber daya secara efisien antara inti tunggal dan total throughput.</p>
<br>
</div>
## Referensi

[IOPS](https://en.wikipedia.org/wiki/IOPS)
[FLOPS](https://en.wikipedia.org/wiki/FLOPS)