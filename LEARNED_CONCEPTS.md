# Bricks Builder - Öğrenilen Konseptler

## ✅ Tamamlanan Öğrenme Aşamaları

### 1. Element System Architecture

#### Element Class Yapısı
```php
class Prefix_Element_Custom extends \Bricks\Element {
  // PROPERTIES
  public $category     = 'custom';      // Element category
  public $name         = 'prefix-name'; // Unique identifier
  public $icon         = 'fas fa-icon'; // Builder icon
  public $css_selector = '.wrapper';    // Default CSS target
  public $scripts      = [];            // JS dependencies
  public $nestable     = false;         // Can contain children

  // BUILDER METHODS
  public function get_label() {
    return esc_html__('Label', 'bricks');
  }

  public function set_control_groups() {
    $this->control_groups['group_id'] = [
      'title' => __('Group', 'bricks'),
      'tab'   => 'content', // or 'style'
    ];
  }

  public function set_controls() {
    $this->controls['field_id'] = [
      'tab'   => 'content',
      'group' => 'group_id',
      'label' => __('Label', 'bricks'),
      'type'  => 'text',
      'default' => 'Default value',
      'required' => ['other_field', '=', 'value'],
      'css' => [
        [
          'property' => 'color',
          'selector' => '.element',
        ]
      ]
    ];
  }

  // FRONTEND METHODS
  public function render() {
    $settings = $this->settings;
    $this->set_attribute('_root', 'class', 'wrapper');
    echo "<div {$this->render_attributes('_root')}>";
    // HTML output
    echo "</div>";
  }
}
```

#### Element Registration
```php
add_action('init', function() {
  $files = [__DIR__ . '/elements/custom.php'];
  foreach ($files as $file) {
    \Bricks\Elements::register_element($file);
  }
}, 11);
```

---

### 2. Control Types (30+ Available)

#### Content Controls
| Control | Type | Output | Usage |
|---------|------|--------|-------|
| `text` | string | Content | Single line input |
| `textarea` | string | Content | Multi-line input |
| `editor` | string | Content | Rich text (WYSIWYG) |
| `code` | string | Content | Code editor |
| `number` | int/float | Content/CSS | Numeric input |
| `select` | string | Content/CSS | Dropdown |
| `checkbox` | bool | Conditional | Toggle |
| `icon` | array | Content | Icon picker |
| `image` | array | Content/CSS | Image uploader |
| `image-gallery` | array | Content | Multiple images |
| `link` | array | Content | Link builder |
| `repeater` | array | Content | Repeatable fields |
| `posts` | array | Content | Post selector |

#### CSS Controls
| Control | Type | Output | Usage |
|---------|------|--------|-------|
| `typography` | array | CSS | Font settings |
| `color` | array | CSS | Color picker |
| `background` | array | CSS | Background settings |
| `border` | array | CSS | Border settings |
| `dimensions` | array | CSS | Margin/Padding |
| `box-shadow` | array | CSS | Shadow settings |
| `text-shadow` | array | CSS | Text shadow |
| `filters` | array | CSS | CSS filters |
| `gradient` | array | CSS | Gradient builder |
| `text-align` | string | CSS | Text alignment |
| `text-decoration` | string | CSS | Text decoration |
| `text-transform` | string | CSS | Text transform |
| `align-items` | string | CSS | Flex align |
| `justify-content` | string | CSS | Flex justify |
| `direction` | string | CSS | Flex direction |

#### Control Parameters
```php
$this->controls['example'] = [
  // Universal parameters
  'tab'          => 'content', // or 'style'
  'group'        => 'group_id',
  'label'        => __('Label', 'bricks'),
  'type'         => 'text',
  'inline'       => true,  // Label and input same line
  'small'        => true,  // 60px width input
  'default'      => 'value',
  'description'  => __('Help text', 'bricks'),
  'pasteStyles'  => false, // Exclude from paste styles

  // Conditional display
  'required'     => ['field_id', '=', 'value'],
  // Operators: =, !=, >=, <=

  // CSS output
  'css' => [
    [
      'property'  => 'color',
      'selector'  => '.element',
      'important' => true, // optional
    ]
  ],

  // Dynamic data support
  'hasDynamicData' => 'text', // or 'image', 'link'

  // Control-specific parameters
  'spellcheck'      => true,  // text
  'trigger'         => 'enter', // text: 'keyup' or 'enter'
  'inlineEditing'   => true,  // text
  'options'         => [],    // select
  'clearable'       => false, // select
  'placeholder'     => 'Text', // various
];
```

---

### 3. Dynamic Data System

