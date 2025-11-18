# QUICK FIXES - ESEMPI DI CODICE PRATICI
## Ika Ika Surf School Tenerife - Correzioni SEO Immediate

---

## 1. ALT TEXT IMMAGINI - ESEMPI CORRETTI

### Homepage - Immagine Hero
```html
<!-- ❌ PRIMA -->
<img src="hero-surf.jpg" alt="">

<!-- ✅ DOPO -->
<img src="hero-surf.jpg"
     alt="Studenti della scuola di surf Ika Ika durante una lezione di gruppo a Playa de las Américas, Tenerife"
     width="1920"
     height="1080">
```

### Galleria Prodotti
```html
<!-- ❌ PRIMA -->
<img src="group-lesson.jpg" alt="group lesson">

<!-- ✅ DOPO -->
<img src="group-lesson.jpg"
     alt="Lezione di surf di gruppo con istruttori certificati a Tenerife - max 8 studenti per sessione"
     width="800"
     height="600">
```

### Immagini Istruttori
```html
<!-- ❌ PRIMA -->
<img src="instructor-1.jpg" alt="instructor">

<!-- ✅ DOPO -->
<img src="instructor-1.jpg"
     alt="Marco, istruttore di surf certificato ISA con 10 anni di esperienza a Ika Ika Surf School Tenerife"
     width="400"
     height="400">
```

### Attrezzatura
```html
<!-- ✅ ESEMPI CORRETTI -->
<img src="surfboard-beginner.jpg"
     alt="Tavola da surf softboard per principianti utilizzata nelle lezioni Ika Ika - sicura e stabile">

<img src="wetsuit.jpg"
     alt="Muta da surf 3/2mm fornita gratuitamente durante le lezioni a Tenerife">

<img src="surf-wax.jpg"
     alt="Cera per tavola da surf applicata prima di ogni lezione - grip ottimale">
```

### Location/Scuola
```html
<img src="school-exterior.jpg"
     alt="Esterno della scuola di surf Ika Ika a Playa de las Américas con tavole colorate e logo">

<img src="beach-location.jpg"
     alt="Spiaggia di Playa de las Américas a Tenerife, location delle lezioni di surf Ika Ika">

<img src="changing-rooms.jpg"
     alt="Spogliatoi e docce presso la scuola di surf Ika Ika - servizi inclusi nel prezzo">
```

---

## 2. CORREZIONE H1 - HOMEPAGE

### Soluzione Raccomandata
```html
<!-- ❌ STRUTTURA ATTUALE (PROBLEMATICA) -->
<header>
  <h1>IKA IKA SURF SCHOOL</h1>
</header>
<section>
  <h1>Surf Lessons for all abilities</h1>
  <h2>Surf School Tenerife - Playa de Las Americas</h2>
</section>

<!-- ✅ STRUTTURA CORRETTA -->
<header>
  <h1>Ika Ika Surf School Tenerife - Professional Surf Lessons for All Levels</h1>
</header>
<section>
  <h2>Expert Surf Instruction at Playa de Las Américas</h2>
  <h3>From Beginners to Advanced Surfers - Group & Private Lessons Available</h3>
</section>
```

### Alternative (se necessario mantenere layout simile)
```html
<!-- Opzione 2: H1 con span stilizzati -->
<h1>
  <span class="brand-name">Ika Ika Surf School</span>
  <span class="tagline">Professional Surf Lessons in Tenerife</span>
</h1>

<!-- CSS associato -->
<style>
h1 {
  display: flex;
  flex-direction: column;
  align-items: center;
}
.brand-name {
  font-size: 3rem;
  font-weight: bold;
}
.tagline {
  font-size: 1.5rem;
  font-weight: normal;
  color: #0066cc;
}
</style>
```

---

## 3. GOOGLE MAPS EMBED - PAGINA CONTATTI

