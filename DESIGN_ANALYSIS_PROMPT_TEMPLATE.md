# 🎨 TASARIM ANALİZİ PROMPT TEMPLATE

Bana screenshot gönderirken **bu formatı kullan**. Bu sayede birebir Bricks JSON üreteceğim.

---

## 📋 PROMPT FORMAT

```
GÖREV: [Screenshot'tan] Bricks Builder JSON oluştur

SEKTÖR: [Örn: Avukatlık, Medical, E-commerce, SaaS]
HEDEF KITLE: [Örn: B2B, B2C, Kurumsal, Bireysel]

---

## 1. LAYOUT STRUCTURE (ÖNEMLİ!)

**SECTIONS (Yukarıdan aşağıya):**
- [ ] Header
- [ ] Hero
- [ ] Features
- [ ] Testimonials
- [ ] FAQ
- [ ] Footer
- [ ] Diğer: _________

**HER SECTION İÇİN:**

### Header:
- Layout: [Flex/Grid]
- Columns: [3 bölüm: Logo | Nav Menu | Buttons]
- Position: [Static/Sticky/Fixed]
- Background: [Renk/Gradient/Transparent]
- Height: [Örn: 80px]

### Hero:
- Layout: [Split 2-column / Centered / Full-width]
- Background: [Solid color / Gradient / Image]
- Gradient Direction: [Top to bottom / Left to right]
- Content Alignment: [Center / Left]
- Height: [Full viewport / Auto]

### [Diğer Section'lar için tekrar et]

---

## 2. TYPOGRAPHY (DETAYLI!)

**Font Family:** [Örn: Inter, Poppins, Roboto]

**Hierarchy:**
- H1: [56px, Bold (700), Navy #1e3a8a]
- H2: [42px, Bold (700), Dark Gray #1f2937]
- H3: [28px, Semibold (600), Dark Gray #1f2937]
- H4: [22px, Semibold (600), Dark Gray #1f2937]
- Body: [16px, Regular (400), Gray #6b7280]
- Small: [14px, Regular (400), Gray #9ca3af]

**Line Height:**
- Headings: [1.2 - 1.3]
- Body: [1.6 - 1.7]

**Letter Spacing:**
- Normal / Wide (1-2px for uppercase)

---

## 3. COLOR PALETTE (EXACT HEX!)

**Primary Colors:**
- Main: #______ (Kullanım: Butonlar, CTA'lar)
- Secondary: #______ (Kullanım: Hover states)

**Accent Colors:**
- Accent 1: #______ (Kullanım: Icons, highlights)
- Accent 2: #______ (Kullanım: ________)

**Neutral Colors:**
- Dark: #______ (Heading text)
- Gray: #______ (Body text)
- Light Gray: #______ (Borders, backgrounds)
- White: #ffffff

**Gradients:**
- Hero BG: [#______ → #______ at 180deg]
- Section BG: [Solid / Gradient]

---

## 4. SPACING SYSTEM (ÇOK ÖNEMLİ!)

**Section Padding:**
- Desktop: [Top: 100px, Bottom: 100px]
- Tablet: [Top: 60px, Bottom: 60px]
- Mobile: [Top: 40px, Bottom: 40px]

**Container:**
- Max Width: [1200px / 1400px]
- Side Padding: [15px / 20px]

**Element Spacing:**
- Gap between cards: [24px / 32px]
- Gap between sections: [80px / 100px]
- Row gap in text: [16px / 20px]

**Card Padding:**
- Inner padding: [Top: 32px, Bottom: 32px, Left: 28px, Right: 28px]

---

## 5. BORDERS & SHADOWS

**Border Radius:**
- Buttons: [25px (fully rounded) / 8px (slightly rounded)]
- Cards: [16px / 12px / 8px]
- Images: [8px / 12px]

**Box Shadow:**
- Cards: [0 4px 20px rgba(0,0,0,0.08)] - Soft
- Hover: [0 8px 30px rgba(0,0,0,0.12)] - Elevated
- Header: [0 2px 10px rgba(0,0,0,0.04)] - Subtle

**Border:**
- Color: [#e5e7eb]
- Width: [1px]

---

## 6. RESPONSIVE BREAKPOINTS

**Desktop (1200px+):**
- Grid: [3 columns]
- Hero: [2 columns split]

**Tablet (768px - 1199px):**
- Grid: [2 columns]
- Hero: [2 columns → 1 column]

**Mobile (< 767px):**
- Grid: [1 column stacked]
- Hero: [1 column]
- Nav: [Hidden, hamburger menu]

**Değişen Değerler:**
- Font sizes: [H1: 56px → 36px]
- Padding: [100px → 60px → 40px]
- Gap: [32px → 24px → 16px]

---

## 7. ELEMENTS DETAYLI

### Buttons:
- **Primary:**
  - BG: #______, Hover: #______
  - Text: #______, Size: 15px, Weight: 600
  - Padding: [12px 28px]
  - Radius: [25px]
  - Shadow: [Evet/Hayır]

- **Secondary:**
  - Border: [2px solid #______]
  - BG: Transparent
  - Hover: [BG: #______, Text: White]

### Cards:
- Background: [White / Light gray]
- Shadow: [0 4px 20px rgba(0,0,0,0.08)]
- Radius: [16px]
- Padding: [32px 28px]
- Hover effect: [Scale 1.05 / Shadow increase / None]

### Icons:
- Size: [24px / 36px / 48px]
- Color: [#______ (accent color)]
- Background: [Circle with BG / None]
- Icon library: [FontAwesome Solid / Outline]

---

## 8. SPECIFIC ELEMENTS

**Nav Menu:**
- Items: [Link 1, Link 2, Link 3]
- Font size: [15px]
- Weight: [500]
- Color: #______, Hover: #______
- Gap between items: [40px / 32px]

**Hero Section:**
- Badge: [Evet/Hayır]
  - Text: "_________"
  - BG: [Semi-transparent white / Color]
  - Padding: [8px 20px]
  - Radius: [20px]

- Main Heading: "_________"
- Subheading: "_________"

- CTA Buttons:
  - Primary: "___________"
  - Secondary: "___________"

**Cards (Features/Services):**
- Count: [3 / 4 / 6]
- Grid: [3 columns]
- Icon position: [Top / Left]
- Icon size: [36px / 48px]
- Title size: [22px]
- Description size: [15px]

**FAQ:**
- Icon: [Evet/Hayır] - [Question circle / Chevron]
- Layout: [Accordion / List]
- Background: [Light gray / White]
- Border: [Evet/Hayır]

---

## 9. CONTENT (Türkçe)

**Sektöre Uyarlanmış İçerik:**

### Header:
- Logo Text: "_________"
- Nav Item 1: "_________"
- Nav Item 2: "_________"
- Nav Item 3: "_________"
- CTA Button: "_________"

### Hero:
- Badge (varsa): "_________"
- Main Heading: "_________"
- Subheading: "_________"
- Primary CTA: "_________"
- Secondary CTA (varsa): "_________"

### [Her section için içerik belirt]

---

## 10. ÖZEL NOTLAR

- [ ] Glassmorphism efekti var mı? (backdrop-blur)
- [ ] Animasyonlar var mı? (Fade in, Slide up, vs.)
- [ ] Custom shapes/dividers var mı?
- [ ] Background patterns var mı?
- [ ] Sticky header mi?
- [ ] Scroll effects var mı?

**Özel İstekler:**
[Buraya ekstra notlarını yaz]

---

## ✅ ÇIKTI BEKLENTİSİ

Yukarıdaki bilgilerle:
1. **Tam Bricks JSON** (copy-paste ready)
2. **Theme Style ID'leri kullan** (navy-primary, gold-accent vs.)
3. **Responsive breakpoints** ekle
4. **Her element ID'si unique** olsun
5. **Parent-child hierarchy doğru** olsun
```

