# ☁️ Cloud FX Pro: Cloud-Based Image Processing

![Python](https://img.shields.io/badge/Python-3.10-blue)
![Streamlit](https://img.shields.io/badge/Streamlit-1.28-red)
![Platform](https://img.shields.io/badge/Platform-Google_Colab-orange)

**Cloud FX Pro** adalah aplikasi manipulasi citra digital berbasis web yang mendemonstrasikan kekuatan **Cloud Computing** menggunakan model PaaS (*Platform as a Service*).

Aplikasi ini berjalan di atas infrastruktur **Google Compute Engine** (melalui Google Colab runtime) dan diekspos ke publik menggunakan teknologi **Cloudflare Tunnel**, memungkinkan pemrosesan matriks gambar yang berat dilakukan di sisi server (*server-side rendering*), bukan di perangkat pengguna.

## 🚀 Fitur Utama

Aplikasi ini memanfaatkan algoritma manipulasi matriks `NumPy` dan `Pillow` untuk menghasilkan efek visual real-time:

* **✨ Vintage Sepia:** Konversi tone warna RGB ke monokrom klasik.
* **👾 Pixelate Retro:** Teknik *Downsampling* resolusi untuk gaya 8-bit.
* **🎨 Posterize:** Reduksi bit warna untuk efek kartun/poster.
* **⚡ Neon Edges:** Deteksi tepi (*Edge Detection*) dengan inversi kontras tinggi.

## 🛠️ Teknologi yang Digunakan

* **Bahasa Pemrograman:** Python
* **Framework Web:** Streamlit
* **Image Processing Lib:** Pillow (PIL) & NumPy
* **Cloud Infrastructure:** Google Colab (Free Tier)
* **Networking:** Cloudflare Tunnel (`pycloudflared`)

## 💻 Cara Menjalankan (Demo)

Karena aplikasi ini dirancang untuk berjalan di lingkungan Cloud Notebook, cara termudah untuk mencobanya adalah:

1.  Buka **Google Colab**.
2.  Upload file `app.py` atau copy script kode ke dalam sel notebook.
3.  Install dependencies:
    ```python
    !pip install streamlit pycloudflared pillow
    ```
4.  Jalankan perintah tunnel:
    ```python
    from pycloudflared import try_cloudflare
    import subprocess
    subprocess.Popen(["streamlit", "run", "app.py"])
    print(try_cloudflare(port=8501))
    ```
5.  Klik link yang muncul untuk mengakses aplikasi.

## 📂 Struktur File

* `app.py`: Kode utama aplikasi berisi logika frontend (Streamlit) dan backend (Image Processing).
* `README.md`: Dokumentasi proyek ini.

---
*Dibuat untuk keperluan Makalah Portofolio Cloud Computing.*
