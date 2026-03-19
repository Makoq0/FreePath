# 🛡️ FreePath

**Türkçe** | [English](#english)

---

## Nedir?

FreePath, Türkiye'deki internet engellerini ve ISP tabanlı DPI (Deep Packet Inspection) sansürünü aşmak için geliştirilmiş açık kaynaklı bir Python aracıdır. VPN kullanmaz, trafiği dışarıya göndermez. Tüm işlemler tamamen yerel olarak senin bilgisayarında gerçekleşir.

## Nasıl Çalışır?

- **DNS Koruması** → ISP DNS zehirlenmesini engeller, Cloudflare 1.1.1.1 kullanır
- **HTTP Fragmentasyon** → Port 80 trafiğinde Host header'ı parçalayarak DPI sistemini atlatır
- **RST Engelleme** → ISP'nin gönderdiği sahte bağlantı kesme paketlerini düşürür
- **UDP Desteği** → Roblox, oyunlar gibi UDP tabanlı uygulamalar için trafik koruması

## Özellikler

- ✅ VPN gerektirmez
- ✅ Verilerini dışarıya göndermez
- ✅ Discord, Roblox, web siteleri çalışır
- ✅ Düşük gecikme, performans kaybı yok
- ✅ Açık kaynak, her satırı okuyabilirsin
- ✅ Program kapanınca DNS otomatik eski haline döner

## Kurulum

### Gereksinimler

- Windows 10/11
- Python 3.8+
- Yönetici (Administrator) yetkisi

### Adımlar

**1. ZİP DOSYASINI İNDİR:**
```bash

```

**2. Kütüphaneyi kur:**
```bash
pip install pydivert
```

**3. WinDivert dosyalarını indir:**

[WinDivert Releases](https://github.com/basil00/WinDivert/releases) sayfasından en son sürümü indir. ZIP içindeki `x64` klasöründen şu iki dosyayı proje klasörüne kopyala:
- `WinDivert.dll`
- `WinDivert64.sys`

**4. Yönetici olarak çalıştır:**
```bash
# CMD'yi yönetici olarak aç
python main.py
```

## EXE Olarak Derleme

```bash
pip install pyinstaller
pyinstaller --onefile --uac-admin --name FreePath --icon=icon.ico --add-data "WinDivert.dll;." --add-data "WinDivert64.sys;." main.py
```

`dist` klasöründe `FreePath.exe` oluşacaktır. (NOT: İNDİRDİĞİNİZ ZİP DOSYASINDA EXE KURULU YAPMANIZA GEREK YOKTUR EXE YOKSA YAPABİLİRSİNİZ)

## Güvenlik

FreePath tamamen yerel çalışır. Dışarıya gönderilen tek şey DNS sorgularıdır (Cloudflare 1.1.1.1). Şifreler, mesajlar veya dosyalar hiçbir şekilde gönderilmez.

## Lisans

Bu proje MIT lisansı ile lisanslanmıştır.
WinDivert, LGPL lisansı altındadır: [WinDivert License](https://reqrypt.org/windivert.html)

---

## English

## What is it?

FreePath is an open-source Python tool designed to bypass internet censorship and ISP-based DPI (Deep Packet Inspection) filtering. It does not use a VPN and does not send your traffic to any external server. Everything runs locally on your machine.

## How it Works

- **DNS Protection** → Prevents ISP DNS poisoning using Cloudflare 1.1.1.1
- **HTTP Fragmentation** → Splits HTTP Host headers to bypass DPI systems on port 80
- **RST Blocking** → Drops fake connection reset packets sent by ISPs
- **UDP Support** → Traffic protection for UDP-based apps like Roblox and games

## Features

- ✅ No VPN required
- ✅ No data sent externally
- ✅ Works with Discord, Roblox, websites
- ✅ Low latency, no performance loss
- ✅ Open source, every line is readable
- ✅ DNS automatically resets when program closes

## Installation

### Requirements

- Windows 10/11
- Python 3.8+
- Administrator privileges

### Steps

**1. Install Zip Folder:**
```bash

```

**2. Install dependencies:**
```bash
pip install pydivert
```

**3. Download WinDivert files:**

Download the latest release from [WinDivert Releases](https://github.com/basil00/WinDivert/releases). From the `x64` folder inside the ZIP, copy these two files to the project folder:
- `WinDivert.dll`
- `WinDivert64.sys`

**4. Run as Administrator:**
```bash
# Open CMD as Administrator
python main.py
```

## Building EXE

```bash
pip install pyinstaller
pyinstaller --onefile --uac-admin --name FreePath --icon=icon.ico --add-data "WinDivert.dll;." --add-data "WinDivert64.sys;." main.py
```

The `FreePath.exe` will be created in the `dist` folder. (NOTE: THE ZIP FILE YOU DOWNLOADED DOES NOT CONTAIN AN EXE FILE; YOU DO NOT NEED TO INSTALL IT. IF THERE IS NO EXE FILE, YOU CAN INSTALL IT.)

## Security

FreePath runs entirely locally. The only external communication is DNS queries to Cloudflare 1.1.1.1. No passwords, messages, or files are ever transmitted.

## License

This project is licensed under the MIT License.
WinDivert is licensed under LGPL: [WinDivert License](https://reqrypt.org/windivert.html)

---

⭐ Beğendiysen yıldız atmayı unutma!


MADE BY CLAUDE
