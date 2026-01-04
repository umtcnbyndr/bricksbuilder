# ⚡ BASIT TASARIM AÇIKLAMA FORMATI

Screenshot atarken **bu kısa formatı** kullan. Sadece gerekli bilgileri yaz.

---

## 📸 SCREENSHOT + AÇIKLAMA

```
[Screenshot'ı at]

Ardından kısa kısa yaz:
```

---

## ✅ CHECKLIST FORMATI

### **1. LAYOUT**

```
□ Kaç section var? Header, Hero, Features, FAQ, Footer
□ Her section'da kaç sütun? 1 / 2 / 3 / 4
□ Layout tipi? Flex / Grid
□ Hizalama? Center / Left / Space-between
```

**Örnek:**
```
✓ Header: 1 satır, 3 bölüm (Logo | Nav | Button), flex, space-between
✓ Hero: 1 sütun, center, gradient arka plan
✓ Hero içinde: 3 beyaz kart, grid 3 sütun
✓ Features: 2 sütun, grid
✓ FAQ: 1 sütun, center
✓ Footer: 4 sütun, grid
```

---

### **2. RENKLER**

```
□ Ana renk (primary)?
□ Vurgu rengi (accent)?
□ Başlık rengi?
□ Metin rengi?
□ Arka plan rengi?
□ Gradient var mı? (Hangi renkler, hangi yön?)
```

**Örnek:**
```
✓ Primary: Lacivert #1e3a8a (butonlar, logoda)
✓ Accent: Altın #d4af37 (iconlarda)
✓ Başlık: Koyu gri #1f2937
✓ Metin: Gri #6b7280
✓ Hero gradient: #1e3a8a → #3b82f6 (yukarıdan aşağı)
```

---

### **3. TYPOGRAPHY**

```
□ Ana başlık (H1) kaç px? Bold mu?
□ Alt başlıklar (H2, H3) kaç px?
□ Normal metin kaç px?
□ Font family? (Inter, Poppins, etc.)
```

**Örnek:**
```
✓ H1: 56px, bold, beyaz (hero'da)
✓ H2: 36px, bold, koyu gri
✓ H3: 22px, bold, lacivert (kartlarda)
✓ Metin: 16px, regular, gri
✓ Font: Inter
```

---

### **4. SPACING**

```
□ Section arası boşluk? (padding top/bottom)
□ Kartlar arası boşluk? (gap)
□ Kart içi boşluk? (padding)
```

**Örnek:**
```
✓ Section padding: 100px üst/alt (mobilde 60px)
✓ Kart gap: 24px
✓ Kart padding: 32px (içten)
```

---

### **5. STIL DETAYLARI**

```
□ Border radius? (Kaç px yuvarlaklık?)
□ Shadow var mı? (Soft / Hard / None?)
□ Button stili? (Rounded / Square?)
```

**Örnek:**
```
✓ Button radius: 25px (tam yuvarlak)
✓ Kart radius: 16px
✓ Kart shadow: 0 4px 20px rgba(0,0,0,0.08) - soft
```

---

### **6. İÇERİK**

```
□ Header'da ne yazıyor?
□ Hero başlığı ne?
□ Buton yazıları ne?
□ Kaç adet kart/item var?
```

**Örnek:**
```
✓ Logo: "Kaya Hukuk"
✓ Nav: Hizmetlerimiz, Uzmanlık Alanları, İletişim
✓ Hero başlık: "Hukuki Haklarınızı Profesyonelce Koruyoruz"
✓ Button: "Ücretsiz Danışma"
✓ 3 hizmet kartı: Ticaret, Gayrimenkul, Aile Hukuku
```

---

### **7. RESPONSIVE**

```
□ Mobilde ne değişiyor?
□ Grid sütun sayısı değişiyor mu? 3 → 1?
□ Nav menü gizleniyor mu?
□ Font size küçülüyor mu?
```

**Örnek:**
```
✓ Mobile: 3 sütun → 1 sütun
✓ Nav gizli (hamburger menü)
✓ H1: 56px → 36px
✓ Padding: 100px → 60px
```

---

## 🎯 KULLANIM ÖRNEĞİ

```
[Screenshot at: FeedSpring homepage]

## 1. LAYOUT
✓ Header: 1 satır, Logo + Nav (3 link) + 2 Button, sticky
✓ Hero: Tam genişlik, center, gradient bg, içinde badge + başlık + 3 badge + 3 kart
✓ Features: 2 sütun, grid, açık gri bg
✓ FAQ: 1 sütun, center, 5 accordion
✓ Footer: 4 sütun + copyright

## 2. RENKLER
✓ Primary: Mavi #5B9FED
✓ Gradient: #5B9FED → #8AB4F8 (hero arka plan)
✓ Başlık: Koyu #1f2937
✓ Metin: Gri #6b7280

## 3. TYPOGRAPHY
✓ H1: 56px, bold, beyaz
✓ H2: 36px, bold
✓ Metin: 18px hero alt yazı, 16px normal
✓ Font: Inter

## 4. SPACING
✓ Section: 100px padding (mobile: 60px)
✓ Kart gap: 24px
✓ Kart padding: 32px 28px

## 5. STIL
✓ Button radius: 25px
✓ Kart radius: 16px
✓ Shadow: 0 4px 20px soft

## 6. İÇERİK
✓ Logo: FeedSpring
✓ Nav: Product, Resources, Pricing
✓ Buttons: Sign In, Start for free
✓ Hero: "Add beautiful social media feeds to any website"
✓ 3 kart: Instagram post, Review, Instagram feed

## 7. RESPONSIVE
✓ Mobile: Nav gizli, 3 kart → 1 kart, H1: 36px
```

**Sonuç:** Bu bilgilerle perfect Bricks JSON üretirim!

---

## 💡 İPUÇLARI

**Renkleri nasıl öğrenebilirsin?**
- Browser'da F12 → Elements → Computed → background-color
- Veya screenshot'tan color picker kullan

**Font size nasıl?**
- F12 → Elements → font-size değerine bak
- Veya tahmini söyle (56px, 36px gibi)

**Padding/Gap nasıl?**
- F12 → Layout sekmesi → margin/padding değerleri
- Veya göz kararı: "büyük boşluk (100px)", "orta (60px)", "küçük (24px)"

**Hepsini bilmene gerek yok!**
- Bilmediğin değerleri atla
- Ben Bricks standartlarına göre tamamlarım
- Sadece gördüğün şeyleri yaz

---

## ✅ ÖZETİ

**KISA FORMAT:**
1. Screenshot at
2. Layout (kaç sütun, flex/grid)
3. Renkler (#hex kodları)
4. Font sizes (56px, 36px, 16px)
5. Spacing (100px padding, 24px gap)
6. Stil (16px radius, soft shadow)
7. İçerik (başlıklar, button yazıları)
8. Responsive (mobilde ne değişiyor)

**Bu kadar!** Ben bu bilgilerle Bricks JSON üreteceğim.
