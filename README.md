# Linda's AI

**Linda's AI** adalah asisten virtual interaktif berbasis web yang menggabungkan backend yang kuat dengan antarmuka frontend yang menarik. Proyek ini menampilkan avatar animasi yang responsif terhadap emosi (mood), manajemen memori percakapan, dan antarmuka obrolan yang modern.

## 🚀 Fitur Utama

### Frontend
* **Avatar Ekspresif:** Karakter visual (Linda) yang berubah ekspresi (netral, senyum, sedih, berkedip, dll.) berdasarkan konteks percakapan.
* **Indikator Mood:** Visualisasi status emosi AI saat ini.
* **Panel Memori:** Antarmuka untuk melihat bagaimana AI menyimpan dan mengingat konteks percakapan.
* **Manajemen Chat:** Fitur ekspor riwayat obrolan dan pintasan keyboard untuk penggunaan yang lebih cepat.
* **Panel Pengaturan:** Konfigurasi API Key dan preferensi pengguna.

### Backend
* **API Berkinerja Tinggi:** Dibangun di atas **FastAPI** untuk respons yang cepat dan *asynchronous*.
* **Layanan LLM:** Integrasi dengan Large Language Models untuk pemrosesan bahasa alami.
* **Sistem Memori:** Layanan khusus untuk mengelola konteks jangka panjang dan pendek.
* **Validasi Data:** Menggunakan **Pydantic** untuk memastikan integritas data yang ketat.

## 🛠️ Teknologi yang Digunakan

**Backend:**
* [Python 3.12+](https://www.python.org/)
* [FastAPI](https://fastapi.tiangolo.com/) - Web framework.
* [Uvicorn](https://www.uvicorn.org/) - ASGI server.
* [Pydantic](https://docs.pydantic.dev/) - Validasi data.
* [Httpx](https://www.python-httpx.org/) - HTTP client asinkron.

**Frontend:**
* [React](https://react.dev/) - Library UI.
* [TypeScript](https://www.typescriptlang.org/) - Bahasa pemrograman yang terstruktur.
* [Vite](https://vitejs.dev/) - Build tool yang cepat.
* CSS Modern untuk styling dan animasi.

## 📋 Prasyarat Instalasi

Pastikan Anda telah menginstal perangkat lunak berikut di komputer Anda:
* **Python** (versi 3.12 atau lebih baru)
* **Node.js** (versi 18 atau lebih baru) & **npm**
* **Git**

## ⚙️ Instalasi dan Menjalankan

Ikuti langkah-langkah berikut untuk menjalankan proyek ini secara lokal:

### 1. Clone Repository

```bash
git clone [https://github.com/fanlleyys/linda-s-ai.git](https://github.com/fanlleyys/linda-s-ai.git)
cd linda-s-ai
2. Setup Backend
Masuk ke direktori backend, buat virtual environment, dan instal dependensi.

Bash

cd backend

# Buat virtual environment (Windows)
python -m venv .venv
# Aktifkan virtual environment (Windows)
.venv\Scripts\activate

# Atau di Linux/macOS:
# python3 -m venv .venv
# source .venv/bin/activate

# Instal dependensi
pip install -r requirements.txt
Jalankan server backend:

Bash

uvicorn app.main:app --reload
Backend akan berjalan di http://localhost:8000

3. Setup Frontend
Buka terminal baru, masuk ke direktori frontend, dan instal dependensi.

Bash

cd frontend

# Instal paket node modules
npm install

# Jalankan server pengembangan
npm run dev
Frontend akan berjalan di http://localhost:5173 (atau port yang ditampilkan di terminal).

📂 Susunan Project
Berikut adalah gambaran umum struktur direktori proyek:

Plaintext

linda-s-ai/
├── backend/                # Kode sumber server (Python/FastAPI)
│   ├── app/
│   │   ├── services/       # Logika bisnis (LLM, Memory, Search)
│   │   ├── config.py       # Konfigurasi aplikasi
│   │   ├── main.py         # Entry point aplikasi
│   │   └── schemas.py      # Model data Pydantic
│   ├── .venv/              # Virtual environment Python
│   ├── Dockerfile          # Konfigurasi Docker backend
│   └── requirements.txt    # Daftar dependensi Python
│
├── frontend/               # Kode sumber antarmuka (React/TS)
│   ├── public/
│   │   └── linda/          # Aset gambar avatar (png)
│   ├── src/
│   │   ├── components/     # Komponen UI (Chat, Avatar, Panels)
│   │   ├── config/         # Konfigurasi frontend
│   │   ├── hooks/          # Custom hooks (e.g., useLindaEmotion)
│   │   ├── lib/            # Utilitas library (SSE)
│   │   ├── utils/          # Fungsi bantuan (Export, Error handling)
│   │   ├── App.tsx         # Komponen utama
│   │   └── main.tsx        # Entry point React
│   ├── .env.development    # Variabel lingkungan frontend
│   ├── index.html          # File HTML utama
│   ├── package.json        # Dependensi Node.js
│   └── vite.config.ts      # Konfigurasi Vite
│
└── README.md               # Dokumentasi proyek
💡 Contoh Penggunaan
Buka browser dan arahkan ke alamat frontend (biasanya http://localhost:5173).

Jika diperlukan, masukkan API Key pada Settings Panel (ikon gerigi).

Ketik pesan di kolom chat, misalnya: "Halo Linda, apa kabar?".

Linda akan membalas pesan Anda. Perhatikan:

Ekspresi wajah avatar berubah sesuai konteks (Senang, Netral, atau Sedih).

Mood Indicator akan memperbarui status emosi.

Lihat Memory Panel untuk melihat bagaimana AI menyimpan informasi dari percakapan Anda.

🤝 Kontribusi
Kontribusi sangat diterima! Jika Anda ingin meningkatkan fitur atau memperbaiki bug:

Fork repositori ini.

Buat branch fitur baru (git checkout -b fitur-keren-anda).

Commit perubahan Anda (git commit -m 'Menambahkan fitur keren').

Push ke branch tersebut (git push origin fitur-keren-anda).

Buat Pull Request.

📄 Lisensi
Proyek ini didistribusikan di bawah lisensi MIT. Lihat file LICENSE untuk informasi lebih lanjut.

Plaintext

MIT License

Copyright (c) [2025] [Alfan Januar]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
