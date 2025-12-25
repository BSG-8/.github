<div align="center">

# ⚡ OCPP–CAN Güvenlik Laboratuvarı

<img src="https://raw.githubusercontent.com/PKief/vscode-material-icon-theme/main/icons/folder-secure.svg" width="150">

<br>

[![Electric Vehicle](https://img.shields.io/badge/Electric_Vehicle-00D26A?style=for-the-badge&logo=tesla&logoColor=white)](https://github.com/BSG-8/ocpp-can-lab)
[![Cyber Security](https://img.shields.io/badge/Cyber_Security-FF6B6B?style=for-the-badge&logo=hackaday&logoColor=white)](https://github.com/BSG-8/ocpp-can-lab)
[![OCPP 2.0](https://img.shields.io/badge/OCPP-2.0.1-0066CC?style=for-the-badge&logo=openapiinitiative&logoColor=white)](https://www.openchargealliance.org/)
[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![CAN Bus](https://img.shields.io/badge/CAN_Bus-Protocol-FF9900?style=for-the-badge&logo=databricks&logoColor=white)](https://github.com/BSG-8/ocpp-can-lab)

<br>

[![ISO 27001](https://img.shields.io/badge/ISO-27001-1D4ED8?style=flat-square&logo=iso&logoColor=white)](https://www.iso.org/)
[![ISO 15118](https://img.shields.io/badge/ISO-15118-059669?style=flat-square&logo=iso&logoColor=white)](https://www.iso.org/)
[![IEC 61851](https://img.shields.io/badge/IEC-61851-7C3AED?style=flat-square&logo=iso&logoColor=white)](https://www.iec.ch/)
[![License](https://img.shields.io/badge/License-MIT-F59E0B?style=flat-square&logo=opensourceinitiative&logoColor=white)](LICENSE)

<br>

### 🔋 Elektrikli Araç Şarj Altyapısı Saldırı/Savunma Simülasyon Ortamı

<br>

[🏠 Hakkında](#-hakkında) • 
[✨ Özellikler](#-özellikler) • 
[🚀 Kurulum](#-kurulum) • 
[🎯 Senaryolar](#-senaryolar) • 
[👥 Ekip](#-ekip) •
[📚 Dokümantasyon](#-dokümantasyon)

<br>

---

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" alt="rainbow" width="100%">

</div>

<br>

## 📖 Hakkında

<table>
<tr>
<td>

Bu proje, **Fırat Üniversitesi Bilgi Sistemleri ve Güvenliği** dersi kapsamında geliştirilmiş olup, elektrikli araç şarj istasyonlarının siber güvenlik açıklarını tespit etmek ve bu tehditlere karşı **yapay zekâ tabanlı savunma sistemleri** geliştirmek amacıyla tasarlanmıştır.

OCPP–CAN Güvenlik Laboratuvarı:

- 🔌 **OCPP Protokol Simülasyonu** — Şarj istasyonu ↔ Merkezi sistem iletişimi
- 🚗 **CAN-Bus Emülasyonu** — Araç içi ağ trafiği simülasyonu  
- 🎯 **Saldırı Senaryoları** — Gerçek dünya tehditlerinin modellenmesi
- 🛡️ **AI Savunma Sistemi** — Anomali tespiti ve otomatik müdahale

</td>
</tr>
</table>

<br>

## 🎯 Proje Hedefleri

<div align="center">

| Hedef | Metrik | Durum |
|:------|:------:|:-----:|
| 🔍 Anomali Tespit Sistemi | ≥ %95 Doğruluk | ✅ |
| ⚡ Sahte Veri & Enerji Hırsızlığı Tespiti | ≥ %90 Hassasiyet | ✅ |
| ⏱️ Gerçek Zamanlı Otomatik Müdahale | ≤ 30 Saniye | ✅ |
| 📋 Güvenlik Checklist Entegrasyonu | 50 Madde | ✅ |
| 📜 Uluslararası Standart Uyumu | %100 | ✅ |

</div>

<br>

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" alt="rainbow" width="100%">

<br>

## ✨ Özellikler

<br>

<table>
<tr>
<td width="50%">

### 🔄 OCPP Protokol Motoru
- OCPP 1.6 & 2.0.1 tam destek
- Charge Point (CP) emülasyonu
- Central System (CSMS) emülasyonu
- WebSocket tabanlı iletişim

</td>
<td width="50%">

### 🚌 CAN-Bus Simülasyonu
- Virtual CAN (vcan0) desteği
- Gerçek zamanlı frame analizi
- Arbitration ID manipülasyonu
- Data payload enjeksiyonu

</td>
</tr>
<tr>
<td width="50%">

### 🎯 Modüler Saldırı Sistemi
- Hook tabanlı mimari
- Pre/Post OCPP interceptor
- Pre/Post CAN interceptor
- Senaryo bazlı izolasyon

</td>
<td width="50%">

### 🛡️ AI Savunma Katmanı
- Makine öğrenimi anomali tespiti
- Gerçek zamanlı tehdit skorlaması
- Otomatik karantina sistemi
- SOC entegrasyonu

</td>
</tr>
</table>

<br>

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" alt="rainbow" width="100%">

<br>

## 🎯 Senaryolar

<div align="center">

### 7 Farklı Saldırı Senaryosu • Gerçek Dünya Tehditleri • AI Tabanlı Tespit

</div>

<br>

---

### 🟢 Senaryo 00 — Baseline (Referans)

<table>
<tr>
<td width="80">
<div align="center">
<img src="https://img.shields.io/badge/00-BASELINE-00D26A?style=for-the-badge" alt="baseline">
</div>
</td>
<td>

**Temiz Referans Akışı**

Saldırı içermeyen, normal OCPP ↔ CAN mesaj akışını simüle eder. Diğer senaryoların karşılaştırma noktası olarak kullanılır.

| Özellik | Değer |
|---------|-------|
| Saldırı Türü | Yok |
| Risk Seviyesi | — |
| Kullanım | Referans & Test |

</td>
</tr>
</table>

---

### 🔴 Senaryo 01 — Debug Backdoor

<table>
<tr>
<td width="80">
<div align="center">
<img src="https://img.shields.io/badge/01-BACKDOOR-DC2626?style=for-the-badge" alt="backdoor">
</div>
</td>
<td>

**CAN Bus Debug Modu ile Arka Kapı Oluşturma**

Şarj istasyonunun debug modunu kötüye kullanarak CAN-Bus üzerinden yetkisiz erişim sağlar. Saldırgan, debug komutları göndererek sistemin iç işleyişine müdahale edebilir.

| Özellik | Değer |
|---------|-------|
| Saldırı Türü | Backdoor / Unauthorized Access |
| Risk Seviyesi | 🔴 Kritik |
| Hedef | CAN Bus Debug Interface |
| Tespit | Debug frame anomali tespiti |

```
Saldırı Vektörü:
┌─────────────┐     Debug CMD      ┌─────────────┐
│   Attacker  │ ─────────────────► │  Charge     │
│             │ ◄───────────────── │  Point      │
└─────────────┘    Shell Access    └─────────────┘
```

**Hazırlayan:** Beşir Can Barutçu

</td>
</tr>
</table>

---

### 🟠 Senaryo 02 — Operasyonel Felç (DoS)

<table>
<tr>
<td width="80">
<div align="center">
<img src="https://img.shields.io/badge/02-DoS-F97316?style=for-the-badge" alt="dos">
</div>
</td>
<td>

**Denial of Service ile Sistem Felci**

Şarj istasyonunu yoğun istek bombardımanına tutarak hizmet veremez hale getirir. Tüm şarj operasyonları durur ve istasyon kullanılamaz.

| Özellik | Değer |
|---------|-------|
| Saldırı Türü | Denial of Service (DoS) |
| Risk Seviyesi | 🟠 Yüksek |
| Hedef | OCPP Message Handler |
| Etki | Şarj hizmeti kesintisi |

```
Saldırı Akışı:
                    ┌──────────────────┐
    ╔═══════════╗   │ Flood Attack     │   ╔═══════════╗
    ║  Attacker ║ ══╪══════════════════╪══►║   CSMS    ║
    ╚═══════════╝   │ 1000+ req/sec    │   ╚═══════════╝
                    └──────────────────┘        💥
                                            OVERLOAD
```

**Hazırlayan:** Yusuf Kaya

</td>
</tr>
</table>

---

### 👻 Senaryo 03 — Hayalet Şarj

<table>
<tr>
<td width="80">
<div align="center">
<img src="https://img.shields.io/badge/03-GHOST-8B5CF6?style=for-the-badge" alt="ghost">
</div>
</td>
<td>

**Hayalet Şarj ile Enerji Hırsızlığı**

Fiziksel olarak bağlı olmayan bir araç için sahte şarj oturumu başlatarak enerji çalınmasını simüle eder. Sayaç verileri manipüle edilerek ücretsiz şarj yapılır.

| Özellik | Değer |
|---------|-------|
| Saldırı Türü | Fraud / Energy Theft |
| Risk Seviyesi | 🟠 Yüksek |
| Hedef | MeterValues, Transaction |
| Mali Etki | Gelir kaybı |

```
Sahte Şarj Akışı:
┌─────────────┐                      ┌─────────────┐
│   Attacker  │  StartTransaction    │    CSMS     │
│  (No EV)    │ ────────────────────►│             │
│             │  MeterValues: 0 kWh  │   Accepts   │
│             │ ────────────────────►│     ✓       │
│             │  StopTransaction     │             │
│  FREE ⚡    │ ────────────────────►│  Billed: $0 │
└─────────────┘                      └─────────────┘
```

**Hazırlayan:** Hüseyin Enes Ertürk

</td>
</tr>
</table>

---

### 🌉 Senaryo 04 — Protocol Bridge

<table>
<tr>
<td width="80">
<div align="center">
<img src="https://img.shields.io/badge/04-BRIDGE-0EA5E9?style=for-the-badge" alt="bridge">
</div>
</td>
<td>

**Protokol Köprüsü Üzerinden Gizli Talep Manipülasyonu**

OCPP ve CAN protokolleri arasındaki çeviri katmanına sızarak mesajları manipüle eder. Man-in-the-Middle (MitM) saldırısı ile veri bütünlüğü bozulur.

| Özellik | Değer |
|---------|-------|
| Saldırı Türü | Man-in-the-Middle (MitM) |
| Risk Seviyesi | 🔴 Kritik |
| Hedef | OCPP ↔ CAN Mapping Layer |
| Etki | Veri manipülasyonu |

```
MitM Saldırısı:
┌────────┐      ┌──────────────┐      ┌────────┐
│  CSMS  │ ◄──► │   Attacker   │ ◄──► │   CP   │
└────────┘      │              │      └────────┘
                │  • Intercept │
   Original     │  • Modify    │      Modified
   Message      │  • Forward   │      Message
                └──────────────┘
```

**Hazırlayan:** Ahmet Küçükköylü

</td>
</tr>
</table>

---

### 🚌 Senaryo 05 — CAN Bus-Off

<table>
<tr>
<td width="80">
<div align="center">
<img src="https://img.shields.io/badge/05-BUS_OFF-EF4444?style=for-the-badge" alt="busoff">
</div>
</td>
<td>

**CAN Bus Kapatma Saldırısı**

CAN Bus hata sayaçlarını kasıtlı olarak artırarak bus-off durumuna zorlar. Bu durum, araç ile şarj istasyonu arasındaki tüm iletişimi keser.

| Özellik | Değer |
|---------|-------|
| Saldırı Türü | DoS / Bus-Off Attack |
| Risk Seviyesi | 🔴 Kritik |
| Hedef | CAN Error Counters |
| Etki | İletişim kesintisi |

```
Bus-Off Saldırısı:
┌─────────────────────────────────────────────────┐
│                  CAN Bus                        │
├─────────────────────────────────────────────────┤
│  Error Frame  Error Frame  Error Frame          │
│  ──────────►  ──────────►  ──────────►          │
│                                                 │
│  TEC: 96 ──► TEC: 128 ──► TEC: 256 ──► BUS-OFF │
│              ⚠️            🔴           💀      │
└─────────────────────────────────────────────────┘
```

**Hazırlayan:** Muhammed Emin Çimen

</td>
</tr>
</table>

---

### 🔐 Senaryo 06 — Firmware Manipulation

<table>
<tr>
<td width="80">
<div align="center">
<img src="https://img.shields.io/badge/06-FIRMWARE-7C3AED?style=for-the-badge" alt="firmware">
</div>
</td>
<td>

**İmzalanmamış Firmware Manipülasyonu**

Sahte veya imzalanmamış firmware güncellemesi enjekte ederek şarj istasyonunun kontrolünü ele geçirmeye çalışır. AI sistemi bunu tespit edip engeller.

| Özellik | Değer |
|---------|-------|
| Saldırı Türü | Code Injection / Firmware Attack |
| Risk Seviyesi | 🔴 Kritik |
| Hedef | UpdateFirmware Handler |
| Tespit | İmza & Hash doğrulama |

```
AI Tespit Sistemi:
┌─────────────────────────────────────────────────────────┐
│                  FIRMWARE VALIDATION                     │
├─────────────────────────────────────────────────────────┤
│                                                         │
│  📥 Incoming Firmware                                   │
│       │                                                 │
│       ▼                                                 │
│  ┌─────────────────────────────────────────────────┐   │
│  │ ✗ signature_valid: FALSE        │ Score: 40    │   │
│  │ ✗ hash_match: FALSE             │ Score: 35    │   │
│  │ ✗ version_check: DOWNGRADE      │ Score: 25    │   │
│  └─────────────────────────────────────────────────┘   │
│       │                                                 │
│       ▼                                                 │
│  ╔═════════════════════════════════════════════════╗   │
│  ║  🚨 ANOMALY SCORE: 100/100                      ║   │
│  ║  🛑 ACTION: BLOCKED & QUARANTINED               ║   │
│  ╚═════════════════════════════════════════════════╝   │
│                                                         │
└─────────────────────────────────────────────────────────┘
```

**Hazırlayan:** Sena Köse

</td>
</tr>
</table>

<br>

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" alt="rainbow" width="100%">

<br>

## 🚀 Kurulum

<details>
<summary><b>📋 Gereksinimler</b></summary>

<br>

| Gereksinim | Versiyon |
|------------|----------|
| Python | 3.10+ |
| İşletim Sistemi | Linux (Ubuntu 20.04+) |
| Git | 2.0+ |
| pip | 21.0+ |

</details>

<br>

### Hızlı Başlangıç

```bash
# 1️⃣ Repoyu klonla
git clone https://github.com/BSG-8/ocpp-can-lab.git
cd ocpp-can-lab

# 2️⃣ Sanal ortam oluştur
python3 -m venv venv
source venv/bin/activate

# 3️⃣ Bağımlılıkları yükle
pip install -r requirements.txt

# 4️⃣ CAN arayüzünü etkinleştir
sudo bash infra/setup_vcan.sh
```

### Çalıştırma

```bash
# Terminal 1 — CSMS Sunucusu
python -m infra.ocpp_server

# Terminal 2 — Senaryo
python -m scenarios.scenario_06_firmware_manipulation.simulate

# Terminal 3 — Log Viewer (Opsiyonel)
streamlit run log_viewer/app.py
```

<br>

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" alt="rainbow" width="100%">

<br>

## 👥 Ekip

<div align="center">

### 🎓 Fırat Üniversitesi • Bilgi Sistemleri ve Güvenliği • 2025 Güz

<br>

<a href="https://github.com/kosesena"><img src="https://avatars.githubusercontent.com/kosesena?s=100" width="100" height="100" style="border-radius:50%"></a>
<a href="https://github.com/huseyineneserturk"><img src="https://avatars.githubusercontent.com/huseyineneserturk?s=100" width="100" height="100" style="border-radius:50%"></a>
<a href="https://github.com/YusufKaya00"><img src="https://avatars.githubusercontent.com/YusufKaya00?s=100" width="100" height="100" style="border-radius:50%"></a>
<a href="https://github.com/muhammedemincmn"><img src="https://avatars.githubusercontent.com/muhammedemincmn?s=100" width="100" height="100" style="border-radius:50%"></a>
<a href="https://github.com/BesircanB"><img src="https://avatars.githubusercontent.com/BesircanB?s=100" width="100" height="100" style="border-radius:50%"></a>
<a href="https://github.com/syhnshn"><img src="https://avatars.githubusercontent.com/syhnshn?s=100" width="100" height="100" style="border-radius:50%"></a>

<a href="https://github.com/KEREMONCEL"><img src="https://avatars.githubusercontent.com/KEREMONCEL?s=100" width="100" height="100" style="border-radius:50%"></a>
<a href="https://github.com/adilenurygt"><img src="https://avatars.githubusercontent.com/adilenurygt?s=100" width="100" height="100" style="border-radius:50%"></a>
<a href="https://github.com/AhmetKucukkoylu"><img src="https://avatars.githubusercontent.com/AhmetKucukkoylu?s=100" width="100" height="100" style="border-radius:50%"></a>
<a href="https://github.com/mirullaherbas"><img src="https://avatars.githubusercontent.com/mirullaherbas?s=100" width="100" height="100" style="border-radius:50%"></a>
<a href="https://github.com/danyalocalir-tech"><img src="https://avatars.githubusercontent.com/danyalocalir-tech?s=100" width="100" height="100" style="border-radius:50%"></a>
<a href="https://github.com/MesutAltunkaynak"><img src="https://avatars.githubusercontent.com/MesutAltunkaynak?s=100" width="100" height="100" style="border-radius:50%"></a>

<br><br>

</div>

| | İsim | GitHub | Senaryo | Açıklama |
|:---:|:-----|:------:|:-------:|:---------|
| 🔐 | **Sena Köse** | [![GitHub](https://img.shields.io/badge/-kosesena-181717?style=flat-square&logo=github)](https://github.com/kosesena) | Firmware Manipulation | İmzasız firmware enjeksiyonu |
| 👻 | **Hüseyin Enes Ertürk** | [![GitHub](https://img.shields.io/badge/-huseyineneserturk-181717?style=flat-square&logo=github)](https://github.com/huseyineneserturk) | Hayalet Şarj | Enerji hırsızlığı simülasyonu |
| 💥 | **Yusuf Kaya** | [![GitHub](https://img.shields.io/badge/-YusufKaya00-181717?style=flat-square&logo=github)](https://github.com/YusufKaya00) | Operasyonel Felç | DoS ile sistem felci |
| 🚌 | **Muhammed Emin Çimen** | [![GitHub](https://img.shields.io/badge/-muhammedemincmn-181717?style=flat-square&logo=github)](https://github.com/muhammedemincmn) | CAN Bus-Off | Bus kapatma saldırısı |
| 🚪 | **Beşir Can Barutçu** | [![GitHub](https://img.shields.io/badge/-BesircanB-181717?style=flat-square&logo=github)](https://github.com/BesircanB) | Debug Backdoor | Arka kapı oluşturma |
| 🔄 | **Seyhan Şahin** | [![GitHub](https://img.shields.io/badge/-syhnshn-181717?style=flat-square&logo=github)](https://github.com/syhnshn) | CAN Reflection | Harici yansıtma saldırısı |
| 👤 | **Kerem Öncel** | [![GitHub](https://img.shields.io/badge/-KEREMONCEL-181717?style=flat-square&logo=github)](https://github.com/KEREMONCEL) | Hayali İstasyon | Sahte durum bildirimi |
| 📡 | **Adile Nur Yiğit** | [![GitHub](https://img.shields.io/badge/-adilenurygt-181717?style=flat-square&logo=github)](https://github.com/adilenurygt) | Frekans Geri Besleme | CAN frekans manipülasyonu |
| 🌉 | **Ahmet Küçükköylü** | [![GitHub](https://img.shields.io/badge/-AhmetKucukkoylu-181717?style=flat-square&logo=github)](https://github.com/AhmetKucukkoylu) | Protocol Bridge | Gizli talep manipülasyonu |
| 🔋 | **Mirullah Erbaş** | [![GitHub](https://img.shields.io/badge/-mirullaherbas-181717?style=flat-square&logo=github)](https://github.com/mirullaherbas) | V2G Deşarj | Deşarj anomali tespiti |
| 🎮 | **Azad Öcalır** | [![GitHub](https://img.shields.io/badge/-danyalocalir--tech-181717?style=flat-square&logo=github)](https://github.com/danyalocalir-tech) | Hijacked Controller | Ele geçirilmiş denetleyici |
| 📴 | **Mehmet Mesut Altunkaynak** | [![GitHub](https://img.shields.io/badge/-MesutAltunkaynak-181717?style=flat-square&logo=github)](https://github.com/MesutAltunkaynak) | CV Manipulation | Çevrimdışı mod zorlama |

<br>

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" alt="rainbow" width="100%">

<br>

## 🏗️ Proje Yapısı

```
📦 ocpp-can-lab
 ┣ 📂 infra                     # Altyapı bileşenleri
 ┃ ┣ 📜 ocpp_client.py          # Charge Point emülatörü
 ┃ ┣ 📜 ocpp_server.py          # CSMS emülatörü
 ┃ ┣ 📜 pipeline.py             # Hook sistemi
 ┃ ┣ 📜 mapping.py              # OCPP ↔ CAN çeviri
 ┃ ┗ 📜 scenario_base.py        # Senaryo temel sınıfı
 ┃
 ┣ 📂 scenarios                 # Saldırı senaryoları
 ┃ ┣ 📂 _template               # Şablon
 ┃ ┣ 📂 scenario_00_baseline
 ┃ ┣ 📂 scenario_01_debug_backdoor
 ┃ ┣ 📂 scenario_02_operasyonel_felc
 ┃ ┣ 📂 scenario_03_hayalet_sarj
 ┃ ┣ 📂 scenario_04_protocol_bridge
 ┃ ┣ 📂 scenario_05_can_bus_off
 ┃ ┗ 📂 scenario_06_firmware_manipulation
 ┃
 ┣ 📂 log_viewer                # Streamlit dashboard
 ┣ 📂 logs                      # Çalışma logları
 ┣ 📜 requirements.txt
 ┣ 📜 config.json
 ┗ 📜 README.md
```

<br>

## 📚 Dokümantasyon

<details>
<summary><b>🔧 Hook Sistemi</b></summary>

<br>

Her senaryo 4 hook fonksiyonu kullanır:

| Hook | Tetiklenme | Kullanım |
|------|------------|----------|
| `pre_ocpp()` | OCPP gönderiminden önce | Mesaj manipülasyonu |
| `post_ocpp()` | OCPP cevabı sonrası | Cevap analizi |
| `pre_can()` | CAN frame öncesi | Frame enjeksiyonu |
| `post_can()` | CAN frame sonrası | Loglama |

```python
class Scenario(ScenarioHooks):
    def pre_ocpp(self, action, payload):
        # Manipülasyon kodu
        return action, payload
```

</details>

<details>
<summary><b>➕ Yeni Senaryo Ekleme</b></summary>

<br>

```bash
# 1. Branch oluştur
git checkout dev
git checkout -b feature/scenario_XX_isim

# 2. Template kopyala
cp -r scenarios/_template scenarios/scenario_XX_isim

# 3. Düzenle ve test et
# 4. PR aç
git push origin feature/scenario_XX_isim
```

</details>

<br>

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" alt="rainbow" width="100%">

<br>

## 🛠️ Teknolojiler

<div align="center">

<img src="https://skillicons.dev/icons?i=python,linux,git,github,vscode&theme=dark" alt="Tech Stack" />

<br><br>

| Kategori | Teknoloji |
|----------|-----------|
| **Backend** | Python 3.10+, AsyncIO, WebSockets |
| **Protokoller** | OCPP 1.6/2.0, CAN 2.0A/B |
| **Simülasyon** | python-can, vcan, SocketCAN |
| **UI** | Streamlit |
| **Güvenlik** | TLS 1.3, RSA, AES-256 |
| **AI/ML** | Anomaly Detection Algorithms |

</div>

<br>

## 📜 Standartlar & Uyumluluk

<div align="center">

| Standart | Açıklama | Uyum |
|----------|----------|:----:|
| **ISO 27001** | Bilgi Güvenliği Yönetim Sistemi | ✅ |
| **ISO 15118** | Araç-Şebeke İletişimi (V2G) | ✅ |
| **OCPP 2.0.1** | Açık Şarj Noktası Protokolü | ✅ |
| **IEC 61851** | EV Şarj Sistemi Güvenliği | ✅ |
| **SAE J1772** | EV Bağlantı Standartları | ✅ |

</div>

<br>

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" alt="rainbow" width="100%">

<br>

## 📄 Lisans

<div align="center">

Bu proje [MIT Lisansı](LICENSE) ile lisanslanmıştır.

<br>

---

<br>

### ⚡ EV Altyapı Güvenliği İçin Geliştirilmiştir ⚡

<br>

**Fırat Üniversitesi** • Bilgi Sistemleri ve Güvenliği • 2025

<br>

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=100&section=footer" width="100%">

</div>