### Implementazione Completa
```html
<!-- Sezione Mappa su /contact-us/ -->
<section class="contact-map">
  <h2>Come Raggiungerci</h2>

  <!-- Google Maps Embed -->
  <div class="map-container">
    <iframe
      src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d879.5!2d-16.731039!3d28.064939!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2zMjjCsDAzJzUzLjgiTiAxNsKwNDMnNTEuNyJX!5e0!3m2!1sen!2s!4v1637000000000"
      width="100%"
      height="450"
      style="border:0;"
      allowfullscreen=""
      loading="lazy"
      referrerpolicy="no-referrer-when-downgrade"
      title="Mappa location Ika Ika Surf School Tenerife - Paseo Guadalajara 40, Playa de las Américas">
    </iframe>
  </div>

  <!-- Indirizzo testuale -->
  <div class="address-info">
    <h3>Indirizzo</h3>
    <address>
      <strong>Ika Ika Surf School Tenerife</strong><br>
      Paseo Guadalajara, 40<br>
      38660 Playa de las Américas<br>
      Santa Cruz de Tenerife, España
    </address>

    <p>
      <strong>Telefono:</strong>
      <a href="tel:+34603155720">+34 603 15 57 20</a>
    </p>

    <p>
      <strong>Email:</strong>
      <a href="mailto:info.ikaikasurfschool@gmail.com">info.ikaikasurfschool@gmail.com</a>
    </p>

    <p>
      <strong>Orari:</strong> Lunedì - Domenica: 09:00 - 20:00
    </p>
  </div>
</section>

<!-- CSS per responsive -->
<style>
.map-container {
  position: relative;
  overflow: hidden;
  padding-top: 56.25%; /* 16:9 Aspect Ratio */
  margin-bottom: 2rem;
}

.map-container iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}

@media (max-width: 768px) {
  .map-container {
    padding-top: 75%; /* More square on mobile */
  }
}
</style>
```

### Schema PostalAddress Aggiornato
```json
{
  "@context": "https://schema.org",
  "@type": "LocalBusiness",
  "name": "Ika Ika Surf School Tenerife",
  "image": "https://ikaikasurfschooltenerife.com/images/school-logo.jpg",
  "@id": "https://ikaikasurfschooltenerife.com",
  "url": "https://ikaikasurfschooltenerife.com",
  "telephone": "+34603155720",
  "priceRange": "€€",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "Paseo Guadalajara, 40",
    "addressLocality": "Playa de las Américas",
    "postalCode": "38660",
    "addressRegion": "Santa Cruz de Tenerife",
    "addressCountry": "ES"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": 28.064939,
    "longitude": -16.731039
  },
  "openingHoursSpecification": {
    "@type": "OpeningHoursSpecification",
    "dayOfWeek": [
      "Monday",
      "Tuesday",
      "Wednesday",
      "Thursday",
      "Friday",
      "Saturday",
      "Sunday"
    ],
    "opens": "09:00",
    "closes": "20:00"
  },
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "5",
    "reviewCount": "183"
  }
}
```

---

## 4. FAQ SCHEMA - HOMEPAGE

### Implementazione JSON-LD
```html
<!-- Inserire nel <head> o prima del </body> della homepage -->
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Cosa devo portare per la mia lezione di surf?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Forniamo tutta l'attrezzatura necessaria: tavola da surf, muta, lycra e assicurazione. Devi solo portare costume da bagno, asciugamano, crema solare e tanta voglia di imparare! Offriamo anche docce e spogliatoi gratuiti."
      }
    },
    {
      "@type": "Question",
      "name": "Offrite lezioni per principianti assoluti?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Assolutamente sì! I nostri istruttori certificati ISA sono specializzati nell'insegnamento ai principianti. Offriamo lezioni di gruppo (max 8 persone) e lezioni private 1-on-1 adatte a tutti i livelli, dai 6 anni in su."
      }
    },
    {
      "@type": "Question",
      "name": "Quanto costa una lezione di surf a Tenerife?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Le nostre lezioni di gruppo partono da 40€ a persona per una sessione di 2 ore, attrezzatura inclusa. Lezioni private 1-on-1 da 60€. Offriamo anche pacchetti multi-lezione con sconti fino al 20%. Controlla le nostre offerte speciali!"
      }
    },
    {
      "@type": "Question",
      "name": "Qual è il periodo migliore per fare surf a Tenerife?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Tenerife offre condizioni eccellenti tutto l'anno! I mesi migliori sono ottobre-marzo per onde più grandi, mentre aprile-settembre è perfetto per principianti con mare più calmo. La temperatura dell'acqua varia tra 19-24°C."
      }
    },
    {
      "@type": "Question",
      "name": "Serve esperienza precedente per iniziare?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "No! Le nostre lezioni per principianti partono dalle basi: sicurezza, tecnica di remata, pop-up e lettura delle onde. Il 90% degli studenti riesce a stare in piedi sulla tavola già nella prima lezione. Iniziamo in acque basse e sicure."
      }
    },
    {
      "@type": "Question",
      "name": "Dove si tengono le lezioni?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Le lezioni si svolgono a Playa de las Américas, una delle migliori spiagge di Tenerife per imparare il surf. La nostra scuola è situata a Paseo Guadalajara 40, a pochi passi dalla spiaggia. Selezioniamo lo spot migliore in base alle condizioni del giorno."
      }
    }
  ]
}
</script>
```

