# Tutorial Setting OpenClash

Simak baik-baik apa saja yang disetting, pastikan sama dengan settingan berikut

# Import Config

- Import Config **DanteWRT-Meta.yaml** terlebih dahulu, Lakukan Pada Tab **Config Manage**

[![Gambar Import Config](https://raw.githubusercontent.com/dantewrt/DanteWRT-Meta/main/images/import-1.PNG "Import Config")](https://raw.githubusercontent.com/dantewrt/DanteWRT-Meta/main/images/import-1.PNG)

- Setelah itu upload **Rule Provider** & **Proxy Provider** seperti biasa

# Plugin Settings

Settingan pada Tab Plugin Settings berikut :

## Operation Mode

- Operation Mode Pastikan pada mode **Redir-Host Mode**, jika belum **SWITCH PAGE TO REDIR-HOST MODE** terlebih dahulu
- Select Mode **Redir-host(tun-mode)**
- Centang Enable Meta Core
- Ceklist/centang opsi sesuai gambar berikut:

[![Gambar Operation Mode](https://raw.githubusercontent.com/dantewrt/DanteWRT-Meta/main/images/operationmode.PNG "Operation Mode")](https://raw.githubusercontent.com/dantewrt/DanteWRT-Meta/main/images/operationmode.PNG)

## Traffic Control

- Ceklist/centang opsi sesuai gambar berikut:

[![Gambar Operation Mode](https://raw.githubusercontent.com/dantewrt/DanteWRT-Meta/main/images/operationmode-2.jpg "Operation Mode")](https://raw.githubusercontent.com/dantewrt/DanteWRT-Meta/main/images/operationmode-2.jpg)

## DNS Settings
- Setting sesuai gambar berikut :

[![Gambar Setting DNS](https://raw.githubusercontent.com/dantewrt/DanteWRT-Meta/main/images/dnssetting-1.PNG "Setting DNS")](https://raw.githubusercontent.com/dantewrt/DanteWRT-Meta/main/images/dnssetting-1.PNG)

# Overwrite Settings

Settingan pada Tab **Overwrite Settings** berikut :

## DNS Settings

- Ceklist/centang opsi dan ikuti settingan sesuai gambar berikut:

[![Gambar Setting DNS](https://raw.githubusercontent.com/dantewrt/DanteWRT-Meta/main/images/dnssetting-2.PNG "Setting DNS")](https://raw.githubusercontent.com/dantewrt/DanteWRT-Meta/main/images/dnssetting-2.PNG)

```
fallback-filter:
  geoip: true
  geoip-code: ID
  ipcidr:
    - 240.0.0.0/4
  domain:
    - "+.google.com"
    - "+.facebook.com"
    - "+.youtube.com"
```

## Meta Settings

- Ceklist/centang opsi dan ikuti settingan sesuai gambar berikut:

[![Gambar Setting Meta](https://raw.githubusercontent.com/dantewrt/DanteWRT-Meta/main/images/metasetting-1.PNG "Setting Meta")](https://raw.githubusercontent.com/dantewrt/DanteWRT-Meta/main/images/metasetting-1.jpg)

[![Gambar Setting Meta](https://raw.githubusercontent.com/dantewrt/DanteWRT-Meta/main/images/metasetting-2.PNG "Setting Meta")](https://raw.githubusercontent.com/dantewrt/DanteWRT-Meta/main/images/metasetting-2.PNG)

```
force-domain:
  - '+.netflix.com'
  - '+.nflxvideo.net'
  - '+.amazonaws.com'
  - '+.media.dssot.com'
```

```
sniff:
  TLS:
    ports: [443, 853, 8443]
  HTTP:
    ports: [80, 8080-8880]
    override-destination: true
 ```
 
[![Gambar Setting Meta](https://raw.githubusercontent.com/dantewrt/DanteWRT-Meta/main/images/metasetting-3.PNG "Setting Meta")](https://raw.githubusercontent.com/dantewrt/DanteWRT-Meta/main/images/metasetting-3.PNG)

```
skip-sni:
  - '+.courier.push.apple.com'
  - 'Mijia Cloud'
  - '+.jd.com'
```

## Kernel Meta

Karena Menggunakan Meta Core, Pastikan Download/Update Core Meta ke versi terbaru terlebih dahulu

- Download kernel [Meta Alpha](https://github.com/MetaCubeX/Clash.Meta/releases/tag/Prerelease-Alpha)
- Pilih file bernama **clash.meta-linux-arm64-alpha-xxx.gz**
- Upload file tersebut pada tab **Config Manage**
- **Upload File Type : [Meta] Core File**

[![Gambar Meta Core](https://raw.githubusercontent.com/dantewrt/DanteWRT-Meta/main/images/metacore.PNG "Meta Core")](https://raw.githubusercontent.com/dantewrt/DanteWRT-Meta/main/images/metacore.PNG)
