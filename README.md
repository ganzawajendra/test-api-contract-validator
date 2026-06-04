# My Project API Documentation

Ini adalah repositori untuk pengembangan backend aplikasi. Semua kontributor wajib mengikuti standar kontrak API yang ada di bawah ini.

## Standar Response API

Untuk menjaga konsistensi antara tim Backend dan Frontend, berikut adalah aturan struktur JSON Response:

1. **Naming Convention**: Semua key di dalam JSON wajib menggunakan format **snake_case** (contoh: `user_id`, `is_active`, `created_at`). Jangan gunakan camelCase.
2. **Wajib Field**: Setiap response data harus dibungkus dalam objek utama yang memiliki field `message` (string) sebagai indikator status respons.
3. **Format Tanggal**: Menggunakan format standar `YYYY-MM-DD`.

### Contoh JSON yang VALID:
```json
{
  "message": "Success",
  "user_id": 99,
  "user_name": "Ganza Wajendra"
}