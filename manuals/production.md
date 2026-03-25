# Manual Departemen - Production

## Tujuan

Manual ini memandu tim Production menjalankan perencanaan produksi berbasis BOM dan work order, termasuk pencatatan output serta konsumsi material.

## Role yang Menggunakan

- production_manager
- production_staff
- inventory_manager (koordinasi material)

## Menu yang Digunakan

- Production > Bill Of Materials
- Production > Work Orders

## Status Dokumen Utama

### Bill Of Material

- draft
- active
- obsolete

### Work Order

- draft
- released
- in_progress
- completed
- cancelled

## SOP Harian

1. Validasi BOM aktif untuk produk yang akan diproduksi.
2. Buat work order baru sesuai rencana produksi.
3. Release work order sebelum eksekusi.
4. Catat output produksi melalui Record Output.
5. Koordinasi dengan Inventory untuk validasi pergerakan material.

## SOP Mingguan

1. Review WO terlambat atau belum selesai.
2. Bandingkan planned qty vs produced qty vs rejected qty.
3. Evaluasi scrap/reject dan tindak perbaikan proses.

## Langkah Operasional Detail

### A. Kelola BOM

1. Buat BOM dengan data:
   - kode BOM
   - produk output
   - output qty
   - satuan
   - status
2. Tambahkan material item:
   - material product
   - qty required
   - wastage percent
3. Aktifkan BOM yang siap dipakai produksi.

### B. Buat dan Release Work Order

1. Buat WO dari BOM.
2. Isi planned qty, due date, catatan.
3. Setelah diverifikasi, klik Release.

### C. Record Output Produksi

1. Buka WO berstatus released/in_progress.
2. Klik Record Output.
3. Isi data:
   - warehouse
   - good qty
   - rejected qty
   - unit cost (opsional)
4. Simpan transaksi.
5. Sistem akan:
   - issue material sesuai kebutuhan BOM
   - mencatat output produk jadi
   - update status WO (in_progress/completed)

## Kontrol Internal Wajib

- WO tidak boleh dijalankan tanpa BOM valid.
- Semua output wajib tercatat pada hari transaksi.
- Selisih reject harus dianalisis penyebabnya.
- Perubahan BOM wajib melalui persetujuan internal.

## Troubleshooting Umum

1. Record Output gagal:
   - cek status WO (harus released/in_progress)
   - cek warehouse terpilih
   - cek qty tidak nol
2. WO tidak bisa release:
   - cek status masih draft
3. Material issue tidak masuk stok:
   - cek integrasi stock ledger dan referensi work_order

## Checklist Produksi

- [ ] BOM produk utama aktif dan valid
- [ ] Semua WO harian sudah direlease
- [ ] Output dan reject tercatat lengkap
- [ ] WO selesai ditutup dengan status completed
- [ ] Laporan efisiensi reject dibahas mingguan
