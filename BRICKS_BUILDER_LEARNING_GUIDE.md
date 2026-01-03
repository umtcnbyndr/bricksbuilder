# Bricks Builder JSON Yapısı - Öğrenme Kılavuzu

## 📋 Temel Yapı

Tüm Bricks Builder template'leri şu yapıdadır:

```json
{
  "id": "unique-id",
  "name": "template-name",
  "title": "Template Title",
  "type": "section",
  "content": [...],           // Element dizisi
  "source": "bricksCopiedElements",
  "version": "1.12.3",
  "globalClasses": [...],     // Global CSS class'lar
  "globalElements": []
}
```

---

## 🧱 Element Yapısı

Her element şu özelliklere sahiptir:

### Temel Özellikler
```json
{
  "id": "abc123",             // Benzersiz 6 karakterlik ID
  "name": "container",        // Element tipi
  "parent": "xyz789",         // Parent element ID (0 = root)
  "children": ["def456"],     // Child element ID'leri
  "settings": {...},          // Tüm stil ve ayarlar
  "label": "Optional Label"   // Opsiyonel etiket
}
```

---

## 🎨 Element Tipleri

### 1. Layout Elements

#### `section`
- En üst seviye container
- Genelde root element (parent: 0)
- Padding/background için kullanılır

#### `container`
- Flexbox container
- Direction: row/column
- Alignment, gap ayarları

#### `block`
- Basit container
- Column yapısında kullanılır

### 2. Content Elements

#### `heading`
```json
{
  "name": "heading",
  "settings": {
    "text": "Başlık metni",
    "tag": "h1",  // h1-h6
    "_typography": {...}
  }
}
```

#### `text`
```json
{
  "name": "text",
  "settings": {
    "text": "<p>HTML formatında metin</p>",
    "_typography": {...}
  }
}
```

#### `text-basic`
```json
{
  "name": "text-basic",
  "settings": {
    "text": "Düz metin",
    "tag": "span"  // veya div, p
  }
}
```

#### `button`
```json
{
  "name": "button",
  "settings": {
    "text": "Button Text",
    "circle": true,          // Rounded corners
    "size": "lg",            // sm, md, lg
    "_background": {...},
    "_typography": {...},
    "_transform_hover": {    // Hover efekti
      "translateY": "-3px"
    }
  }
}
```

#### `image`
```json
{
  "name": "image",
  "settings": {
    "image": {
      "url": "https://...",
      "external": true,
      "filename": "image.jpg"
    },
    "_objectFit": "cover"
  }
}
```

### 3. Interactive Elements

#### `form`
```json
{
  "name": "form",
  "settings": {
    "fields": [
      {
        "type": "text",         // text, email, textarea
        "label": "Name",
        "placeholder": "Your name",
        "required": true,
        "id": "unique_id",
        "width": "100"
      }
    ],
    "actions": ["email"],
    "successMessage": "...",
    "emailTo": "admin_email",
    "submitButtonText": "Submit"
  }
}
```

#### `list`
```json
{
  "name": "list",
  "settings": {
    "items": [
      {
        "title": "Item text",
        "id": "unique_id",
        "icon": {
          "library": "fontawesomeSolid",
          "icon": "fas fa-check"
        },
        "link": {
          "type": "external",
          "newTab": true
        }
      }
    ],
    "separatorDisable": true
  }
}
```

#### `divider`
```json
{
  "name": "divider",
  "settings": {
    "color": {
      "raw": "var(--color-secondary)"
    }
  }
}
```

---

## 🎯 Settings Pattern'leri

### Typography
```json
"_typography": {
  "font-size": "16px",
  "font-family": "Inter",
  "font-weight": "600",
  "color": {
    "hex": "#3B82F6",
    "id": "primary-blue"
  },
  "text-transform": "uppercase",
  "letter-spacing": "1px",
  "line-height": "1.1em",
  "text-align": "center"
}
```

### Background
```json
"_background": {
  "color": {
    "hex": "#ffffff",
    "id": "white-bg"
  }
}
```

### Spacing
```json
"_margin": {
  "top": "20",
  "bottom": "20",
  "left": "0",
  "right": "0"
},
"_padding": {
  "top": "80",
  "bottom": "80",
  "left": "15",
  "right": "15"
}
```

### Sizing
```json
"_width": "100%",
"_widthMax": "1366",
"_height": "auto",
"_minHeight": "80vh"
```

### Flexbox
```json
"_direction": "row",              // row, column
"_justifyContent": "center",      // flex-start, center, flex-end, space-between
"_alignItems": "center",          // flex-start, center, flex-end
"_alignSelf": "center",
"_columnGap": "var(--spacing-lg)",
"_rowGap": "var(--spacing-lg)"
```

### Border
```json
"_border": {
  "width": {
    "top": "1",
    "right": "1",
    "bottom": "1",
    "left": "1"
  },
  "style": "solid",
  "color": {
    "raw": "var(--color-secondary)"
  }
}
```

### Box Shadow
```json
"_boxShadow": {
  "values": {
    "offsetX": "0",
    "offsetY": "4",
    "blur": "16"
  },
  "color": {
    "hex": "#000000",
    "rgb": "rgba(0, 0, 0, 0.06)"
  }
}
```

---

## 📱 Responsive Breakpoints

### Suffix Pattern
```
_property:breakpoint
```

### Breakpoint'ler
- `:tablet_portrait` - Tablet
- `:mobile_landscape` - Mobile yatay
- `:mobile_portrait` - Mobile dikey

### Örnekler
```json
{
  "_direction": "row",
  "_direction:tablet_portrait": "column",
  "_width": "800px",
  "_width_mobile_portrait": "100%",
  "_typography": {
    "font-size": "64px"
  },
  "_typography_mobile_landscape": {
    "font-size": "42px"
  }
}
```