#### Post Fields
```
{post_title}                    - Post başlığı
{post_id}                       - Post ID
{post_url}                      - Post URL
{post_slug}                     - Post slug
{post_type}                     - Post type
{post_date}                     - Yayın tarihi
{post_modified}                 - Güncelleme tarihi
{post_time}                     - Yayın zamanı
{post_comments_count}           - Yorum sayısı
{post_content}                  - İçerik
{post_excerpt}                  - Özet
{read_more}                     - "Read more" linki
{featured_image}                - Öne çıkan görsel
```

#### Dynamic Data Filters
```
{post_title:link}               - Başlığı link yap
{post_title:link:3}             - Başlığı 3 kelime ile sınırla + link
{post_title:link:newTab}        - Yeni sekmede aç
{post_date:human_time_diff}     - "1 hour ago" formatı
{post_excerpt:55}               - 55 kelime sınırı
{post_excerpt:format:10}        - HTML koru, 10 kelime
{featured_image:medium_large}   - Görsel boyutu
{featured_image:large:link}     - Görsel + link
```

#### Taxonomy Fields
```
{post_terms_category}           - Kategoriler (linkli)
{post_terms_post_tag}           - Etiketler (linkli)
{post_terms_TAXONOMY}           - Custom taxonomy
{post_terms_category:plain}     - Linksiz kategoriler
{term_id}                       - Term ID
{term_name}                     - Term adı
{term_slug}                     - Term slug
{term_count}                    - Term sayısı
{term_url}                      - Term arşiv URL
{term_description}              - Term açıklaması
{term_meta:KEY}                 - Term meta data
```

#### Author Fields
```
{author_id}                     - Yazar ID
{author_name}                   - Yazar adı
{author_bio}                    - Yazar biyografisi
{author_email}                  - Yazar email
{author_website}                - Yazar website
{author_archive_url}            - Yazar arşiv URL
{author_avatar}                 - Yazar avatarı
{author_meta:META_KEY}          - Yazar meta data

Filters:
{author_bio:20}                 - 20 kelime bio
{author_name:link}              - Yazar adı link
{author_email:link}             - Email link
{author_website:link}           - Website link
{author_avatar:200}             - 200px avatar
```

#### Query Loop Fields
```
{query_loop_index}              - Loop index (0'dan başlar)
{query_loop_index @start-at:1}  - 1'den başlayan index
{query_loop_index @pad:2}       - 0-padded (01, 02, 03...)
```

#### Custom Fields Integration

**ACF (Advanced Custom Fields)**
```
{acf_FIELD_NAME}                - ACF field value
{acf_get_row_layout}            - Flexible layout adı
```

**Meta Box**
```
{mb_FIELD_NAME}                 - Meta Box field
```

**JetEngine**
```
{jet_FIELD_NAME}                - JetEngine field
```

**Toolset**
```
{toolset_FIELD_NAME}            - Toolset field
```

**Pods**
```
{pods_FIELD_NAME}               - Pods field
```

**CMB2**
```
{cmb2_FIELD_NAME}               - CMB2 field
```

---

### 4. Helper Functions

#### Render Functions
```php
// Set HTML attribute
$this->set_attribute($key, $attribute, $value);
// Example:
$this->set_attribute('_root', 'class', 'my-class');
$this->set_attribute('title', 'id', 'main-title');

// Render HTML attributes
$this->render_attributes($key);
// Example:
echo "<div {$this->render_attributes('_root')}>";

// Render dynamic data tag
$this->render_dynamic_data_tag($tag, $context, $args);
// Example:
$title = $this->render_dynamic_data_tag('{post_title}', 'text');

// Render content with dynamic data
$this->render_dynamic_data($content);
// Example:
$text = $this->render_dynamic_data($this->settings['content']);

// Render element placeholder
$this->render_element_placeholder([
  'icon-class'  => 'ti-paragraph',
  'title'       => __('No content', 'bricks'),
  'description' => __('Please add content', 'bricks'),
]);
```

#### Global Helper Functions (functions.php)
```php
// Check if builder is active
bricks_is_builder()
bricks_is_builder_iframe()
bricks_is_builder_main()
bricks_is_frontend()

// Check AJAX/REST
bricks_is_ajax_call()
bricks_is_rest_call()
bricks_is_builder_call()

// Render dynamic data in custom code
bricks_render_dynamic_data($content, $post_id, $context);
// Example:
$output = bricks_render_dynamic_data(
  'Title: {post_title}',
  get_the_ID(),
  'text'
);
```

---

### 5. Filters & Hooks

#### Most Important Filters

