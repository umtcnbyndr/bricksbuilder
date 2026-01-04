# ACCESSIBILITY KURALLARI

## Semantic HTML
```json
// Header
{ "tag": "header" }

// Main
{ "tag": "main" }

// Footer
{ "tag": "footer" }

// Nav (nav-menu zaten <nav> kullanır)
```

## Alt Text
```json
// Content görsel
{ "image": { "alt": "Açıklayıcı metin" } }

// Decorative görsel
{ "image": { "alt": "" } }
```

## Renk Kontrastı
- Text: min **4.5:1**
- Büyük text: min **3:1**
- UI elements: min **3:1**

❌ Açık gri text beyaz üzerinde
✅ Koyu gri text beyaz üzerinde

## Keyboard
- Focus state görünür olmalı
- Tab sırası mantıklı olmalı

## Form
- Her input'ta label ZORUNLU
- Error mesajları açık
- Required alanlar belirtilmiş

## Typography
- Min font: **16px**
- Line height: **1.5+**

## Touch
- Min target: **44x44px**

## Link Text
```
❌ "Buraya tıklayın"
✅ "Hizmetlerimizi inceleyin"
```

## ARIA (Gerektiğinde)
```json
{
  "_attributes": {
    "role": "banner",
    "aria-label": "Ana menü"
  }
}
```

## Checklist
- [ ] Alt text tüm görsellerde
- [ ] Kontrast yeterli
- [ ] Focus state var
- [ ] Form label'ları var
- [ ] Font min 16px
- [ ] Touch target 44px+