---

## 🎨 Global Classes

### Yapı
```json
{
  "id": "jkkjia",
  "name": "ren-pad-top-bottom-lg",
  "settings": {
    "_padding": {
      "bottom": "var(--spacing-lg)",
      "top": "var(--spacing-lg)"
    }
  },
  "modified": 1739690341,
  "user_id": 1
}
```

### Kullanım
```json
{
  "settings": {
    "_cssGlobalClasses": [
      "jkkjia",
      "duychn"
    ]
  }
}
```

### Yaygın Global Classes
- `ren-container-width-lg` - Max width 1366px
- `ren-pad-top-bottom-lg` - Top/bottom padding
- `ren-gap-lg` - Large gap
- `ren-text-secondary` - Secondary color
- `ren-heading-2` - H2 style

---

## 🔧 Hover & Interaction States

### Hover Efektleri
```json
"_transform_hover": {
  "translateY": "-3px"
},
"_boxShadow_hover": {
  "values": {
    "offsetY": "5",
    "blur": "10"
  },
  "color": {
    "hex": "#3B82F6",
    "rgb": "rgba(59, 130, 246, 0.4)"
  }
}
```

### Transitions
```json
"_cssTransition": "all 0.2s ease-in-out"
```

---

## 🏗️ ID Generation Pattern

Element ID'leri 6 karakterlik rastgele stringlerdir:
- `zvmfva`, `wzwdwl`, `ypyjef`, `qrdsta`
- Lowercase harfler
- Tekrarsız olmalı

Basit generator:
```javascript
function generateId() {
  return Math.random().toString(36).substring(2, 8);
}
```

---

## 🧩 Hierarchical Structure (Parent-Child İlişkisi)

### Örnek Yapı
```
section (parent: 0)
  └── container (parent: section_id)
      ├── block (parent: container_id)
      │   ├── heading (parent: block_id)
      │   └── text (parent: block_id)
      └── block (parent: container_id)
          └── image (parent: block_id)
```

### JSON Gösterimi
```json
[
  {
    "id": "sec1",
    "name": "section",
    "parent": 0,
    "children": ["cont1"]
  },
  {
    "id": "cont1",
    "name": "container",
    "parent": "sec1",
    "children": ["blk1", "blk2"]
  },
  {
    "id": "blk1",
    "name": "block",
    "parent": "cont1",
    "children": ["head1", "txt1"]
  },
  {
    "id": "head1",
    "name": "heading",
    "parent": "blk1",
    "children": []
  }
]
```

---

## 📐 Yaygın Layout Pattern'leri

### 1. Two Column Layout
```json
{
  "name": "container",
  "settings": {
    "_direction": "row",
    "_direction:tablet_portrait": "column"
  },
  "children": ["block1", "block2"]
}
```

### 2. Centered Hero Section
```json
{
  "name": "container",
  "settings": {
    "_minHeight": "80vh",
    "_justifyContent": "center",
    "_alignItems": "center",
    "_direction": "column",
    "_textAlign": "center"
  }
}
```

### 3. Card/Box Component
```json
{
  "name": "block",
  "settings": {
    "_padding": {
      "left": "var(--spacing-sm)",
      "top": "var(--spacing-sm)",
      "right": "var(--spacing-sm)",
      "bottom": "var(--spacing-sm)"
    },
    "_border": {
      "width": {"top": "1", "right": "1", "bottom": "1", "left": "1"},
      "style": "solid"
    }
  }
}
```

---

## 🎨 CSS Variables

Yaygın kullanılan CSS variables:

### Spacing
- `var(--spacing-xs)` - Extra small
- `var(--spacing-sm)` - Small
- `var(--spacing-md)` - Medium
- `var(--spacing-lg)` - Large

### Typography
- `var(--text-xs)` - Extra small
- `var(--text-sm)` - Small
- `var(--text-md)` - Medium
- `var(--text-lg)` - Large
- `var(--text-xl)` - Extra large
- `var(--text-2xl)` - 2X large

### Colors
- `var(--color-primary)` - Primary color
- `var(--color-secondary)` - Secondary color
- `var(--color-tertiary)` - Tertiary color
- `var(--color-accent)` - Accent color
- `var(--color-light)` - Light color

---

## ✅ Template Oluşturma Checklist

1. **Root metadata** oluştur (id, name, title, type)
2. **Section element** ekle (parent: 0)
3. **Container hierarchy** oluştur
4. **Content elements** ekle (heading, text, button, etc.)
5. **Settings** tanımla (typography, spacing, etc.)
6. **Responsive breakpoints** ekle
7. **Global classes** tanımla (opsiyonel)
8. **Hover states** ekle (opsiyonel)
9. **Parent-child ilişkilerini** kontrol et
10. **Unique ID'leri** kontrol et

---

## 🚀 İleri Seviye Özellikler

### Icon Libraries
- `fontawesomeSolid` - Font Awesome Solid
- `themify` - Themify Icons
- `ionicons` - Ionicons

### Form Actions
- `email` - Email gönder
- `redirect` - Yönlendir
- `mailchimp` - Mailchimp entegrasyonu

### Link Types
- `internal` - WordPress internal link
- `external` - External URL
- `media` - Media file

---

## 💡 Best Practices

1. **CSS Variables kullan** - Hard-coded değerler yerine
2. **Global classes kullan** - Tekrar eden stiller için
3. **Responsive breakpoints ekle** - Mobile-first yaklaşım
4. **Semantic HTML kullan** - Doğru heading tags (h1-h6)
5. **Accessible forms** - Label ve placeholder kullan
6. **Optimized images** - External URL veya local
7. **Transition effects** - Smooth hover states
