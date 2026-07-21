# Fitur Yang Ditawarkan (Enterprise On-Premise Edition)

Sistem ERP Manufaktur ini dirancang untuk **Skala Industri** dengan model *On-Premise / Single-Tenant* (Jual Putus). Arsitektur dibangun menggunakan *Service-Repository Pattern* untuk menjamin performa tinggi, keamanan data dari *race condition*, dan skalabilitas.

## 1) System Administration

- Multi-user management & Audit Log aktivitas user
- Role dan permission management
- **[NEW]** Company Settings (Pengaturan Metode Costing: FIFO / Moving Average)
- **[NEW]** Manajemen Pajak Default (Persentase PPN)
- **[NEW]** Queue & Job Monitoring Dashboard

## 2) Human Resources

- Master data karyawan & Pencatatan attendance
- Pengelolaan leave
- Payroll processing dan slip gaji
- **[NEW]** Kalkulasi otomatis PPh 21

## 3) Sales & Distribution (Penjualan) - [NEW]

- Master Data Customer & Price List
- Sales Quotation (Penawaran Harga)
- Sales Order (SO) dengan status tracking
- Delivery Order (DO) / Surat Jalan
- Sales Invoice & Integrasi Pajak (PPN)
- Retur Penjualan (Sales Return)

## 4) Inventory & Warehouse Management (WMS)

- Master produk dan kategori (Raw Material, WIP, Finish Good)
- **[NEW]** Multi-Gudang (Warehouse) dan Lokasi (Bin/Rak)
- **[NEW]** Inter-Warehouse Transfer (Mutasi antar gudang)
- **[NEW]** Inventory Costing (Valuasi stok berdasarkan FIFO atau Moving Average)
- Monitoring stok real-time (Aman dari *race condition* dengan *Pessimistic Locking*)
- Stock ledger per produk & Alert reorder point
- Stock adjustment terkontrol

## 5) Quality Control (QC) - [NEW]

- **[NEW]** QC Inbound (Pengecekan kualitas saat barang masuk dari Supplier)
- **[NEW]** QC Outbound (Pengecekan kualitas barang jadi sebelum masuk gudang / dijual)
- Pencatatan barang *Reject* dan *Rework*

## 6) Procurement (Pembelian)

- Purchase Request (PR) & Approval PR terstruktur
- Konversi PR ke Purchase Order (PO) & Approval PO
- Integrasi PPN Pembelian
- Goods Receipt (Terintegrasi dengan QC Inbound sebelum masuk stok)

## 7) Finance & Accounting

- Accounts Payable (AP) & Accounts Receivable (AR)
- Journal Entry management
- **[ENHANCED]** Auto jurnal dari transaksi operasional (Dieksekusi Asinkron via Laravel Queue)
- Laporan keuangan otomatis:
  - Trial balance (Neraca Saldo)
  - Balance sheet (Neraca)
  - Income statement (Laba/Rugi)
  - Cash flow statement (Arus Kas)

## 8) Production

- Bill of Material (BOM) multi-level
- **[NEW]** Material Requirement Planning (MRP) - Prediksi kebutuhan bahan baku dari SO
- Work Order (WO) & Release tracking progres WO
- Integrasi material issue ke stok (Aman dari *race condition*)
- Record output, reject, dan integrasi dengan QC Outbound

## 9) Asset Management

- Master fixed asset & Lifecycle (draft, active, disposed)
- Maintenance scheduling
- Depreciation posting (Penyusutan Aset otomatis ke jurnal)

## 10) Dashboard dan Monitoring

- KPI overview & Cash flow chart
- Pending approval widget (Tugas-tugas yang butuh aksi user)
- Stock alert widget & Recent activity widget

---

## Nilai Bisnis & Arsitektur Utama

- **Premium Architecture:** Dibangun dengan pola *Service-Repository* di Laravel.
- **Data Integrity:** *Idempotency Keys* mencegah submit data ganda, dan *Database Locking* menjamin stok & jurnal finansial tidak pernah selisih akibat *Race Condition*.
- **Skalabilitas Tinggi:** Pemrosesan laporan keuangan dan jurnal dilakukan di *background* (*Queue Database driver*).
- **Fleksibilitas:** Konfigurasi metode valuasi *Costing* yang bisa disesuaikan (Namun disarankan tidak diubah di tengah jalan untuk menjaga integritas COGS historis).
- **Siap Jual:** Tidak membutuhkan instalasi Redis yang rumit, cukup *Stack* dasar (PHP, MySQL, Web Server) membuatnya sangat mudah di- *deploy* di server internal (*On-Premise*) milik klien.
