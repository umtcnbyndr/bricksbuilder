# BRICKS ELEMENT REFERANSI

## LAYOUT ELEMENTS

### section
```json
{
  "name": "section",
  "settings": {
    "tag": "section|header|footer|main|aside|article|nav|div",
    "_width": "100%",
    "_height": "auto|100vh",
    "_minHeight": "value",
    "_padding": {},
    "_background": {},
    "_display": "block|flex|grid"
  }
}
```

### container
```json
{
  "name": "container",
  "settings": {
    "tag": "div|section|article|nav|header|footer|aside|a",
    "_width": "90%",
    "_widthMax": "85.375rem",
    "_display": "flex|grid|block",
    "_direction": "row|column",
    "_justifyContent": "flex-start|center|flex-end|space-between|space-around",
    "_alignItems": "flex-start|center|flex-end|stretch",
    "_columnGap": "var(--spacing-md)",
    "_rowGap": "var(--spacing-md)",
    "_flexWrap": "nowrap|wrap",
    "_gridTemplateColumns": "repeat(3, 1fr)",
    "_gridGap": "var(--spacing-md)"
  }
}
```

### block
```json
{
  "name": "block",
  "settings": {
    "tag": "div",
    "_width": "100%"
  }
}
```
**Not:** Container gibi ama default width %100

### div
```json
{
  "name": "div",
  "settings": {
    "tag": "div|span|a"
  }
}
```
**Not:** İçeriği kadar yer kaplar

---

## CONTENT ELEMENTS

### heading
```json
{
  "name": "heading",
  "settings": {
    "text": "Başlık metni",
    "tag": "h1|h2|h3|h4|h5|h6|div|span",
    "link": {
      "type": "internal|external",
      "url": "..."
    },
    "_typography": {}
  }
}
```
**SEO:** Sayfa başına 1 H1!

### text
```json
{
  "name": "text",
  "settings": {
    "text": "<p>HTML içerik</p>",
    "_typography": {}
  }
}
```
**Not:** Rich text, HTML destekli

### text-basic
```json
{
  "name": "text-basic",
  "settings": {
    "text": "Basit metin",
    "tag": "span|p|div",
    "_typography": {}
  }
}
```
**Not:** Inline metin için

### button
```json
{
  "name": "button",
  "settings": {
    "text": "Button Text",
    "link": {
      "type": "internal|external",
      "url": "/contact/",
      "newTab": true,
      "rel": "noopener noreferrer"
    },
    "size": "sm|md|lg",
    "style": "primary|secondary|outline|ghost",
    "icon": {
      "library": "themify|fontawesome",
      "icon": "ti-arrow-right"
    },
    "iconPosition": "left|right",
    "_padding": {},
    "_background": {},
    "_typography": {},
    "_border": {}
  }
}
```

### image
```json
{
  "name": "image",
  "settings": {
    "image": {
      "url": "https://...",
      "id": 123,
      "alt": "Açıklayıcı metin",
      "external": true
    },
    "_width": "100%",
    "_height": "auto",
    "_objectFit": "cover|contain|fill",
    "_aspectRatio": "16/9|4/3|1/1",
    "_border": {}
  }
}
```
**SEO:** Alt text ZORUNLU!

### icon
```json
{
  "name": "icon",
  "settings": {
    "icon": {
      "library": "themify|fontawesome|ionicons",
      "icon": "ti-check"
    },
    "_width": "2rem",
    "_height": "2rem",
    "_typography": {
      "color": {}
    }
  }
}
```

### video
```json
{
  "name": "video",
  "settings": {
    "videoType": "youtube|vimeo|file",
    "youtubeId": "VIDEO_ID",
    "vimeoId": "VIDEO_ID",
    "fileUrl": "...",
    "overlay": true,
    "playIcon": {}
  }
}
```

---

## NAVIGATION

### nav-menu
```json
{
  "name": "nav-menu",
  "settings": {
    "menu": "primary|menu_id",
    "menuTypography": {
      "font-family": "Inter",
      "font-size": "var(--text-base)",
      "font-weight": "500",
      "color": {}
    },
    "menuTypography_hover": {},
    "mobileMenu": "tablet_portrait|mobile_portrait",
    "mobileMenuPosition": "left|right",
    "mobileMenuToggleColor": {}
  }
}
```

