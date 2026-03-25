# Manual Departemen - Procurement

## Tujuan

Manual ini memandu tim Procurement dari Purchase Request sampai Goods Receipt agar alur pembelian berjalan tertib dan terdokumentasi.

## Role yang Menggunakan

- procurement_staff
- procurement_manager
- inventory_manager (koordinasi penerimaan)
- finance_manager (monitor dampak AP)

## Menu yang Digunakan

- Procurement > Purchase Requests
- Procurement > Purchase Orders
- Procurement > Goods Receipts

## Status Dokumen Utama

### Purchase Request

- draft
- submitted
- approved
- rejected
- converted

### Purchase Order

- draft
- sent
- partial_received
- received
- invoiced
- completed
- cancelled

### Goods Receipt

- draft
- received
- cancelled

## SOP Harian

1. Buat PR untuk kebutuhan pembelian yang valid.
2. Submit PR untuk approval sesuai otorisasi.
3. Ubah PR approved menjadi PO draft melalui aksi Convert to PO.
4. Submit dan approve PO sebelum pengiriman vendor.
5. Catat penerimaan aktual melalui aksi Receive Goods pada PO.

## SOP Mingguan

1. Tinjau PR/PO yang pending approval.
2. Follow up PO overdue ke vendor.
3. Rekonsiliasi GR dengan PO dan vendor invoice.

## Langkah Operasional Detail

### A. Buat dan Submit Purchase Request

1. Buka Purchase Requests > Create.
2. Isi header PR (tanggal, needed date, requester, alasan).
3. Isi item PR minimal 1 baris (produk, qty, satuan, estimasi harga).
4. Simpan draft.
5. Jalankan aksi Submit jika data final.

### B. Approval PR

1. Approver membuka PR berstatus submitted.
2. Pilih Approve atau Reject.
3. Wajib isi catatan approval/rejection.
4. PR approved dapat dikonversi ke PO.

### C. Konversi PR ke PO

1. Pada PR approved, klik Convert to PO.
2. Pilih vendor aktif, target delivery, catatan, dan terms.
3. Sistem membuat PO draft dengan item dari PR.

### D. Kelola Purchase Order

1. Review detail item, harga, pajak, payment term, dan currency.
2. Submit PO, lalu lakukan approval.
3. PO yang disetujui menjadi dasar penerimaan barang.

### E. Penerimaan Barang (Goods Receipt)

1. Dari PO yang valid, jalankan aksi Receive Goods.
2. Isi gudang, lokasi (opsional), tanggal, item, qty diterima/ditolak.
3. Simpan penerimaan.
4. Sistem melakukan update stok ledger.
5. Sistem dapat membuat dampak ke AP/jurnal otomatis sesuai proses finance.

## Kontrol Internal Wajib

- PR, approval, dan PO harus dipisah minimal dua peran.
- Harga dan vendor final wajib diverifikasi sebelum approve PO.
- Semua penerimaan harus ada referensi PO yang sah.
- Selisih qty diterima vs ditolak wajib tercatat alasannya.

## Troubleshooting Umum

1. PR tidak bisa di-convert ke PO:
   - pastikan status PR sudah approved
2. Aksi approve/reject tidak muncul:
   - cek permission role
   - cek status dokumen
3. Goods receipt gagal disimpan:
   - cek qty diterima valid
   - cek gudang tujuan terpilih

## Checklist Procure-to-Receive

- [ ] Seluruh PR prioritas sudah diproses
- [ ] PO kritis sudah approved dan dikirim ke vendor
- [ ] Semua barang datang sudah dibuatkan GR
- [ ] Selisih penerimaan terdokumentasi
- [ ] Rekonsiliasi mingguan dengan Inventory dan Finance selesai