---

## 📸 SCREENSHOT GÖNDERİRKEN:

**Örnek Kullanım:**

```
GÖREV: FeedSpring one-page sitesinden Bricks JSON oluştur

SEKTÖR: Avukatlık
HEDEF KITLE: B2B (Kurumsal müşteriler)

---

## 1. LAYOUT STRUCTURE

**SECTIONS:**
- [x] Header (sticky)
- [x] Hero (full-width centered)
- [x] Features (2-column grid, 2 sections)
- [x] FAQ (centered, accordion)
- [x] Footer (4-column + CTA card)

### Header:
- Layout: Flex (3 bölüm: Logo | Nav | Buttons)
- Columns: Logo (left) | Nav 3 items (center) | 2 buttons (right)
- Position: Sticky (top: 0)
- Background: White (#ffffff)
- Shadow: 0 2px 10px rgba(0,0,0,0.04)
- Height: 70px

### Hero:
- Layout: Centered, full-width
- Background: Gradient (top to bottom, #5B9FED → #8AB4F8)
- Content Alignment: Center
- Height: Auto
- Contains:
  - Badge (semi-transparent white)
  - Large heading (56px white)
  - Subheading (18px white)
  - 3 platform badges (horizontal flex)
  - 3 white cards (3-column grid)

[... devamı]
```

---

## 🎯 BU FORMAT NEDEN EN İYİSİ?

✅ **Structured**: Her detay kategorize edilmiş
✅ **Complete**: Hiçbir detay atlanmaz
✅ **Pixel-perfect**: Exact değerler isteniyor
✅ **Responsive**: Breakpoint'ler dahil
✅ **Bricks-specific**: Element hierarchy, ID'ler, settings formatı

**Kullanımı:**
1. Screenshot'ı çek
2. Template'i kopyala
3. Değerleri doldur
4. Bana gönder
5. Perfect JSON al!