### HTML FAQ visibile sulla pagina
```html
<!-- Sezione FAQ da aggiungere alla homepage -->
<section class="faq-section" id="faq">
  <h2>Domande Frequenti</h2>

  <div class="faq-container">
    <div class="faq-item">
      <h3 class="faq-question">Cosa devo portare per la mia lezione di surf?</h3>
      <div class="faq-answer">
        <p>Forniamo tutta l'attrezzatura necessaria: tavola da surf, muta, lycra e assicurazione. Devi solo portare costume da bagno, asciugamano, crema solare e tanta voglia di imparare! Offriamo anche docce e spogliatoi gratuiti.</p>
      </div>
    </div>

    <div class="faq-item">
      <h3 class="faq-question">Offrite lezioni per principianti assoluti?</h3>
      <div class="faq-answer">
        <p>Assolutamente sì! I nostri istruttori certificati ISA sono specializzati nell'insegnamento ai principianti. Offriamo lezioni di gruppo (max 8 persone) e lezioni private 1-on-1 adatte a tutti i livelli, dai 6 anni in su.</p>
      </div>
    </div>

    <div class="faq-item">
      <h3 class="faq-question">Quanto costa una lezione di surf a Tenerife?</h3>
      <div class="faq-answer">
        <p>Le nostre lezioni di gruppo partono da 40€ a persona per una sessione di 2 ore, attrezzatura inclusa. Lezioni private 1-on-1 da 60€. Offriamo anche pacchetti multi-lezione con sconti fino al 20%. <a href="/surf-lessons/">Controlla le nostre offerte speciali</a>!</p>
      </div>
    </div>

    <!-- Aggiungi altre FAQ... -->
  </div>
</section>

<!-- CSS per stile accordion (opzionale) -->
<style>
.faq-container {
  max-width: 800px;
  margin: 0 auto;
}

.faq-item {
  margin-bottom: 1.5rem;
  border: 1px solid #e0e0e0;
  border-radius: 8px;
  overflow: hidden;
}

.faq-question {
  background: #f5f5f5;
  padding: 1rem 1.5rem;
  margin: 0;
  cursor: pointer;
  font-size: 1.1rem;
  transition: background 0.3s;
}

.faq-question:hover {
  background: #e8e8e8;
}

.faq-answer {
  padding: 1rem 1.5rem;
  background: white;
}

.faq-answer p {
  margin: 0;
  line-height: 1.6;
}
</style>
```

---

## 5. ROBOTS.TXT OTTIMIZZATO

