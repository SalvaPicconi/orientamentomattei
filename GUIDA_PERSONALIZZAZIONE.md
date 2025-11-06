# 🎨 Guida Rapida Personalizzazione

## 1️⃣ Modificare i Colori

Apri `style.css` e modifica le variabili all'inizio del file:

```css
:root {
    /* COLORI PRINCIPALI - Modifica questi per cambiare l'intero tema */
    --primary-green: #1a8c73;    /* Verde principale */
    --primary-pink: #e91e63;     /* Rosa accento */
    --primary-cyan: #00bcd4;     /* Azzurro */
    --primary-lime: #8bc34a;     /* Verde lime */
}
```

## 2️⃣ Sostituire le Immagini

### Logo della Scuola
1. Prepara il logo in formato PNG (sfondo trasparente)
2. Salvalo come `images/logo.png`
3. Apri `index.html` e cerca il tag logo

### Foto Hero (Scuola)
1. Sostituisci `images/page_1_img_1.png` con una foto di alta qualità
2. Oppure modifica in `style.css` alla riga `.school-photo`

### Altre Immagini
- Laboratori: `images/page_13_img_X.png`
- Progetti: `images/page_15_img_X.png`
- Open Day: `images/page_21_img_X.png`

## 3️⃣ Aggiornare i Testi

### Date Open Day
Cerca in `index.html`:
```html
<div class="date-card primary">
    <h3>13 Dicembre</h3> <!-- MODIFICA QUI -->
    <p class="time">dalle 9:00 alle 13:00</p>
</div>
```

### Contatti
Cerca la sezione `<section class="section contatti">`:
```html
<p class="large-text">070 4657043</p> <!-- MODIFICA QUI -->
<p>orientamattei@gmail.com</p> <!-- MODIFICA QUI -->
```

### Link Social
```html
<a href="https://instagram.com/ILTUOACCOUNT" class="social-btn instagram">
<a href="https://facebook.com/LATUAPAGINA" class="social-btn facebook">
```

## 4️⃣ Aggiungere/Rimuovere Indirizzi di Studio

Cerca la sezione `<div class="indirizzi-grid">` e copia/modifica questo blocco:

```html
<div class="indirizzo-card">
    <div class="card-header COLORECLASSE">
        <h4>NOME INDIRIZZO</h4>
        <p class="subtitle">Descrizione breve</p>
    </div>
    <div class="card-body">
        <!-- Contenuto -->
    </div>
</div>
```

Colori disponibili per `COLORECLASSE`:
- `afm` - Gradiente viola
- `sia` - Gradiente rosa
- `turismo` - Gradiente azzurro
- `cat` - Gradiente verde
- `ssas` - Gradiente giallo-rosa

## 5️⃣ Modificare il Menu di Navigazione

Cerca `<ul class="nav-menu">` in `index.html`:

```html
<li><a href="#sezione" class="nav-link">Nome Voce</a></li>
```

Assicurati che `#sezione` corrisponda all'`id` della sezione nel contenuto:
```html
<section class="section" id="sezione">
```

## 6️⃣ Cambiare i Font

Nel file `index.html`, cerca:
```html
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@...">
```

Vai su [Google Fonts](https://fonts.google.com/), scegli un font e sostituisci il link.

Poi in `style.css` aggiorna:
```css
body {
    font-family: 'NuovoFont', sans-serif;
}
```

## 7️⃣ Aggiungere Google Analytics

Prima del tag `</head>` in `index.html`:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=TUO-ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'TUO-ID');
</script>
```

## 8️⃣ Aggiungere un Form di Contatto

Opzione A - EmailJS (Gratuito):
1. Crea account su [EmailJS](https://www.emailjs.com/)
2. Configura il servizio
3. Aggiungi questo codice prima di `</body>`:

```html
<script src="https://cdn.jsdelivr.net/npm/@emailjs/browser@3/dist/email.min.js"></script>
<script>
    emailjs.init('TUO_PUBLIC_KEY');
</script>
```

Opzione B - Formspree (Gratuito):
```html
<form action="https://formspree.io/f/TUO_ID" method="POST">
  <input type="email" name="email" required>
  <textarea name="message" required></textarea>
  <button type="submit">Invia</button>
</form>
```

## 9️⃣ Ottimizzare le Immagini

### Online (Consigliato):
- [TinyPNG](https://tinypng.com/) - Compressione PNG/JPG
- [Squoosh](https://squoosh.app/) - Conversione WebP

### Dimensioni Consigliate:
- Hero image: 1920x1080px
- Card images: 600x400px
- Icons: 200x200px
- Logo: 500x500px

## 🔟 Test e Pubblicazione

### Test Locale:
1. Apri `index.html` in Chrome
2. Premi F12 per aprire DevTools
3. Testa su diverse dimensioni (icona mobile)

### Test Online:
1. Carica su hosting
2. Testa velocità: [PageSpeed Insights](https://pagespeed.web.dev/)
3. Controlla responsive: [Responsive Design Checker](https://responsivedesignchecker.com/)

## 📚 Risorse Utili

- **Icone**: [Font Awesome](https://fontawesome.com/), [Flaticon](https://www.flaticon.com/)
- **Immagini**: [Unsplash](https://unsplash.com/), [Pexels](https://www.pexels.com/)
- **Colori**: [Coolors](https://coolors.co/), [Adobe Color](https://color.adobe.com/)
- **Font**: [Google Fonts](https://fonts.google.com/)

## ⚠️ Note Importanti

1. **Backup**: Fai sempre una copia prima di modificare
2. **Browser**: Svuota la cache (Ctrl+F5) per vedere le modifiche
3. **Immagini**: Mantieni nomi file senza spazi e caratteri speciali
4. **Mobile**: Testa sempre su dispositivi reali, non solo nel browser

## 🆘 Problemi Comuni

**Il menu non funziona su mobile**
→ Controlla che `script.js` sia caricato correttamente

**Le animazioni sono lente**
→ Riduci le dimensioni delle immagini

**I colori non cambiano**
→ Svuota la cache del browser (Ctrl+Shift+Del)

**Il sito non si vede bene su mobile**
→ Verifica che ci sia il tag viewport in `<head>`:
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

---

**Buona personalizzazione! 🚀**
