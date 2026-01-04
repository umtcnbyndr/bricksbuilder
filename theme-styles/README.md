# Theme Styles Kullanım Kılavuzu

## 1. Theme Style Import Etme

### Adım 1: WordPress Admin'e Git
```
WordPress Dashboard → Bricks → Settings → Theme Styles
```

### Adım 2: Import Yap
1. "Import Theme Styles" butonuna tıkla
2. `law-firm-theme-style.json` dosyasını seç
3. Import et

### Adım 3: Aktif Et
1. İmport edilen "Law Firm Professional Theme" görünecek
2. Conditions ayarla (örn: "Entire Website" veya specific pages)
3. Kaydet

## 2. Template JSON'larda Kullanım

### ❌ ÖNCESİ (Hard-coded renk):
```json
"_typography": {
  "color": {
    "hex": "#1e3a8a"
  }
}
```

### ✅ SONRASI (Theme'den gelen renk):
```json
"_typography": {
  "color": {
    "hex": "#1e3a8a",
    "id": "navy-primary"
  }
}
```

## 3. Avantajları

✓ **Tek yerden renk yönetimi**: Tüm renkleri theme style'da değiştir, tüm site güncellenir
✓ **Farklı temalar**: Her client için farklı theme style (law-firm, medical, tech, vs.)
✓ **Tutarlılık**: Tüm sayfalarda aynı renkler kullanılır
✓ **Export/Import**: Bir projeden diğerine kopyala

## 4. Renk Paleti

| ID | Ad | Hex | Kullanım |
|----|----|----|----------|
| `navy-primary` | Navy Primary | #1e3a8a | Ana butonlar, başlıklar |
| `navy-secondary` | Navy Secondary | #1e40af | Hover durumları |
| `blue-light` | Blue Light | #3b82f6 | Gradient sonu |
| `blue-lightest` | Blue Lightest | #dbeafe | Gradient başlangıç |
| `gold-accent` | Gold Accent | #d4af37 | İkonlar, vurgular |
| `gold-dark` | Gold Dark | #b8941f | Gold hover |
| `dark-heading` | Dark Heading | #1f2937 | Ana başlıklar |
| `gray-text` | Gray Text | #6b7280 | Paragraflar |
| `gray-light` | Gray Light | #f9fafb | Arka planlar |
| `white` | White | #ffffff | Beyaz arka plan, yazılar |
| `blue-gradient-start` | Blue Gradient Start | #e0e7ff | Gradient başlangıç |

## 5. Yeni Sektör İçin Tema Oluşturma

### Örnek: Medical Clinic Theme

```json
{
  "medical-clinic-clean": {
    "label": "Medical Clinic Clean Theme",
    "settings": {
      "colors": {
        "palette": [
          {
            "id": "teal-primary",
            "name": "Teal Primary",
            "value": {"hex": "#0d9488"}
          },
          {
            "id": "orange-accent",
            "name": "Orange Accent",
            "value": {"hex": "#f97316"}
          }
        ]
      }
    }
  }
}
```

## 6. Template JSON Güncelleme

Tüm AI-generated JSON'larımızı theme ID'lerle güncelleyeceğiz:

**Önce:**
```json
"_background": {
  "color": {"hex": "#1e3a8a"}
}
```

**Sonra:**
```json
"_background": {
  "color": {
    "hex": "#1e3a8a",
    "id": "navy-primary"
  }
}
```

Bu sayede client'a farklı renkler vermek istersen sadece theme style'ı değiştirirsin!
