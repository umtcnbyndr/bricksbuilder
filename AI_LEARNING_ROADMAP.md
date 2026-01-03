# AI Bricks Builder Öğrenme Yol Haritası

## 📋 Mevcut Kaynaklar

✅ **bricks_academy_learn.txt** - 229 makale, 31,013 satır
✅ **brickstema/** - Bricks 2.1.4 tema dosyaları
✅ **bricks-child/** - Custom element örneği
✅ **128 template** - Full sites + sections

---

## 🎯 Öğrenme Aşamaları

### Faz 1: Temel Yapı ✅ TAMAMLANDI
- [x] JSON template yapısı
- [x] Element hiyerarşisi (parent-child)
- [x] Settings pattern'leri
- [x] Responsive breakpoints
- [x] Global classes

### Faz 2: Element Sistemi 🔄 ŞU AN
- [ ] Element architecture (bricks-child/elements/title.php)
- [ ] Control types (text, typography, icon, etc.)
- [ ] Render functions (PHP + Vue.js)
- [ ] Element conditions
- [ ] Custom element creation

### Faz 3: Dynamic Data
- [ ] Dynamic Data tag sistemi
- [ ] Post meta & custom fields
- [ ] Query loops
- [ ] WooCommerce data
- [ ] Custom dynamic data tags

### Faz 4: Advanced Features
- [ ] Global Elements
- [ ] Components
- [ ] Interactions
- [ ] Theme Styles
- [ ] Template conditions

### Faz 5: AI Integration
- [ ] Template generation AI'ı
- [ ] Natural language → JSON converter
- [ ] Content generation
- [ ] Image suggestion system

---

## 📚 Öncelikli Makaleler (Academy)

### Element Creation
1. **Create Your Own Elements** - Custom element nasıl yapılır
2. **Element Controls** - Control types
3. **Element Conditions** - Conditional rendering
4. **Nestable Elements (API)** - Parent-child elements
5. **Global Elements** - Reusable components

### Dynamic Data
1. **Dynamic Data** - Giriş
2. **Create Your Own Dynamic Data Tag** - Custom tags
3. **Creating dynamic WooCommerce archive pages** - E-commerce
4. **Filter: bricks/dynamic_data/*** - Customization hooks

### Core Concepts
1. **Block Element** - Layout temel
2. **Container Element** - Flexbox yapısı
3. **Div Element** - Wrapper element
4. **Form Element** - Form handling
5. **Components** - Component system

### Filters & Actions (Top 20)
1. `bricks/element/render` - Element render control
2. `bricks/elements/{element_name}/controls` - Custom controls
3. `bricks/frontend/render_data` - Output modification
4. `bricks/query/loop_object_id` - Query customization
5. `bricks/form/action/{form_action}` - Form actions
6. `bricks/dynamic_data/***` - Dynamic data hooks
7. `bricks/active_templates` - Template control
8. `bricks/builder/elements` - Element list modification
9. `bricks/setup/control_options` - Control options
10. `bricks/content/html_after_begin` - Content injection

---

## 🧩 Custom Element Anatomy (Öğrenildi)

```php
class Element_Custom extends \Bricks\Element {
  // 1. Properties
  public $category     = 'custom';
  public $name         = 'custom-name';
  public $icon         = 'fas fa-icon';
  public $css_selector = '.wrapper';

  // 2. Label
  public function get_label() {}

  // 3. Control Groups (tabs)
  public function set_control_groups() {}

  // 4. Controls (settings)
  public function set_controls() {
    $this->controls['field_name'] = [
      'tab'   => 'content',
      'label' => 'Field Label',
      'type'  => 'text',
      'hasDynamicData' => 'text',
      'default' => 'Default value',
      'css' => [
        ['property' => 'color', 'selector' => '.element']
      ]
    ];
  }

  // 5. Frontend Render (PHP)
  public function render() {
    $settings = $this->settings;
    echo "<div {$this->render_attributes('_root')}>";
    // HTML output
    echo "</div>";
  }

  // 6. Builder Render (Vue.js) - Optional
  public static function render_builder() {
    ?>
    <script type="text/x-template" id="tmpl-bricks-element-custom">
      <component :is="tag">
        <contenteditable
          v-if="settings.field"
          :settings="settings"
          controlKey="field"/>
      </component>
    </script>
    <?php
  }
}
```

---

## 🎨 Control Types (Öğrenilecek)

### Basic Controls
- `text` - Text input
- `textarea` - Multi-line text
- `number` - Numeric input
- `select` - Dropdown
- `checkbox` - Boolean toggle
- `radio` - Radio buttons

### Advanced Controls
- `typography` - Font settings
- `color` - Color picker
- `background` - Background settings
- `border` - Border settings
- `dimensions` - Spacing (margin/padding)
- `shadow` - Box shadow
- `filters` - CSS filters
- `icon` - Icon picker
- `image` - Image upload
- `link` - Link selector
- `editor` - Rich text editor
- `code` - Code editor

---

## 🔧 Dynamic Data Tags (Öğrenilecek)

### Post Tags
- `{post_title}` - Post başlığı
- `{post_excerpt}` - Özet
- `{post_content}` - İçerik
- `{post_date}` - Tarih
- `{post_author}` - Yazar

### Custom Field Tags
- `{acf_field_name}` - ACF field
- `{meta_box_field}` - Meta Box field

### WooCommerce Tags
- `{woo_product_price}` - Ürün fiyatı
- `{woo_product_stock}` - Stok durumu
- `{woo_product_rating}` - Değerlendirme

### Custom Tags
```php
add_filter('bricks/dynamic_data_tags', function($tags) {
  $tags[] = [
    'name'  => '{custom_tag}',
    'label' => 'Custom Tag',
    'group' => 'custom',
  ];
  return $tags;
});

add_filter('bricks/dynamic_data/render_tag', function($value, $tag, $post_id) {
  if ($tag === 'custom_tag') {
    return 'Custom value';
  }
  return $value;
}, 10, 3);
```

---

## 📐 Template JSON Generation Strategy

### AI Template Generator Flow
```
User Input (Natural Language)
         ↓
    AI Analysis
    - Parse intent
    - Extract components
    - Identify layout
         ↓
  Component Selection
    - Header type
    - Hero style
    - Sections needed
    - Color scheme
         ↓
  JSON Generation
    - Generate IDs
    - Build hierarchy
    - Apply settings
    - Add content
         ↓
   Output JSON
```

### Example Mapping
```
User: "Diş kliniği için modern bir site, mavi tema, hizmetler bölümü, randevu formu"

AI Breakdown:
- Industry: Dental
- Style: Modern
- Colors: Blue theme (#3B82F6)
- Sections:
  * Header (sticky navigation)
  * Hero (dental imagery, appointment CTA)
  * Services (3-column grid, icons)
  * Contact Form (appointment booking)
  * Footer

Template Selection:
- Base: smile/template-header-smile
- Hero: hero-section-1 (modified)
- Services: features-01 (3 columns)
- Form: contact-01 (appointment fields)

JSON Generation:
- Merge templates
- Replace content with AI-generated text
- Apply blue color scheme
- Add dental-specific icons
```

---

## 🚀 Next Steps

### Şu An Yapılacak:
1. **Element Controls** makalesini oku
2. Control type'ları öğren
3. Custom element oluştur
4. Dynamic data tag kullan

### Sonra:
1. Template generator AI mantığını kur
2. Natural language parser yaz
3. JSON builder fonksiyonu oluştur
4. Test et ve optimize et

---

## 💡 AI Template Generator Pseudocode

```javascript
async function generateTemplate(userInput) {
  // 1. Analyze user input
  const analysis = await analyzeInput(userInput);

  // 2. Select base templates
  const templates = selectTemplates(analysis.industry, analysis.style);

  // 3. Generate content
  const content = await generateContent(analysis);

  // 4. Build JSON
  const json = {
    id: generateId(),
    name: `ai-generated-${Date.now()}`,
    type: 'section',
    content: []
  };

  // 5. Add sections
  templates.forEach(template => {
    const section = cloneTemplate(template);
    replaceContent(section, content);
    applyTheme(section, analysis.colors);
    json.content.push(...section.content);
  });

  // 6. Fix IDs and hierarchy
  fixHierarchy(json.content);

  return json;
}
```

---

## 📖 Öğrenme Durumu

- ✅ JSON Structure
- ✅ Element Types
- ✅ Settings Patterns
- ✅ Responsive Breakpoints
- ✅ Basic Element Creation
- 🔄 Control Types (in progress)
- ⏳ Dynamic Data
- ⏳ Query Loops
- ⏳ Template Conditions
- ⏳ AI Integration
