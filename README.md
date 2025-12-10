
# 🔥 Proxy Scraper Ultra v2.5

<div align="center">
  
![Python](https://img.shields.io/badge/Python-3.7%2B-blue?style=for-the-badge&logo=python)
![Requests](https://img.shields.io/badge/Requests-2.28%2B-green?style=for-the-badge)
![Rich](https://img.shields.io/badge/Rich-13.0%2B-orange?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)
![Platform](https://img.shields.io/badge/Platform-Linux%20%7C%20Windows%20%7C%20macOS-lightgrey?style=for-the-badge)

<p align="center">
  <img src="https://img.shields.io/badge/Proxies-Scraped-2M%2B-brightgreen?style=flat-square">
  <img src="https://img.shields.io/badge/Sources-40%2B-9cf?style=flat-square">
  <img src="https://img.shields.io/badge/Protocols-HTTP%20%7C%20HTTPS%20%7C%20SOCKS4%20%7C%20SOCKS5-blueviolet?style=flat-square">
</p>

<h3>⚡ Tool Scrape Jutaan Proxy dari Berbagai Sumber Publik</h3>

[🚀 Fitur](#-fitur) • [📦 Instalasi](#-instalasi) • [🎮 Penggunaan](#-penggunaan) • [📁 Struktur](#-struktur-proyek) • [🤝 Berkontribusi](#-berkontribusi)

</div>

## 📸 Preview

<div align="center">
  
```ascii
⠀⠀⠀⠀⠀⠀⠀ ⣀⣀⣤⣤⣤⣤⡼⠀⢀⡀⣀⢱⡄⡀⠀⠀⠀⢲⣤⣤⣤⣤⣀⣀⡀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⣠⣴⣾⣿⣿⣿⣿⣿⡿⠛⠋⠁⣤⣿⣿⣿⣧⣷⠀⠀⠘⠉⠛⢻⣷⣿⣽⣿⣿⣷⣦⣄⡀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⢀⣴⣞⣽⣿⣿⣿⣿⣿⣿⣿⠁⠀⠀⠠⣿⣿⡟⢻⣿⣿⣇⠀⠀⠀⠀⠀⣿⣿⣿⣿⣿⣿⣿⣿⣟⢦⡀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⣠⣿⡾⣿⣿⣿⣿⣿⠿⣻⣿⣿⡀⠀⠀⠀⢻⣿⣷⡀⠻⣧⣿⠆⠀⠀⠀⠀⣿⣿⣿⡻⣿⣿⣿⣿⣿⠿⣽⣦⡀⠀⠀⠀⠀
⠀⠀⠀⠀⣼⠟⣩⣾⣿⣿⣿⢟⣵⣾⣿⣿⣿⣧⠀⠀⠀⠈⠿⣿⣿⣷⣈⠁⠀⠀⠀⠀⣰⣿⣿⣿⣿⣮⣟⢯⣿⣿⣷⣬⡻⣷⡄⠀⠀⠀
⠀⠀⢀⡜⣡⣾⣿⢿⣿⣿⣿⣿⣿⢟⣵⣿⣿⣿⣷⣄⠀⣰⣿⣿⣿⣿⣿⣷⣄⠀⢀⣼⣿⣿⣿⣷⡹⣿⣿⣿⣿⣿⣿⢿⣿⣮⡳⡄⠀⠀
⠀⢠⢟⣿⡿⠋⣠⣾⢿⣿⣿⠟⢃⣾⢟⣿⢿⣿⣿⣿⣾⡿⠟⠻⣿⣻⣿⣏⠻⣿⣾⣿⣿⣿⣿⡛⣿⡌⠻⣿⣿⡿⣿⣦⡙⢿⣿⡝⣆⠀
⠀⢯⣿⠏⣠⠞⠋⠀⣠⡿⠋⢀⣿⠁⢸⡏⣿⠿⣿⣿⠃⢠⣴⣾⣿⣿⣿⡟⠀⠘⢹⣿⠟⣿⣾⣷⠈⣿⡄⠘⢿⣦⠀⠈⠻⣆⠙⣿⣜⠆
⢀⣿⠃⡴⠃⢀⡠⠞⠋⠀⠀⠼⠋⠀⠸⡇⠻⠀⠈⠃⠀⣧⢋⣼⣿⣿⣿⣷⣆⠀⠈⠁⠀⠟⠁⡟⠀⠈⠻⠀⠀⠉⠳⢦⡀⠈⢣⠈⢿⡄
⣸⠇⢠⣷⠞⠁⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠙⠻⠿⠿⠋⠀⢻⣿⡄⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠈⠙⢾⣆⠈⣷
⡟⠀⡿⠁⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⣴⣶⣤⡀⢸⣿⠇⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢻⡄⢹
⡇⠀⠃⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢸⡇⠀⠈⣿⣼⡟⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠈⠃⢸
⢡⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠈⠻⠶⣶⡟⠋⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡼
⠈⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢀⡾⠋⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠁
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢸⡁⢠⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢀⣿⣿⣼⣀⣠⠂⠀
╔══════════════════════════════════════════════════════════════╗
║                     [ INFORMASI ]                            ║
╠══════════════════════════════════════════════════════════════╣
║ [x] Developers : ChixazoExecuted                             ║
║ [x] Objective : Scrape Proxy 2M+                             ║
║ [x] Version : 2.5                                            ║
║                                                              ║
║ [1] START                                                    ║
║ [2] CONTACT DEVELOPERS                                       ║
║ [3] EXIT                                                     ║
╚══════════════════════════════════════════════════════════════╝

⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
```

</div>

✨ Fitur

<table>
  <tr>
    <td width="50%">
      <h4>🚀 Performa Tinggi</h4>
      <ul>
        <li>Scraping dari 40+ sumber terpercaya</li>
        <li>Mendukung 4 protokol berbeda</li>
        <li>Deduplikasi otomatis</li>
        <li>Real-time progress tracking</li>
      </ul>
    </td>
    <td width="50%">
      <h4>🎨 User Experience</h4>
      <ul>
        <li>UI terminal yang menarik</li>
        <li>Color-coded output</li>
        <li>Menu interaktif</li>
        <li>Cross-platform compatibility</li>
      </ul>
    </td>
  </tr>
</table>

📦 Instalasi

Prasyarat

Pastikan Python 3.7+ sudah terinstall di sistem Anda:

```bash
python --version
```

Step 1: Clone Repository

```bash
git clone https://github.com/ChixazoExecuted/scrape_proxy.git
cd scrape_proxy
```

Step 2: Install Dependencies

```bash
pip install requests rich
```

Step 3: Verifikasi

```bash
python run.py
```

Tampilan Menu

Opsi yang Tersedia

No Opsi Deskripsi Output
1️⃣ START Memulai scraping proxies.txt
2️⃣ CONTACT Hubungi developer Telegram
3️⃣ EXIT Keluar program -

Contoh Output

```ascii
[ LIVE ] FOUND PROXY : 1524
[ LIVE ] FOUND PROXY : 2389
[ TIMEOUT ] Connection timeout for URL
[ ERROR ] Failed to fetch from URL

✓ Saved 25,430 proxies to proxies.txt
  1. 192.168.1.1:8080
  2. 10.0.0.1:3128
  3. 172.16.0.1:9050
  ... and 25,427 more
```

📁 Struktur Proyek

```
proxy-scraper-ultimate/
├── run.py          # Main script
├── README.md                 # Dokumentasi ini
├── requirements.txt          # Dependencies
├── proxies.txt              # Output file (generated)
├── LICENSE                  # MIT License
└── .gitignore              # Git ignore rules
```

🎯 Sumber Proxy

Script ini mengumpulkan proxy dari:

· ProxyScrape API (8 endpoints)
· GitHub Repositories (15+ sources)
· Public Proxy Lists (10+ websites)
· Open Proxy APIs (5+ services)

⚡ Quick Commands

Basic Usage

```bash
# Run the scraper
python run.py

# Select option 1 to start scraping
```

🛠️ Troubleshooting

Masalah Solusi
ModuleNotFoundError pip install requests rich
Permission denied Gunakan python3 atau sudo
No proxies found Cek koneksi internet
Slow scraping Tunggu beberapa menit

📊 Statistik

· Rata-rata proxies: 20,000 - 50,000 per run
· Waktu eksekusi: 2-5 menit
· File size: ~1-5 MB
· Success rate: ~85%

🤝 Berkontribusi

Kontribusi sangat diterima! Ikuti langkah:

1. Fork repository
2. Buat branch: git checkout -b feature/AmazingFeature
3. Commit changes: git commit -m 'Add AmazingFeature'
4. Push: git push origin feature/AmazingFeature
5. Buat Pull Request

🐛 Report Bug

1. Cek Issues
2. Buat issue baru dengan detail lengkap
3. Sertakan screenshot jika memungkinkan

📝 Lisensi

Distributed under MIT License. See LICENSE for more information.

👨‍💻 Developer

ChixazoExecuted - @chixazo

Connect

<p align="left">
  <a href="https://t.me/chixazo">
    <img src="https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" height="30">
  </a>
  <a href="https://github.com/ChixazoExecuted">
    <img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white" height="30">
  </a>
</p>

⭐ Support

Jika project ini membantu Anda, berikan ⭐ di GitHub!

---

<div align="center">

⚠️ Disclaimer: Tool ini hanya untuk tujuan edukasi. Gunakan dengan bertanggung jawab.

Made with ❤️ by ChixazoExecuted

</div>
```
