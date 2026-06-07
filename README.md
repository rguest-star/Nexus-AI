# NEXUS — AI-Powered Code Editor

Browser-based code editor dengan AI assistant terintegrasi. Tidak perlu instalasi, tidak perlu backend — cukup buka satu file HTML.

![NEXUS Screenshot](screenshot.png)

## ✨ Fitur

- **Monaco Editor** — editor yang sama dengan VS Code, lengkap dengan syntax highlighting dan autocomplete
- **AI Chat** — tanya langsung ke AI soal kode Anda (Claude, GPT-4, Gemini, Groq, OpenRouter)
- **Multi-provider** — dukung provider online dan offline (Ollama, LM Studio, Jan)
- **File manager** — buat, edit, hapus file dalam project
- **Terminal** — terminal simulasi terintegrasi
- **Debugger** — breakpoint dan step-through debugging
- **LSP** — AI-powered completions, hover docs, dan diagnostics
- **Themes** — dark / light mode
- **Single file** — semua dalam satu `.html`, tidak perlu build step

---

## 🚀 Cara Pakai

### Opsi 1 — GitHub Pages (direkomendasikan)

Setelah fork/clone repo ini, aktifkan GitHub Pages di **Settings → Pages → Source: main branch**. Akses lewat:

```
https://<username>.github.io/<repo-name>/nexus_fixed.html
```

### Opsi 2 — Server lokal

```bash
# Python (biasanya sudah terinstall)
python -m http.server 8000

# Node.js
npx serve .

# PHP
php -S localhost:8000
```

Lalu buka `http://localhost:8000/nexus_fixed.html`.

> ⚠️ **Jangan buka langsung via double-click** (`file://`). Browser memblokir penyimpanan API key di protokol `file://`. Gunakan server lokal atau GitHub Pages.

---

## 🤖 Konfigurasi AI Provider

Klik ikon **AI** di toolbar → pilih provider → masukkan API key → Simpan & Aktifkan.

| Provider | Tipe | API Key | Link |
|----------|------|---------|------|
| **Claude** (Anthropic) | Online | `sk-ant-...` | [console.anthropic.com](https://console.anthropic.com/settings/keys) |
| **OpenAI** | Online | `sk-...` | [platform.openai.com](https://platform.openai.com/api-keys) |
| **Gemini** | Online | `AIza...` | [aistudio.google.com](https://aistudio.google.com/app/apikey) |
| **Groq** | Online | `gsk_...` | [console.groq.com](https://console.groq.com/keys) |
| **OpenRouter** | Online | `sk-or-...` | [openrouter.ai](https://openrouter.ai/keys) |
| **Ollama** | Offline | — | Jalankan `ollama serve` |
| **LM Studio** | Offline | — | Aktifkan Local Server di app |
| **Jan** | Offline | — | Aktifkan API Server di app |
| **Custom** | Offline | Opsional | URL endpoint bebas |

> **Keamanan:** API key disimpan di `sessionStorage` browser (hilang saat tab ditutup). Key tidak pernah dikirim ke server lain selain API provider yang bersangkutan. Tidak ada key yang tersimpan di repo ini.

---

## 🛠️ Teknologi

- [Monaco Editor](https://microsoft.github.io/monaco-editor/) — VS Code editor engine
- [DOMPurify](https://github.com/cure53/DOMPurify) — sanitasi output AI
- [JetBrains Mono](https://www.jetbrains.com/legalforms/font-license/) — font monospace
- Vanilla JS, HTML, CSS — tidak ada framework, tidak ada build tool

---

## 📁 Struktur Repo

```
.
├── nexus_fixed.html   # Aplikasi utama (single file)
├── README.md
├── LICENSE
└── .gitignore
```

---

## 🤝 Kontribusi

Pull request welcome! Untuk perubahan besar, buka issue dulu untuk diskusi.

---

## 📄 Lisensi

[MIT](LICENSE)
