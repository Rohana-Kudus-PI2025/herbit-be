# HERBIT API Documentation with Cookie-Based JWT Authentication

> API Documentation lengkap untuk platform HERBIT, aplikasi habit tracker ramah lingkungan yang memberdayakan perempuan untuk menerapkan kebiasaan hijau, mendapatkan poin, dan menukarnya dengan reward & voucher.

---

## Live API Deployment (Vercel)

Server API sudah di-deploy dan bisa diakses secara publik melalui:
**[https://herbit-backend.vercel.app/](https://herbit-backend.vercel.app/)**

---

## Quick Links

- [Interactive API Documentation](https://documenter.getpostman.com/view/47645269/2sB3WsNzEy)

- [![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/47645269-18e73855-1b70-4c0d-b219-4c4a3dac328a?action=collection%2Ffork&source=rip_markdown&collection-url=entityId%3D47645269-18e73855-1b70-4c0d-b219-4c4a3dac328a%26entityType%3Dcollection%26workspaceId%3D76d9a83e-3e52-4cbe-84f9-e5c9c82d3e01#?env%5Bherbit-prod%5D=W3sia2V5IjoiYWRtaW5fdG9rZW4iLCJ2YWx1ZSI6IiIsImVuYWJsZWQiOnRydWUsInR5cGUiOiJzZWNyZXQiLCJzZXNzaW9uVmFsdWUiOiIiLCJzZXNzaW9uSW5kZXgiOjB9LHsia2V5IjoiYmFzZV91cmwiLCJ2YWx1ZSI6Imh0dHBzOi8vaGVyYml0LWJhY2tlbmQudmVyY2VsLmFwcC9hcGkiLCJlbmFibGVkIjp0cnVlLCJ0eXBlIjoiZGVmYXVsdCIsInNlc3Npb25WYWx1ZSI6Imh0dHBzOi8vaGVyYml0LWJhY2tlbmQudmVyY2VsLmFwcC9hcGkiLCJzZXNzaW9uSW5kZXgiOjF9LHsia2V5IjoiY29va2llX25hbWUiLCJ2YWx1ZSI6ImFjY2Vzc190b2tlbiIsImVuYWJsZWQiOnRydWUsInR5cGUiOiJkZWZhdWx0Iiwic2Vzc2lvblZhbHVlIjoiYWNjZXNzX3Rva2VuIiwic2Vzc2lvbkluZGV4IjoyfSx7ImtleSI6ImF1dGhfcm9sZSIsInZhbHVlIjoidXNlciIsImVuYWJsZWQiOnRydWUsInR5cGUiOiJkZWZhdWx0Iiwic2Vzc2lvblZhbHVlIjoidXNlciIsInNlc3Npb25JbmRleCI6M30seyJrZXkiOiJ1c2VyX3Rva2VuIiwidmFsdWUiOiIiLCJlbmFibGVkIjp0cnVlLCJ0eXBlIjoic2VjcmV0Iiwic2Vzc2lvblZhbHVlIjoiIiwic2Vzc2lvbkluZGV4Ijo0fV0=)
- Download Collection:
  - [Herbit_API_Collection.json](./Downloads/HERBIT.postman_collection.json)
  - [Herbit_Production_Environment.json](./Downloads/herbit-prod.postman_environment.json)

---

## Features

### Public Endpoints

- Register dan login pengguna baru
- Melihat daily habits publik
- Melihat daftar rewards & vouchers aktif

### User Endpoints

- Checklist daily eco-habits (tumbler, tolak plastik, hemat listrik)
- Melihat progres pohon (daun & buah)
- Klaim reward streak & voucher
- Mengelola profil (username, email, foto)
- Proyek eco-enzim (upload progress, klaim poin)
- Game mini untuk edukasi lingkungan
- Notifikasi personal

### Admin Endpoints

- Login admin
- CRUD voucher, reward, dan daily task
- Verifikasi proyek eco-enzim pengguna
- Melihat riwayat klaim & poin pengguna
- Statistik redemptions dan milestone

## API Documentations

### Option 1: Interactive Documentation (Postman)

Dokumentasi interaktif lengkap dengan contoh request/response:

- [Interactive API Documentation](https://documenter.getpostman.com/view/47645269/2sB3WsNzEy)

Features:

- ✅ Semua endpoints dengan examples
- ✅ Auto-updated dari collection
- ✅ Bisa test langsung dengan "Run in Postman"
- ✅ Copy-paste ready code snippets

- [![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/47645269-18e73855-1b70-4c0d-b219-4c4a3dac328a?action=collection%2Ffork&source=rip_markdown&collection-url=entityId%3D47645269-18e73855-1b70-4c0d-b219-4c4a3dac328a%26entityType%3Dcollection%26workspaceId%3D76d9a83e-3e52-4cbe-84f9-e5c9c82d3e01#?env%5Bherbit-prod%5D=W3sia2V5IjoiYWRtaW5fdG9rZW4iLCJ2YWx1ZSI6IiIsImVuYWJsZWQiOnRydWUsInR5cGUiOiJzZWNyZXQiLCJzZXNzaW9uVmFsdWUiOiIiLCJzZXNzaW9uSW5kZXgiOjB9LHsia2V5IjoiYmFzZV91cmwiLCJ2YWx1ZSI6Imh0dHBzOi8vaGVyYml0LWJhY2tlbmQudmVyY2VsLmFwcC9hcGkiLCJlbmFibGVkIjp0cnVlLCJ0eXBlIjoiZGVmYXVsdCIsInNlc3Npb25WYWx1ZSI6Imh0dHBzOi8vaGVyYml0LWJhY2tlbmQudmVyY2VsLmFwcC9hcGkiLCJzZXNzaW9uSW5kZXgiOjF9LHsia2V5IjoiY29va2llX25hbWUiLCJ2YWx1ZSI6ImFjY2Vzc190b2tlbiIsImVuYWJsZWQiOnRydWUsInR5cGUiOiJkZWZhdWx0Iiwic2Vzc2lvblZhbHVlIjoiYWNjZXNzX3Rva2VuIiwic2Vzc2lvbkluZGV4IjoyfSx7ImtleSI6ImF1dGhfcm9sZSIsInZhbHVlIjoidXNlciIsImVuYWJsZWQiOnRydWUsInR5cGUiOiJkZWZhdWx0Iiwic2Vzc2lvblZhbHVlIjoidXNlciIsInNlc3Npb25JbmRleCI6M30seyJrZXkiOiJ1c2VyX3Rva2VuIiwidmFsdWUiOiIiLCJlbmFibGVkIjp0cnVlLCJ0eXBlIjoic2VjcmV0Iiwic2Vzc2lvblZhbHVlIjoiIiwic2Vzc2lvbkluZGV4Ijo0fV0=)

#### Catatan Penting (Postman)

**SEBELUM FORKING** melalui tombol **Run in Postman** pastikan setting berikut agar forking berhasil:

1. Buka **Settings** di Postman (⚙️ icon di kiri atas)
2. Pilih tab **Profile**
3. Pastikan **Make profile public** dalam keadaan **ON** (toggle aktif)
4. Pilih tab **Workbench**
5. Pastikan **Make workbench public** dalam keadaan **ON** (toggle aktif)

**SETELAH FORKING**, lakukan ini agar request tidak error:

1. Buka tab **Environments** di Postman
2. Pilih environment **herbit-prod**
3. Klik **Set Active** (pojok kanan atas)

### Option 2: Download Postman Collection

Download dan import ke Postman:

- Download Collection:
  - [Herbit_API_Collection.json](./Downloads/HERBIT.postman_collection.json)
  - [Herbit_Production_Environment.json](./Downloads/herbit-prod.postman_environment.json)

### Option 3: Manual Documentation

Base URL: `https://herbit-backend.vercel.app/api`

> **Note:** HERBIT menggunakan **cookie JWT (`access_token`)**.  
> Setelah login, cookie otomatis dikirim di setiap request.  
> Untuk tes manual di Postman, sertakan:
>
> - `Cookie: access_token={{user_token}}` untuk user
> - `Cookie: access_token={{admin_token}}` untuk admin

---

#### 1. Public Endpoints

| Method | Endpoint                 | Description                                          | Auth Required |
| ------ | ------------------------ | ---------------------------------------------------- | ------------- |
| GET    | `/daily`                 | Ambil daftar tugas eco-habit harian publik           | ❌            |
| GET    | `/vouchers`              | Lihat semua voucher aktif yang bisa diklaim publik   | ❌            |
| GET    | `/vouchers/:id`          | Detail voucher berdasarkan ID                        | ❌            |
| GET    | `/ecoenzim/projects`     | Lihat daftar proyek eco-enzim publik                 | ❌            |
| GET    | `/ecoenzim/projects/:id` | Detail proyek eco-enzim publik berdasarkan ID        | ❌            |
| GET    | `/articles`              | Artikel publik seputar kebiasaan ramah lingkungan    | ❌            |
| GET    | `/leaderboard`           | Lihat papan peringkat pengguna dengan poin tertinggi | ❌            |
| GET    | `/faqs`                  | Pertanyaan umum terkait HERBIT                       | ❌            |

---

#### 2. Authentication Endpoints

| Method | Endpoint                | Description                | Auth Required |
| ------ | ----------------------- | -------------------------- | ------------- |
| POST   | `/auth/register`        | Register user baru         | ❌            |
| POST   | `/auth/login`           | Login user dan set cookie  | ❌            |
| GET    | `/auth/me`              | Get current user info      | ✅            |
| POST   | `/auth/forgot-password` | Kirim link reset password  | ❌            |
| POST   | `/auth/forget-password` | Reset password via token   | ❌            |
| POST   | `/admin/login`          | Login admin dan set cookie | ❌            |

---

#### 3. Public Endpoints User Endpoints

| Method | Endpoint                       | Description                      | Auth Required |
| ------ | ------------------------------ | -------------------------------- | ------------- |
| GET    | `/users/home-summary`          | Ringkasan data untuk homepage    | ✅            |
| GET    | `/users/profile-summary`       | Statistik profil dan eco points  | ✅            |
| GET    | `/checklists/today`            | Checklist habit harian hari ini  | ✅            |
| PATCH  | `/checklists/:id/complete`     | Tandai habit selesai             | ✅            |
| PATCH  | `/checklists/:id/uncheck`      | Batalkan penyelesaian habit      | ✅            |
| GET    | `/progress/weekly`             | Lihat progres mingguan           | ✅            |
| GET    | `/leaves`                      | Daftar daun (perkembangan pohon) | ✅            |
| GET    | `/fruits`                      | Daftar buah (milestone)          | ✅            |
| PATCH  | `/fruits/:id/claim`            | Klaim buah/milestone             | ✅            |
| GET    | `/tree`                        | Lihat data pohon habit           | ✅            |
| POST   | `/rewards/:code/claim`         | Klaim reward berdasarkan kode    | ✅            |
| POST   | `/vouchers/:id/preview`        | Pratinjau voucher                | ✅            |
| POST   | `/vouchers/:id/claim`          | Klaim voucher menggunakan poin   | ✅            |
| GET    | `/redemptions/me`              | Lihat riwayat voucher user       | ✅            |
| GET    | `/ecoenzim/projects`           | Daftar proyek eco-enzim user     | ✅            |
| POST   | `/ecoenzim/projects`           | Tambah proyek eco-enzim          | ✅            |
| PUT    | `/ecoenzim/projects/:id`       | Update proyek eco-enzim          | ✅            |
| POST   | `/ecoenzim/projects/:id/claim` | Klaim poin proyek eco-enzim      | ✅            |
| DELETE | `/ecoenzim/projects/:id`       | Hapus proyek eco-enzim           | ✅            |
| POST   | `/ecoenzim/uploads`            | Upload progres bulanan (foto)    | ✅            |
| GET    | `/notifications`               | Lihat notifikasi user            | ✅            |
| DELETE | `/notifications/clear-all`     | Hapus semua notifikasi           | ✅            |
| PATCH  | `/users/username`              | Update username                  | ✅            |
| PATCH  | `/users/email`                 | Update email                     | ✅            |
| POST   | `/users/profile-photo`         | Upload foto profil               | ✅            |
| GET    | `/users/profile-photo/:id`     | Ambil foto profil                | ✅            |

---

#### 4. Admin Endpoints

| Method | Endpoint                         | Description                   | Auth Required | Role  |
| ------ | -------------------------------- | ----------------------------- | ------------- | ----- |
| POST   | `/admin/login`                   | Login admin dan set cookie    | ❌            | —     |
| GET    | `/admin/users`                   | Lihat semua pengguna          | ✅            | Admin |
| GET    | `/admin/vouchers`                | Lihat daftar voucher          | ✅            | Admin |
| POST   | `/admin/vouchers`                | Tambah voucher baru           | ✅            | Admin |
| PATCH  | `/admin/vouchers/:id`            | Update voucher                | ✅            | Admin |
| DELETE | `/admin/vouchers/:id`            | Hapus voucher                 | ✅            | Admin |
| POST   | `/admin/vouchers/:id/activate`   | Aktifkan voucher              | ✅            | Admin |
| POST   | `/admin/vouchers/:id/deactivate` | Nonaktifkan voucher           | ✅            | Admin |
| GET    | `/admin/rewards`                 | Lihat daftar rewards          | ✅            | Admin |
| POST   | `/admin/rewards`                 | Tambah reward baru            | ✅            | Admin |
| GET    | `/admin/daily`                   | Lihat daftar daily eco-habit  | ✅            | Admin |
| POST   | `/admin/daily`                   | Tambah daily eco-habit        | ✅            | Admin |
| PATCH  | `/admin/daily/:id`               | Update daily eco-habit        | ✅            | Admin |
| DELETE | `/admin/daily/:id`               | Hapus daily eco-habit         | ✅            | Admin |
| PUT    | `/ecoenzim/uploads/:id/verify`   | Verifikasi unggahan eco-enzim | ✅            | Admin |
| GET    | `/admin/points-history`          | Riwayat poin semua pengguna   | ✅            | Admin |
| GET    | `/admin/points-history/:userId`  | Riwayat poin berdasarkan user | ✅            | Admin |

---

## Request & Response Examples

## 1. Register User

**Request:**

```http
POST /api/auth/register
Content-Type: application/json

{
  "email": "anggi@mail.com",
  "password": "password123",
  "username": "angginew"
}
```

**Response (201 Created):**

```json
{
  "success": true,
  "message": "Registered"
}
```

---

### 2. Login User

**Request:**

```http
POST /api/auth/login
Content-Type: application/json

{
  "email": "anggi@mail.com",
  "password": "password12345678"
}
```

**Response (200 OK):**

```json
{
  "success": true,
  "data": {
    "user": {
      "id": "68fc8ecd879dcc0fd1697d61",
      "email": "anggi@mail.com",
      "username": "angginew",
      "photoUrl": "/api/users/profile-photo/690c3736fd417896d1299af9",
      "role": "user"
    }
  },
  "message": "Logged in"
}
```

---

### 3. Get Current User

**Request:**

```http
GET /api/auth/me
Cookie: access_token={user_token}
```

**Response (200 OK):**

```json
{
  "success": true,
  "data": {
    "id": "68fc8ecd879dcc0fd1697d61",
    "email": "anggi@mail.com",
    "username": "angginew",
    "role": "user"
  }
}
```

---

### 4. Update Username

**Request:**

```http
PATCH /api/users/username
Cookie: access_token={user_token}
Content-Type: application/json

{
  "username": "anggihabit"
}
```

**Response (200 OK):**

```json
{
  "success": true,
  "message": "Username updated successfully",
  "data": {
    "username": "anggihabit"
  }
}
```

---

### 5. Complete Daily Checklist

**Request:**

```http
PATCH /api/checklists/6901906d924044088e0f05c6/complete
Cookie: access_token={user_token}
```

**Response (200 OK):**

```json
{
  "success": true,
  "message": "Checklist completed",
  "data": {
    "taskId": "6901906d924044088e0f05c6",
    "completedAt": "2025-10-29T09:41:54.243Z"
  }
}
```

---

### 6. Claim Voucher

**Request:**

```http
POST /api/vouchers/6901f22b4aa31c8d43252c67/claim
Cookie: access_token={user_token}
Content-Type: application/json
```

**Response (200 OK):**

```json
{
  "success": true,
  "message": "Voucher claimed",
  "data": {
    "redemptionId": "6901f2304aa31c8d43252c92",
    "pointsUsed": 300
  }
}
```

---

### 7. Create Ecoenzym Project

**Request:**

```http
POST /api/ecoenzim/projects
Cookie: access_token={user_token}
Content-Type: application/json

{
  "projectName": "Eco Enzyme Batch Oktober",
  "description": "Proyek membuat eco-enzim dari sisa buah",
  "startDate": "2025-10-01",
  "endDate": "2025-10-31"
}
```

**Response (201 Created):**

```json
{
  "success": true,
  "message": "Ecoenzym project created",
  "data": {
    "id": "690c3736fd417896d1299af9",
    "projectName": "Eco Enzyme Batch Oktober",
    "status": "active"
  }
}
```

---

### 8. Admin Login

**Request:**

```http
POST /api/admin/login
Content-Type: application/json

{
  "email": "admin@mail.com",
  "password": "admin12345678"
}
```

**Response (200 OK):**

```json
{
  "success": true,
  "data": {
    "user": {
      "id": "68ff12003c54f90ccd9b5201",
      "email": "admin@mail.com",
      "username": "superadmin",
      "role": "admin"
    }
  },
  "message": "Admin logged in"
}
```

---

### 9. Admin Create Daily Habit

**Request:**

```http
POST /api/admin/daily
Cookie: access_token={admin_token}
Content-Type: application/json

{
  "title": "Hemat listrik harian",
  "category": "eco-action",
  "symbol": "💡"
}
```

**Response (201 Created):**

```json
{
  "success": true,
  "message": "Daily created",
  "data": {
    "id": "6901906d924044088e0f05c6",
    "title": "Hemat listrik harian",
    "category": "eco-action"
  }
}
```

---

### 10. Error Example - Unauthorized

**Response (401 Unauthorized):**

```json
{
  "success": false,
  "message": "Not authorized. Please login first."
}
```