**Element Rendering**
```php
// Control element render
add_filter('bricks/element/render', function($render, $element) {
  // Return false to prevent render
  return $render;
}, 10, 2);

// Modify element data
add_filter('bricks/frontend/render_data', function($render_data) {
  // Modify before render
  return $render_data;
});

// Custom element controls
add_filter('bricks/elements/{element_name}/controls', function($controls) {
  // Add/modify controls
  return $controls;
});

// Custom control groups
add_filter('bricks/elements/{element_name}/control_groups', function($groups) {
  // Add/modify control groups
  return $groups;
});
```

**Dynamic Data**
```php
// Custom dynamic data tags
add_filter('bricks/dynamic_data_tags', function($tags) {
  $tags[] = [
    'name'  => '{custom_tag}',
    'label' => 'Custom Tag',
    'group' => 'custom',
  ];
  return $tags;
});

// Render custom tag
add_filter('bricks/dynamic_data/render_tag', function($value, $tag, $post_id) {
  if ($tag === 'custom_tag') {
    return 'Custom value';
  }
  return $value;
}, 10, 3);

// Modify term separator
add_filter('bricks/dynamic_data/post_terms_separator', function($separator) {
  return ' | ';
});

// Modify read more text
add_filter('bricks/dynamic_data/read_more', function($text, $post_id) {
  return 'Continue reading';
}, 10, 2);
```

**Query Loops**
```php
// Modify query vars
add_filter('bricks/query/query_vars', function($query_vars, $settings, $element_id) {
  // Modify query
  return $query_vars;
}, 10, 3);

// Get loop object ID
add_filter('bricks/query/loop_object_id', function($object_id, $object_type) {
  return $object_id;
}, 10, 2);
```

**Form Actions**
```php
// Custom form action
add_filter('bricks/form/action/{form_action}', function($data, $form) {
  // Process form data
  return $data;
}, 10, 2);

// Modify meta value before update
add_filter('bricks/form/update_post/meta_value', function($value, $key) {
  return $value;
}, 10, 2);
```

#### Important Actions
```php
// Before query loop
add_action('bricks/query/before_loop', function($query_object) {
  // Run before loop
});

// After query loop
add_action('bricks/query/after_loop', function($query_object) {
  // Run after loop
});

// CSS file generation
add_action('bricks/generate_css_file', function($post_id) {
  // Run when CSS generated
});
```

---

### 6. Template Structure (JSON)

#### Minimal Template
```json
{
  "id": "unique-id",
  "name": "template-name",
  "type": "section",
  "content": [
    {
      "id": "elem1",
      "name": "container",
      "parent": 0,
      "children": ["elem2"],
      "settings": {
        "_width": "100%",
        "_direction": "row"
      }
    },
    {
      "id": "elem2",
      "name": "heading",
      "parent": "elem1",
      "children": [],
      "settings": {
        "text": "Heading text",
        "tag": "h1"
      }
    }
  ],
  "globalClasses": [],
  "globalElements": []
}
```

---

### 7. Constants (Bricks 2.1.4)

```php
BRICKS_VERSION              = '2.1.4'
BRICKS_PATH                 = tema klasörü
BRICKS_URL                  = tema URL
BRICKS_BUILDER_PARAM        = 'bricks'
BRICKS_DB_PAGE_CONTENT      = '_bricks_page_content_2'
BRICKS_DB_GLOBAL_CLASSES    = 'bricks_global_classes'
BRICKS_DB_COMPONENTS        = 'bricks_components'
BRICKS_DB_THEME_STYLES      = 'bricks_theme_styles'
```

---

## 🎯 Sonraki Adımlar

1. ✅ Element system
2. ✅ Control types
3. ✅ Dynamic data basics
4. ⏳ Query loops (deep dive)
5. ⏳ WooCommerce integration
6. ⏳ AI template generator

---

## 💡 AI Template Generator Konsept

### Giriş → JSON Pipeline
```
1. User Input: "Diş kliniği için modern site, mavi tema"
         ↓
2. AI Parse:
   - Industry: dental
   - Style: modern
   - Color: blue (#3B82F6)
   - Required sections: header, hero, services, contact
         ↓
3. Template Match:
   - Header: smile/header
   - Hero: hero-simple (modified)
   - Services: features-01
   - Contact: contact-01
         ↓
4. Content Generate:
   - AI generates headings, descriptions, CTAs
   - Dental-specific terms
   - Professional tone
         ↓
5. JSON Build:
   - Merge templates
   - Replace placeholder text
   - Apply blue theme
   - Generate unique IDs
   - Fix parent-child relations
         ↓
6. Output: Complete Bricks JSON
```

### AI Prompt Template
```
Generate Bricks Builder JSON template for:
- Industry: {industry}
- Style: {style}
- Sections: {sections}
- Colors: {colors}

Requirements:
- Use dynamic data tags where appropriate
- Responsive breakpoints for mobile/tablet
- Professional content
- SEO-friendly structure
```
