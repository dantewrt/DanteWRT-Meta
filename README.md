**Table of Contents**

- [Setting OpenClash](#setting-openclash)
  - [Plugin Settings](#plugin-settings)
    - [Operation Mode](#operation-mode)
    - [Traffic Control](#traffic-control)
    - [DNS Settings](#dns-settings)
  - [Overwrite Settings](#overwrite-settings)
    - [DNS Settings](#dns-settings)
    - [Meta Settings](#meta-settings)
- [GEOIP](#geoip)
- [GEOSITE](#geosite)
- [Kernel Meta](#kernel-meta)
- [Credits](#credits)

## Setting OpenClash

### Plugin Settings

Settingan pada Tab Plugin Settings berikut :

#### Operation Mode

- Operation Mode Pastikan pada mode **Redir-Host Mode**, jika belum **SWITCH PAGE TO REDIR-HOST MODE** terlebih dahulu
- Select Mode **Redir-host(tun-mode)**
- Centang Enable Meta Core
- Ceklist/centang opsi sesuai gambar berikut:

[![Gambar Operation Mode](https://raw.githubusercontent.com/dantewrt/DanteWRT-Meta/main/images/operationmode.PNG "Operation Mode")](https://raw.githubusercontent.com/dantewrt/DanteWRT-Meta/main/images/operationmode.PNG)

##### Traffic Control

- Ceklist/centang opsi sesuai gambar berikut:

[![Gambar Operation Mode](https://raw.githubusercontent.com/dantewrt/DanteWRT-Meta/main/images/operationmode-2.PNG "Operation Mode")](https://raw.githubusercontent.com/dantewrt/DanteWRT-Meta/main/images/operationmode-2.PNG)

##### DNS Settings
- Setting sesuai gambar berikut :

[![Gambar Setting DNS](https://raw.githubusercontent.com/dantewrt/DanteWRT-Meta/main/images/dnssetting-1.PNG "Setting DNS")](https://raw.githubusercontent.com/dantewrt/DanteWRT-Meta/main/images/dnssetting-1.PNG)

### Overwrite Settings

Settingan pada Tab **Overwrite Settings** berikut :

#### DNS Settings

- Ceklist/centang opsi dan ikuti settingan sesuai gambar berikut:

[![Gambar Setting DNS](https://raw.githubusercontent.com/dantewrt/DanteWRT-Meta/main/images/dnssetting-2.PNG "Setting DNS")](https://raw.githubusercontent.com/dantewrt/DanteWRT-Meta/main/images/dnssetting-2.PNG)

#### Meta Settings

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
### GEOIP

Wajib menggunakan GeoIP.dat silahkan setting sesuai gambar

```sh
https://raw.githubusercontent.com/rfxcll/v2ray-rules-dat/release/GeoIP.dat
```

[![Gambar Setting GeoIP](https://raw.githubusercontent.com/rfxcll/open_meta/main/images/metasetting-3.jpg "Setting GeoIP")](https://raw.githubusercontent.com/rfxcll/open_meta/main/images/metasetting-3.jpg)

Jika belum ada GeoIP pada folder `/etc/openclash/` maka silahkan download terlebih dahulu.

```sh
curl -o /etc/openclash/GeoIP.dat https://raw.githubusercontent.com/rfxcll/v2ray-rules-dat/release/GeoIP.dat
chmod 744 /etc/openclash/GeoIP.dat
```

### GEOSITE

Karena semua rule kami pindahkan ke GeoSite.dat maka perlu setting `Custom GeoSite URL` menggunakan hasil compile custom list yang telah kami sediakan.

```sh
https://raw.githubusercontent.com/rfxcll/v2ray-rules-dat/release/GeoSite.dat
```

Perhatikan gambar berikut.

[![Gambar Setting GeoSite](https://raw.githubusercontent.com/rfxcll/open_meta/main/images/metasetting-4.jpg "Setting GeoSite")](https://raw.githubusercontent.com/rfxcll/open_meta/main/images/metasetting-4.jpg)

WAJIB menggunakan GeoSite custom kami. Silahkan download terlebih dahulu.

```sh
curl -o /etc/openclash/GeoSite.dat https://raw.githubusercontent.com/rfxcll/v2ray-rules-dat/release/GeoSite.dat
chmod 744 /etc/openclash/GeoSite.dat
```

### Kernel Meta

Karena Menggunakan Meta Core, Pastikan Download/Update Core Meta ke versi terbaru terlebih dahulu

- Download kernel **--> [Meta Alpha](https://github.com/MetaCubeX/Clash.Meta/releases/tag/Prerelease-Alpha)**
- Pilih file bernama **clash.meta-linux-arm64-alpha-xxx.gz**
- Upload file tersebut pada tab **Config Manage**
- **Upload File Type : [Meta] Core File**

[![Gambar Meta Core](https://raw.githubusercontent.com/dantewrt/DanteWRT-Meta/main/images/metacore.PNG "Meta Core")](https://raw.githubusercontent.com/dantewrt/DanteWRT-Meta/main/images/metacore.PNG)

## Credits

- [rfxcll/open_meta](https://github.com/rfxcll/open_meta)
- [malikshi/open_meta](https://github.com/malikshi/open_meta)
