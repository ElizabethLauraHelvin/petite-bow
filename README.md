# Petite Bow — Toko Coquette

- backend/   -> Node.js + Express (REST API + login JWT) + SQLite (toko.db dibuat otomatis)
- frontend/  -> HTML, CSS, JavaScript (dilayani oleh backend)

Jalan (butuh Node.js 18+):
    cd backend
    npm install
    npm start
Buka http://localhost:3000

Endpoint API:
    POST /api/auth/register   {name,email,password,phone,address}
    POST /api/auth/login      {email,password}
    GET  /api/auth/me         (Bearer token)
    GET  /api/products[?category=Fashion]
    GET  /api/products/:id
    POST /api/orders          (login) {payment,shipping,items:[{productId,qty}]}
    GET  /api/orders          (login) riwayat pesanan sendiri

Jika sebelumnya sudah punya toko.db versi lama, pesanan lama otomatis dipindah
ke tabel orders_legacy / order_items_legacy.
