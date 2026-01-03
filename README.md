# OpenMusicAPI

&#x20;

OpenMusicAPI adalah proyek **API Back-End** yang dibuat sebagai **syarat lulus kelas Belajar Fundamental Back-End dengan JavaScript**. Proyek ini bertujuan untuk menyediakan layanan pengelolaan data album musik menggunakan Node.js, Hapi, dan PostgreSQL.

---

## Dependensi

- **Node.js** - runtime environment JavaScript
- **Hapi** - framework untuk membuat API
- **PostgreSQL** - database relasional
- **node-pg-migrate**- untuk migrasi database
- **dotenv** - untuk konfigurasi environment variables
- **joi** - validasi input
- **nanoid** - untuk generate ID unik
- **auto-bind** - bind otomatis context class

---

## Instalasi

1. **Clone repository**

```bash
git clone <URL_REPOSITORY_ANDA>
cd OpenMusicAPI
```

2. **Install semua dependencies**

```bash
npm install
```

3. **Install dependencies**

```bash
# Install Hapi
npm install @hapi/hapi

# Install PostgreSQL client untuk Node.js
npm install pg

# Install node-pg-migrate untuk migrasi database
npm install node-pg-migrate

# Install dotenv untuk environment variables
npm install dotenv

# Install Joi untuk validasi input
npm install joi

# Install nanoid untuk generate ID unik
npm install nanoid

# Install auto-bind untuk bind otomatis context class
npm install auto-bind
```

4. **Setup environment** Buat file `.env` untuk konfigurasi database:

```env
PGHOST=localhost
PGUSER=your_username
PGPASSWORD=your_password
PGDATABASE=your_database
PGPORT=5432
```

5. **Jalankan server**

```bash
npm start
```

server is running => `http://localhost:3000`.

---

## Endpoint API

### 1. Tambah Album

```
POST /albums
```

**Request body**:

```json
{
  "name": "Nama Album",
  "year": 2025
}
```

**Response**:

```json
{
  "status": "success",
  "message": "Album berhasil ditambahkan",
  "data": {
    "albumId": "album-xxxx"
  }
}
```

---

### 2. Ambil Album berdasarkan ID

```
GET /albums/{id}
```

**Response**:

```json
{
  "status": "success",
  "data": {
    "album": {
      "id": "album-xxxx",
      "name": "Nama Album",
      "year": 2025,
    }
  }
}
```

---

### 3. Update Album

```
PUT /albums/{id}
```

**Request body**:

```json
{
  "name": "Nama Album Baru",
  "year": 2026
}
```

**Response**:

```json
{
  "status": "success",
  "message": "Album berhasil diperbarui"
}
```

---

### 4. Hapus Album

```
DELETE /albums/{id}
```

**Response**:

```json
{
  "status": "success",
  "message": "Album berhasil dihapus"
}
```

---

## Lisensi

Project ini bersifat open-source dan dapat digunakan untuk keperluan pembelajaran.

