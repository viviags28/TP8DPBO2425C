# Janji
Saya Vivi Agustina Suryana dengan NIM 2400456 mengerjakan Tugas Praktikum 8 dalam mata kuliah Desain dan Pemrograman Berorientasi Objek Untuk keberkahan-Nya, maka saya tidak melakukan kecurangan seperti yang telah dispesifikasikan.

# TP MVC 25 - Sistem Manajemen Dosen dan Department

## Deskripsi Program
Aplikasi web untuk mengelola data dosen dan department menggunakan arsitektur Model-View-Controller (MVC). Aplikasi ini menyediakan fungsi CRUD (Create, Read, Update, Delete) untuk kedua entitas tersebut.

## Desain Program

### Arsitektur MVC

#### 1. Model
- Menangani logika data dan komunikasi dengan database
- Terdiri dari class DB (koneksi database), Department, dan Lecturer
- Bertanggung jawab untuk semua operasi database

#### 2. View
- Menampilkan antarmuka pengguna
- Terpisah berdasarkan modul (departments dan lecturers)
- Menggunakan template system dengan header dan footer

#### 3. Controller
- Menangani logika aplikasi dan request dari user
- DepartmentController untuk mengelola department
- LecturerController untuk mengelola dosen
- Menghubungkan Model dan View

## Struktur Folder
```
tp_mvc25/
│
├── config/
│   └── config.php
│
├── models/
│   ├── DB.php
│   ├── Department.php
│   └── Lecturer.php
│
├── views/
│   ├── templates/
│   │   ├── header.php
│   │   └── footer.php
│   │
│   ├── departments/
│   │   ├── index.php
│   │   ├── create.php
│   │   └── edit.php
│   │
│   └── lecturers/
│       ├── index.php
│       ├── create.php
│       └── edit.php
│
├── controllers/
│   ├── DepartmentController.php
│   └── LecturerController.php
│
└── index.php
```

## 🔄 Alur Kerja

### 1. Routing
- Router utama (index.php) menerima request
- Membaca parameter controller dan action dari URL
- Memuat controller yang sesuai dan menjalankan method

### 2. Flow Data
```
User Request → Router → Controller → Model → Database
                                     ↓
User Response ← View ← Controller ← Model
```

### 3. Contoh Alur
- User mengakses halaman dosen
- Router memanggil LecturerController::index()
- Controller meminta data dari Model Lecturer
- Model mengambil data dari database
- Controller mengirim data ke View
- View menampilkan data dalam format HTML

## Struktur Database
Database terdiri dari dua tabel utama:

1. **departments**: Menyimpan data jurusan
2. **lecturers**: Menyimpan data dosen dengan relasi ke departments

## Fitur yang Tersedia

### Untuk Department:
- Melihat daftar department
- Menambah department baru
- Mengedit data department
- Menghapus department

### Untuk Dosen:
- Melihat daftar dosen
- Menambah dosen baru
- Mengedit data dosen
- Menghapus dosen
- Relasi dengan department

## Dokumentasi

### Tampilan Awal Department
[Halaman utama menampilkan daftar department yang tersedia]

### Tampilan Awal Dosen  
[Halaman utama menampilkan daftar dosen yang tersedia]

### Full Test CRUD
[Documentation untuk testing semua fungsi CRUD]


Saya **Vivi Agustina Suryana** dengan **NIM 2400456** mengerjakan Tugas Praktikum 8 dalam mata kuliah Desain dan Pemrograman Berorientasi Objek. Untuk keberkahan-Nya, maka saya tidak melakukan kecurangan seperti yang telah dispesifikasikan.
