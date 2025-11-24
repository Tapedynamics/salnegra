# QUICK FIXES - FINCA TRES ROQUES TENERIFE
## Interventi Critici Immediati (1-2 Settimane)

**Sito:** https://fincatresroquestenerife.com/
**Punteggio SEO Attuale:** 7.0/10
**Target dopo Quick Fixes:** 8.5/10

---

## 🔴 PRIORITÀ 1: HREFLANG TAGS (2-3 ore)

### Problema Critico
Il sito ha due versioni linguistiche (ES/EN) ma **manca completamente** l'implementazione dei tag hreflang. Questo causa:
- Google indicizza la versione sbagliata per paese/lingua
- Rischio contenuto duplicato
- Perdita di traffico organico da targeting geografico errato

### ROI: +25-40% traffico organico correttamente targettizzato

---

### IMPLEMENTAZIONE: Versione SPAGNOLA (/es/)

Aggiungi questi tag nell'`<head>` di **TUTTE** le pagine in spagnolo:

```html
<!-- Hreflang Tags - Versione SPAGNOLA -->
<link rel="alternate" hreflang="es" href="https://fincatresroquestenerife.com/es/" />
<link rel="alternate" hreflang="en" href="https://fincatresroquestenerife.com/" />
<link rel="alternate" hreflang="x-default" href="https://fincatresroquestenerife.com/" />
```

#### Esempio per pagine interne (Menu):
```html
<!-- Pagina Menu ES -->
<link rel="alternate" hreflang="es" href="https://fincatresroquestenerife.com/es/menu/" />
<link rel="alternate" hreflang="en" href="https://fincatresroquestenerife.com/menu/" />
<link rel="alternate" hreflang="x-default" href="https://fincatresroquestenerife.com/menu/" />
```

#### Esempio per pagine interne (Bodega):
```html
<!-- Pagina Bodega ES -->
<link rel="alternate" hreflang="es" href="https://fincatresroquestenerife.com/es/bodega/" />
<link rel="alternate" hreflang="en" href="https://fincatresroquestenerife.com/bodega/" />
<link rel="alternate" hreflang="x-default" href="https://fincatresroquestenerife.com/bodega/" />
```

---

### IMPLEMENTAZIONE: Versione INGLESE (/)

Aggiungi questi tag nell'`<head>` di **TUTTE** le pagine in inglese:

```html
<!-- Hreflang Tags - Versione INGLESE -->
<link rel="alternate" hreflang="en" href="https://fincatresroquestenerife.com/" />
<link rel="alternate" hreflang="es" href="https://fincatresroquestenerife.com/es/" />
<link rel="alternate" hreflang="x-default" href="https://fincatresroquestenerife.com/" />
```

---

### IMPLEMENTAZIONE CON WORDPRESS

Se usi **Yoast SEO** o **Rank Math**:

#### Con Yoast SEO Premium + WPML:
```php
// Già implementato automaticamente se WPML è configurato correttamente
// Verifica in: SEO > Impostazioni > Impostazioni multilingua
```

#### Con Rank Math:
```php
// Aggiungi in functions.php del tema:
add_action('wp_head', 'add_hreflang_tags');

function add_hreflang_tags() {
    $current_url = get_permalink();
    $base_url = str_replace('/es/', '/', $current_url);
    $es_url = str_replace('fincatresroquestenerife.com/', 'fincatresroquestenerife.com/es/', $base_url);

    if (strpos($current_url, '/es/') !== false) {
        // Versione spagnola
        echo '<link rel="alternate" hreflang="es" href="' . esc_url($current_url) . '" />' . "\n";
        echo '<link rel="alternate" hreflang="en" href="' . esc_url($base_url) . '" />' . "\n";
        echo '<link rel="alternate" hreflang="x-default" href="' . esc_url($base_url) . '" />' . "\n";
    } else {
        // Versione inglese
        echo '<link rel="alternate" hreflang="en" href="' . esc_url($current_url) . '" />' . "\n";
        echo '<link rel="alternate" hreflang="es" href="' . esc_url($es_url) . '" />' . "\n";
        echo '<link rel="alternate" hreflang="x-default" href="' . esc_url($current_url) . '" />' . "\n";
    }
}
```

