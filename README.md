# 🔧 ST-Link V2 Clone (Rev.2) — KiCad PCB Design

STM32 tabanlı bir **ST-Link V2 programlayıcı** kart tasarımıdır.  
Projede amaç, USB–SWD arayüzünü stabilize edecek şekilde hat eşitlemesi yapılmış,  
üretime uygun iki katmanlı bir PCB ortaya çıkarmaktır.

---

## ⚙️ Teknik Özellikler

- 🧠 **Mikrodenetleyici:** STM32F103C8T6  
- 🔌 **Bağlantı:** USB FS (12 Mbps), D+ / D− diferansiyel hat eş uzunluklu  
- ⚡ **Besleme:** 5V → 3.3V LDO regülatör  
- 🔒 **Koruma:** TVS diyot ile ESD koruması  
- 📡 **Arabirim:** SWD, UART pin header (JTAG alternatifi)  
- 🧩 **Katman sayısı:** 2  
- 🔍 **Min. İz kalınlığı:** 0.25 mm  
- 🕳 **Via boyutu:** 0.3 / 0.6 mm  
- 🧱 **PCB boyutu:** Yaklaşık 70.750 × 30 mm  
- 🧾 **DRC:** Hatasız (clearance & unconnected 0)

---

## 🧠 Tasarım Notları

- D+ / D− hatları eş uzunlukta ve paralel route edildi.  
- 3.3V ve 5V güç yolları kalınlaştırılarak düşük dirençli hat elde edildi.  
- Decoupling kondansatörleri MCU’ya yakın konumlandırıldı.  
- Kristal çevresi kısa loop ve GND guard ile izole edildi.  
- GND plane sürekliliği korunarak düşük EMI hedeflendi.  
- Tüm komponentler okunabilir ve üretim dostu silkscreen düzeninde yerleştirildi.

---

## 🧩 Görseller

### PCB Üst Katman (3D)
![PCB Top](stlinkv2_clone/outputs/pcb_top.png)

### PCB Alt Katman (3D)
![PCB Bottom](stlinkv2_clone/outputs/pcb_bottom.png)

### Düzenleme Görünümü (KiCad)
![PCB Layout](stlinkv2_clone/outputs/pcb_layout.png)

---

## 🧰 Üretim & Çıktılar

- Gerber + Drill dosyaları `hardware/outputs/gerbers_drill_zip` klasöründe.  
- JLCPCB / PCBWay üretim kurallarına tam uyumlu.  
- Şematik dosyası `.pdf` formatında eklendi (`schematic.pdf`).  
- BOM listesi ve netlist otomatik oluşturulabilir (`KiCad v7+` uyumlu).

---

## 🧑‍💻 Geliştirici Notu

> Bu proje eğitim ve prototip amaçlı hazırlanmıştır.  
> Geliştirmeye açıktır: SWD pin koruma, hedef güç algılama (target power detect)  
> ve LED status indikatörleri eklenebilir.

---

## 📁 Klasör Yapısı

stlinkv2-clone/
│ ├─ kicad_proj_files/
│ ├─ outputs/
│ │ ├─ gerbers_drill_zip/
│ │ ├─ pcb_top.png
│ │ ├─ pcb_bottom.png
│ │ └─ schematic.pdf
│ └─ bom.csv
└─ README.md


---

## 👤 Tasarım
**Mert Çubuk**  
Elektrik-Elektronik Mühendisi | Embedded Systems & PCB Design  
📅 Ekim 2025  
🔗 [LinkedIn](https://www.linkedin.com/in/mert-%C3%A7ubuk-06b53536a/) 