```
# Robots.txt per Ika Ika Surf School Tenerife
# Ultimo aggiornamento: 2025-11-18

User-agent: *

# Consenti accesso a risorse importanti
Allow: /wp-admin/admin-ajax.php
Allow: /wp-content/uploads/

# Blocca aree sensibili e admin
Disallow: /wp-admin/
Disallow: /wp-includes/
Disallow: /wp-content/plugins/
Disallow: /wp-content/themes/
Disallow: /wp-content/cache/

# Blocca aree WooCommerce private
Disallow: /cart/
Disallow: /checkout/
Disallow: /my-account/
Disallow: /wp-content/uploads/wc-logs/
Disallow: /wp-content/uploads/wp-file-manager/

# Blocca parametri URL non necessari
Disallow: /*?s=
Disallow: /*?p=
Disallow: /*&
Disallow: /*/*?replytocom

# Blocca feed duplicati (opzionale)
Disallow: /feed/
Disallow: /*/feed/
Disallow: /comments/feed/

# Sitemap principale
Sitemap: https://ikaikasurfschooltenerife.com/sitemap_index.xml

# Sitemap specifici (se disponibili)
Sitemap: https://ikaikasurfschooltenerife.com/post-sitemap.xml
Sitemap: https://ikaikasurfschooltenerife.com/page-sitemap.xml
Sitemap: https://ikaikasurfschooltenerife.com/product-sitemap.xml
```

---

## 6. OPEN GRAPH TAGS COMPLETI

### Template per tutte le pagine
```html
<!-- Meta tags base (in ogni pagina) -->
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<!-- SEO Base -->
<title>Ika Ika Surf School Tenerife | Surf Lessons Playa de las Américas</title>
<meta name="description" content="Experience Ika Ika Surf School Tenerife. Expert surf lessons for all levels at Playa de las Américas. Rated 5/5 stars. Book your surf adventure today!">
<link rel="canonical" href="https://ikaikasurfschooltenerife.com/">

<!-- Open Graph / Facebook -->
<meta property="og:type" content="website">
<meta property="og:url" content="https://ikaikasurfschooltenerife.com/">
<meta property="og:title" content="Ika Ika Surf School Tenerife | Best Surf Lessons">
<meta property="og:description" content="Join expert surf lessons at Playa de las Américas. Group & private lessons for all levels. Rated 5/5 stars by 183+ students. Book today!">
<meta property="og:image" content="https://ikaikasurfschooltenerife.com/images/og-image-home.jpg">
<meta property="og:image:width" content="1200">
<meta property="og:image:height" content="630">
<meta property="og:site_name" content="Ika Ika Surf School Tenerife">
<meta property="og:locale" content="en_US">
<meta property="og:locale:alternate" content="it_IT">
<meta property="og:locale:alternate" content="es_ES">
<meta property="og:locale:alternate" content="fr_FR">
<meta property="og:locale:alternate" content="de_DE">

<!-- Twitter Card -->
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:url" content="https://ikaikasurfschooltenerife.com/">
<meta name="twitter:title" content="Ika Ika Surf School Tenerife | Best Surf Lessons">
<meta name="twitter:description" content="Expert surf lessons at Playa de las Américas. All levels welcome. Book your surf adventure in Tenerife today!">
<meta name="twitter:image" content="https://ikaikasurfschooltenerife.com/images/twitter-card-home.jpg">

<!-- Additional SEO -->
<meta name="robots" content="index, follow, max-snippet:-1, max-image-preview:large, max-video-preview:-1">
<meta name="googlebot" content="index, follow">
```

### Pagina Prodotto (esempio: Group Surf Lesson)
```html
<!-- Open Graph Product -->
<meta property="og:type" content="product">
<meta property="og:url" content="https://ikaikasurfschooltenerife.com/product/surf-lesson/">
<meta property="og:title" content="Group Surf Lesson Tenerife - €40 | Ika Ika Surf School">
<meta property="og:description" content="Join our fun group surf lessons in Tenerife! Max 8 students, 2 hours, all equipment included. Perfect for beginners. Book now!">
<meta property="og:image" content="https://ikaikasurfschooltenerife.com/images/group-lesson-og.jpg">
<meta property="product:price:amount" content="40.00">
<meta property="product:price:currency" content="EUR">
<meta property="product:availability" content="in stock">
<meta property="product:condition" content="new">
```

