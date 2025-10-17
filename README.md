# Tugas-PBO-Pertemuan-Kesembilan
 Koneksi IReport, Jasper dan JFrame  Form Netbeans dengan PostgreSQL serta Exception Java di Netbeans.
# KONEKSI JFRAME FORM dengan POSGRESQL 
Konektivitas antara JFrame Form dan tabel di PostgreSQL adalah proses 
menghubungkan aplikasi Java berbasis GUI dengan basis data PostgreSQL agar data dapat 
ditampilkan, ditambahkan, diubah, atau dihapus langsung melalui antarmuka pengguna. 
JFrame Form berperan sebagai tampilan interaktif yang berisi komponen seperti tombol, text 
field, dan tabel, sedangkan PostgreSQL menyimpan data dalam bentuk tabel. Koneksi 
dilakukan menggunakan JDBC (Java Database Connectivity), sehingga setiap aksi pada 
JFrame Form, seperti menekan tombol simpan atau hapus, akan diterjemahkan menjadi 
perintah SQL yang dieksekusi pada tabel PostgreSQL.     
# JASPER REPORT NEATBEANS 
JasperReports adalah sebuah library open-source berbasis Java yang berfungsi sebagai 
mesin pelaporan (reporting engine). JasperReports digunakan untuk membuat berbagai jenis 
laporan seperti faktur, slip gaji, laporan keuangan, atau rekap data pegawai dan mahasiswa. 
Library ini mampu mengambil data dari berbagai sumber, seperti database, file XML, 
JavaBeans, CSV, atau JSON, kemudian mengolahnya menjadi laporan yang dapat diekspor 
ke berbagai format, seperti PDF, Excel, HTML, CSV, dan DOCX.      
# IREPORT DESIGNER di NETBEANS 
iReport Designer adalah sebuah aplikasi antarmuka grafis (GUI) yang digunakan 
untuk mendesain laporan JasperReports dengan cara yang lebih mudah dan visual. Dengan 
iReport, pengguna tidak perlu menulis XML secara manual karena semua elemen laporan 
seperti teks, tabel, gambar, grafik, subreport, serta parameter dapat diatur menggunakan 
fitur drag and drop. Selain itu, iReport juga memungkinkan pengguna untuk mengatur 
layout laporan seperti header, detail, dan footer, serta melakukan preview hasil laporan 
secara langsung dengan data yang diambil dari database. 
# INTEGRASI ANTARA JASPER REPORT DAN IREPORT DESIGNER 
Dalam pengembangan aplikasi Java menggunakan NetBeans, JasperReports dan iReport 
sering digunakan secara bersamaan. Biasanya, iReport digunakan untuk mendesain laporan dan 
menghasilkan file .jrxml dan .jasper, sedangkan JasperReports digunakan dalam kode Java untuk 
menampilkan laporan tersebut. Pengguna dapat menambahkan library JasperReports ke dalam proyek 
NetBeans, membuat koneksi database, lalu memanggil laporan menggunakan kelas seperti 
JasperFillManager, JasperPrint, dan JasperViewer.
# Langkah - langkah membuat Jasper Report
1. Siapkan Database di PostgreSQL
2. Hubungkan Database ke NetBeans
3. Tambahkan Library, Klik kanan pada Libraries → Add Library → pilih PostgreSQL JDBC Driver, Klik kanan lagi → Add JAR/Folder → tambahkan semua file library JasperReports (biasanya jasperreports-x.x.x.jar dan dependensinya).
4. Tambahkan Plugin iReport ke NetBeans, Buka Tools → Plugins → Downloaded → Add Plugin, Pilih file .nbm plugin iReport (biasanya dari folder hasil ekstraksi iReport), Klik Open → Install → Finish.
5. Buat Report Baru. Klik kanan pada package project → New → Report Wizard. Pilih ukuran kertas (A4 atau Letter) → Next. Beri nama file, misalnya laporanHewan.jrxml → Next. Buat New Data Source → Database JDBC Connection. Pilih koneksi PostgreSQL yang sudah dibuat. Klik Test dan Save. Pilih tabel dan pindahkan semua field ke kanan → Next → Finish.
6. Desain Laporan di iReport Designer. Buka file .jrxml yang baru dibuat. Atur layout (header, detail, footer). Tambahkan: Text Field untuk nama kolom. Image jika ingin menampilkan logo. Title dan tanggal laporan di bagian header. Simpan laporan → otomatis menghasilkan file .jasper.
7. Integrasi JasperReport ke JFrame. Tambahkan tombol “Cetak” di JFrame.
8. Jalankan dan Cetak. Jalankan aplikasi. Klik tombol Cetak di JFrame → laporan akan muncul di Jasper Viewer. Kamu bisa menyimpan hasilnya ke PDF, Excel, atau DOCX.
