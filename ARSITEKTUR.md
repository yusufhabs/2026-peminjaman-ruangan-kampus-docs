# Arsitektur Sistem - Peminjaman Ruangan Kampus

## Gambaran Umum
Sistem ini menggunakan arsitektur Client-Server dengan 3 komponen utama:
Backend API, Frontend Web, dan Mobile App.

## Komponen Sistem

### Backend (ASP.NET Core Web API)
- Framework  : ASP.NET Core Web API (.NET 8)
- Database   : MySQL (via Pomelo EF Core)
- ORM        : Entity Framework Core
- Port       : 5248

### Frontend (React + TypeScript)
- Framework  : React 18 + TypeScript
- Build Tool : Vite
- HTTP Client: Axios
- Port       : 5173

### Mobile (Flutter)
- Framework  : Flutter 3
- Language   : Dart
- HTTP Client: package:http
- Target     : Web, Android, iOS

### Database
- DBMS       : MySQL 8.0
- ORM        : Entity Framework Core
- Migration  : EF Core Migrations

## Alur Komunikasi
Frontend (React) -------|
|---> Backend API (ASP.NET) ---> Database (MySQL)
Mobile (Flutter) -------|

## Branching Strategy
main
|-->develop
|-->feature/peminjaman-ruangan-crud
|--> feature/peminjaman-ruangan-ui
|--> feature/peminjaman-ruangan-mobile
|--> feature/data-seeding


