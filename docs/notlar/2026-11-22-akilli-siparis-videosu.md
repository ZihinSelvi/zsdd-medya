# Çalışma Notu: Akıllı Sipariş Yanıtlama Videosu ve ZSDD Marka Kiti

**Oturum:** 22 Kasım 2026, Claude Code masaüstü (yerel klasör: `Claudeiçindeneme`)

## Amaç
Restoranlara WhatsApp'tan gelen siparişleri net siparişe dönüştüren sistemi tanıtan 20 saniyelik dikey (Reels) video hazırlamak; bu sırada ZSDD marka bilgilerini (font, logo) tek yerde doğru hâle getirmek.

## Yapılanlar
- [x] İlk sürüm: yatay 16:9 tipografik animasyon (HTML) ve MP4'ü (`akilli-siparis-yanitlama.html`, `.mp4`).
- [x] Dikey 9:16 sürüm ve müzik eklendi (`akilli-siparis-yanitlama-dikey.mp4`). Eski logo ve fontla; **paylaşma**.
- [x] **Ozan Sihay motion skill'i** masaüstündeki `ozansihay-motion.skill` dosyasından kuruldu (`%USERPROFILE%\.claude\skills\ozansihay-motion\`). Skill adı dosyada `zihniselvi-motion` olarak değiştirildi.
- [x] Video skill'le baştan yapıldı: **v2** (`akilli-siparis-yanitlama-dikey-v2.mp4`, kaynak `akilli-siparis-yanitlama-fis.html`).
  - Fikir: dağınık WhatsApp mesajları → yazıcıdan adım adım çıkan tek sipariş fişi.
  - 1080×1920, 30 fps, 20 sn. Ses: telefon titreşimi, tam sessizlik, yazıcı beslemesi, kalimba (−16 LUFS).
  - Klişe testi: 1 puan (koyu lacivert zemin + mavi vurgu; marka paleti).
- [x] Skill revizeleri:
  - Stil kartına **"Marka kiti"** satırı; ZSDD işlerinde palet, font ve logo `references/zsdd-marka-kiti.md` dosyasından otomatik gelir.
  - Orijinal logo skill'e kopyalandı: `assets/zsdd-logo.png`.
  - Klişe listesinden **"saf beyaz"** çıkarıldı (ZSDD kitinde beyaz var).
- [x] ZSDD fontu **Argentum Sans** olarak düzeltildi: skill'in marka kitinde, v2 videoda ve claude.ai'deki ZSDD Tasarım Sistemi'nde (font dosyaları yüklendi).
- [x] ZSDD Tasarım Sistemi'ne orijinal logo ("Logolar" grubu, marka kitabında "Logo" bölümü) ve logolu yeni kapak eklendi (sürüm 9): https://claude.ai/artifact/Q2oeipU9rbWBsW3uFKk4Lr

## Öğrendiklerim
- **Orijinal ZSDD logosu** iç içe iki spiral halka + "ZİHNİ SELVİ / DİJİTAL DANIŞMANLIK" yazısı; kaynak OneDrive `DİJİTAL PAZARLAMA\ZİHNİSELVİ DD\LOGOLAR\` (`LOGO PNG 2.png`, vektör `LOGO.cdr`). Tasarım Sistemi'ndeki beş kareli artı **logo değil**, süs motifiydi.
- ZSDD fontu **Argentum Sans**; Bricolage Grotesque değil. `@fontsource/argentum-sans` dosyalarında Türkçe harflerin hepsi var.
- `.skill` dosyası bir zip arşividir; Not Defteri'nde karışık görünür. Düzenleme kurulu klasördeki `.md` dosyalarında yapılır.
- OneDrive kapalıyken bulutta duran dosyalar okunamaz; OneDrive'ı başlatınca iner.
- Video, HTML'den kare kare render edilir (Playwright + ffmpeg). Metin/zamanlama değişikliği için HTML'deki "OLAY LİSTESİ" kare numaraları değiştirilip yeniden render alınır (~2 dk).
- Bu klasör bir git deposu değil; buradan doğrudan push/merge yapılamaz.

## Dosyalar
Depoda (`ZihinSelvi/zsdd-medya`): `videolar/akilli-siparis-yanitlama/` klasöründe; eski sürümler depoya konmadı, yalnızca yerel klasörde.

| Dosya | Ne |
|---|---|
| `akilli-siparis-yanitlama-dikey-v2.mp4` | **Son video** |
| `akilli-siparis-yanitlama-fis.html` | v2'nin kaynağı (stil kartı dosyanın başında) |
| `fonts/` | Argentum Sans 300/800, IBM Plex Mono 500 |
| `assets/zsdd-logo.png` | Orijinal logo |
| `akilli-siparis-yanitlama.html` / `.mp4`, `-dikey.mp4` | Eski sürümler (eski logo/font) |

## Sonraki adımlar
- [ ] `zsdd-kapak` skill'i hâlâ Bricolage kullanıyor ve logo içermiyor; Argentum Sans + orijinal logoya göre güncellenmeli.
- [ ] Canva marka kitindeki font atamalarını Argentum Sans yap.
- [ ] Logonun vektör sürümünü (`LOGO.cdr`) SVG ya da PDF olarak dışa aktar; Tasarım Sistemi'ne eklenebilir.
- [ ] Not Defteri'nde açık kalan eski `SKILL.md` varsa **kaydetmeden** kapat (yoksa skill değişikliklerinin üzerine yazar).
