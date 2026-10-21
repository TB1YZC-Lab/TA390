# Değişiklikler / Changelog

## v1.3 — 2026-10-21

İlk genel sürüm. Telsiz yazılımı, Windows programı ve Android uygulaması v1.3.

First public release. Firmware, Windows program and Android app v1.3.

### Türkçe

**Kanal ekranı**

- Sessiz kanala özeldir (SK1+3 veya Hızlı Menü): sessizdeki kanalın adı üstü çizili görünür, diğer kanallar duyulur. Telsiz açılınca tüm kanallar seslidir.
- Hızlı menü ayarları (FM / DMR filtreleri, CC / TS filtresi, Röle Atla, Sessiz, Güç) sadece seçili kanala uygulanır; kaydedilmez.
- Tek kanal DMR ekranı Çift Takip gibi: kanal adı, altında küçük yazıyla TG listesi / TG; en altta sadece bölge adı.
- SK2+2: bölge taraması (görüşme olan kanalda bekler, Kırmızı iptal eder); Yukarı uzun tarama kaldırıldı.
- "Kanal --> VFO" kaldırıldı, 0 uzun basış sessiz kısayolu kaldırıldı.

**VFO ekranı**

- Tek VFO (A / B kaldırıldı); ekrandaki frekanstan dinler, VFO ayrıntılarındaki TX frekansından gönderir (otomatik röle kaydırması ve SK1+0 kaldırıldı). Frekans ortalı, "R" harfi yok; VFO ayrıntılarında ad satırı yok.
- 1 uzun: adımlı tarama (bant boyu), 2 uzun: aralık taraması (Yeşil = Başlat), 3 uzun: FM / DMR tarama, 4 uzun: dar / geniş bant, 5 uzun: filtre taraması (FM ton, DMR CC / TS / TG), 6 uzun: kanal olarak kaydet.
- Taramada Yukarı / Aşağı yön seçer, Kırmızı durdurur (tekrar basınca kanal ekranı). DMR taraması FM gibi hızlıdır ve DMR yayınında durur.
- VFO'ya her girişte bütün filtreler kaldırılır.
- VFO ekranı: frekans, sinyal gücü (S7 -101 dBm), adım ve TX farkı (TX -7.600, aynıysa TX 0), 7 uzun: adım değiştir (SK1+5 kaldırıldı), 8 uzun / 9 uzun: TX kayması - / + (kanal ayrıntısındaki topuz değerleri: 0.6 ... 9.4 MHz), tarama satırı ve frekans kayıtlı bir kanalınsa o kanalın adı.
- VFO Hızlı Menüsü'nden Tx/Rx satırları, VFO A/B, Çift Takip, Ton Tarama, Frekans Bağlama ve VFO > Yeni Kanal kaldırıldı. VFO'da TG yok: DMR modunda sadece DMR yayını aranır; ekranda TG yazmaz. SK1+4 ve Yukarı uzun tarama kaldırıldı. * FM'de bant değiştirmez.

**Üst satır**

- FM dar bant "FM  N" olarak ayrı yazılır (5 piksel boşluk, sonraki simgeler 3 piksel).

**Kısayollar ve diğer**

- Tuş kilidi: kilitliyken üst satırda kilit simgesi, ekranda 2 saniye "Tuşlar Kilitli". Önce Yeşil, sonra * kilitler; kilitliyken önce Yeşil, sonra * açar. SK2+* ile açma kaldırıldı.
- SK2+1: APRS konumunu hemen gönderir; uyarı yazıları ekrana sığacak şekilde iki satır.
- APRS paketlerinde cihaz kodu APTA39 (aprs.fi kaydı istendi).
- Ses ayarlarında DMR Rx AGC, FM Mik. satırının altına alındı.
- Telsizdeki kısayol listesi (Türkçe ve İngilizce) güncellendi.
- Kanal Ayrıntısı'na TG satırı eklendi: DMR kanalında TG listesindeki konuşma grupları döner düğmeyle gezilir, Yeşil ile kaydedilince kanal o TG ile açılır (kısayola gerek kalmaz).
- Kanal Ayrıntısı'ndan Adım (VFO ayrıntısında kalır), Susturma, Uyarı, Ekonomi ve TA Tx TS1 / TS2 kaldırıldı: susturma, uyarı sesleri ve Eko genel ayarlardan; DMR ID satırında ikinci ID yoksa kayıtlı ID yazar.
- Ana menü > Kişiler doğrudan bütün DMR kişilerini açar (grup, özel, herkes tek listede), listenin başında + Yeni Kişi; FM DTMF kişileri menüden kaldırıldı.
- SK1 ile görünen frekans ayrıntısında R / T yerine Rx / Tx yazar.
- APRS ayarlarına DMR TA eklendi (bütün kanallar): DMR konuşmasında Konum (GPS), Metin ya da İkisi de gönderilir.
- Ayarlar > Telsiz'deki Tarama Bek. kaldırıldı: tarama ve Çift Takip kanal başına sabit 30 ms (en hızlı) bakar. Çift Takip çalışırken güç tasarrufu (Eko) tamamen kapalı.

