# 🤖 ChatBot‑LLM

A simple chatbot interface leveraging Google’s LLM (Gemini API).

## Fitur Utama

- Mengirim prompt teks ke Gemini API.
- Menampilkan balasan dari AI.
- Mendukung konfigurasi model dan pengelolaan API key.

## Prasyarat

- Python 3.8+ .
- Akun Google.
- API key Gemini dari **Google AI Studio**.
- (Opsional) Billing di Google Cloud jika ingin akses tier berbayar / produksi.

## Cara Daftar dan Dapatkan API Key Gemini

1. Kunjungi **Google AI Studio** (aistudio.google.com) dan login dengan akun Google. 
2. Klik tombol **"Get API Key"** di pojok kanan atas. 
3. Pilih **"Create API Key"**, buat key baru dalam project baru atau yang sudah ada. 
4. Setujui Terms of Service (centang "Google APIs Terms of Service"). 
5. API key langsung tampil — **salin dan simpan dengan aman** (ini satu‑satunya kesempatan melihat key penuh). 
6. (Opsional) Jika ingin akses ke tier produksi atau model Pro (tanpa batasan free tier), aktifkan billing melalui Google Cloud Console. 

### Ringkasan Cepat

| Langkah | Deskripsi |
|--------|-----------|
| 1 | Login ke Google AI Studio |
| 2 | “Get API Key” → “Create API Key” |
| 3 | Pilih project |
| 4 | Setujui TOS |
| 5 | Salin key (simpan aman) |
| 6 | (Opsional) Aktifkan billing untuk akses berbayar |

---

## Cara Integrasi di Project

### Contoh Python

```bash
pip install google-generativeai
````

```python
import google.generativeai as genai

# Konfigurasi API key
genai.configure(api_key="YOUR_GEMINI_API_KEY")

# Pilih model
model = genai.GenerativeModel("gemini-1.5-flash")

# Contoh chat
response = model.generate_content("Halo, apa kabar?")
print(response.text)
```

## Catatan Biaya & Limit

* Free tier (AI Studio): hingga 60 request/menit, \~1000 request/hari. ([blog.google][1])
* Untuk penggunaan di atas itu, aktifkan billing & masuk ke tier berbayar.
* Token input/output dihitung, dan ada biaya tambahan untuk context caching. ([reddit.com][9], [reddit.com][8])

---

## License

MIT © 2025 (Iwan Cilibur)

---

## Kontribusi

Selamat datang! Fork, buat pull request, dan beri bintang ⭐ kalau terbantu!

```

[1]: https://blog.google/technology/ai/gemini-api-developers-cloud/?utm_source=chatgpt.com "Google Gemini API: New developer and enterprise AI products"
[2]: https://docs.aicontentlabs.com/articles/google-gemini-api-key/?utm_source=chatgpt.com "How to Set Up the Google Gemini API Key in AI Content Labs"
[3]: https://www.androidcentral.com/apps-software/google-gemini?utm_source=chatgpt.com "Google Gemini AI: 2.5 Pro, Live, features, connected apps, and more"
[4]: https://dev.to/explinks/how-to-obtain-a-gemini-api-key-step-by-step-guide-4m97?utm_source=chatgpt.com "How to Obtain a Gemini API Key (Step-by-Step Guide) - DEV Community"
[5]: https://www.geeksforgeeks.org/how-to-use-google-gemini-api-key/?utm_source=chatgpt.com "How to Access and Use Google Gemini API Key (with Examples) - GeeksforGeeks"
[6]: https://ai.google.dev/tutorials/setup?utm_source=chatgpt.com "Get a Gemini API key  |  Google AI for Developers"
[7]: https://www.reddit.com/r/Bard/comments/1e7oi6f?utm_source=chatgpt.com "Can't not sign up for Google Cloud to use Gemini API"
[8]: https://www.reddit.com/r/GeminiAI/comments/1g4lz3b?utm_source=chatgpt.com "Need help: Gemini API and their stupid pricing"
[9]: https://www.reddit.com/r/GoogleGeminiAI/comments/1jmevb0?utm_source=chatgpt.com "Gemini 2.5 API in Privacy Mode?"
