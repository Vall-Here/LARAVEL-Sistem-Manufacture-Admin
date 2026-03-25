# Manual Departemen - Inventory

## Tujuan

Manual ini memandu tim Inventory menjaga akurasi stok, melakukan penyesuaian yang terkontrol, dan memantau pergerakan barang melalui ledger.

## Role yang Menggunakan

- inventory_manager
- inventory_staff
- auditor (view)

## Menu yang Digunakan

- Inventory > Products
- Product Detail > Stock Ledger
- Dashboard > Stock Alert

## SOP Harian

1. Monitor produk dengan stok rendah dari dashboard dan daftar produk.
2. Pastikan setiap pergerakan stok berasal dari transaksi resmi (GR, produksi, adjustment berizin).
3. Validasi produk nonaktif agar tidak dipakai transaksi baru.

## SOP Mingguan

1. Review produk dengan stok negatif atau tidak wajar.
2. Cocokkan saldo ledger terhadap transaksi Procurement dan Production.
3. Lakukan adjustment hanya untuk koreksi yang disetujui.

## SOP Bulanan

1. Jalankan stock opname internal.
2. Tuntaskan selisih stok dengan berita acara adjustment.
3. Serahkan hasil rekonsiliasi ke Finance untuk tutup buku.

## Langkah Operasional Detail

### A. Kelola Master Produk

1. Buka menu Products.
2. Isi data inti:
   - SKU
   - nama produk
   - kategori
   - satuan
   - tipe produk (raw_material/work_in_progress/finished_good/consumable/asset)
3. Isi parameter kontrol:
   - min stock
   - max stock
   - reorder point
   - standard cost

### B. Monitor Stok Saat Ini

1. Gunakan kolom Stok Saat Ini pada daftar produk.
2. Prioritaskan produk dengan indikator di bawah reorder point.
3. Konfirmasi kebutuhan pembelian ke tim Procurement.

### C. Penyesuaian Stok (Adjust Stock)

1. Aksi Adjust Stock hanya untuk inventory_manager.
2. Pilih produk, gudang, qty, tipe penyesuaian, dan alasan.
3. Pastikan alasan jelas dan dapat diaudit.
4. Simpan bukti fisik/surat koreksi di arsip internal.

### D. Audit Ledger Produk

1. Buka detail produk.
2. Tinjau relation Stock Ledger.
3. Verifikasi reference_type transaksi (manual_adjustment, goods_receipt, work_order, dsb).

## Kontrol Internal Wajib

- Larangan edit saldo langsung di database.
- Semua koreksi stok wajib melalui adjustment beralasan.
- Pisahkan petugas opname dan petugas approval koreksi.

## Troubleshooting Umum

1. Stok negatif:
   - cek urutan transaksi dan tanggal input
   - cek apakah ada pengeluaran tanpa penerimaan sebelumnya
2. Stok tidak sesuai fisik:
   - lakukan cycle count
   - input adjustment dengan dokumentasi bukti
3. Produk tidak bisa dipilih di transaksi:
   - cek status produk aktif
   - cek relasi satuan/kategori

## Checklist Stock Control

- [ ] Master produk inti sudah lengkap
- [ ] Reorder point seluruh produk utama sudah terdefinisi
- [ ] Semua adjustment memiliki alasan dan bukti
- [ ] Ledger mingguan telah direview
- [ ] Hasil stock opname bulanan terdokumentasi
