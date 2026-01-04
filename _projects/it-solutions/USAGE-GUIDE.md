# IT Solutions Website - Kullanım Kılavuzu

## 🚀 Hızlı Başlangıç

### 1. Tüm Siteyi Kullan (ÖNERİLEN)

```bash
# Dosya: FULL-SITE.json (73KB)
```

**Adımlar:**
1. `FULL-SITE.json` dosyasını aç
2. Tüm içeriği kopyala (Ctrl+A → Ctrl+C)
3. Bricks Builder'da yeni sayfa oluştur
4. Sayfada yapıştır (Ctrl+V)
5. ✅ 12 section otomatik yüklenir!

**İçerik:**
- ✅ Header (sticky, nav menu, CTA)
- ✅ Hero (H1, CTA, image)
- ✅ Services (4 cards)
- ✅ Stats (4 metrics)
- ✅ About (25+ years)
- ✅ Success Story (form + features)
- ✅ Testimonials (3 reviews)
- ✅ Projects (4 cards)
- ✅ Skills (3 progress bars)
- ✅ Team (3 experts)
- ✅ Newsletter (banner)
- ✅ Footer (4 columns)

---

### 2. Tek Section Kullan

```bash
# Dosyalar: sections/*.json (1-10 KB her biri)
```

**Örnek: Sadece Header İstiyorum**

1. `sections/header.json` dosyasını aç
2. İçeriği kopyala
3. Bricks'te yapıştır
4. ✅ Header eklendi!

**Tüm Section'lar:**
- `header.json` - Sticky header (3KB)
- `hero.json` - Ana hero section (9.3KB)
- `services.json` - Servis kartları (4.9KB)
- `stats.json` - İstatistikler (878B)
- `about.json` - Hakkımızda (8.1KB)
- `success-story.json` - Form + özellikler (9.1KB)
- `testimonials.json` - Müşteri yorumları (8.8KB)
- `projects.json` - Proje kartları (8.1KB)
- `skills.json` - Beceri barları (6.4KB)
- `team.json` - Ekip üyeleri (1.8KB)
- `newsletter.json` - Newsletter banner (1.5KB)
- `footer.json` - Footer (7KB)

---

## 🎨 Özelleştirme

### Renkleri Değiştir

**Yöntem 1: Global Classes Düzenle**
```json
// global-classes.json içinde
{
  "id": "gc011k",
  "name": "ren-bg-primary",
  "settings": {
    "_background": {
      "color": {
        "hex": "#4A3AFF"  ← Buraya yeni renk
      }
    }
  }
}
```

**Yöntem 2: Config Güncelle**
```json
// config.json içinde
{
  "colors": {
    "primary": "#4A3AFF",     ← Moru değiştir
    "secondary": "#1A1D2E",   ← Koyu lacivert değiştir
    "accent": "#FFD93D"       ← Sarıyı değiştir
  }
}
```

### Logo Değiştir

1. `sections/header.json` aç
2. "RENS" text'ini bul
3. Kendi logo text'inle değiştir

```json
{
  "settings": {
    "text": "SENIN LOGO",  ← Buraya
    "tag": "div"
  }
}
```

### Nav Menu Linklerini Değiştir

1. `sections/header.json` aç
2. "menu" array'ini bul
3. Linkleri düzenle

```json
{
  "settings": {
    "menu": [
      {
        "text": "Ana Sayfa",  ← Buraya
        "url": "#home"        ← Buraya
      }
    ]
  }
}
```

### Görselleri Değiştir

**Tüm görseller Unsplash'ten:**
- Hero: `photo-1522071820081-009f0129c71c`
- About: `photo-1600880292203-757bb62b4baf`
- Projects: `photo-1460925895917-afdab827c52f` vb.

**Değiştirme:**
1. Section JSON'unu aç
2. `"image"` objesini bul
3. `"url"` değiştir
4. `"alt"` text güncelle

---

## 🔧 Global Classes Referansı

| Class ID | İsim | Açıklama |
|----------|------|----------|
| `gc001a` | ren-container-width-xl | Max width 1366px container |
| `gc002b` | ren-pad-section-lg | Section padding (2xl) |
| `gc003c` | ren-pad-section-md | Section padding (xl) |
| `gc004d` | ren-gap-xl | Gap xl (64px) |
| `gc005e` | ren-gap-lg | Gap lg (40px) |
| `gc006f` | ren-gap-md | Gap md (24px) |
| `gc007g` | ren-heading-1 | H1 typography (48px) |
| `gc008h` | ren-heading-2 | H2 typography (32px) |
| `gc009i` | ren-heading-3 | H3 typography (24px) |
| `gc010j` | ren-text-body | Body text (16px) |
| `gc011k` | ren-bg-primary | Mor background |
| `gc012l` | ren-bg-light | Açık gri background |
| `gc013m` | ren-text-white | Beyaz text |
| `gc014n` | ren-text-primary | Mor text |
| `gc015o` | ren-text-dark | Koyu text |
| `gc016p` | ren-button-primary | Sarı button |
| `gc017q` | ren-card | Card style (shadow, radius) |
| `gc018r` | ren-grid-3-col | 3 column grid (responsive) |
| `gc019s` | ren-grid-4-col | 4 column grid (responsive) |
| `gc020t` | ren-grid-2-col | 2 column grid (responsive) |
| `gc021u` | ren-flex-center | Flex center (both axis) |
| `gc022v` | ren-text-center | Text align center |

---

## 📱 Responsive

Tüm section'lar responsive:

- **Desktop:** 1200px+ (default)
- **Tablet:** 768-991px (`:tablet_portrait`)
- **Mobile:** max 478px (`:mobile_portrait`)

**Örnekler:**
```json
{
  "_gridTemplateColumns": "repeat(4, 1fr)",                    // Desktop: 4 column
  "_gridTemplateColumns:tablet_portrait": "repeat(2, 1fr)",    // Tablet: 2 column
  "_gridTemplateColumns:mobile_portrait": "1fr"                // Mobile: 1 column
}
```

---

## ✅ SEO Checklist

- [x] **Tek H1** var (Hero section'da)
- [x] **H2-H6 sıralaması** doğru
- [x] **Alt text** tüm görsellerde
- [x] **Semantic HTML** kullanıldı (header, nav, footer)
- [x] **Nav menu** nav-menu elementi ile
- [x] **External linkler** yok (internal navigation)

---

## 🐛 Troubleshooting

### Problem: Section'lar import olmuyor

**Çözüm:**
1. JSON syntax'ını kontrol et (JSONLint.com)
2. `"source": "bricksCopiedElements"` var mı kontrol et
3. Global classes import edilmiş mi?

### Problem: Renkler yanlış

**Çözüm:**
1. Global classes'ı import et (`global-classes.json`)
2. CSS variables tema stillerine ekle
3. Sayfayı yenile

### Problem: Nav menu gözükmüyor

**Çözüm:**
1. Header section'ı kullan (`sections/header.json`)
2. `nav-menu` elementi kullanıldı, `text-link` değil
3. Menu array'inin doğru format olduğunu kontrol et

### Problem: Responsive çalışmıyor

**Çözüm:**
1. Breakpoint suffix'lerini kontrol et (`:tablet_portrait`, `:mobile_portrait`)
2. Browser DevTools ile test et
3. Global classes import edilmiş mi?

---

## 📞 Yardım

1. **README.md** oku
2. **config.json** kontrol et
3. **global-classes.json** import et
4. Section dosyalarını tek tek test et
5. FULL-SITE.json kullan

---

**Created:** 2026-01-04
**Version:** 1.0
**Elements:** 214
**Sections:** 12
**Global Classes:** 22
