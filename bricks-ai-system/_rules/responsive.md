# RESPONSIVE KURALLARI

## Breakpoints
| Breakpoint | Suffix | Genişlik |
|------------|--------|----------|
| Desktop | (yok) | 1200px+ |
| Tablet | `:tablet_portrait` | 768-1199px |
| Mobile | `:mobile_portrait` | 0-767px |

## Syntax
```json
{
  "_direction": "row",
  "_direction:mobile_portrait": "column",
  
  "_gridTemplateColumns": "repeat(3, 1fr)",
  "_gridTemplateColumns:tablet_portrait": "repeat(2, 1fr)",
  "_gridTemplateColumns:mobile_portrait": "1fr",
  
  "_display": "flex",
  "_display:mobile_portrait": "none"
}
```

## Grid Patterns
```
3 col → 2 col → 1 col
4 col → 2 col → 1 col
2 col → 1 col
```

## Typography Scale
| Element | Desktop | Mobile |
|---------|---------|--------|
| H1 | `--text-5xl` | `--text-3xl` |
| H2 | `--text-4xl` | `--text-2xl` |
| H3 | `--text-2xl` | `--text-xl` |
| Body | `--text-base` | `--text-base` |

**Min font: 16px!**

## Spacing Scale
| Spacing | Desktop | Mobile |
|---------|---------|--------|
| Section | `--spacing-2xl` | `--spacing-xl` |
| Gap | `--spacing-lg` | `--spacing-md` |

## Visibility
```json
// Mobile'da gizle
{ "_display:mobile_portrait": "none" }

// Sadece mobile'da göster
{ "_display": "none", "_display:mobile_portrait": "flex" }
```

## Touch Target
Mobile'da tıklanabilir: **min 44x44px**

## Checklist
- [ ] Grid mobile'da 1 column
- [ ] Font-size responsive
- [ ] Padding/gap mobile'da küçük
- [ ] Touch target 44px+
- [ ] Nav mobile'da hamburger
