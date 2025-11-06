# 🚀 Guida Rapida Pubblicazione Online

## Opzioni di Hosting (dal più facile al più avanzato)

### ⚡ OPZIONE 1: Netlify (CONSIGLIATA - GRATUITA)

**Tempo: 2 minuti**

1. Vai su [netlify.com](https://www.netlify.com/)
2. Clicca "Sign up" (puoi usare GitHub, GitLab o email)
3. Una volta loggato, trascina l'intera cartella del sito nell'area "Drop"
4. **FATTO!** Il sito è online con un URL tipo: `nome-random.netlify.app`

**Vantaggi:**
- ✅ Completamente gratuito
- ✅ HTTPS automatico
- ✅ Deploy in 30 secondi
- ✅ Dominio personalizzato possibile
- ✅ Aggiornamenti semplicissimi (drag & drop)

---

### 🌐 OPZIONE 2: GitHub Pages (GRATUITA)

**Tempo: 5 minuti**

1. Crea un account su [github.com](https://github.com/) se non ce l'hai
2. Clicca "New repository"
3. Nome: `meucci-mattei-decimomannu` (o quello che vuoi)
4. Seleziona "Public"
5. Clicca "Create repository"
6. Carica tutti i file:
   - Clicca "uploading an existing file"
   - Trascina tutti i file e cartelle
   - Clicca "Commit changes"
7. Vai su Settings > Pages
8. Sotto "Source" seleziona "main" branch
9. Clicca "Save"
10. **FATTO!** Il sito sarà disponibile su: `tuousername.github.io/meucci-mattei-decimomannu`

**Vantaggi:**
- ✅ Gratuito per sempre
- ✅ HTTPS incluso
- ✅ Ideale per progetti scolastici
- ✅ Controllo versioni incluso

---

### ☁️ OPZIONE 3: Vercel (GRATUITA)

**Tempo: 2 minuti**

Praticamente identica a Netlify:

1. Vai su [vercel.com](https://vercel.com/)
2. Sign up (usa GitHub per semplicità)
3. Clicca "Add New Project"
4. Trascina la cartella del sito
5. Clicca "Deploy"
6. **FATTO!** URL tipo: `meucci-mattei.vercel.app`

---

### 🏢 OPZIONE 4: Hosting Tradizionale (A PAGAMENTO)

**Esempio: Aruba, SiteGround, HostGator, ecc.**

**Tempo: 10-15 minuti**

1. Acquista un piano hosting (da 30-50€/anno)
2. Scarica un client FTP (FileZilla è gratuito)
3. Connettiti con le credenziali fornite dall'hosting
4. Carica tutti i file nella cartella `public_html` o `www`
5. **FATTO!** Il sito sarà su `tuodominio.it`

**Quando scegliere questa opzione:**
- Vuoi un dominio personalizzato tipo `iismattei-decimomannu.it`
- Hai budget (30-100€/anno)
- Vuoi email personalizzate (@iismattei.it)
- Serve supporto tecnico professionale

**Provider consigliati in Italia:**
- Aruba.it (più usato in Italia)
- SiteGround.com (ottimo supporto)
- Register.it
- Keliweb.it

---

## 🎯 Quale Opzione Scegliere?

### Per iniziare SUBITO e GRATIS:
**→ Netlify o Vercel** (consigliato)

### Se vuoi un progetto educativo su GitHub:
**→ GitHub Pages**

### Se hai budget e vuoi dominio personalizzato:
**→ Hosting tradizionale** + dominio personalizzato

---

## 📝 Dopo la Pubblicazione

### 1. Testa il Sito
- Apri su diversi dispositivi (PC, tablet, smartphone)
- Verifica che tutte le immagini si carichino
- Testa tutti i link e pulsanti
- Controlla il menu mobile

### 2. Ottimizza per Google

Aggiungi questo nel `<head>` di `index.html`:

```html
<!-- SEO Meta Tags -->
<meta name="description" content="IIS Meucci-Mattei Sede Decimomannu. Una strada per ogni passione, un indirizzo per ogni attitudine. Scopri i nostri indirizzi di studio: AFM, SIA, Turismo, CAT Archeo Design e SSAS.">
<meta name="keywords" content="IIS Meucci Mattei, Decimomannu, scuola superiore, AFM, SIA, Turismo, CAT, SSAS, liceo, istituto tecnico">
<meta name="author" content="IIS Meucci-Mattei">

<!-- Open Graph per Social Media -->
<meta property="og:title" content="IIS Meucci-Mattei - Sede Decimomannu">
<meta property="og:description" content="Una strada per ogni passione, un indirizzo per ogni attitudine!">
<meta property="og:image" content="URL_IMMAGINE_ANTEPRIMA">
<meta property="og:url" content="URL_TUO_SITO">
<meta property="og:type" content="website">
```

### 3. Configura Google Analytics

1. Vai su [analytics.google.com](https://analytics.google.com/)
2. Crea un account
3. Ottieni il codice di tracking
4. Incollalo prima di `</head>` in `index.html`

### 4. Aggiungi Google Search Console

1. Vai su [search.google.com/search-console](https://search.google.com/search-console)
2. Aggiungi la proprietà (URL del sito)
3. Verifica la proprietà
4. Invia la sitemap (vedi sotto come crearla)

---

## 🗺️ Creare una Sitemap (Opzionale ma Consigliato)

Crea un file `sitemap.xml`:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url>
    <loc>URL_TUO_SITO</loc>
    <lastmod>2025-01-01</lastmod>
    <priority>1.0</priority>
  </url>
</urlset>
```

Caricalo nella root del sito insieme a `index.html`.

---

## 🔒 SSL/HTTPS

**Netlify, Vercel e GitHub Pages:** HTTPS automatico ✅

**Hosting tradizionale:** 
- Alcuni hosting includono SSL gratuito (Let's Encrypt)
- Altrimenti chiedi supporto tecnico per attivarlo
- Costo: 0-50€/anno

---

## 📊 Monitorare le Prestazioni

Testa velocità del sito:
- [PageSpeed Insights](https://pagespeed.web.dev/)
- [GTmetrix](https://gtmetrix.com/)

Obiettivi:
- ✅ PageSpeed Score > 90
- ✅ Tempo caricamento < 3 secondi
- ✅ Mobile-friendly: 100%

---

## 🔄 Aggiornare il Sito

### Netlify/Vercel:
Trascina di nuovo la cartella aggiornata → Deploy automatico

### GitHub Pages:
Carica i file modificati su GitHub → Aggiornamento automatico

### Hosting tradizionale:
Carica i file modificati via FTP

---

## ⚠️ Checklist Finale Prima della Pubblicazione

- [ ] Tutte le immagini sono ottimizzate
- [ ] Link social media aggiornati con URL reali
- [ ] Date Open Day aggiornate
- [ ] Contatti (email, telefono) verificati
- [ ] Link form prenotazioni funzionante
- [ ] Testato su Chrome, Firefox, Safari
- [ ] Testato su mobile
- [ ] Meta tags SEO aggiunti
- [ ] Google Analytics configurato (opzionale)
- [ ] Favicon aggiunto (opzionale)

---

## 🆘 Problemi Comuni

**"Il sito non si aggiorna"**
→ Svuota cache browser (Ctrl+Shift+Del)

**"Le immagini non si vedono"**
→ Verifica che la cartella `images/` sia stata caricata

**"Il menu non funziona"**
→ Controlla che `script.js` sia stato caricato

**"Errore 404"**
→ Verifica che `index.html` sia nella root

---

## 📞 Supporto

Per domande tecniche:
- 📧 orientamattei@gmail.com
- 📞 070 4657043

Per problemi con l'hosting:
- Controlla la documentazione del provider
- Contatta il supporto tecnico dell'hosting

---

## 🎉 Congratulazioni!

Una volta pubblicato, condividi il link:
- Con studenti e famiglie
- Sui social media della scuola
- Nella firma email
- Nei materiali informativi

**Il tuo sito è pronto per il mondo! 🚀**

---

*Ultimo aggiornamento: Novembre 2025*
