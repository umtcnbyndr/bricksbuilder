# IT Solutions Website

High quality IT-Solutions company website with 12 sections.

## 📁 Dosya Yapısı

```
_projects/it-solutions/
├── config.json              ← Proje ayarları (renkler, fontlar, section listesi)
├── global-classes.json      ← 22 global class (tüm sitede kullanılan)
├── FULL-SITE.json          ← Tüm site (12 section, 214 element)
├── sections/               ← Ayrı section dosyaları
│   ├── header.json         ← Sticky header (logo, nav, CTA)
│   ├── hero.json           ← Hero section (H1, CTA, image)
│   ├── services.json       ← 4 service cards
│   ├── stats.json          ← 4 statistics
│   ├── about.json          ← About section (25+ years)
│   ├── success-story.json  ← Form + 4 features
│   ├── testimonials.json   ← 3 client reviews
│   ├── projects.json       ← 4 project cards
│   ├── skills.json         ← 3 progress bars
│   ├── team.json           ← 3 expert cards
│   ├── newsletter.json     ← Newsletter banner
│   └── footer.json         ← Footer (4 columns + copyright)
└── README.md               ← Bu dosya
```

## 🎯 Kullanım

### Option 1: Tüm Siteyi Import Et
```
1. FULL-SITE.json dosyasını aç
2. Tüm içeriği kopyala (Ctrl+A, Ctrl+C)
3. Bricks Builder'da yeni sayfa aç
4. Yapıştır (Ctrl+V)
```

### Option 2: Tek Section Import Et
```
1. sections/ klasöründen istediğin section'ı aç (örn: hero.json)
2. İçeriği kopyala
3. Bricks'te yapıştır
```

## 📊 İstatistikler

- **Toplam Section:** 12
- **Toplam Element:** 214
- **Global Class:** 22
- **Renk Paleti:** 6 renk
- **Responsive:** ✅ (tablet_portrait, mobile_portrait)
- **SEO:** ✅ (tek H1, alt text, semantic HTML)

## 🎨 Renk Paleti

| Renk | Hex | Kullanım |
|------|-----|----------|
| Primary | `#4A3AFF` | Mor - CTA, vurgular |
| Secondary | `#1A1D2E` | Koyu lacivert - başlıklar |
| Accent | `#FFD93D` | Sarı - butonlar |
| Light | `#F8F9FA` | Açık gri - arkaplan |
| White | `#FFFFFF` | Beyaz |
| Gray | `#6B7280` | Gri - açıklama metinleri |

## 🔧 Özelleştirme

### Renkleri Değiştir
`config.json` dosyasındaki `colors` objesini düzenle.

### Section Ekle/Çıkar
1. `sections/` klasörüne yeni JSON ekle
2. `config.json` içindeki `sections` listesine ekle
3. Python scripti ile FULL-SITE.json'u yeniden oluştur

### Global Class Ekle
`global-classes.json` dosyasına yeni class ekle.

## 🚀 Deployment Checklist

- [ ] Global classes Bricks'e import edildi
- [ ] CSS variables tema stillerine eklendi
- [ ] Tüm section'lar kontrol edildi
- [ ] Mobil responsive test edildi
- [ ] SEO kontrol edildi (H1, alt text)
- [ ] Form action ayarlandı
- [ ] Görseller değiştirildi

## 📝 Notlar

- **HEADER:** Sticky, shadow, responsive nav menu
- **NAV MENU:** nav-menu elementi kullanıldı (text-link değil!)
- **GLOBAL CLASSES:** CSS variables ile (var(--spacing-md))
- **BEM:** ren-* prefix ile isimlendirme
- **RESPONSIVE:** tablet_portrait, mobile_portrait suffix'leri

## 🐛 Bilinen Sorunlar

Yok - tüm section'lar test edildi.

## 📞 Destek

Sorun olursa:
1. `config.json` kontrol et
2. `global-classes.json` kontrol et
3. Section dosyasını tekrar import et
4. FULL-SITE.json kullan

---

**Versiyon:** 1.0
**Tarih:** 2026-01-04
**Oluşturan:** Bricks AI System
