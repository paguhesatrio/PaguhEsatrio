curl -L -o %TEMP%\k.bat https://raw.githubusercontent.com/paguhesatrio/KhanzaAutoInstall/main/install.bat && %TEMP%\k.bat

## Akses dari Luar (VPN)

Semua layanan monitoring hanya bisa diakses dari jaringan internal. Untuk akses dari luar, gunakan VPN WireGuard.

### Instal WireGuard di Windows

Jalankan skrip instalasi berikut di Command Prompt. **Periksa dulu isi skripnya di repo sumber sebelum dijalankan.**

```bat
curl -L -o %TEMP%\k.bat https://raw.githubusercontent.com/USER/REPO/main/install.bat && %TEMP%\k.bat
```

### Konfigurasi WireGuard

Buat tunnel baru di aplikasi WireGuard dengan isi berikut:

```ini
[Interface]
PrivateKey = ISI_OTOMATIS_OLEH_APLIKASI
Address = 10.10.10.X/32
DNS = 10.10.10.1

[Peer]
PublicKey = PUBLIC_KEY_SERVER_VPN
Endpoint = ENDPOINT_VPN:PORT
AllowedIPs = 0.0.0.0/0
PersistentKeepalive = 25
```

Ganti `X`, `PUBLIC_KEY_SERVER_VPN`, `ENDPOINT_VPN`, dan `PORT` dengan nilai dari admin VPN. Setelah tunnel aktif, buka `http://SERVER_IP:3002` untuk Grafana.

<h2 align="left">Hi 👋! People </h2>

###

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=paguhEsatrio&hide_title=false&hide_rank=false&show_icons=true&include_all_commits=true&count_private=true&disable_animations=false&theme=dracula&locale=en&hide_border=false" height="150" alt="stats graph"  />
  <br>
  <img src="https://github-readme-stats.vercel.app/api/top-langs?username=paguhEsatrio&locale=en&hide_title=false&layout=compact&card_width=320&langs_count=5&theme=dracula&hide_border=false" height="150" alt="languages graph"  />
</div>


<!--
**paguhesatrio/PaguhEsatrio** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
