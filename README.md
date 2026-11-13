# KELOMPOK B CAPSTONE PROJECT

- Arif Maulana (051522256)
- Bryan Adam Samuel S (049864261)
- Nurlaelatus Solihah (049932443)
- Sukmawandi (050629283)
- Teddy Aldrin P (051318287)

# Ma Rahma POS

Sistem kasir dan manajemen bahan baku untuk Ayam Penyet Ma Rahma.

Stack: Laravel 13, Blade, Tailwind CSS, Vite, SweetAlert2, MySQL.

## Persyaratan

- PHP 8.3+
- Composer
- Node.js 20+
- MySQL 8+

## Instalasi

```bash
composer install
cp .env.example .env
php artisan key:generate
```

Sesuaikan database di `.env`:

```env
APP_NAME="Ma Rahma POS"
APP_TIMEZONE=Asia/Jakarta
APP_LOCALE=id

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=ayam_penyet_ma_rahma
DB_USERNAME=root
DB_PASSWORD=
```

Buat database MySQL, lalu:

```bash
php artisan migrate --seed
npm install
npm run build
php artisan serve
```

Untuk development frontend:

```bash
composer run dev
```

## Akun demo

| Peran   | Username | Password |
|---------|----------|----------|
| Pemilik | owner    | password |
| Kasir   | cashier  | password |

## Fitur utama

- Login / logout dengan peran Kasir dan Pemilik
- Kasir (POS): keranjang, total otomatis, metode tunai/QRIS/transfer
- Menu, bahan baku, dan resep
- Pengurangan stok otomatis dari resep saat transaksi
- Pergerakan stok manual + peringatan stok minimum
- Riwayat penjualan dan struk cetak browser
- Laporan penjualan, menu terlaris, dan posisi stok
- Manajemen pengguna (pemilik)

## Pengujian

```bash
php artisan test
```
