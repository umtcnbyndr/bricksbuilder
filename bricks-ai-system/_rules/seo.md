# SEO KURALLARI

## HTML Tag Seçimi
| Tag | Kullanım | Sayfa Başına |
|-----|----------|--------------|
| `header` | Site header | 1 |
| `main` | Ana içerik | 1 |
| `footer` | Site footer | 1 |
| `nav` | Navigasyon | 1-2 |
| `section` | Bölümler | Sınırsız |
| `article` | Blog/ürün | Sınırsız |

## Heading Kuralları
```
H1 → Sayfa başlığı (1 TANE!)
├── H2 → Bölüm başlıkları
│   └── H3 → Alt başlıklar
└── H2 → Bölüm başlıkları
```

**Örnek:**
```
H1: "İstanbul Diş Kliniği"
├── H2: "Hizmetlerimiz"
│   ├── H3: "İmplant"
│   └── H3: "Beyazlatma"
├── H2: "Neden Biz?"
└── H2: "İletişim"
```

## Görsel SEO
```json
{
  "name": "image",
  "settings": {
    "image": {
      "alt": "Açıklayıcı metin"  // ZORUNLU!
    }
  }
}
```

## Link SEO
```json
// Internal
{ "link": { "type": "internal", "url": "/hizmetler/" } }

// External
{ 
  "link": { 
    "type": "external", 
    "url": "https://...",
    "newTab": true,
    "rel": "noopener noreferrer"  // GÜVENLİK!
  } 
}
```

## Checklist
- [ ] H1 sayfa başına 1 tane
- [ ] Heading sırası doğru
- [ ] Alt text tüm görsellerde
- [ ] External link rel="noopener"
- [ ] Semantic HTML taglar