### Pagina Blog Post
```html
<!-- Open Graph Article -->
<meta property="og:type" content="article">
<meta property="og:url" content="https://ikaikasurfschooltenerife.com/understanding-surf-gear-for-beginners/">
<meta property="og:title" content="Understanding Surf Gear for Beginners: Essential Insights">
<meta property="og:description" content="Complete guide to surf gear for beginners in Tenerife. Learn about boards, wetsuits, and essential equipment from our expert instructors.">
<meta property="og:image" content="https://ikaikasurfschooltenerife.com/images/blog-surf-gear.jpg">
<meta property="article:published_time" content="2025-09-15T10:00:00+00:00">
<meta property="article:modified_time" content="2025-09-20T14:30:00+00:00">
<meta property="article:author" content="Ika Ika Surf School">
<meta property="article:section" content="Surf Tips">
<meta property="article:tag" content="surf gear">
<meta property="article:tag" content="beginners">
<meta property="article:tag" content="surf equipment">
```

---

## 7. INTERNAL LINKING - ESEMPI

### Da Blog a Pagine Servizio
```html
<!-- Nell'articolo "Understanding Surf Gear for Beginners" -->
<p>
  Una volta che hai familiarità con l'attrezzatura, il prossimo passo è
  <a href="/surf-lessons/"
     title="Prenota lezioni di surf per principianti a Tenerife">
    prenotare la tua prima lezione di surf
  </a>
  con i nostri istruttori certificati ISA.
</p>

<p>
  Se preferisci un'attenzione personalizzata, le nostre
  <a href="/product/1-on-1-surf-lessons/"
     title="Lezioni private di surf 1-on-1 a Playa de las Américas">
    lezioni private 1-on-1
  </a>
  sono perfette per progressi rapidi.
</p>
```

### Homepage → Pagine Interne
```html
<!-- Sezione "Why Choose Us" -->
<section class="why-choose-us">
  <h2>Perché Scegliere Ika Ika Surf School</h2>

  <ul class="benefits-list">
    <li>
      <strong>Istruttori Certificati ISA</strong> -
      <a href="/about/" title="Scopri il team Ika Ika">
        Scopri il nostro team di esperti
      </a>
    </li>
    <li>
      <strong>Attrezzatura Premium Inclusa</strong> -
      <a href="/blog/understanding-surf-gear-for-beginners/"
         title="Guida all'attrezzatura da surf">
        Leggi la nostra guida all'attrezzatura
      </a>
    </li>
    <li>
      <strong>Location Perfetta</strong> -
      <a href="/contact-us/" title="Come raggiungerci a Playa de las Américas">
        Vedi dove ci troviamo
      </a>
    </li>
  </ul>
</section>
```

### Footer Navigation (in tutte le pagine)
```html
<footer>
  <nav class="footer-navigation">
    <div class="footer-column">
      <h4>Lezioni</h4>
      <ul>
        <li>
          <a href="/surf-lessons/"
             title="Tutti i corsi di surf disponibili">
            Tutti i Corsi
          </a>
        </li>
        <li>
          <a href="/product/surf-lesson/"
             title="Lezioni di gruppo - max 8 persone">
            Lezioni di Gruppo
          </a>
        </li>
        <li>
          <a href="/product/1-on-1-surf-lessons/"
             title="Lezioni private personalizzate">
            Lezioni Private
          </a>
        </li>
        <li>
          <a href="/product/private-group-surf-lessons/"
             title="Lezioni per gruppi privati">
            Gruppi Privati
          </a>
        </li>
      </ul>
    </div>

    <div class="footer-column">
      <h4>Risorse</h4>
      <ul>
        <li>
          <a href="/blog/"
             title="Blog con consigli surf e guide">
            Blog & Consigli
          </a>
        </li>
        <li>
          <a href="/about/"
             title="Chi siamo e la nostra storia">
            Chi Siamo
          </a>
        </li>
        <li>
          <a href="/contact-us/"
             title="Contattaci per informazioni">
            Contatti
          </a>
        </li>
      </ul>
    </div>

    <div class="footer-column">
      <h4>Informazioni</h4>
      <ul>
        <li>
          <a href="/privacy-policy/"
             rel="nofollow">
            Privacy Policy
          </a>
        </li>
        <li>
          <a href="/refund_returns/"
             rel="nofollow">
            Termini e Condizioni
          </a>
        </li>
      </ul>
    </div>
  </nav>

  <!-- Schema Organization per footer -->
  <script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "Organization",
    "name": "Ika Ika Surf School Tenerife",
    "url": "https://ikaikasurfschooltenerife.com",
    "logo": "https://ikaikasurfschooltenerife.com/images/logo.png",
    "sameAs": [
      "https://www.facebook.com/ikaikasurfschool",
      "https://www.instagram.com/ikaikasurfschool"
    ]
  }
  </script>
</footer>
```

