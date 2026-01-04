# 📸 SCREENSHOT İLE TASARIM AÇIKLAMA FORMATI

Bana screenshot gönderirken **bu formatı kullan**. Bricks element yapısına göre hazırlandı.

---

## 🎯 KULLANIM

```
[Screenshot'ı at]

Ardından bu formatla açıkla:
```

---

## 📋 AÇIKLAMA FORMATI

### **SECTION 1: HEADER**

**Element Yapısı:**
```
section (sticky, bg: white)
└─ container (max-width: 1200px)
   └─ block (flex, justify-between)
      ├─ logo-group (flex, gap: 12px)
      │  ├─ icon (balance-scale, 28px, navy)
      │  └─ heading (text: "Kaya Hukuk", 22px, bold)
      ├─ nav-links (flex, gap: 40px) [mobilde gizli]
      │  ├─ text-link ("Hizmetlerimiz", 15px, gray)
      │  ├─ text-link ("Uzmanlık", 15px, gray)
      │  └─ text-link ("İletişim", 15px, gray)
      └─ buttons (flex, gap: 20px) [mobilde gizli]
         ├─ text-link ("Giriş Yap", 15px, gray)
         └─ button ("Ücretsiz Danışma", navy, rounded)
```

**Settings:**
- Section: `_position: sticky`, `_background: white`, `_padding: 20px top/bottom`, `_boxShadow: 0 2px 10px rgba(0,0,0,0.04)`
- Logo icon: `28px`, `color: navy #1e3a8a`
- Logo text: `22px`, `font-weight: 700`, `color: navy`
- Nav links: `15px`, `font-weight: 500`, `color: gray #6b7280`, hover: `navy`
- Button: `bg: navy #1e3a8a`, `padding: 12px 28px`, `border-radius: 25px`, `white text`

**Responsive:**
- Mobile: Nav ve buttons gizli (`_display:mobile_portrait: none`)

---

### **SECTION 2: HERO**

**Element Yapısı:**
```
section (gradient bg, padding: 100px)
└─ container (max-width: 1200px)
   └─ block (flex-column, center aligned, gap: 32px)
      ├─ badge ("25 Yıllık Deneyim")
      ├─ heading (H1: "Hukuki Haklarınızı...")
      ├─ text-basic (subheading, açıklama)
      ├─ platforms-block (flex, gap: 16px, 3 badge)
      │  ├─ badge-1 (icon + "İstanbul Barosu")
      │  ├─ badge-2 (icon + "TBB Üyesi")
      │  └─ badge-3 (icon + "Sigortalı Hizmet")
      └─ cards-grid (3 columns, gap: 24px)
         ├─ card-1 (icon + title + desc)
         ├─ card-2 (icon + title + desc)
         └─ card-3 (icon + title + desc)
```

**Settings:**
- Section: `_background: gradient linear 180deg (#1e3a8a → #3b82f6)`, `_padding: 100px top/bottom` (mobile: 60px)
- Badge: `bg: rgba(255,255,255,0.2)`, `padding: 8px 20px`, `border-radius: 20px`, `white text 14px`
- H1: `56px` (mobile: 36px), `font-weight: 700`, `white`, `line-height: 1.2`, `max-width: 900px`
- Subheading: `18px` (mobile: 16px), `font-weight: 400`, `color: #e0e7ff`, `max-width: 700px`
- Platform badges: `bg: rgba(255,255,255,0.15)`, `padding: 10px 16px`, `radius: 20px`, `icon 16px + text 14px white`
- Cards: `bg: white`, `padding: 32px 28px`, `radius: 16px`, `shadow: 0 4px 20px rgba(0,0,0,0.08)`
- Card icon: `36px`, `color: gold #d4af37`
- Card title: `22px`, `bold`, `navy #1e3a8a`
- Card desc: `15px`, `regular`, `gray #6b7280`

**Responsive:**
- Grid: 3 columns → 1 column (tablet_portrait: 1fr)
- Padding: 100px → 60px (mobile)

---

### **SECTION 3: FEATURES**

**Element Yapısı:**
```
section (bg: light gray #f9fafb, padding: 100px)
└─ container
   └─ grid (2 columns, gap: 80px)
      ├─ left-block (flex-column, gap: 20px)
      │  ├─ heading (H2: "Tüm Hukuki...")
      │  └─ text-basic (açıklama)
      └─ right-block (flex-column, gap: 20px)
         ├─ heading (H2: "Deneyimli Kadro...")
         └─ text-basic (açıklama)
```

**Settings:**
- Section: `bg: #f9fafb`, `padding: 100px top/bottom` (mobile: 60px)
- Grid: `2 columns` (tablet: 1 column), `gap: 80px` (mobile: 40px)
- H2: `36px` (mobile: 28px), `font-weight: 700`, `color: #1f2937`
- Text: `16px`, `line-height: 1.7`, `color: #6b7280`

**Responsive:**
- Grid: 2 columns → 1 column (tablet_portrait: 1fr)