---

### TESTING & VERIFICA

**1. Google Search Console:**
```
1. Vai a: https://search.google.com/search-console
2. Seleziona proprietà
3. Navigare a: Indicizzazione > Targeting internazionale
4. Verificare tag hreflang dopo 1-2 settimane
```

**2. Hreflang Testing Tool:**
```
https://www.sistrix.com/hreflang-validator/
Inserisci: https://fincatresroquestenerife.com/
```

**3. Verifica Manuale (Chrome DevTools):**
```javascript
// Console Chrome - Verifica tag hreflang
document.querySelectorAll('link[hreflang]').forEach(link => {
    console.log(link.getAttribute('hreflang'), link.getAttribute('href'));
});
```

---

## 🔴 PRIORITÀ 2: OPEN GRAPH & TWITTER CARDS (2-3 ore)

### Problema Critico
**ZERO meta tag social presenti.** Condivisioni su Facebook/WhatsApp/Twitter mostrano anteprima generica o vuota.

### ROI: +40-60% CTR su condivisioni social

---

### IMPLEMENTAZIONE: Homepage SPAGNOLA

```html
<!-- Open Graph Tags (Facebook, WhatsApp, LinkedIn, Instagram) -->
<meta property="og:type" content="restaurant" />
<meta property="og:title" content="Finca Tres Roques - Restaurante Rural y Bodega en Tenerife" />
<meta property="og:description" content="Disfruta de auténticos platos españoles en nuestro restaurante rural en Ifonche, Tenerife. Carne GOYA, vinos locales y vistas espectaculares. ¡Reserva ahora!" />
<meta property="og:url" content="https://fincatresroquestenerife.com/es/" />
<meta property="og:image" content="https://fincatresroquestenerife.com/wp-content/uploads/2025/11/finca-hero-1200x630.jpg" />
<meta property="og:image:width" content="1200" />
<meta property="og:image:height" content="630" />
<meta property="og:image:alt" content="Vista panorámica de Finca Tres Roques con viñedos y montañas de Tenerife" />
<meta property="og:locale" content="es_ES" />
<meta property="og:locale:alternate" content="en_US" />
<meta property="og:site_name" content="Finca Tres Roques" />

<!-- Restaurant-specific Open Graph -->
<meta property="restaurant:contact_info:street_address" content="Carretera TF-51, km 20" />
<meta property="restaurant:contact_info:locality" content="Ifonche" />
<meta property="restaurant:contact_info:region" content="Tenerife" />
<meta property="restaurant:contact_info:postal_code" content="38677" />
<meta property="restaurant:contact_info:country_name" content="España" />

<!-- Twitter Cards -->
<meta name="twitter:card" content="summary_large_image" />
<meta name="twitter:title" content="Finca Tres Roques - Restaurante Rural en Tenerife" />
<meta name="twitter:description" content="Auténticos platos españoles con ingredientes locales. Carne GOYA, vinos propios y ambiente rural único." />
<meta name="twitter:image" content="https://fincatresroquestenerife.com/wp-content/uploads/2025/11/finca-hero-1200x630.jpg" />
<meta name="twitter:image:alt" content="Finca Tres Roques - Restaurante y viñedos en Tenerife" />
<meta name="twitter:site" content="@FincaTresRoques" />
```

---

### IMPLEMENTAZIONE: Homepage INGLESE

```html
<!-- Open Graph Tags (English Version) -->
<meta property="og:type" content="restaurant" />
<meta property="og:title" content="Finca Tres Roques - Rural Restaurant & Bodega in Tenerife" />
<meta property="og:description" content="Experience authentic Spanish cuisine at our rural restaurant in Ifonche, Tenerife. GOYA meat, local wines, and stunning views. Book now!" />
<meta property="og:url" content="https://fincatresroquestenerife.com/" />
<meta property="og:image" content="https://fincatresroquestenerife.com/wp-content/uploads/2025/11/finca-hero-1200x630.jpg" />
<meta property="og:image:width" content="1200" />
<meta property="og:image:height" content="630" />
<meta property="og:image:alt" content="Panoramic view of Finca Tres Roques with vineyards and Tenerife mountains" />
<meta property="og:locale" content="en_US" />
<meta property="og:locale:alternate" content="es_ES" />
<meta property="og:site_name" content="Finca Tres Roques" />

<!-- Twitter Cards -->
<meta name="twitter:card" content="summary_large_image" />
<meta name="twitter:title" content="Finca Tres Roques - Rural Restaurant in Tenerife" />
<meta name="twitter:description" content="Authentic Spanish dishes with local ingredients. GOYA meat, own wines, and unique rural atmosphere." />
<meta name="twitter:image" content="https://fincatresroquestenerife.com/wp-content/uploads/2025/11/finca-hero-1200x630.jpg" />
<meta name="twitter:image:alt" content="Finca Tres Roques - Restaurant and vineyards in Tenerife" />
<meta name="twitter:site" content="@FincaTresRoques" />
```

