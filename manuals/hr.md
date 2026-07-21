# Sumber Daya Manusia (HR)

Modul **HR (Human Resources)** digunakan untuk mengelola data inti karyawan perusahaan Anda. Modul ini merupakan fondasi bagi modul lain yang memerlukan data karyawan (seperti yang bertugas di Produksi, atau siapa yang melakukan approval).

## 1. Daftar Karyawan (Employees)

Fitur ini berfungsi sebagai *database* sentral untuk seluruh staf perusahaan.

### Menambahkan Karyawan Baru
1. Buka menu **HR > Karyawan**.
2. Klik tombol **New Employee**.
3. Isi informasi dasar:
   - **ID Karyawan (Employee ID)**: Nomor Induk Karyawan (NIP/NIK).
   - **Nama Lengkap**.
   - **Email & Nomor Telepon**.
   - **Departemen & Jabatan (Position)**.
   - **Tanggal Bergabung (Join Date)**.
4. Klik **Create**.

> [!IMPORTANT]
> Sistem secara otomatis membuatkan akun *User* (User Login) saat karyawan baru dibuat. Akun User ini dibutuhkan jika karyawan tersebut harus login ke dalam sistem ERP. Kata sandi (*password*) bawaan biasanya sama dengan alamat emailnya (harap instruksikan karyawan untuk segera mengubah kata sandinya!).

## 2. Struktur Organisasi

Dengan mengisi field *Department* dan *Position*, Anda dapat memetakan hirarki perusahaan.
Ini sangat berguna ketika mengatur **Approval Workflow** di pengaturan sistem, karena *approver* biasanya dipilih berdasarkan perannya (misal: "Manager Procurement").

## 3. Status Karyawan

Anda dapat mengontrol status keaktifan karyawan.
- **Active**: Karyawan yang masih bekerja. Mereka dapat mengakses sistem (jika memiliki hak akses) dan dipilih dalam penugasan kerja.
- **Resigned / Terminated**: Karyawan yang sudah tidak bekerja. Mengubah status ini secara otomatis akan **memblokir akses login** mereka ke dalam ERP demi alasan keamanan.

---

> [!TIP]
> **Integrasi**: Di masa depan, modul ini dapat dikembangkan untuk mengelola Absensi (*Attendance*), Cuti (*Leave*), dan Penggajian (*Payroll*). Untuk saat ini, pastikan data *Employee ID* dan *Department* selalu up-to-date!
