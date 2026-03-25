# Manual Departemen - Finance

## Tujuan

Manual ini memandu tim Finance mengelola account mapping, AR/AP, jurnal, dan penutupan periode dengan integritas pembukuan.

## Role yang Menggunakan

- finance_manager
- finance_staff
- auditor

## Menu yang Digunakan

- Finance > Journal Entries
- Finance > Account Mappings
- Finance > Accounts Payable
- Finance > Accounts Receivable

## SOP Harian

1. Pantau AR/AP jatuh tempo.
2. Catat pembayaran AP (Record Payment) yang sudah dibayar.
3. Catat penerimaan AR (Record Receipt) yang sudah diterima.
4. Review jurnal posted dan validasi saldo debit-kredit.

## SOP Mingguan

1. Review jurnal void/reversal untuk transaksi koreksi.
2. Validasi mapping akun utama tidak berubah tanpa persetujuan.
3. Rekonsiliasi AR/AP dengan Procurement dan Sales/Admin.

## SOP Bulanan

1. Pastikan semua transaksi periode sudah masuk.
2. Posting item bulanan (termasuk depresiasi dari modul Assets).
3. Jalankan pemanasan cache laporan bulanan:
   - php artisan reports:generate
4. Review laporan:
   - trial balance
   - balance sheet
   - income statement
   - cash flow statement

## Langkah Operasional Detail

### A. Account Mapping

1. Buka Account Mappings.
2. Pastikan mapping key wajib terisi akun aktif.
3. Mapping penting:
   - default_cash
   - default_bank
   - accounts_receivable
   - accounts_payable
   - inventory_raw_material
   - inventory_finished_good
   - salary_expense
   - tax_payable

### B. Kelola Accounts Payable

1. AP terbentuk dari proses goods receipt/jurnal otomatis.
2. Buka AP outstanding.
3. Klik Record Payment saat pembayaran dilakukan.
4. Isi amount, payment date, payment source, note.
5. Sistem membuat jurnal pembayaran AP otomatis.

### C. Kelola Accounts Receivable

1. Buat invoice AR dari menu Accounts Receivable.
2. Isi invoice number, invoice date, due date, amount.
3. Saat ada penerimaan, klik Record Receipt.
4. Isi amount, payment date, payment source, note.
5. Sistem membuat jurnal penerimaan AR otomatis.

### D. Kontrol Journal Entry

1. Gunakan Journal Entries untuk audit pembukuan.
2. Untuk koreksi transaksi tertentu, gunakan aksi Void jika memenuhi syarat.
3. Void akan membuat jurnal reversal otomatis dan menandai jurnal asal sebagai voided.

## Kontrol Internal Wajib

- Dilarang edit manual jurnal otomatis tanpa prosedur koreksi.
- Void jurnal wajib disertai alasan yang jelas.
- Rekonsiliasi bank/kas dilakukan periodik.
- Pisahkan petugas input penerimaan/pembayaran dari approver akhir.

## Troubleshooting Umum

1. Payment/receipt gagal:
   - cek outstanding tidak nol
   - cek amount tidak melebihi outstanding
2. Jurnal tidak bisa di-void:
   - cek status jurnal harus posted
   - cek reference_type termasuk yang diizinkan
3. Laporan tidak update:
   - jalankan reports:generate
   - cek transaksi posted pada periode terkait

## Checklist Closing Finance

- [ ] Seluruh AR/AP periode direkonsiliasi
- [ ] Jurnal koreksi sudah selesai
- [ ] Depresiasi bulanan sudah diposting
- [ ] Laporan TB/BS/IS/CF sudah direview
- [ ] Arsip laporan dan bukti closing tersimpan
