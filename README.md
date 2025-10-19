# trafelmeta-ai
Berikut contoh **README.md** lengkap dan profesional untuk proyek chatbot kamu — sudah disesuaikan dengan kode TravelMate AI Chatbot berbasis **LLaMA LLM** 👇

---

```markdown
# ✈️ TravelMate AI - Chatbot Wisata Cerdas Berbasis LLaMA LLM

![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![Framework](https://img.shields.io/badge/Framework-Gradio-orange.svg)
![Model](https://img.shields.io/badge/Model-LLaMA_3.1_/_LLaMA_2-green.svg)
![License](https://img.shields.io/badge/License-MIT-lightgrey.svg)

---

## 🧠 Deskripsi Proyek

**TravelMate AI** adalah chatbot berbasis **Large Language Model (LLM)** yang dirancang untuk menjadi **asisten perjalanan pintar**.  
Chatbot ini dibangun menggunakan **LLaMA (Meta AI)** — model bahasa besar yang mampu memahami dan merespons bahasa alami secara kontekstual.

Dengan TravelMate AI, pengguna dapat:
- Merencanakan itinerary perjalanan
- Mendapat rekomendasi destinasi & kuliner
- Menghitung estimasi biaya perjalanan
- Mendapat tips, rute, dan inspirasi wisata  
Semua dilakukan melalui percakapan alami, interaktif, dan menyenangkan. 🌏✨

---

## 🚀 Fitur Utama

| Fitur | Deskripsi |
|-------|------------|
| 🧭 **Natural Language Understanding (LLM)** | Menggunakan model **LLaMA 3.1 (API)** atau **LLaMA 2 (Local)** untuk memahami bahasa alami |
| 🧠 **Contextual Chat** | Chatbot mengingat konteks percakapan sebelumnya |
| 🗺️ **Itinerary Generator** | Membuat rencana perjalanan berdasarkan durasi, lokasi, dan budget |
| 🍜 **Kuliner & Tips Lokal** | Rekomendasi makanan khas dan tips wisata di berbagai destinasi |
| 💰 **Budget Estimator** | Memberikan estimasi biaya harian di berbagai kota |
| 🔗 **Dual Mode (API / Local)** | Bisa dijalankan via **API Groq/Together AI** atau **model lokal (offline)** |
| 💬 **Interactive UI** | Dibangun dengan **Gradio UI** agar mudah digunakan |

---

## ⚙️ Arsitektur Sistem

```

User 🧍
│
▼
Gradio Frontend 💬
│
▼
TravelMate Engine 🧠 (Python)
├── Mode 1: API LLaMA 3.1 via Groq / Together AI
└── Mode 2: Local LLaMA 2-7B (Hugging Face Transformers)
│
▼
Response Generation ✈️

````

---

## 💡 Teknologi yang Digunakan