### Programlar

- Windows programı ve Android uygulaması aynı işlevlere sahip: yazılım yükleme / güncelleme (donör otomatik indirilir), Flash / MCU ROM / kalibrasyon yedeği ve geri yükleme, boot resmi, uydu bilgileri, telsiz saati, CPS (Genel, Kanallar, Bölgeler, Kişiler, TG Listeleri, APRS, Telsiz Ayarları; sürükle-bırak).
- Android uygulaması: koyu tema, USB OTG ile çalışır.

### English

**Channel screen**

- Mute is per channel (SK1+3 or Quick Menu): the name of the muted channel is struck through, the other channels are heard. All channels are audible after power on.
- The Quick Menu settings (FM / DMR filters, CC / TS filter, Talkaround, Mute, Power) apply to the selected channel only; they are not saved.
- The single channel DMR screen looks like Dual Watch: channel name, TG list / TG in small text below it, only the zone name at the bottom.
- SK2+2: zone scan (stops on a channel with a call, Red cancels); the Up long press scan was removed.
- "Channel --> VFO" and the 0 long press mute shortcut were removed.

**VFO screen**

- Single VFO (A / B removed): it listens on the displayed frequency and transmits on the TX frequency of the VFO details (automatic repeater shift and SK1+0 removed). Centred frequency, no "R" letter, no name row in the VFO details.
- 1 long: step scan (whole band), 2 long: range scan (Green = Start), 3 long: FM / DMR scan, 4 long: narrow / wide, 5 long: filter scan (FM tone, DMR CC / TS / TG), 6 long: save as a channel.
- While scanning Up / Down sets the direction, Red stops (pressed again: channel screen). The DMR scan is as fast as the FM scan and stops on DMR traffic.
- All the filters are cleared each time the VFO is entered.
- VFO screen: frequency, signal strength (S7 -101 dBm), step and TX offset (TX -7.600, TX 0 when the same), 7 long: change the step (SK1+5 removed), 8 long / 9 long: TX shift - / + (the knob values of the channel details: 0.6 ... 9.4 MHz), scan line, and the channel name when the frequency belongs to a stored channel.
- Removed from the VFO Quick Menu: Tx/Rx rows, VFO A/B, Dual Watch, Tone scan, Freq. bind and VFO --> New channel. No TG in the VFO: in DMR mode only DMR traffic is searched; no TG on the screen. SK1+4 and the Up long scan removed. * does not change the bandwidth in FM.

**Header line**

- FM narrow band is shown as a separate "FM  N".

**Shortcuts and other**

- Keypad lock: a lock icon in the header while locked, "Keys locked" for 2 seconds. Green then * locks; while locked Green then * unlocks. SK2+* unlock removed.
- SK2+1: sends the APRS position at once; the messages are on two lines to fit the screen.
- APRS packets use the device code APTA39.
- Sound options: DMR Rx AGC moved below FM mic.
- The shortcut list of the radio (Turkish and English) was updated.
- Channel details: new TG row: on a DMR channel the TGs of the TG list are browsed with the knob; saved with Green, the channel opens with that TG (no shortcut needed).
- Channel details: Step (kept in the VFO details), Squelch, Beep, Eco and TA Tx TS1 / TS2 removed: squelch, beeps and Eco come from the general settings; the DMR ID row shows the radio ID when there is no channel ID.
- Main menu > Contacts opens all the DMR contacts directly (group, private, all call in one list), with + New contact at the top; FM DTMF contacts removed from the menu.
- The frequency details shown with SK1 use Rx / Tx instead of R / T.
- APRS options: DMR TA added (all channels): Location (GPS), Text or Both sent during DMR calls.
- Radio options: Scan dwell removed: scan and Dual Watch look at each channel for a fixed 30 ms (fastest). Power saving (Eco) is fully off while Dual Watch is running.

### Programs

- The Windows program and the Android app have the same functions: firmware flashing / update (the donor is downloaded automatically), Flash / MCU ROM / calibration backup and restore, boot image, satellite data, radio clock, CPS (General, Channels, Zones, Contacts, TG Lists, APRS, Radio Settings; drag and drop).
- Android app: dark theme, works over USB OTG.
