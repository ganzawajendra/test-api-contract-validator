# Project API Contract Guidelines

Selamat datang di repositori dokumentasi kontrak API. Dokumen ini berfungsi sebagai acuan tunggal (single source of truth) bagi tim Backend dan Frontend dalam menyusun serta mengonsumsi data JSON.

## Standar Response API Resmi

Semua endpoint API pada proyek ini wajib mengembalikan struktur data yang seragam sesuai dengan standarisasi internal berikut:

### 1. Aturan Penamaan (Naming Convention)
* **Format Key**: Semua nama field (*key*) di dalam JSON wajib menggunakan format **snake_case** (huruf kecil dengan pemisah garis bawah).
* **Contoh Valid**: `user_id`, `room_name`, `booking_status`, `created_at`.
* **Dilarang**: Menggunakan `camelCase` (`userId`) atau `PascalCase` (`UserId`).

### 2. Struktur Objek Wajib (Mandatory Fields)
Setiap response JSON yang dikembalikan dari server harus dibungkus dalam objek utama yang minimal memiliki 2 field berikut:
1. `code` : Berisi tipe data *integer* (contoh: `200`, `400`, `500`) sebagai kode status HTTP.
2. `data` : Berisi objek utama atau *array* tempat data aplikasi disimpan.

---

## Contoh JSON Response

### 1. Contoh Standar JSON yang VALID (Sesuai Dokumentasi):
```json
{
  "code": 200,
  "data": {
    "booking_id": 105,
    "room_name": "Ruang Meeting Utama",
    "is_available": true
  }
}