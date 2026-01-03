# Bricks Builder Template Library

Bricks Builder icin hazir template ve section koleksiyonu. Tum dosyalar direkt Copy-Paste veya Import ile kullanilabilir.

---

## Klasor Yapisi

```
bricksbuilder/
├── sections/           # Kategorize edilmis section'lar
│   ├── headers/        # Header template'leri (14 adet)
│   ├── footers/        # Footer template'leri (6 adet)
│   ├── hero/           # Hero section'lar (9 adet)
│   ├── contact/        # Iletisim formlari (44 adet)
│   ├── features/       # Ozellik grids (4 adet)
│   ├── testimonials/   # Musteri yorumlari
│   ├── cta/            # Call-to-action
│   ├── about/          # Hakkimizda
│   ├── services/       # Hizmetler
│   ├── team/           # Takim (2 adet)
│   ├── blog/           # Blog section'lar (2 adet)
│   └── other/          # Diger
│
├── full-sites/         # Tam site template'leri
│   ├── smile/          # Klinik/Dental sitesi (9 template)
│   ├── promover/       # Marketing ajans (10 template)
│   ├── uplift/         # Kurumsal site (8 template)
│   ├── cosmetics/      # Guzellik/E-ticaret (10 template)
│   └── simple/         # Minimalist SaaS (8 template)
│
└── wireframesfull.md   # Orijinal wireframe koleksiyonu
```

---

## Nasil Kullanilir

### Yontem 1: Copy-Paste (Onerilen)

1. JSON dosyasini ac
2. Tum icerigi kopyala (Ctrl+A, Ctrl+C)
3. Bricks Editor'de sag tik → **Paste**

### Yontem 2: Import

1. Bricks → Templates → Import
2. JSON dosyasini sec
3. Import et

---

## Template Onizleme

### Full Sites

| Site | Tur | Template Sayisi |
|------|-----|-----------------|
| **Smile** | Dental Klinik | 9 |
| **Promover** | Marketing Ajans | 10 |
| **Uplift** | Kurumsal | 8 |
| **Cosmetics** | E-ticaret/Guzellik | 10 |
| **Simple** | SaaS/Startup | 8 |

### Section Kategorileri

| Kategori | Adet | Aciklama |
|----------|------|----------|
| Headers | 14 | Sticky, mega menu, minimal |
| Footers | 6 | Cesitli footer tasarimlari |
| Hero | 9 | Farkli hero section varyasyonlari |
| Contact | 44 | Form cesitleri, harita, bilgi |
| Features | 4 | Ozellik grid'leri |
| Team | 2 | Takim uyesi kartlari |
| Blog | 2 | Blog post listeleme |
| CTA | 1 | Call-to-action section |
| Services | 1 | Hizmet kartlari |

---

## Bricks Builder JSON Yapisi

Her template su formatta:

```json
{
  "content": [...],           // Element dizisi
  "source": "bricksCopiedElements",
  "version": "1.12.3",
  "globalClasses": [...],     // Global CSS class'lar
  "globalElements": []
}
```

### Element Yapisi

```json
{
  "id": "abc123",             // Unique ID
  "name": "container",        // Element tipi
  "parent": "xyz789",         // Parent ID (0 = root)
  "children": ["def456"],     // Child ID'ler
  "settings": {               // Tum ayarlar
    "_direction": "row",
    "_background": {...},
    "_typography": {...}
  }
}
```

### Desteklenen Element Tipleri

- `section`, `container`, `block`
- `heading`, `text`, `text-basic`
- `button`, `icon`, `image`
- `nav-menu`, `logo`
- `form`, `list`, `icon-box`
- `divider`, `video`, `slider`

---

## Responsive Breakpoint'ler

Bricks Builder suffix'leri:

| Suffix | Cihaz |
|--------|-------|
| (default) | Desktop |
| `:tablet_portrait` | Tablet |
| `:mobile_landscape` | Mobile Yatay |
| `:mobile_portrait` | Mobile Dikey |

Ornek:
```json
{
  "_direction": "row",
  "_direction:tablet_portrait": "column"
}
```

---

## Global Class Sistemi

Template'lerde kullanilan ortak class'lar:

| Class | Islem |
|-------|-------|
| `ren-container-width-lg` | Max width 1366px |
| `ren-pad-top-bottom-lg` | Ust-alt padding |
| `ren-gap-lg` | Buyuk gap |
| `ren-text-secondary` | Ikincil renk |
| `ren-heading-2` | H2 stili |

---

## Hizli Baslangic

### Kurumsal Site Icin

1. `full-sites/uplift/` klasorunden header ve footer al
2. `sections/hero/` klasorunden hero sec
3. `sections/contact/` klasorunden iletisim formu ekle

### Landing Page Icin

1. `full-sites/simple/` klasorunden header al
2. `sections/hero/` + `sections/features/` + `sections/cta/` ekle
3. Footer ekle

---

## Katki

Yeni template eklemek icin:
1. Bricks'te section'u olustur
2. Sag tik → Copy
3. JSON olarak kaydet
4. Uygun klasore ekle
5. PR olustur

---

## Lisans

Bu template'ler serbest kullanim icindir. Ticari projelerde kullanilabilir.
