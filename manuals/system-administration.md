# Sistem & Administrasi

Modul **System Settings** adalah ruang kendali utama bagi *Super Administrator*. Anda dapat mengelola otorisasi, hak akses, dan pengaturan global perusahaan di sini.

## 1. Manajemen Pengguna (Users)

Bagian ini digunakan untuk memberi izin login kepada karyawan.

1. Buka **System > Users**.
2. Anda akan melihat daftar akun yang bisa masuk ke ERP.
3. Anda dapat men-klik *Edit* pada pengguna tertentu untuk mengubah *Roles* (Peran) mereka.
4. **Catatan:** Biasakan membuat *User* melalui menu **HR > Karyawan**. Sistem otomatis akan membuatkan akun *User* dan menautkannya dengan data absensi karyawan tersebut.

## 2. Hak Akses (Roles & Permissions)

Sistem menggunakan model berbasis *Spatie Permission*, yang memberikan kontrol granular (sangat detail) terhadap siapa yang bisa melihat atau mengedit menu tertentu.

1. Buka **System > Roles & Permissions**.
2. Anda bisa membuat *Role* baru (contoh: `Warehouse Manager`).
3. Anda bisa mencentang kotak-kotak izin (*Permissions*), misalnya: `inventory.view`, `inventory.create`, `inventory.update`.
4. Setelah *Role* disimpan, masuk ke menu **Users** dan berikan *Role* ini ke staf gudang Anda. Mereka hanya akan bisa melihat menu Gudang saat login!

## 3. Company Settings (Pengaturan Perusahaan)

Pengaturan ini menyimpan data fundamental yang akan muncul di dokumen cetak (Invoice, DO, dll).

Buka **System Settings > Company Setting**:
- **Company Name**: Nama resmi badan usaha.
- **Tax Number (NPWP)**: Akan tercetak di dokumen Faktur Pajak.
- **Default Currency**: Mata uang utama (`IDR`).

## 4. Jejak Audit (Audit Log)

Sistem ERP ini merekam **setiap tindakan penting** yang dilakukan oleh *user* (terutama operasi hapus atau ubah harga/jumlah).

1. Buka **System > Audit Log**.
2. Administrator dapat memantau jika ada kecurangan atau perubahan data yang tidak sah.
3. Anda bisa memfilter berdasarkan *User* atau Modul untuk mempersempit pencarian investigasi.

> [!CAUTION]
> Jangan pernah memberikan *Role* **Super Admin** kepada staf biasa. Super Admin bisa melewati semua *Approval Workflow* dan melihat seluruh laporan keuangan yang sensitif!
