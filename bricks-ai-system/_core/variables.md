# CSS VARIABLES

## Kullanım
```json
{ "font-size": "var(--text-xl)" }
{ "color": { "raw": "var(--color-primary)" } }
{ "padding": { "top": "var(--spacing-lg)" } }
```

---

## COLORS

| Variable | Default | Kullanım |
|----------|---------|----------|
| `--color-primary` | #3b82f6 | CTA, linkler, vurgular |
| `--color-secondary` | #1f2937 | Başlıklar, ana text |
| `--color-tertiary` | #6b7280 | Açıklamalar, alt text |
| `--color-accent` | #10b981 | Başarı, özel vurgular |
| `--color-light` | #f8fafc | Açık arkaplan |
| `--color-dark` | #111827 | Koyu arkaplan |
| `--color-white` | #ffffff | Beyaz |
| `--color-error` | #ef4444 | Hata |
| `--color-success` | #22c55e | Başarı |
| `--color-warning` | #f59e0b | Uyarı |

---

## SPACING

| Variable | Değer | Pixel |
|----------|-------|-------|
| `--spacing-3xs` | 0.25rem | 4px |
| `--spacing-2xs` | 0.5rem | 8px |
| `--spacing-xs` | 0.75rem | 12px |
| `--spacing-sm` | 1rem | 16px |
| `--spacing-md` | 1.5rem | 24px |
| `--spacing-lg` | 2.5rem | 40px |
| `--spacing-xl` | 4rem | 64px |
| `--spacing-2xl` | 6rem | 96px |
| `--spacing-3xl` | 8rem | 128px |

**Kullanım Önerileri:**
- Section padding: `--spacing-2xl`
- Container gap: `--spacing-lg`
- Element gap: `--spacing-md`
- İç padding: `--spacing-sm` - `--spacing-md`

---

## TYPOGRAPHY

| Variable | Değer | Pixel |
|----------|-------|-------|
| `--text-2xs` | 0.625rem | 10px |
| `--text-xs` | 0.75rem | 12px |
| `--text-sm` | 0.875rem | 14px |
| `--text-base` | 1rem | 16px |
| `--text-md` | 1.125rem | 18px |
| `--text-lg` | 1.25rem | 20px |
| `--text-xl` | 1.5rem | 24px |
| `--text-2xl` | 2rem | 32px |
| `--text-3xl` | 2.5rem | 40px |
| `--text-4xl` | 3rem | 48px |
| `--text-5xl` | 3.5rem | 56px |

**Kullanım Önerileri:**
- H1: `--text-5xl` (mobile: `--text-3xl`)
- H2: `--text-4xl` (mobile: `--text-2xl`)
- H3: `--text-2xl`
- Body: `--text-base`
- Small: `--text-sm`

**Not:** Body text minimum 16px (--text-base)!

---

## RADIUS

| Variable | Değer | Pixel |
|----------|-------|-------|
| `--radius-sm` | 0.25rem | 4px |
| `--radius-md` | 0.5rem | 8px |
| `--radius-lg` | 0.75rem | 12px |
| `--radius-xl` | 1rem | 16px |
| `--radius-2xl` | 1.5rem | 24px |
| `--radius-full` | 9999px | Pill/Circle |

---

## BRICKS'E IMPORT

Theme Styles'a eklenecek CSS:

```css
:root {
  /* Colors */
  --color-primary: #3b82f6;
  --color-secondary: #1f2937;
  --color-tertiary: #6b7280;
  --color-accent: #10b981;
  --color-light: #f8fafc;
  --color-dark: #111827;
  --color-white: #ffffff;
  --color-error: #ef4444;
  --color-success: #22c55e;
  --color-warning: #f59e0b;
  
  /* Spacing */
  --spacing-3xs: 0.25rem;
  --spacing-2xs: 0.5rem;
  --spacing-xs: 0.75rem;
  --spacing-sm: 1rem;
  --spacing-md: 1.5rem;
  --spacing-lg: 2.5rem;
  --spacing-xl: 4rem;
  --spacing-2xl: 6rem;
  --spacing-3xl: 8rem;
  
  /* Typography */
  --text-2xs: 0.625rem;
  --text-xs: 0.75rem;
  --text-sm: 0.875rem;
  --text-base: 1rem;
  --text-md: 1.125rem;
  --text-lg: 1.25rem;
  --text-xl: 1.5rem;
  --text-2xl: 2rem;
  --text-3xl: 2.5rem;
  --text-4xl: 3rem;
  --text-5xl: 3.5rem;
  
  /* Radius */
  --radius-sm: 0.25rem;
  --radius-md: 0.5rem;
  --radius-lg: 0.75rem;
  --radius-xl: 1rem;
  --radius-2xl: 1.5rem;
  --radius-full: 9999px;
}
```

---

## PROJE BAZLI OVERRIDE

Her projede farklı renkler kullanılabilir:

```json
// _projects/dis-klinigi/config.json
{
  "colors": {
    "primary": "#0ea5e9",
    "secondary": "#0f172a",
    "accent": "#22d3ee"
  }
}
```

Sonra CSS'e:
```css
:root {
  --color-primary: #0ea5e9;
  ...
}
```