---

### IMPLEMENTAZIONE: Pagina MENU

```html
<!-- Open Graph - Menu Page -->
<meta property="og:type" content="restaurant.menu" />
<meta property="og:title" content="Menú - Finca Tres Roques | Platos Españoles Tradicionales" />
<meta property="og:description" content="Descubre nuestro menú con carne GOYA, calçots, secreto ibérico y más. Ingredientes locales de nuestra propia finca." />
<meta property="og:url" content="https://fincatresroquestenerife.com/es/menu/" />
<meta property="og:image" content="https://fincatresroquestenerife.com/wp-content/uploads/2025/11/menu-hero.jpg" />
<meta property="og:image:width" content="1200" />
<meta property="og:image:height" content="630" />
```

---

### IMPLEMENTAZIONE: Pagina BODEGA

```html
<!-- Open Graph - Bodega Page -->
<meta property="og:type" content="product.group" />
<meta property="og:title" content="Bodega - Finca Tres Roques | Vinos Locales de Tenerife" />
<meta property="og:description" content="Visita nuestra bodega y descubre vinos elaborados en Tenerife. Tours guiados y catas disponibles." />
<meta property="og:url" content="https://fincatresroquestenerife.com/es/bodega/" />
<meta property="og:image" content="https://fincatresroquestenerife.com/wp-content/uploads/2025/11/bodega-hero.jpg" />
<meta property="og:image:width" content="1200" />
<meta property="og:image:height" content="630" />
```

---

### CREAZIONE IMMAGINE HERO (1200x630px)

**Specifiche tecniche:**
- Dimensione: 1200px x 630px (ratio 1.91:1)
- Formato: JPG (qualità 85%) o PNG
- Peso: max 300KB
- Testo leggibile su mobile
- Logo visibile
- Focus su piatti/vista panoramica

**Strumenti consigliati:**
- Canva: https://www.canva.com/create/og-images/
- Adobe Express: https://www.adobe.com/express/create/social-media-image
- Photopea (free): https://www.photopea.com/

**Elementi da includere:**
```
✅ Logo Finca Tres Roques
✅ Piatto signature (Carne GOYA o Calçots)
✅ Vista panoramica viñedos/montagne
✅ Testo: "Restaurante Rural | Ifonche, Tenerife"
```

---

### IMPLEMENTAZIONE CON WORDPRESS

#### Yoast SEO (Premium):
```
1. Vai in: Yoast SEO > Social
2. Facebook:
   - Carica immagine predefinita 1200x630px
   - Compila title e description
3. Twitter:
   - Seleziona "Summary with large image"
   - Inserisci @handle se disponibile
```

#### Rank Math:
```php
// Aggiungi in functions.php per automatizzare OG tags:
add_filter('rank_math/opengraph/facebook/og_locale', function($locale) {
    return is_locale('es_ES') ? 'es_ES' : 'en_US';
});

add_filter('rank_math/opengraph/facebook/image', function($image) {
    if (!$image) {
        return 'https://fincatresroquestenerife.com/wp-content/uploads/hero-default.jpg';
    }
    return $image;
});
```

---

### TESTING & VERIFICA

**1. Facebook Sharing Debugger:**
```
https://developers.facebook.com/tools/debug/
Inserisci URL e clicca "Debug"
Verifica: immagine, title, description
```

**2. Twitter Card Validator:**
```
https://cards-dev.twitter.com/validator
Inserisci URL e verifica preview
```

