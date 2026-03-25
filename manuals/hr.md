# Manual Departemen - HR

## Tujuan

Manual ini memandu tim HR mengelola data karyawan, absensi, cuti, payroll, dan slip gaji secara konsisten.

## Role yang Menggunakan

- hr_manager
- hr_staff
- company_admin (review)

## Menu yang Digunakan

- HR > Employees
  - tab/relasi Attendance
  - tab/relasi Leave
  - tab/relasi Payroll

## SOP Harian

1. Input karyawan baru atau update data karyawan.
2. Catat absensi harian setiap karyawan.
3. Tindak lanjuti pengajuan cuti (approve/reject sesuai kebijakan).
4. Validasi karyawan nonaktif agar tidak masuk payroll periode berikutnya.

## SOP Bulanan

1. Tutup data absensi periode berjalan.
2. Review cuti dan ketidakhadiran final.
3. Buat/validasi payroll per karyawan.
4. Ubah status payroll hingga paid setelah pembayaran dilakukan.
5. Export slip gaji PDF untuk distribusi.

## Langkah Operasional Detail

### A. Kelola Master Karyawan

1. Buat data karyawan di menu Employees.
2. Isi data wajib:
   - NIK
   - nama
   - departemen
   - jabatan
   - tipe karyawan
   - tanggal masuk
   - gaji pokok
3. Lengkapi data bank dan kontak darurat.
4. Jika karyawan memiliki akun panel, pastikan user_id terhubung.

### B. Input Attendance

1. Buka detail karyawan.
2. Masuk ke relasi Attendance.
3. Tambah data per tanggal dengan status:
   - present
   - absent
   - late
   - half_day
   - holiday
   - permission
   - sick
4. Isi check in, check out, jam kerja, lembur bila tersedia.

### C. Kelola Leave

1. Buka relasi Leave pada karyawan.
2. Isi tipe cuti, tanggal mulai-selesai, total hari, status, alasan.
3. Pastikan status akhir sesuai keputusan manajer.

### D. Kelola Payroll

1. Buka relasi Payroll pada karyawan.
2. Isi komponen periode payroll:
   - bulan dan tahun
   - gaji pokok
   - lembur
   - gaji kotor
   - gaji bersih
   - status payroll
3. Gunakan status terkontrol:
   - draft
   - processed
   - approved
   - paid
4. Setelah status paid, lakukan verifikasi dampak jurnal payroll pada tim Finance.

### E. Export Slip Gaji

1. Dari daftar karyawan, jalankan aksi Export PDF Slip.
2. Pastikan payroll periode terbaru sudah tersedia.
3. Simpan dan distribusikan ke karyawan sesuai kebijakan kerahasiaan.

## Kontrol Internal Wajib

- Gaji pokok dan data bank harus divalidasi dua tingkat.
- Perubahan data payroll harus terdokumentasi.
- Status paid hanya setelah konfirmasi transfer/bukti pembayaran.
- HR dan Finance wajib rekonsiliasi payroll bulanan.

## Troubleshooting Umum

1. Slip gaji gagal dibuat:
   - cek apakah payroll karyawan sudah ada
2. Nilai payroll terlihat salah:
   - cek absensi, lembur, dan status keaktifan karyawan
3. Karyawan tidak muncul pada proses operasional:
   - cek status aktif dan relasi departemen/jabatan

## Checklist Tutup Payroll

- [ ] Absensi periode sudah final
- [ ] Cuti dan izin sudah terverifikasi
- [ ] Payroll seluruh karyawan sudah approved
- [ ] Payroll berstatus paid sudah direkonsiliasi dengan Finance
- [ ] Slip gaji terdistribusi
