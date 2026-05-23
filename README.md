# 🚛 Sistem Manajemen Logistik CV Mugi Jaya

> Proyek Pemrograman — Kelompok 9  
> Program Studi Informatika, Universitas AMIKOM Yogyakarta  
> Tahun Ajaran 2025/2026  
> Dosen Pengampu: Bambang Pilu Hartato, S.Kom., M.Eng

---

## 📋 Deskripsi Proyek

Sistem Manajemen Logistik CV Mugi Jaya adalah platform digital terintegrasi yang dirancang untuk mengoptimalkan rantai pasok, manajemen pergudangan, Quality Control (QC), dan pengawasan operasional armada perusahaan.

Sistem ini menggunakan arsitektur **Client-Server** dengan pendekatan **multi-platform**:
- **Web Application** — untuk kebutuhan manajerial dan monitoring di kantor
- **Mobile Application (Offline-First)** — untuk pekerja lapangan di area minim sinyal

---

## ✨ Fitur Utama

| Fitur | Deskripsi |
|---|---|
| 🗺️ GPS Tracking Armada | Pemantauan posisi truk secara real-time |
| 📦 Warehouse Management System | Pemetaan rak di 8 gudang secara terpusat |
| ✅ Quality Control Digital | Checklist QC berlapis dengan unggah foto bukti |
| 📍 Presensi Berbasis GPS | Check-in/out mandor lapangan dengan anti-fake GPS |
| 📊 Executive Dashboard | Monitoring operasional khusus Direktur Utama |
| 🔔 Smart Notification | Peringatan otomatis anomali GPS, stok, dan insiden |
| 📝 Laporan Insiden & RCA | Formulir Root Cause Analysis terstruktur |
| 🛒 Pengadaan Darurat | Alur birokrasi digital pengajuan barang darurat |

---

## 👥 Anggota Kelompok

| Nama | NIM | Peran |
|---|---|---|
| Pandu Jelang Ramadhan | 23.11.5890 | Pendahuluan & Latar Belakang |
| Michael Jehezkiel Herjuno Wijoyo | 23.11.5901 | Desain Sistem & Repository |
| Arfaghany Adzhana Wibowo | 23.11.5879 | Kebutuhan Sistem |
| Zaky Naufal 'Alim Budiansyah | 23.11.5877 | Kebutuhan Sistem |
| Desta Anandika Rajendra Maheswara | 23.11.5907 | Use Case & User Interaction |
| Muhamad Rofi Aljufri | 23.11.5912 | Penjelasan Tambahan |

---

## 🏗️ Arsitektur Sistem

```
┌─────────────────────────────────────────────────┐
│                  CLIENT LAYER                   │
│   Web App (Desktop/Tablet)  │  Mobile App       │
│   Direktur, Admin, Manajemen│  Mandor, Driver,  │
│                             │  Petugas Gudang   │
└──────────────┬──────────────┴────────┬──────────┘
               │    RESTful API        │ WebSocket
               ▼                       ▼
┌─────────────────────────────────────────────────┐
│              APPLICATION & API LAYER            │
│        Business Logic + RBAC Middleware         │
└──────────────┬──────────────────────────────────┘
               │
┌──────────────▼──────────────────────────────────┐
│             DATABASE & STORAGE LAYER            │
│  Relational DB │ In-Memory Cache │ Cloud Storage │
└─────────────────────────────────────────────────┘
               │
┌──────────────▼──────────────────────────────────┐
│           EXTERNAL INTEGRATIONS                 │
│     Mapping API  │  Push Notification Gateway   │
└─────────────────────────────────────────────────┘
```

---

## 🌿 Struktur Branch

```
main
├── dev
│   ├── feature/gps-tracking
│   ├── feature/inventory-wms
│   ├── feature/qc-handover
│   ├── feature/attendance
│   └── feature/dashboard
```

| Branch | Keterangan |
|---|---|
| `main` | Kode stabil, siap produksi |
| `dev` | Branch pengembangan aktif, merge dari semua feature |
| `feature/gps-tracking` | Modul monitoring GPS armada real-time |
| `feature/inventory-wms` | Modul manajemen stok & peta rak gudang |
| `feature/qc-handover` | Modul Quality Control & serah terima barang |
| `feature/attendance` | Modul presensi mandor berbasis GPS |
| `feature/dashboard` | Executive Dashboard & RBAC |

---

## 🛠️ Teknologi yang Digunakan

- **Frontend Web:** React.js / Next.js
- **Mobile:** React Native (Offline-First dengan local storage)
- **Backend:** Node.js + Express / Laravel
- **Database:** PostgreSQL (relational) + Redis (cache)
- **Storage:** Cloud Object Storage (foto QC & dokumen)
- **Real-time:** WebSocket
- **Maps:** Google Maps API / Leaflet.js

---

## 📁 Struktur Folder

```
logistik-cv-mugi-jaya/
├── docs/               # Dokumentasi (ERD, diagram, wireframe)
├── frontend/           # Web application
├── mobile/             # Mobile application
├── backend/            # API server & business logic
├── database/           # Skema database & migration
└── README.md
```

---

## 📄 Lisensi

Proyek ini dibuat untuk keperluan akademik — Proyek Pemrograman, Universitas AMIKOM Yogyakarta.
