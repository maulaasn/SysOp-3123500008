<div align="center">
  <h1 class="text-align: center;font-weight: bold">Praktikum 2<br>Sistem Operasi</h1>
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

## Daftar Isi

1. [Pendahuluan](#pendahuluan)
2. [Perbedaan Legacy dan UEFI](#perbedaan-legacy-dan-uefi)
3. [Referensi](#referensi)

## Pengertian BIOS

<p>BIOS atau Basic Input Output System adalah perangkat lunak atau program antarmuka tingkat dasar sebagai pengatur proses input output data pada sebuah komputer. Sederhananya, BIOS diartikan sebagai suatu perangkat instruksi elektronik yang digunakan komputer untuk memulai sistem operasi.

BIOS ini terletak di dalam chip komputer dan dirancang sedemikian rupa untuk melindunginya dari kerusakan disk. Pembeda BIOS dengan program komputer yang lainnya adalah terletak pada bagian penyimpanan.</p>

<h3>Legacy Bios</h3>

<p><b>Legacy Bios</b> adalah proses boot yang digunakan oleh firmware BIOS. Legacy ini akan menyimpan daftar perangkat penyimpanan yang dapat di boot meliputi Floopy Disk Drives, Hard Disk Drives, Optical Disk Drives, dan sebagainya. Ketika Anda menyalakan komputer, BIOS akan melakukan Power On Self-Test (POST), kemudian sebuah speaker dari sistem internal mengeluarkan bunyi bip pendek sekali untuk menunjukkan bahwa booting berjalan normal. Bunyi bip ini membantu untuk mengidentifikasi kode dan dapat bertindak untuk memecahkan masalah lanjutan.

Setelah proses POST selesai, firmware akan memuat sektor pertama dari setiap target perangkat penyimpanan ke dalam memori. Firmware di sini juga memindai MBR (Master Boot Record) yang valid. Setelah ditemukan MBR yang valid, maka firmware akan melanjutkan eksekusi ke bootloader untuk pemilihan partisi tempat booting. Ketika salah satu bagian valid tidak ditemukan, firmware akan meneruskan ke perangkat berikutnya sesuai prioritas urutan yang dapat di boot.</p>

<h3>UEFI</h3>

<p><b>UEFI (Unified Extensible Firmware Interface)</b> adalah proses boot yang digunakan oleh firmware UEFI. Firmware UEFI akan menyimpan daftar volume boot yang valid atau disebut dengan Partisi Layanan EFI. Firmware UEFI merupakan penerus dari BIOS. UEFI menggunakan GUID Partition Table (GPT) sedangkan BIOS menggunakan skema partisi Master BOOT Record (MBR). Kedua format MBR dan GPT ini akan menentukan informasi partisi fisik pada Hard Disk.

Adapun saat prosedur POST (Power On Self-Test), firmware UEFI akan memindai semua perangkat penyimpanan yang dapat di boot dan terhubung ke sistem untuk menemukan GUID Partition Table (GPT) yang valid. Berbeda dengan MBR di Legacy, GPT di sini tidak berisi bootloader, firmware ini sendiri akan memeriksa GPT untuk menemukan Partisi Layanan EFI untuk boot.

Dengan mode boot UEFI, Anda dimungkinkan melakukan pengontrolan antarmuka menggunakan perangkat mouse, sedangkan di BIOS biasanya menggunakan keyboard untuk mengontrol opsi. UEFI termasuk mode boot yang modern dan dijamin aman, ini juga dapat mencegah perangkat lunak berbahaya.</p>

## Perbedaan Legacy dan UEFI

![App Screenshot](img/perbedaan%20legacy%20uefi.jpg)

| <p align="center">Spesifikasi</p>   | <p align="center">Legacy</p>  | <p align="center">UEFI</p>  |
| ----------- | ---------- | --------- |
| Skema Pemeriksaan Partisi | Master Boot Record (MBR) | GUID Partition Table (GPT) |
| Proses Booting | Proses booting komputer menggunakan firmware BIOS. | Proses booting pada komputer modern yang menyediakan kemampuan lebih canggih daripada BIOS. |
| Jumlah maksimum partisi primer | 4 partisi | Tidak terbatas (tergantung pada sistem operasi; pada Windows dapat digunakan hingga 128 partisi). |
| Ukuran partisi maksimum | 2 terabyte (2.000 Gigabyte) | 18 exabyte (18 miliar Gigabyte) |
| Ukuran hard drive maksimum | 2 terabyte (2.000 Gigabyte) | 18 exabyte (18 miliar Gigabyte) |
| Keamanan | Sektor data tidak menggunakan checksum | Sektor data menggunakan checksum CRC32 dan tabel partisi GUID cadangan. |
| Keramahan Pengguna | Kurang ramah pengguna | UEFI lebih ramah pengguna daripada Legacy Boot. |
| Nama partisi | Tersimpan pada partisi | ID GUID unik disertai dengan nama 36 karakter. |
| Dukungan multi boot | Kurang mumpuni | Bagus, dengan entri boot loader dalam partisi terpisah. |
</div>

## Perbedaan dalam Proses

Proses booting pada UEFI (Unified Extensible Firmware Interface) melibatkan beberapa langkah yang berbeda dibandingkan dengan Legacy BIOS. Berikut adalah langkah-langkah umum dalam proses booting UEFI:
1. **Power On Self Test (POST)**: Proses booting dimulai dengan POST, di mana firmware UEFI melakukan pemeriksaan awal terhadap perangkat keras untuk memastikan semuanya berfungsi dengan baik.
2. **UEFI Firmware Initialization**: Setelah POST selesai, firmware UEFI diinisialisasi. Ini termasuk mengidentifikasi dan menginisialisasi perangkat keras, seperti CPU, RAM, dan perangkat penyimpanan.
3. **UEFI Boot Manager**: Setelah firmware diinisialisasi, UEFI Boot Manager dimuat. Boot Manager adalah program yang bertanggung jawab untuk memilih perangkat booting yang tepat. Boot Manager dapat memuat beberapa file konfigurasi, seperti NVRAM (Non-Volatile Random Access Memory) atau file konfigurasi di partisi EFI System.
4. **Boot Option Menu**: Jika ada lebih dari satu perangkat booting yang tersedia, Boot Manager akan menampilkan menu opsi booting, di mana pengguna dapat memilih perangkat booting yang diinginkan.
5. **Loading Boot Loader**: Setelah perangkat booting dipilih, Boot Manager akan memuat boot loader yang sesuai. Boot loader adalah program yang bertanggung jawab untuk memuat sistem operasi ke dalam memori dan memulai eksekusi.
6. **Loading Kernel**: Boot loader kemudian memuat kernel sistem operasi ke dalam memori dan memulai eksekusi. Kernel adalah bagian utama dari sistem operasi yang bertanggung jawab untuk mengelola sumber daya perangkat keras dan menjalankan aplikasi.
7. **Init Process**: Setelah kernel dimuat, init process (biasanya systemd pada distribusi Linux modern) dimulai. Init process adalah proses pertama yang dijalankan setelah kernel, dan bertanggung jawab untuk memulai proses lain dan mengelola sistem.
8. **User Space**: Setelah init process selesai, sistem operasi memasuki user space, di mana pengguna dapat mulai menjalankan aplikasi.

Proses booting pada UEFI memiliki beberapa keuntungan, termasuk kemampuan untuk boot dari partisi GPT yang lebih besar, dukungan untuk booting jaringan (PXE boot), dan fitur keamanan seperti Secure Boot.

Proses booting pada Legacy BIOS (Basic Input/Output System) melibatkan beberapa langkah yang berbeda dibandingkan dengan UEFI. Berikut adalah langkah-langkah umum dalam proses booting Legacy BIOS:
1. **Power On Self Test (POST)**: Proses booting dimulai dengan POST, di mana firmware BIOS melakukan pemeriksaan awal terhadap perangkat keras untuk memastikan semuanya berfungsi dengan baik.
2. **BIOS Initialization**: Setelah POST selesai, BIOS diinisialisasi. Ini termasuk mengidentifikasi dan menginisialisasi perangkat keras, seperti CPU, RAM, dan perangkat penyimpanan.
Master Boot Record (MBR) Loading: Setelah BIOS diinisialisasi, BIOS akan mencari MBR di perangkat booting yang ditentukan. MBR adalah bagian pertama dari disk yang berisi kode boot loader.
4. **Boot Loader Loading**: Setelah MBR ditemukan, BIOS akan memuat boot loader yang sesuai. Boot loader adalah program yang bertanggung jawab untuk memuat sistem operasi ke dalam memori dan memulai eksekusi.
5. **Loading Kernel**: Boot loader kemudian memuat kernel sistem operasi ke dalam memori dan memulai eksekusi. Kernel adalah bagian utama dari sistem operasi yang bertanggung jawab untuk mengelola sumber daya perangkat keras dan menjalankan aplikasi.
6. **Init Process**: Setelah kernel dimuat, init process (biasanya systemd pada distribusi Linux modern) dimulai. Init process adalah proses pertama yang dijalankan setelah kernel, dan bertanggung jawab untuk memulai proses lain dan mengelola sistem.
7. **User Space: Setelah init process selesai, sistem operasi memasuki user space, di mana pengguna dapat mulai menjalankan aplikasi.
Proses booting pada Legacy BIOS memiliki beberapa kelemahan, termasuk keterbatasan dalam ukuran partisi booting (hingga 2TB) dan jumlah partisi primer (hingga 4), serta tidak adanya fitur keamanan seperti Secure Boot.

## Referensi

- [BIOS](https://www.acerid.com/berita-teknologi/fungsi-bios-pada-sistem-komputasi)
- [Perbedaan Legacy dan UEFI](https://dianisa.com/perbedaan-legacy-bios-dan-uefi/)