### logo
```json
{
  "name": "logo",
  "settings": {
    "logo": {
      "id": 123,
      "url": "..."
    },
    "logoText": "Brand Name",
    "link": { "url": "/" },
    "_typography": {}
  }
}
```

---

## FORM

### form
```json
{
  "name": "form",
  "settings": {
    "fields": [
      {
        "type": "text|email|tel|textarea|select|checkbox|radio",
        "label": "Alan Adı",
        "placeholder": "...",
        "required": true,
        "id": "field_id"
      }
    ],
    "submitButtonText": "Gönder",
    "successMessage": "Teşekkürler!",
    "actions": ["email"],
    "emailTo": "info@example.com"
  }
}
```

---

## COMMON SETTINGS

### _typography
```json
{
  "_typography": {
    "font-family": "Inter",
    "font-size": "var(--text-base)",
    "font-weight": "400|500|600|700|800",
    "font-style": "normal|italic",
    "line-height": "1.5",
    "letter-spacing": "0.05em",
    "text-transform": "none|uppercase|lowercase|capitalize",
    "text-align": "left|center|right",
    "text-decoration": "none|underline",
    "color": {
      "raw": "var(--color-secondary)"
    }
  }
}
```

### _background
```json
{
  "_background": {
    "color": {
      "raw": "var(--color-primary)",
      "hex": "#3b82f6"
    },
    "image": {
      "url": "...",
      "size": "cover|contain",
      "position": "center",
      "repeat": "no-repeat"
    },
    "gradient": {
      "type": "linear|radial",
      "angle": "180",
      "stops": [
        { "color": { "hex": "#fff" }, "position": "0" },
        { "color": { "hex": "#f8fafc" }, "position": "100" }
      ]
    }
  }
}
```

### _padding / _margin
```json
{
  "_padding": {
    "top": "var(--spacing-lg)",
    "right": "var(--spacing-md)",
    "bottom": "var(--spacing-lg)",
    "left": "var(--spacing-md)"
  }
}
```

### _border
```json
{
  "_border": {
    "width": {
      "top": "1",
      "right": "1",
      "bottom": "1",
      "left": "1"
    },
    "style": "solid|dashed|dotted",
    "color": {
      "hex": "#e5e7eb"
    },
    "radius": {
      "top": "var(--radius-lg)",
      "right": "var(--radius-lg)",
      "bottom": "var(--radius-lg)",
      "left": "var(--radius-lg)"
    }
  }
}
```

### _boxShadow
```json
{
  "_boxShadow": {
    "values": {
      "offsetX": "0",
      "offsetY": "4",
      "blur": "16",
      "spread": "0"
    },
    "color": {
      "rgb": "rgba(0, 0, 0, 0.08)"
    }
  }
}
```

### _hover states
```json
{
  "_background_hover": {},
  "_typography_hover": {},
  "_transform_hover": {
    "translateY": "-4px"
  },
  "_boxShadow_hover": {}
}
```

### _cssGlobalClasses
```json
{
  "_cssGlobalClasses": ["class-id-1", "class-id-2"]
}
```

### _attributes (ARIA/Custom)
```json
{
  "_attributes": {
    "role": "banner",
    "aria-label": "Ana menü",
    "data-custom": "value"
  }
}
```

### _cssTransition
```json
{
  "_cssTransition": "all 200ms ease"
}
```

---

## RESPONSIVE SUFFIX

Property'lerin sonuna ekle:

```json
{
  "_direction": "row",
  "_direction:tablet_portrait": "column",
  "_direction:mobile_portrait": "column",
  
  "_display": "flex",
  "_display:mobile_portrait": "none",
  
  "_gridTemplateColumns": "repeat(3, 1fr)",
  "_gridTemplateColumns:tablet_portrait": "repeat(2, 1fr)",
  "_gridTemplateColumns:mobile_portrait": "1fr"
}
```

| Breakpoint | Suffix | Genişlik |
|------------|--------|----------|
| Desktop | (yok) | 1200px+ |
| Tablet | `:tablet_portrait` | 768-1199px |
| Mobile | `:mobile_portrait` | 0-767px |