| Komponen | Teknologi |
|-----------|------------|
| Bahasa Pemrograman | Python 3.10+ |
| UI Framework | Gradio |
| NLP Model | LLaMA 3.1 / LLaMA 2 |
| Library | `transformers`, `torch`, `requests`, `accelerate`, `bitsandbytes`, `sentencepiece` |
| API Provider | [Groq Cloud](https://console.groq.com), [Together AI](https://api.together.xyz) |

---

## 🔧 Cara Menjalankan

### 1️⃣ Clone Repository
```bash
git clone https://github.com/username/travelmate-ai.git
cd travelmate-ai
````

### 2️⃣ Install Dependencies

#### a. Mode API (Disarankan)

```bash
pip install gradio requests
```

#### b. Mode Lokal (Butuh 4GB+ RAM)

```bash
pip install gradio transformers torch accelerate bitsandbytes sentencepiece
```

### 3️⃣ Tambahkan API Key

Edit bagian konfigurasi di kode:

```python
API_CONFIG = {
    "groq": {
        "api_key": "YOUR_GROQ_API_KEY_HERE"
    },
    "together": {
        "api_key": "YOUR_TOGETHER_API_KEY_HERE"
    }
}
```

Dapatkan API key gratis di:

* [https://console.groq.com](https://console.groq.com)
* [https://api.together.xyz](https://api.together.xyz)

### 4️⃣ Jalankan Program

```bash
python travelmate_ai.py
```

Setelah berjalan, akan muncul link Gradio seperti:

```
Running on public URL: https://xxxxx.gradio.live
```

Klik link tersebut untuk mulai chatting! 💬

---

## 🧩 Konfigurasi

```python
USE_API = True  # Gunakan True untuk mode API (cepat & ringan)
LOCAL_MODEL = "meta-llama/Llama-2-7b-chat-hf"
```

* **Mode API:** Menggunakan model LLaMA 3.1 (via Groq/Together)
* **Mode Lokal:** Menggunakan LLaMA 2 7B via Hugging Face (offline, butuh GPU)

---

## 🧳 Contoh Percakapan

**Kamu:**

> Aku mau liburan 5 hari ke Bali dengan budget 5 juta, rekomendasiin dong!

**TravelMate AI 🤖:**

> 🏝️ Wah seru banget! Dengan budget 5 juta untuk 5 hari, kamu bisa:
>
> * Menginap di guesthouse Seminyak (Rp 250k/malam)
> * Explore Ubud, Uluwatu, dan Nusa Penida
> * Coba kuliner: Babi Guling, Sate Lilit, dan Nasi Campur Bali
>
> Mau aku bantu buatkan itinerary harian juga? 📅✨

---

## 🎨 Tampilan Antarmuka

UI dibangun dengan **Gradio** dan mendukung tema modern berwarna ungu dengan gradient:

* Chatbot interaktif dengan bubble chat
* Textbox input cepat
* Tombol **Send 🚀**
* Contoh pertanyaan (Examples)
* Panel informasi model & tips penggunaan

---

## 🧠 System Prompt (LLaMA Personality)

Chatbot dikonfigurasi agar memiliki kepribadian:

* Ramah dan antusias 🥰
* Menggunakan Bahasa Indonesia santai dengan sedikit istilah Inggris
* Selalu menambahkan emoji & struktur rapi
* Fokus pada **travel advice yang spesifik dan bermanfaat**

---

## 🧾 Contoh Destinasi yang Dikenali

| Destinasi      | Info Utama                      |
| -------------- | ------------------------------- |
| **Bali**       | Pantai, budaya, kuliner khas    |
| **Tokyo**      | Teknologi, budaya Jepang modern |
| **Bangkok**    | Street food, kuil, pasar malam  |
| **Yogyakarta** | Warisan budaya, candi, kuliner  |
| **Singapore**  | Urban tourism, efisien & bersih |

---

## 💻 Struktur File

```
📂 travelmate-ai/
 ├── travelmate_ai.py          # File utama chatbot
 ├── README.md                 # Dokumentasi proyek
 └── requirements.txt          # (Opsional) daftar dependensi
```

---

## 🧩 Fallback Mode

Jika API key tidak terdeteksi, chatbot akan:

* Menggunakan **mode fallback** (rule-based)
* Memberikan jawaban dari **basis pengetahuan lokal**
* Tetap interaktif namun tanpa LLM

---

## 📜 Lisensi

Proyek ini dilisensikan di bawah lisensi **MIT License** — kamu bebas menggunakannya untuk keperluan akademik atau pengembangan.

---

## 👨‍💻 Kontributor

Dikembangkan oleh:
**Ngurah Adi**
💡 Dengan dukungan teknologi LLaMA (Meta AI) dan Gradio UI.

---

## 🌐 Demo (Opsional)

Jika kamu menjalankan `share=True`, sistem akan memberikan link seperti:

```
https://xxxxx.gradio.live
```

yang bisa kamu bagikan untuk diuji oleh orang lain secara online.

---

## 🧭 Catatan

* Model **LLaMA lokal** memerlukan GPU (NVIDIA 6GB+ disarankan).
* Mode **API (Groq/Together)** direkomendasikan untuk uji coba cepat.
* Pastikan koneksi internet stabil jika menggunakan API.

---

> ✈️ *“TravelMate AI — Your smart companion for every journey.”*

```

---

Apakah kamu mau saya buatkan juga file **`requirements.txt`** yang cocok dengan program ini (supaya bisa langsung diinstal dengan `pip install -r requirements.txt`)?
```
