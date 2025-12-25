# 🔌 OCPP–CAN Güvenlik Laboratuvarı

<div align="center">

![EV Security](https://img.shields.io/badge/EV-Security-green?style=for-the-badge)
![OCPP](https://img.shields.io/badge/OCPP-2.0-blue?style=for-the-badge)
![Python](https://img.shields.io/badge/Python-3.10+-yellow?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-red?style=for-the-badge)

**Elektrikli Araç Şarj Altyapısı Saldırı/Savunma Simülasyon Ortamı**

[Hakkında](#-hakkında) •
[Özellikler](#-özellikler) •
[Kurulum](#-kurulum) •
[Senaryolar](#-senaryolar) •
[Ekip](#-ekip)

</div>

---

## 📖 Hakkında

Bu proje, **Fırat Üniversitesi Bilgi Sistemleri ve Güvenliği** dersi kapsamında geliştirilmiştir.

OCPP–CAN Güvenlik Laboratuvarı, Elektrikli Araç (EV) şarj altyapısını güvenlik açısından modellemek ve analiz etmek için oluşturulmuş **modüler bir simülasyon ortamıdır**. Proje, OCPP mesaj akışı ile EV içindeki CAN-Bus davranışını birleştirerek saldırı senaryolarının modellenmesini mümkün kılar.

### 🎯 Proje Amacı

Şarj istasyonları ile merkezi yönetim sistemleri arasındaki veri iletişiminde:

- 🔓 Zayıf şifreleme, yetkisiz erişim, Man-in-the-Middle (MitM) saldırıları
- 🔧 Firmware ve yazılım güncelleme zafiyetleri
- ⚡ Enerji hırsızlığı ve sahte veri enjeksiyonu
- 🚗 CAN-Bus manipülasyonu ve araç sistemlerine müdahale

gibi riskleri analiz etmek ve bu tehditlere karşı **anomali tespiti**, **gerçek zamanlı izleme** ve **otomatik müdahale mekanizmaları** geliştirmektir.

---

## 🎯 Hedefler

| Hedef | Açıklama | Metrik |
|-------|----------|--------|
| 🔍 **Anomali Tespiti** | Şarj istasyonlarındaki olağan dışı davranışları saptamak | ≥%95 doğruluk |
| 📋 **Güvenlik Checklist** | 50 maddelik kontrol listesiyle risk puanı üretmek | Tam kapsam |
| ⚡ **Sahte Veri Tespiti** | Enerji hırsızlığı ve manipülasyonu tespit etmek | ≥%90 hassasiyet |
| ⏱️ **Gerçek Zamanlı Müdahale** | Şüpheli işlemlere otomatik müdahale | ≤30 saniye |
| 📜 **Standart Uyumu** | ISO 27001, ISO 15118, OCPP 2.0 uyumluluğu | %100 uyum |

---

## ⚡ Özellikler

```
┌─────────────────────────────────────────────────────────────────┐
│                    OCPP-CAN GÜVENLİK LABI                       │
├─────────────────────────────────────────────────────────────────┤
│  🔄 OCPP İstemci & Sunucu Emülasyonu                            │
│     └─ Tam şarj noktası protokol simülasyonu                    │
│                                                                 │
│  🔀 OCPP → CAN Çeviri Katmanı                                   │
│     └─ OCPP mesajlarının CAN-Bus verisine dönüştürülmesi        │
│                                                                 │
│  🚌 CAN-Bus Simülasyonu                                         │
│     └─ vcan0 tabanlı sanal araç veri yolu                       │
│                                                                 │
│  🎯 Modüler Saldırı Senaryoları                                 │
│     └─ Hook tabanlı anomali enjeksiyon sistemi                  │
│                                                                 │
│  🛡️ Savunma Mekanizmaları                                       │
│     └─ AI tabanlı anomali tespiti ve otomatik müdahale          │
│                                                                 │
│  📊 Log Görüntüleyici                                           │
│     └─ Streamlit tabanlı görsel analiz arayüzü                  │
└─────────────────────────────────────────────────────────────────┘
```

---

## 🏗️ Proje Yapısı

```
ocpp-can-lab/
│
├── 📁 infra/                      # Temel altyapı bileşenleri
│   ├── ocpp_client.py             # Şarj Noktası (CP) emülatörü
│   ├── ocpp_server.py             # CSMS emülatörü
│   ├── mapping.py                 # OCPP → CAN dönüşüm mantığı
│   ├── pipeline.py                # Hook sistemi + işlem hattı
│   ├── scenario_base.py           # Senaryo temel sınıfı
│   └── setup_vcan.sh              # VCAN kurulumu
│
├── 📁 scenarios/                  # Saldırı senaryoları
│   ├── _template/                 # Yeni senaryo şablonu
│   ├── scenario_00_baseline/      # Temiz referans (saldırı yok)
│   ├── scenario_01_debug_backdoor/
│   ├── scenario_02_operasyonel_felc/
│   ├── scenario_03_hayalet_sarj/
│   ├── scenario_04_protocol_bridge/
│   ├── scenario_05_can_bus_off/
│   └── scenario_06_firmware_manipulation/
│
├── 📁 log_viewer/                 # Streamlit log görüntüleyici
├── 📁 logs/                       # Çalışma çıktıları
├── 📁 .devcontainer/              # Codespaces geliştirme ortamı
│
├── requirements.txt               # Python bağımlılıkları
├── config.json                    # Proje yapılandırması
└── README.md
```

---

## 🚀 Kurulum

### Gereksinimler

- Python 3.10+
- Linux (CAN simülasyonu için)
- Git

### 1️⃣ Repoyu Klonlayın

```bash
git clone https://github.com/BSG-8/ocpp-can-lab.git
cd ocpp-can-lab
```

### 2️⃣ Sanal Ortamı Kurun

```bash
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

### 3️⃣ CAN Arayüzünü Etkinleştirin

```bash
sudo bash infra/setup_vcan.sh
```

---

## ▶️ Çalıştırma

### Temel Kullanım

```bash
# Terminal 1 — CSMS Sunucusu
python -m infra.ocpp_server

# Terminal 2 — Senaryo Çalıştırma
python -m scenarios.scenario_XX_isim.simulate
```

### Log Görüntüleyici

```bash
streamlit run log_viewer/app.py
```

Tarayıcınızda `http://localhost:8501` adresinde açılacaktır.

---

## 🎯 Senaryolar

### Senaryo Listesi

| # | Senaryo | Açıklama | Saldırı Türü |
|---|---------|----------|--------------|
| 00 | **Baseline** | Temiz referans akışı | Yok |
| 01 | **Debug Backdoor** | CAN Bus debug ile arka kapı oluşturma | Backdoor |
| 02 | **Operasyonel Felç** | DoS saldırısı ile sistem felci | DoS |
| 03 | **Hayalet Şarj** | Sahte şarj ile enerji hırsızlığı | Fraud |
| 04 | **Protocol Bridge** | Protokol köprüsü manipülasyonu | MitM |
| 05 | **CAN Bus-Off** | CAN Bus kapatma saldırısı | DoS |
| 06 | **Firmware Manipulation** | İmzasız firmware enjeksiyonu | Injection |

### Senaryo Çalıştırma Örneği

```bash
# Firmware Manipülasyonu senaryosunu çalıştır
python -m scenarios.scenario_06_firmware_manipulation.simulate
```

### Hook Sistemi

Her senaryo 4 hook fonksiyonu kullanır:

| Hook | Tetiklenme Zamanı | Kullanım Alanı |
|------|-------------------|----------------|
| `pre_ocpp()` | OCPP mesajı gönderilmeden önce | Mesaj manipülasyonu |
| `post_ocpp()` | OCPP cevabı alındıktan sonra | Cevap analizi |
| `pre_can()` | CAN frame gönderilmeden önce | Frame enjeksiyonu |
| `post_can()` | CAN frame gönderildikten sonra | Loglama & raporlama |

---

## 👥 Ekip

### Fırat Üniversitesi — Bilgi Sistemleri ve Güvenliği (2025 Güz)

<table>
<tr>
<th>#</th>
<th>Ad Soyad</th>
<th>GitHub</th>
<th>Senaryo</th>
</tr>
<tr>
<td>1</td>
<td><b>Sena Köse</b></td>
<td><a href="https://github.com/kosesena">@kosesena</a></td>
<td>🔐 Firmware Manipülasyonu</td>
</tr>
<tr>
<td>2</td>
<td><b>Hüseyin Enes Ertürk</b></td>
<td><a href="https://github.com/huseyineneserturk">@huseyineneserturk</a></td>
<td>👻 Hayalet Şarj ile Enerji Hırsızlığı</td>
</tr>
<tr>
<td>3</td>
<td><b>Yusuf Kaya</b></td>
<td><a href="https://github.com/YusufKaya00">@YusufKaya00</a></td>
<td>💥 Operasyonel Felç (DoS)</td>
</tr>
<tr>
<td>4</td>
<td><b>Muhammed Emin Çimen</b></td>
<td><a href="https://github.com/muhammedemincmn">@muhammedemincmn</a></td>
<td>🚌 CAN Bus-Off Saldırısı</td>
</tr>
<tr>
<td>5</td>
<td><b>Beşir Can Barutçu</b></td>
<td><a href="https://github.com/BesircanB">@BesircanB</a></td>
<td>🚪 CAN Bus Debug Backdoor</td>
</tr>
<tr>
<td>6</td>
<td><b>Seyhan Şahin</b></td>
<td><a href="https://github.com/syhnshn">@syhnshn</a></td>
<td>🔄 Harici CAN Yansıtma (Reflection)</td>
</tr>
<tr>
<td>7</td>
<td><b>Kerem Öncel</b></td>
<td><a href="https://github.com/KEREMONCEL">@KEREMONCEL</a></td>
<td>👤 Hayali İstasyon - Sahte Durum</td>
</tr>
<tr>
<td>8</td>
<td><b>Adile Nur Yiğit</b></td>
<td><a href="https://github.com/adilenurygt">@adilenurygt</a></td>
<td>📡 CAN Bus Frekans Geri Besleme</td>
</tr>
<tr>
<td>9</td>
<td><b>Ahmet Küçükköylü</b></td>
<td><a href="https://github.com/AhmetKucukkoylu">@AhmetKucukkoylu</a></td>
<td>🌉 Protokol Köprüsü Gizli Talep Manipülasyonu</td>
</tr>
<tr>
<td>10</td>
<td><b>Mirullah Erbaş</b></td>
<td><a href="https://github.com/mirullaherbas">@mirullaherbas</a></td>
<td>🔋 V2G Deşarj Anomalisi</td>
</tr>
<tr>
<td>11</td>
<td><b>Azad Öcalır</b></td>
<td><a href="https://github.com/danyalocalir-tech">@danyalocalir-tech</a></td>
<td>🎮 Ele Geçirilmiş Denetleyici ile CAN Bus-Off</td>
</tr>
<tr>
<td>12</td>
<td><b>Mehmet Mesut Altunkaynak</b></td>
<td><a href="https://github.com/MesutAltunkaynak">@MesutAltunkaynak</a></td>
<td>📴 Hedefli CV Manipülasyonu ile Çevrimdışı Mod</td>
</tr>
</table>

---

## 🛠️ Teknolojiler

<div align="center">

| Kategori | Teknolojiler |
|----------|--------------|
| **Programlama** | Python 3.10+, AsyncIO |
| **Protokoller** | OCPP 1.6/2.0, CAN-Bus |
| **Simülasyon** | python-can, vcan |
| **Web Arayüz** | Streamlit |
| **Güvenlik** | TLS, AES, RSA |
| **ML/AI** | Anomali Tespiti Algoritmaları |

</div>

---

## 📜 Standartlar

Bu proje aşağıdaki uluslararası standartlara uyumludur:

| Standart | Açıklama |
|----------|----------|
| **ISO 15118** | Araç-Şebeke İletişimi |
| **ISO 27001** | Bilgi Güvenliği Yönetim Sistemi |
| **OCPP 2.0** | Açık Şarj Noktası Protokolü |
| **IEC 61851** | EV Şarj Sistemi Güvenliği |

---

## 🧩 Yeni Senaryo Ekleme

1. **Branch oluştur:**
```bash
git checkout dev
git checkout -b feature/scenario_XX_isim
```

2. **Template'i kopyala:**
```bash
cp -r scenarios/_template scenarios/scenario_XX_isim
```

3. **Dosyaları düzenle:**
   - `hooks.py` — Saldırı mantığı
   - `simulate.py` — Senaryo adını güncelle
   - `README.md` — Dokümantasyon

4. **Test et ve PR aç:**
```bash
git add .
git commit -m "Senaryo XX: İsim eklendi"
git push origin feature/scenario_XX_isim
```

---

## 📊 Proje İstatistikleri

```
📁 Toplam Senaryo: 7 (Baseline + 6 Saldırı)
👥 Ekip Üyesi: 12
📝 Toplam Commit: 19+
🔀 Aktif Branch: dev
```

---

## 📝 Lisans

Bu proje **MIT Lisansı** ile lisanslanmıştır. Detaylar için [LICENSE](LICENSE) dosyasına bakın.

---

## 🙏 Teşekkürler

- **Open Charge Alliance** — OCPP protokolü
- **Python-CAN** — CAN-Bus kütüphanesi
- **Fırat Üniversitesi** — Akademik destek

---

<div align="center">

**⚡ EV Altyapı Güvenliği İçin Geliştirilmiştir ⚡**

Fırat Üniversitesi • Bilgi Sistemleri ve Güvenliği • 2025

</div>
