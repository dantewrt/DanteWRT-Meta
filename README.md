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
- [Test Adblock](#test-adblock)
- [Credits](#credits)

## Setting OpenClash

### Plugin Settings

Settingan pada Tab Plugin Settings berikut :

#### Operation Mode

- Operation Mode Pastikan pada mode **Fake-IP Mode**, jika belum **SWITCH PAGE TO FAKE-IP MODE** terlebih dahulu
- Select Mode **Fake-IP(tun-mode)**
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

[![Gambar Setting Meta](https://raw.githubusercontent.com/dantewrt/DanteWRT-Meta/main/images/metasetting-1.PNG "Setting Meta")](https://raw.githubusercontent.com/dantewrt/DanteWRT-Meta/main/images/metasetting-1.PNG)

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
    ports: [443, 8443]
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
  - dlg.io.mi.com
```
### GEOIP

Wajib menggunakan GeoIP.dat, silahkan download terlebih dahulu,
copy lalu pastekan diterminal

```sh
curl -o /etc/openclash/GeoIP.dat https://raw.githubusercontent.com/rfxcll/v2ray-rules-dat/release/GeoIP.dat
chmod 744 /etc/openclash/GeoIP.dat
```

### GEOSITE

Karena semua rule kami pindahkan ke GeoSite.dat maka perlu setting `Custom GeoSite URL` menggunakan hasil compile custom list yang telah kami sediakan.
Silahkan download `Custom GeoSite URL` terlebih dahulu,
copy lalu pastekan diterminal

```sh
curl -o /etc/openclash/GeoSite.dat https://raw.githubusercontent.com/rfxcll/v2ray-rules-dat/release/GeoSite.dat
chmod 744 /etc/openclash/GeoSite.dat
```

*Daftar GeoSite yang digunakan*
  - **DNS DoH**
    - `geosite:rule-doh`
  - **Adblock**
    - `geosite:rule-malicious`
    - `geosite:oisd-full`
    - `geosite:rule-ads`
  - **Porn 18+**
    - `geosite:oisd-nsfw`
    - `geosite:category-porn`
  - **Marketplace-ID**
    - `geosite:ecommerce-id`
       - Lazada
       - Tokopedia
       - Shopee
       - [Cek List disini](https://github.com/rfxcll/v2ray-rules-dat/blob/rule/rule_streaming.txt)
  - **Streaming**
    - `geosite:rule-streaming`
       - [Cek List disini](https://github.com/rfxcll/v2ray-rules-dat/blob/rule/rule_streaming.txt)
  - **Sosmed**
    - `geosite:rule-sosmed`
       - [Cek List disini](https://github.com/rfxcll/v2ray-rules-dat/blob/rule/rule_sosmed.txt)
  - **Gaming**
    - `geosite:rule-gaming`
       - [Cek List disini](https://github.com/rfxcll/v2ray-rules-dat/blob/rule/rule_gaming.txt)

### Kernel Meta

Karena Menggunakan Meta Core, Pastikan Download/Update Core Meta ke versi terbaru terlebih dahulu

- Download kernel **--> [Meta Alpha](https://github.com/MetaCubeX/Clash.Meta/releases/tag/Prerelease-Alpha)**
- Pilih file bernama **clash.meta-linux-arm64-alpha-xxx.gz**
- Upload file tersebut pada tab **Config Manage**
- **Upload File Type : [Meta] Core File**

[![Gambar Meta Core](https://raw.githubusercontent.com/dantewrt/DanteWRT-Meta/main/images/metacore.PNG "Meta Core")](https://raw.githubusercontent.com/dantewrt/DanteWRT-Meta/main/images/metacore.PNG)

## Test Adblock

### `Adblock 92%`

[![Gambar Test Adblock](https://raw.githubusercontent.com/dantewrt/DanteWRT-Meta/main/images/adblock1.PNG "Meta Core")](https://raw.githubusercontent.com/dantewrt/DanteWRT-Meta/main/images/adblock1.PNG)
[![Gambar Test Adblock](https://raw.githubusercontent.com/dantewrt/DanteWRT-Meta/main/images/adblock2.PNG "Meta Core")](https://raw.githubusercontent.com/dantewrt/DanteWRT-Meta/main/images/adblock2.PNG)

### `Bypass Website Adblock Warning`

[![Gambar Test Adblock](https://raw.githubusercontent.com/dantewrt/DanteWRT-Meta/main/images/adblock3.PNG "Meta Core")](https://raw.githubusercontent.com/dantewrt/DanteWRT-Meta/main/images/adblock3.PNG)

## Credits

- [rfxcll/open_meta](https://github.com/rfxcll/open_meta)
- [malikshi/open_meta](https://github.com/malikshi/open_meta)