---

### **SECTION 4: FAQ**

**Element Yapısı:**
```
section (bg: white, padding: 100px)
└─ container (max-width: 800px)
   └─ block (flex-column, center, gap: 40px)
      ├─ icon (question-circle, 48px, navy)
      ├─ tag-text ("SIK SORULAN SORULAR", 14px uppercase)
      ├─ heading (H2: "Sıkça Sorulan Sorular")
      ├─ faq-list (flex-column, gap: 16px)
      │  ├─ faq-item-1 (flex, justify-between, bg: light gray)
      │  │  ├─ text ("Soru 1...")
      │  │  └─ icon (chevron-right)
      │  ├─ faq-item-2
      │  ├─ faq-item-3
      │  ├─ faq-item-4
      │  └─ faq-item-5
      └─ button ("Tüm Sorular", navy)
```

**Settings:**
- Icon: `48px`, `navy #1e3a8a`
- Tag: `14px`, `font-weight: 600`, `uppercase`, `letter-spacing: 0.05em`, `gray #6b7280`
- H2: `42px` (mobile: 32px), `bold`, `dark #1f2937`, `margin-top: -20px`
- FAQ items: `bg: #f9fafb`, `padding: 20px 28px`, `radius: 12px`, `cursor: pointer`
- FAQ text: `16px`, `font-weight: 500`, `dark #1f2937`
- FAQ icon: `14px`, `gray #6b7280`
- Button: `bg: navy`, `padding: 14px 32px`, `radius: 25px`, `white text 15px bold`

---

### **SECTION 5: FOOTER**

**Element Yapısı:**
```
section (bg: #f9fafb, padding: 80px top / 40px bottom)
└─ container
   └─ footer-content (flex-column, gap: 60px)
      ├─ footer-top (grid 4 columns, gap: 40px)
      │  ├─ column-1 (HİZMETLER)
      │  │  ├─ title (H3, uppercase, 12px)
      │  │  ├─ link-1
      │  │  ├─ link-2
      │  │  └─ link-3
      │  ├─ column-2 (UZMANLIK)
      │  ├─ column-3 (KURUMSAL)
      │  └─ column-4 (CTA card)
      │     └─ card (white bg, padding: 28px 24px, radius: 12px)
      │        ├─ heading ("Hemen İletişime Geçin")
      │        ├─ text (açıklama)
      │        └─ button ("İletişim", navy, full-width)
      └─ footer-bottom (flex, justify-between, border-top)
         ├─ copyright-text
         └─ legal-links (flex, gap: 28px)
            ├─ link ("Kullanım Koşulları")
            └─ link ("Gizlilik Politikası")
```

**Settings:**
- Section: `bg: #f9fafb`, `padding: 80px top / 40px bottom` (mobile: 50px / 30px)
- Grid: `4 columns` (tablet: 2 columns, mobile: 1 column), `gap: 40px`
- Column title: `12px`, `bold`, `uppercase`, `letter-spacing: 0.05em`, `gray #6b7280`
- Links: `14px`, `regular`, `dark #1f2937`, hover: `navy`
- CTA card: `bg: white`, `padding: 28px 24px`, `radius: 12px`
- CTA title: `18px`, `bold`, `dark`
- CTA text: `14px`, `line-height: 1.6`, `gray`
- CTA button: `bg: navy`, `padding: 12px 24px`, `radius: 8px`, `full-width`, `white text`
- Footer bottom: `border-top: 1px solid #e5e7eb`, `padding-top: 28px`
- Copyright: `14px`, `gray #6b7280`

**Responsive:**
- Grid: 4 cols → 2 cols (tablet) → 1 col (mobile)
- Footer bottom: flex → column (mobile, gap: 16px)

---

## ✅ BUNU NASIL KULLANACAKSIN?

### **Örnek:**

```
[Screenshot at]

SECTION 1: HEADER

Element Yapısı:
section (sticky)
└─ container
   └─ block (flex, space-between)
      ├─ logo (icon 28px + text 22px bold)
      ├─ nav (3 links, 15px, gap: 40px)
      └─ button (navy bg, rounded 25px)

Settings:
- Section: sticky top:0, bg:white, padding:20px, shadow:soft
- Nav: gray #6b7280, hover:navy
- Button: bg:#1e3a8a, padding:12px 28px

Responsive:
- Mobile: nav gizli
```

**Sonuç:** Ben bundan perfect Bricks JSON üretirim!

---

## 🎯 NEDEN BU FORMAT?

✅ **Bricks yapısına uygun**: Element hierarchy (parent → child)
✅ **Settings detaylı**: Exact values (_background, _padding, _typography)
✅ **Responsive dahil**: Breakpoint'lerde değişenler
✅ **Kısa ama net**: Gereksiz detay yok, sadece Bricks JSON için gerekli bilgi

**Not:** Her section için bu formatı tekrarla. Ben bunları okuyup Bricks JSON settings'e çevireceğim.