---

## 8. IMAGE OPTIMIZATION - GUIDA PRATICA

### Conversione WebP (usando plugin WordPress)

**Plugin raccomandato:** ShortPixel o Imagify

#### Configurazione ShortPixel
```
Settings → ShortPixel:
✅ Lossy compression (best for photos)
✅ Convert to WebP
✅ Optimize thumbnails
✅ Lazy load
✅ Resize large images (max 1920px width)
✅ Backup original images
```

### Responsive Images (srcset)
```html
<!-- Immagine hero responsive -->
<picture>
  <source
    type="image/webp"
    srcset="
      /images/hero-surf-400w.webp 400w,
      /images/hero-surf-800w.webp 800w,
      /images/hero-surf-1200w.webp 1200w,
      /images/hero-surf-1920w.webp 1920w"
    sizes="100vw">

  <source
    type="image/jpeg"
    srcset="
      /images/hero-surf-400w.jpg 400w,
      /images/hero-surf-800w.jpg 800w,
      /images/hero-surf-1200w.jpg 1200w,
      /images/hero-surf-1920w.jpg 1920w"
    sizes="100vw">

  <img
    src="/images/hero-surf-1200w.jpg"
    alt="Studenti Ika Ika Surf School durante lezione di gruppo a Playa de las Américas"
    width="1920"
    height="1080"
    loading="lazy">
</picture>
```

### Lazy Loading nativo
```html
<!-- Per immagini sotto la piega (below the fold) -->
<img
  src="/images/instructor-team.jpg"
  alt="Team di istruttori certificati Ika Ika Surf School Tenerife"
  width="800"
  height="600"
  loading="lazy"
  decoding="async">

<!-- Per immagini hero (above the fold) -->
<img
  src="/images/hero-main.jpg"
  alt="Surf lesson Tenerife - Ika Ika Surf School"
  width="1920"
  height="1080"
  loading="eager"
  fetchpriority="high">
```

---

## 9. CANONICAL TAGS - IMPLEMENTAZIONE

### Pagina Standard
```html
<link rel="canonical" href="https://ikaikasurfschooltenerife.com/surf-lessons/">
```

### Pagine Multilingua
```html
<!-- Versione Inglese (EN) -->
<link rel="canonical" href="https://ikaikasurfschooltenerife.com/surf-lessons/">
<link rel="alternate" hreflang="en" href="https://ikaikasurfschooltenerife.com/surf-lessons/">
<link rel="alternate" hreflang="it" href="https://ikaikasurfschooltenerife.com/it/lezioni-di-surf/">
<link rel="alternate" hreflang="es" href="https://ikaikasurfschooltenerife.com/es/clases-de-surf/">
<link rel="alternate" hreflang="fr" href="https://ikaikasurfschooltenerife.com/fr/cours-de-surf/">
<link rel="alternate" hreflang="de" href="https://ikaikasurfschooltenerife.com/de/surfkurse/">
<link rel="alternate" hreflang="x-default" href="https://ikaikasurfschooltenerife.com/surf-lessons/">

<!-- Versione Italiana (IT) -->
<link rel="canonical" href="https://ikaikasurfschooltenerife.com/it/lezioni-di-surf/">
<link rel="alternate" hreflang="en" href="https://ikaikasurfschooltenerife.com/surf-lessons/">
<link rel="alternate" hreflang="it" href="https://ikaikasurfschooltenerife.com/it/lezioni-di-surf/">
<link rel="alternate" hreflang="es" href="https://ikaikasurfschooltenerife.com/es/clases-de-surf/">
<link rel="alternate" hreflang="fr" href="https://ikaikasurfschooltenerife.com/fr/cours-de-surf/">
<link rel="alternate" hreflang="de" href="https://ikaikasurfschooltenerife.com/de/surfkurse/">
<link rel="alternate" hreflang="x-default" href="https://ikaikasurfschooltenerife.com/surf-lessons/">
```

