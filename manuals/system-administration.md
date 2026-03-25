# Manual Departemen - System Administration

## Tujuan

Manual ini dipakai oleh super admin dan company admin untuk mengelola konfigurasi sistem, pengguna, role, dan kontrol akses.

## Role yang Menggunakan

- super_admin
- company_admin
- auditor (view audit sesuai hak akses)

## Menu yang Digunakan

- System > Company Settings
- System > Users
- System > Roles & Permissions
- System > Audit Log

## SOP Harian

1. Verifikasi user baru/keluar dari HR dan update akun di menu Users.
2. Pastikan role user sesuai fungsi kerja (least privilege).
3. Tinjau audit log untuk aktivitas sensitif.
4. Tindak lanjuti akun yang gagal login berulang.

## SOP Mingguan

1. Review akun tidak aktif atau tidak dipakai.
2. Revoke semua sesi untuk akun risiko tinggi jika diperlukan.
3. Validasi konsistensi role dengan struktur organisasi terbaru.

## SOP Bulanan

1. Review Company Settings:
   - identitas perusahaan
   - timezone dan fiscal year
   - konfigurasi payroll dan inventory
   - format nomor dokumen
2. Review Account Mapping minimal:
   - default_cash
   - default_bank
   - accounts_payable
   - accounts_receivable
   - inventory_raw_material
   - inventory_finished_good
   - salary_expense
   - tax_payable
3. Uji kirim email dari Company Settings (test email).

## Langkah Operasional Detail

### A. Kelola Company Settings

1. Buka menu Company Settings.
2. Lengkapi blok data:
   - Identitas Perusahaan
   - Pengaturan Sistem
   - Pengaturan Penggajian
   - Pengaturan Inventory
   - Account Mapping
   - Email Configuration
   - Nomor Dokumen
3. Simpan dan pastikan notifikasi sukses muncul.
4. Jika ganti SMTP, lakukan test email sebelum tutup sesi.

### B. Kelola User

1. Buat user baru melalui menu Users.
2. Isi nama, email, password, dan role.
3. Opsional: link ke data karyawan.
4. Saat user resign atau mutasi:
   - nonaktifkan user atau ubah role
   - revoke sesi lama
5. Untuk insiden keamanan:
   - lakukan reset password
   - aktifkan force password change

### C. Kelola Role dan Permission

1. Role & Permissions hanya dikelola super_admin.
2. Gunakan pola berikut:
   - role entry: input data/transaksi
   - role approver: approval final
   - role reviewer/auditor: monitor dan evaluasi
3. Hindari pemberian hak create, approve, dan void ke user yang sama kecuali ada alasan kontrol internal.

## Kontrol Internal Wajib

- Pisahkan fungsi input dan approval.
- Batasi impersonate hanya untuk super_admin.
- Simpan bukti perubahan hak akses (change log internal).
- Gunakan password policy minimal 8 karakter dan rotasi berkala.

## Troubleshooting Umum

1. User tidak bisa login:
   - cek company code
   - cek status aktif user
   - cek role masih melekat
2. Menu hilang pada user:
   - cek permission role
   - cek user berada pada company yang benar
3. Email notifikasi tidak terkirim:
   - cek SMTP host/port/credential
   - lakukan test email dari Company Settings

## Checklist Serah Terima Admin

- [ ] Company Settings lengkap
- [ ] Mapping akun wajib sudah terisi
- [ ] Struktur role final sudah disetujui manajemen
- [ ] Daftar user aktif valid
- [ ] SOP reset password dan revoke session dipahami admin
