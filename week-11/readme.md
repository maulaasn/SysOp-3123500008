<div align="center">
  <h1 class="text-align: center;font-weight: bold">Praktikum 11<br>Sistem Operasi</h1>
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

## Scheduling Algorithms

### First-Come First-Serve Algorithm (FCFS)

#### Contoh perhitungan proses secara teori

![App Screenshot](img/teori-fcfs.png)

#### Hasil percobaan running program

![App Screenshot](img/fcfs.png)

#### Flowchart FCFS

![App Screenshot](img/flowchart-fcfs.png)

#### Analisis
First-Come First-Serve (FCFS) Scheduling adalah seperti sistem antrian linier, dimana proses yang pertama datang (arrival time paling awal) akan dijalankan atau dilayani terlebih dahulu, sehingga proses berjalan berurutan. Namun, jika antriannya panjang dan proses yang dilayani memiliki durasi yang tidak merata, maka FCFS bisa menjadi kurang efisien.

--- 

### Shortest Job First (SJF)

#### Contoh perhitungan proses secara teori

![App Screenshot](img/teori-sjf.png)

#### Hasil percobaan running program

![App Screenshot](img/sjf.png)

#### Flowchart SJF

![App Screenshot](img/flowhart-sjf.png)

#### Analisis
Shortest Job First (SJF) Scheduling adalah algoritma penjadwalan yang efektif untuk meminimalkan waktu tunggu rata-rata dan meningkatkan kinerja sistem, terutama ketika terdapat proses dengan burst time yang tidak merata. Proses ini berjalan dengan memprioritaskan jumlah burst time yang paling sedikit dan melihat arrival time nya. Proses berjalannya adalah proses yang pertama kali datang akan di execute sampai selesai dahulu, lalu proses yang ada di ready queue akan dibandingkan manakah yang memiliki burst time yang paling sedikit, akan di-execute. Jika ada kondisi dimana suatu proses memiliki burst time yang sama, maka yang didahulukan adalah proses yang arrival timenya lebih kecil (yang datang lebih dulu).

---

### Round Robin (RR)

#### Contoh perhitungan proses secara teori

![App Screenshot](img/teori-roundrobin.png)

#### Hasil percobaan running program

![App Screenshot](img/round-robin.png)

#### Flowchart Round Robin

![App Screenshot](img/flowchart-roundrobin.png)

#### Analisis
Round-Robin (RR) Scheduling merupakan salah satu algoritma scheduling pada CPU dimana semua proses yang dijalankan oleh algoritma ini akan dieksekusi secara Cyclic. Dengan kata lain, algoritma ini akan menjalankan suatu proses dalam batas waktu tertentu dan apabila proses tersebut telah berjalan melewati batas waktu yang ditentukan, maka proses ini akan otomatis diberhentikan sementara dan dimasukkan ke dalam antrian proses (queue) yang paling belakang (kemudian algoritma ini akan lanjut menjalankan proses lain dari queue yang paling depan). Dari percobaan diatas, detail output dari queue bagaimana proses berjalan yaitu dimulai dari P1 -> P2 -> P1 -> P3 -> P2.