### Pagina con Paginazione (Blog)
```html
<!-- Pagina 1 (prima pagina) -->
<link rel="canonical" href="https://ikaikasurfschooltenerife.com/blog/">
<link rel="next" href="https://ikaikasurfschooltenerife.com/blog/page/2/">

<!-- Pagina 2 -->
<link rel="canonical" href="https://ikaikasurfschooltenerife.com/blog/page/2/">
<link rel="prev" href="https://ikaikasurfschooltenerife.com/blog/">
<link rel="next" href="https://ikaikasurfschooltenerife.com/blog/page/3/">

<!-- Pagina 3 (ultima) -->
<link rel="canonical" href="https://ikaikasurfschooltenerife.com/blog/page/3/">
<link rel="prev" href="https://ikaikasurfschooltenerife.com/blog/page/2/">
```

---

## 10. PERFORMANCE - CSS CRITICAL

### Inline Critical CSS (Above the Fold)
```html
<head>
  <!-- Critical CSS inline -->
  <style>
    /* Reset base */
    *{margin:0;padding:0;box-sizing:border-box}
    body{font-family:Arial,sans-serif;line-height:1.6}

    /* Header navigation */
    header{background:#0066cc;color:#fff;padding:1rem 0}
    .logo{font-size:1.5rem;font-weight:bold}

    /* Hero section */
    .hero{
      background:url('/images/hero-surf-thumb.jpg') center/cover;
      min-height:500px;
      display:flex;
      align-items:center;
      justify-content:center;
      color:#fff
    }
    .hero h1{font-size:2.5rem;text-shadow:2px 2px 4px rgba(0,0,0,0.5)}

    /* CTA button */
    .btn-primary{
      background:#ff6600;
      color:#fff;
      padding:1rem 2rem;
      border:none;
      border-radius:5px;
      font-size:1.1rem;
      cursor:pointer
    }
  </style>

  <!-- Defer non-critical CSS -->
  <link
    rel="preload"
    href="/css/main.css"
    as="style"
    onload="this.onload=null;this.rel='stylesheet'">
  <noscript>
    <link rel="stylesheet" href="/css/main.css">
  </noscript>
</head>
```

### Preconnect a domini esterni
```html
<head>
  <!-- Preconnect Google Fonts -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

  <!-- Preconnect Google Analytics -->
  <link rel="preconnect" href="https://www.googletagmanager.com">
  <link rel="preconnect" href="https://www.google-analytics.com">

  <!-- DNS Prefetch -->
  <link rel="dns-prefetch" href="//fonts.googleapis.com">
  <link rel="dns-prefetch" href="//www.googletagmanager.com">
</head>
```

---

## CHECKLIST FINALE IMPLEMENTAZIONE

### Priorità ALTA (Questa settimana)
- [ ] Aggiungere alt text a tutte le immagini (template esempi sopra)
- [ ] Correggere H1 duplicati homepage
- [ ] Correggere H1 pagina /surf-lessons/
- [ ] Aggiungere Google Maps embed su /contact-us/
- [ ] Implementare FAQ schema homepage

### Priorità MEDIA (Prossime 2 settimane)
- [ ] Ottimizzare robots.txt
- [ ] Aggiungere canonical tags mancanti
- [ ] Implementare Open Graph completo tutte pagine
- [ ] Convertire 20 immagini principali a WebP
- [ ] Aggiungere internal links da 5 articoli blog

### Priorità BASSA (Mese prossimo)
- [ ] Implementare srcset responsive per tutte le immagini hero
- [ ] Critical CSS inline
- [ ] Preconnect domini esterni
- [ ] FAQ schema su /about/ e /surf-lessons/

---

**Ultima modifica:** 18 Novembre 2025
**Autore:** Claude Code SEO Audit

Per domande o supporto implementazione, consultare il report principale: `SEO_AUDIT_REPORT_IkaIkaSurfSchool.md`
