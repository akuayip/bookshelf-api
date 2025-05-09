# 📚 Bookshelf API

Bookshelf API adalah proyek backend sederhana menggunakan **Node.js** dan **Hapi.js** yang dirancang untuk mengelola data buku. Proyek ini merupakan bagian dari submission kelas **Belajar Membuat Aplikasi Back-End untuk Pemula** di Dicoding.

---

## 🚀 Fitur Utama

- Menambahkan buku baru  
  `POST /books`
- Menampilkan seluruh buku  
  `GET /books`
- Menampilkan detail buku berdasarkan ID  
  `GET /books/{bookId}`
- Mengubah data buku  
  `PUT /books/{bookId}`
- Menghapus buku  
  `DELETE /books/{bookId}`

### 🧭 Query Opsional

- `?name=keyword` → Filter nama buku (non-case-sensitive)
- `?reading=1/0` → Filter berdasarkan status sedang dibaca
- `?finished=1/0` → Filter berdasarkan status selesai dibaca

---

## 📁 Struktur Proyek

```
bookshelf-api/
├── src/
│   ├── handlers/
│   │   └── booksHandler.js
│   ├── routes/
│   │   └── books.js
│   └── server.js
├── utils/
│   └── books.js
├── package.json
├── package-lock.json
├── .gitignore
└── eslint.config.mjs
```

---

## ⚙️ Menjalankan Proyek

1. Clone repository:

   ```bash
   git clone https://github.com/username/bookshelf-api.git
   cd bookshelf-api
   ```

2. Install dependency:

   ```bash
   npm install
   ```

3. Jalankan server:

   ```bash
   npm run start
   ```

4. Akses server di:

   ```
   http://localhost:9000
   ```

---

## 🧪 Pengujian

Proyek diuji menggunakan **Postman Collection & Environment** dari Dicoding:

- Semua request [Mandatory] dan [Optional] ✅ berhasil
- Validasi berjalan dengan benar:
  - `name` wajib diisi
  - `readPage` tidak boleh melebihi `pageCount`
- Format respons mengikuti standar: `status`, `message`, dan `data`

---

## 📌 Catatan

- Data disimpan **sementara (in-memory)** di `utils/books.js`
- Tidak menggunakan database eksternal
- Tidak menggunakan `nodemon` pada script `start`
- Kompatibel dengan Node.js v18+

---

## 📄 Lisensi

Proyek ini dibuat untuk keperluan edukasi dan submission. Silakan digunakan atau dikembangkan lebih lanjut sesuai kebutuhan.
