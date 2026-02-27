# Coach Raffael - IT Coaching & Mentoring

Professionelle Landingpage für IT-Coaching und Mentoring Services.

## 🚀 Live Demo

Nach dem Deployment verfügbar unter: `https://dein-username.github.io/Coach-Raffael/`

## 📋 Inhalt

- **Dark Theme** mit blauen Akzenten
- **Responsives Design** für alle Geräte
- **Kontaktformular** mit Formspree Integration
- **Social Links** zu GitHub, LinkedIn, Twitter
- **SEO optimiert** für IT-Coaching Keywords

## 🛠️ Technologien

- HTML5
- CSS3 (Custom Properties)
- Vanilla JavaScript
- Font Awesome Icons
- Google Fonts (Inter)

## 📁 Struktur

```
Coach-Raffael/
├── index.html              # Hauptseite
├── styles.css              # Stylesheet
├── script.js               # JavaScript Funktionen
├── .github/
│   └── workflows/
│       └── deploy.yml      # GitHub Actions Deployment
└── README.md               # Diese Datei
```

## 🚀 Deployment

### Schritt 1: Repository erstellen

1. Gehe zu [github.com/new](https://github.com/new)
2. Repository-Name: `Coach-Raffael`
3. Wähle "Public"
4. Klicke "Create repository"

### Schritt 2: Dateien hochladen

```bash
# Lokalen Ordner erstellen
git clone https://github.com/dein-username/Coach-Raffael.git
cd Coach-Raffael

# Alle Dateien kopieren (aus diesem Template)
# Dann:
git add .
git commit -m "Initial commit"
git push origin main
```

### Schritt 3: GitHub Pages aktivieren

1. Gehe zu **Settings** → **Pages**
2. Source: **GitHub Actions**
3. Das Deployment startet automatisch

### Schritt 4: Formspree konfigurieren

1. Gehe zu [formspree.io](https://formspree.io)
2. Erstelle ein neues Formular
3. Kopiere die Form-ID
4. Ersetze in `index.html`:
   ```html
   action="https://formspree.io/f/YOUR_FORM_ID"
   ```

## ✏️ Anpassungen

### Persönliche Daten

Bearbeite in `index.html`:
- **Zeile 13**: Titel ändern
- **Zeile 20**: Email-Adresse
- **Zeile 21**: Telefonnummer
- **Zeile 22**: LinkedIn URL
- **Social Links** im Footer

### Farben

In `styles.css` Zeile 2-12:
```css
:root {
    --primary: #3b82f6;        /* Hauptfarbe */
    --primary-hover: #2563eb;  /* Hover */
    --primary-light: #60a5fa;  /* Hell */
    --bg-dark: #0f172a;        /* Hintergrund */
    --bg-card: #1e293b;        /* Karten */
    /* ... */
}
```

### Bilder

Ersetze den Platzhalter im About-Bereich:
```html
<!-- Zeile ~94 -->
<div class="about-image-placeholder">
    <img src="dein-bild.jpg" alt="Raffael">
</div>
```

## 📱 Features

- ✅ Smooth Scrolling Navigation
- ✅ Animations on Scroll
- ✅ Responsive Mobile Menu
- ✅ Form Validation
- ✅ Social Media Integration
- ✅ SEO Meta Tags
- ✅ Fast Loading

## 📞 Kontakt

- Email: contact@coach-raffael.de
- LinkedIn: /in/coach-raffael
- GitHub: /coach-raffael

---

**© 2025 Coach Raffael - Alle Rechte vorbehalten**
