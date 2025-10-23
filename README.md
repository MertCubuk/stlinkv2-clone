# ST-Link V2 Clone (Rev.2) — KiCad PCB Design

STM32 tabanlı bir ST-Link V2 programlayıcı kart tasarımıdır.  
Projede amaç, USB–SWD arayüzünü stabilize edecek şekilde hat eşitlemesi yapılmış,  
üretime uygun iki katmanlı bir PCB ortaya çıkarmaktır.

---

## Teknik Özellikler

- Mikrodenetleyici: STM32F103C8T6  
- Bağlantı: USB FS (12 Mbps), D+ / D− diferansiyel hat eş uzunluklu  
- Besleme: 5V → 3.3V LDO regülatör  
- Koruma: TVS diyot ile ESD koruması
- Arabirim: SWD, UART pin header (JTAG alternatifi)  
- Katman sayısı: 2  
- Minimum iz kalınlığı: 0.25 mm  
- Minimum via boyutu: 0.3 / 0.6 mm  
- PCB boyutu: Yaklaşık 70.75 × 30 mm  
- DRC: Hatasız (clearance & unconnected 0)

---

## Tasarım Notları

- D+ / D− hatları eş uzunlukta ve paralel olarak route edildi.  
- 3.3V ve 5V güç yolları kalınlaştırılarak düşük dirençli hat elde edildi.  
- Decoupling kondansatörleri MCU’ya fiziksel olarak en yakın konumda yerleştirildi.  
- Kristal çevresi kısa loop ve GND guard ile izole edildi.  
- GND plane sürekliliği korunarak düşük EMI hedeflendi.  
- Bileşenlerin silkscreen konumları okunabilirlik ve üretim kolaylığına göre düzenlendi.

---

## Görseller

### PCB Üst Katman (3D)
![PCB Top](stlinkv2_clone/outputs/pcb_top.png)

### PCB Alt Katman (3D)
![PCB Bottom](stlinkv2_clone/pcb_bottom.png)

### Düzenleme Görünümü (KiCad)
![PCB Layout](stlinkv2_clone/pcb_layout.jpeg)

---

## Üretim ve Çıktılar

- Gerber + Drill dosyaları `outputs/gerbers_drill.rar` klasöründe yer alır.  
- JLCPCB / PCBWay üretim kurallarına uyumludur.  
- Şematik dosyası `.pdf` formatında eklendi (`stlinkv2_schmatic.pdf`).  
- BOM listesi ve netlist, KiCad v9+ üzerinde otomatik oluşturulabilir.

---


## Tasarım

Mert Çubuk  
Elektrik-Elektronik Mühendisi | Embedded Systems & PCB Design  
Ekim 2025  
LinkedIn: [https://www.linkedin.com/in/mert-%C3%A7ubuk-06b53536a/]  


