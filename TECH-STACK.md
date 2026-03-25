# Tech Stack

## Core Platform

| Komponen | Teknologi |
|---|---|
| Backend Framework | Laravel 11 |
| Admin Panel | Filament 3 |
| Language | PHP 8.2+ |
| Frontend Build Tool | Vite |
| Reactive UI | Livewire |

## Data dan Infrastruktur

| Komponen | Teknologi |
|---|---|
| Database | MySQL / MariaDB / PostgreSQL / SQLite |
| Cache | Redis (opsional) |
| Queue | Redis / Database Queue |
| File Storage | Local / S3 compatible |

## Library Pendukung

| Area | Package |
|---|---|
| Role & Permission | spatie/laravel-permission |
| Activity Log | spatie/laravel-activitylog |
| PDF Export | barryvdh/laravel-dompdf |
| Excel Export | rap2hpoutre/fast-excel |

## Arsitektur Singkat

- Domain-based structure per modul (HR, Inventory, Procurement, Finance, Production, Assets)
- Session-based active company context
- Gate dan policy untuk kontrol akses
- Scheduler untuk tugas operasional harian dan bulanan

## Keamanan dan Operasional

- Source code privat terpisah dari repository promosi ini
- Credential dan environment disimpan di .env pada deployment
- Audit trail tersedia untuk aktivitas penting