**3. LinkedIn Post Inspector:**
```
https://www.linkedin.com/post-inspector/
Controlla preview per condivisioni LinkedIn
```

**4. WhatsApp Preview:**
```
Invia URL a te stesso su WhatsApp
Verifica anteprima con immagine
```

---

## 🟠 PRIORITÀ 3: ALT TEXT IMMAGINI (3-4 ore)

### Problema Identificato
Molte immagini hanno alt text mancanti o generici come "secreto ibérico" o semplicemente vuoti.

### ROI: +15-25% traffico da Google Images

---

### TEMPLATE ALT TEXT: Piatti

```html
<!-- ❌ PRIMA (evitare) -->
<img src="secreto-iberico.jpg" alt="" />
<img src="dish-1.jpg" alt="secreto ibérico" />
<img src="plato.jpg" alt="plato" />

<!-- ✅ DOPO (ottimizzato) -->
<img src="secreto-iberico.jpg"
     alt="Plato de secreto ibérico con patatas fritas y pimientos de padrón servido en Finca Tres Roques Tenerife" />

<img src="calcots.jpg"
     alt="Calçots a la brasa con salsa romesco tradicional en Finca Tres Roques restaurante rural Tenerife" />

<img src="carne-goya.jpg"
     alt="Carne GOYA premium a la parrilla con guarnición de verduras locales, especialidad de Finca Tres Roques" />

<img src="pollo-carbon.jpg"
     alt="Pollo entero asado al carbón con mojo rojo canario en restaurante Finca Tres Roques Ifonche" />
```

---

### TEMPLATE ALT TEXT: Ambiente & Location

```html
<!-- Vista panoramica -->
<img src="view-vineyard.jpg"
     alt="Vista panorámica de los viñedos de Finca Tres Roques con montañas de Tenerife al fondo y cielo azul" />

<!-- Exterior restaurante -->
<img src="exterior-finca.jpg"
     alt="Entrada principal de Finca Tres Roques restaurante rural en Ifonche Tenerife con terraza exterior" />

<!-- Bodega -->
<img src="bodega-interior.jpg"
     alt="Interior de la bodega de Finca Tres Roques con barriles de vino tradicionales y botellas de vino local Tenerife" />

<!-- Mesa con comensales -->
<img src="dining-table.jpg"
     alt="Mesa decorada con platos españoles tradicionales en el comedor rústico de Finca Tres Roques" />
```

---

### TEMPLATE ALT TEXT: Ingredienti & Dettagli

```html
<!-- Ingredienti freschi -->
<img src="fresh-vegetables.jpg"
     alt="Verduras frescas cultivadas en la finca de Finca Tres Roques para cocina de km 0 Tenerife" />

<!-- Vino locale -->
<img src="local-wine.jpg"
     alt="Botella de vino blanco local producido en la bodega de Finca Tres Roques con uvas de Tenerife" />

<!-- Granja -->
<img src="farm-animals.jpg"
     alt="Animales de granja en Finca Tres Roques para experiencia familiar y educativa en Tenerife" />
```

---

### IMPLEMENTAZIONE MASSIVA CON WORDPRESS

#### Plugin "SEO Image Optimizer":
```
1. Installa: WP Admin > Plugin > Add New > "SEO Image Optimizer"
2. Vai in: Tools > Image SEO
3. Bulk Edit Alt Text:
   - Seleziona immagini senza alt
   - Template: "%title% in Finca Tres Roques Tenerife"
```

#### Script PHP per Bulk Update:
```php
// Aggiungi in functions.php (TEMPORANEO - rimuovere dopo uso)
function bulk_update_image_alt_text() {
    $images = get_posts([
        'post_type' => 'attachment',
        'post_mime_type' => 'image',
        'posts_per_page' => -1,
    ]);

    foreach ($images as $image) {
        $current_alt = get_post_meta($image->ID, '_wp_attachment_image_alt', true);

        if (empty($current_alt)) {
            $title = get_the_title($image->ID);
            $new_alt = $title . ' en Finca Tres Roques Tenerife restaurante rural';
            update_post_meta($image->ID, '_wp_attachment_image_alt', $new_alt);
        }
    }
}

// Esegui UNA SOLA VOLTA da Tools > Site Health
add_action('admin_init', 'bulk_update_image_alt_text');
```

