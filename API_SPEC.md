# API Specification - Sistem Peminjaman Ruangan Kampus

## Base URL
http://localhost:5248/api

## Endpoints

### 1. Get All Peminjaman
- Method  : GET
- URL     : /peminjaman
- Query   : search (opsional)
- Response: 200 OK

### 2. Get Detail Peminjaman
- Method  : GET
- URL     : /peminjaman/{id}
- Response: 200 OK / 404 Not Found

### 3. Create Peminjaman
- Method  : POST
- URL     : /peminjaman
- Body    :
  {
    "namaPeminjam": "string (required)",
    "nomorRuangan": "string (required)",
    "tanggalPinjam": "datetime (required)",
    "tanggalKembali": "datetime (required)",
    "keperluan": "string",
    "status": "string"
  }
- Response: 201 Created / 400 Bad Request

### 4. Update Peminjaman
- Method  : PUT
- URL     : /peminjaman/{id}
- Body    : sama dengan Create
- Response: 200 OK / 404 Not Found

### 5. Delete Peminjaman (Soft Delete)
- Method  : DELETE
- URL     : /peminjaman/{id}
- Response: 200 OK / 404 Not Found

### 6. Update Status Peminjaman
- Method  : PATCH
- URL     : /peminjaman/{id}/status
- Body    : "menunggu" / "disetujui" / "ditolak"
- Response: 200 OK / 404 Not Found

## Status Peminjaman
| Status    | Keterangan                        |
|-----------|-----------------------------------|
| menunggu  | Pengajuan belum diproses          |
| disetujui | Pengajuan telah disetujui admin   |
| ditolak   | Pengajuan ditolak admin           |