# Manual Departemen - Assets

## Tujuan

Manual ini memandu tim Assets mengelola siklus aset tetap, penjadwalan maintenance, dan posting depresiasi bulanan.

## Role yang Menggunakan

- asset_manager
- finance_manager (sinkron depresiasi)
- auditor

## Menu yang Digunakan

- Assets > Asset Categories
- Assets > Fixed Assets
- Fixed Asset Detail > Depreciation Logs
- Fixed Asset Detail > Maintenance Schedules

## Status Aset

- draft
- active
- disposed

## SOP Harian

1. Catat aset baru segera setelah perolehan.
2. Pastikan lokasi aset terbaru tercatat.
3. Tinjau jadwal maintenance mendekati jatuh tempo.

## SOP Mingguan

1. Follow up maintenance planned dan in_progress.
2. Update status maintenance selesai/cancelled sesuai kondisi lapangan.
3. Validasi aset yang tidak produktif untuk rencana disposal.

## SOP Bulanan

1. Posting depresiasi untuk aset aktif.
2. Rekonsiliasi nilai buku dengan tim Finance.
3. Review aset yang akan disposisi atau penggantian.

## Langkah Operasional Detail

### A. Kelola Kategori Aset

1. Definisikan kategori aset aktif.
2. Gunakan kategori konsisten untuk pelaporan dan audit.

### B. Kelola Fixed Asset

1. Buat fixed asset baru.
2. Isi data wajib:
   - kode aset
   - nama aset
   - kategori
   - tanggal perolehan
   - nilai perolehan
   - nilai residu
   - umur manfaat (bulan)
   - metode depresiasi
3. Simpan aset dalam status draft.
4. Jalankan Activate saat aset siap dipakai.

### C. Schedule Maintenance

1. Pada aset aktif, klik Schedule Maintenance.
2. Isi tanggal jadwal, tipe, dan deskripsi.
3. Pantau notifikasi due maintenance harian (scheduler).

### D. Post Depreciation

1. Pada aset aktif, klik Post Depreciation.
2. Isi periode bulan dan tahun.
3. Simpan untuk membuat log depresiasi dan jurnal terkait.

### E. Dispose Asset

1. Pastikan ada persetujuan internal disposal.
2. Jalankan aksi Dispose pada aset aktif.
3. Isi catatan disposal.
4. Verifikasi status berubah menjadi disposed.

## Kontrol Internal Wajib

- Data nilai aset harus didukung dokumen perolehan.
- Depresiasi diposting rutin di akhir periode.
- Disposal harus memiliki approval manajemen.
- Maintenance kritis harus dipantau lewat scheduler harian.

## Troubleshooting Umum

1. Depresiasi gagal diposting:
   - cek aset berstatus active
   - cek account mapping terkait depresiasi
2. Maintenance due tidak muncul notifikasi:
   - cek scheduler notify:maintenance-due aktif
   - cek status maintenance masih planned
3. Aset tidak bisa diedit:
   - aset disposed memang dibatasi dari edit rutin

## Checklist Asset Governance

- [ ] Kategori aset sudah standar
- [ ] Semua aset aktif memiliki umur manfaat
- [ ] Maintenance schedule aset kritikal sudah terisi
- [ ] Depresiasi bulan berjalan selesai diposting
- [ ] Daftar aset disposed tervalidasi dokumennya