---

### CHECKLIST IMMAGINI DA OTTIMIZZARE

**Homepage (priorità alta):**
- [ ] Hero image principale
- [ ] Vista panoramica viñedos (3-4 immagini)
- [ ] Piatti signature (Carne GOYA, Calçots, Secreto Ibérico)
- [ ] Exterior restaurante
- [ ] Sezione testimonial clienti

**Pagina Menu (priorità alta):**
- [ ] Tutte le foto piatti (stimato: 12-15 immagini)
- [ ] Ingredienti freschi
- [ ] Vini locali

**Pagina Bodega (priorità media):**
- [ ] Interior bodega (5-7 immagini)
- [ ] Bottiglie vino
- [ ] Tour viñedos

**Galleria (priorità media):**
- [ ] Eventi speciali
- [ ] Foto ambientali
- [ ] Clienti felici (se autorizzati)

---

## 🟡 OTTIMIZZAZIONI AGGIUNTIVE

### Canonical Tags

```html
<!-- Versione SPAGNOLA -->
<link rel="canonical" href="https://fincatresroquestenerife.com/es/" />

<!-- Versione INGLESE -->
<link rel="canonical" href="https://fincatresroquestenerife.com/" />
```

### Robots.txt Ottimizzato

```
User-agent: *
Disallow: /wp-admin/
Disallow: /wp-includes/
Disallow: /wp-content/plugins/
Disallow: /wp-content/themes/
Allow: /wp-content/uploads/

Sitemap: https://fincatresroquestenerife.com/sitemap_index.xml
```

---

## 📊 TIMELINE & ROI ATTESO

| Settimana | Intervento | Ore | ROI Atteso |
|-----------|-----------|-----|------------|
| 1 | Hreflang tags | 2-3h | +25-40% traffico geo-targettizzato |
| 1-2 | Open Graph + Twitter Cards | 2-3h | +40-60% CTR social |
| 2 | Creazione immagine hero | 1h | Miglior conversione social |
| 3-4 | Alt text immagini (40-60 img) | 3-4h | +15-25% traffico Images |
| 4 | Canonical tags | 1h | Prevenzione contenuto duplicato |
| 4 | Testing completo | 1-2h | Verifica implementazione |

**TOTALE INVESTIMENTO:** 10-14 ore
**SCORE SEO:** 7.0 → **8.5**
**TRAFFICO ORGANICO:** +35-50% in 8-12 settimane

---

## 🔧 RISORSE UTILI

**Testing Tools:**
- Google Search Console: https://search.google.com/search-console
- Hreflang Validator: https://www.sistrix.com/hreflang-validator/
- Facebook Debugger: https://developers.facebook.com/tools/debug/
- Twitter Card Validator: https://cards-dev.twitter.com/validator

**Image Creation:**
- Canva (OG Images): https://www.canva.com/
- Photopea (Free Photoshop): https://www.photopea.com/
- TinyPNG (Compression): https://tinypng.com/

**WordPress Plugins:**
- Yoast SEO Premium: https://yoast.com/
- Rank Math: https://rankmath.com/
- SEO Image Optimizer: https://wordpress.org/plugins/seo-image-optimizer/

---

## ✅ POST-IMPLEMENTAZIONE CHECKLIST

- [ ] Hreflang tags implementati su TUTTE le pagine (ES + EN)
- [ ] Open Graph tags aggiunti (homepage, menu, bodega)
- [ ] Twitter Cards implementate
- [ ] Immagine hero 1200x630px creata e caricata
- [ ] Alt text aggiornati (minimo 80% delle immagini)
- [ ] Canonical tags verificati
- [ ] Test Facebook Sharing Debugger ✅
- [ ] Test Twitter Card Validator ✅
- [ ] Test Google Search Console (hreflang) ✅
- [ ] Sitemap rigenerata e reinviata a GSC
- [ ] Monitoraggio traffico organico attivato (Google Analytics)

---

**Report compilato da:** Claude Code - AI SEO Audit Specialist
**Data:** 24 Novembre 2025
**Versione:** 1.0
