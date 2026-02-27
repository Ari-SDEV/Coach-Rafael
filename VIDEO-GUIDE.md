# Video Snippets Guide für Coach-Raffael

## 📁 Ordnerstruktur

```
assets/
└── videos/
    ├── ki-integration.mp4        # AI/Integration Video
    ├── software-dev.mp4          # Coding Video
    ├── lectures.mp4              # Teaching Video
    ├── ki-integration-fallback.gif # Fallback GIF
    ├── software-dev-fallback.gif
    ├── lectures-fallback.gif
    ├── ai-thumb.jpg              # Thumbnail
    ├── dev-thumb.jpg
    └── lecture-thumb.jpg
```

## 🎬 Video-Spezifikationen

### Format
- **Format:** MP4 (H.264 codec)
- **Auflösung:** 1280x720 (16:9)
- **Länge:** 5-15 Sekunden
- **Loop:** Nahtlos wiederholbar
- **Audio:** Kein Ton (muted)

### Video-Attribute
Das Video wird automatisch:
- **autoplay** - Startet automatisch
- **loop** - Wiederholt endlos
- **muted** - Ohne Ton
- **playsinline** - Spielt auf Mobilgeräten inline ab

## 🎥 Video-Ideen

### 1. KI Integration (ki-integration.mp4)
**Was zeigen:**
- OpenClaw Interface
- KI-Chat oder Automatisierung
- Beispiel: "Hallo OpenClaw" → Antwort generieren
- Code-Generierung durch KI
- Kurzer Workflow: Prompt eingeben → Ergebnis

**Tip:** Bildschirmaufnahme mit OBS oder ShareX

### 2. Software Development (software-dev.mp4)
**Was zeigen:**
- Code schreiben in IDE (VS Code)
- Tippen, Kompilieren, Ergebnis
- Terminal-Befehle ausführen
- Git commit/push
- Kurze Build-Animation

**Tip:** 10-15 Sekunden, schneller Tippen zeigen

### 3. Lectures (lectures.mp4)
**Was zeigen:**
- Whiteboard oder Präsentation
- Erklären eines Konzepts (Code, Diagramm)
- Kurze Unterrichtsszene
- Schüler/Student reagiert
- Virtuelles Classroom Setup

**Tip:** Webcam-Aufnahme mit gutem Licht

## 🛠️ Tools für Video-Erstellung

### Bildschirmaufnahme
- **Windows:** OBS Studio (kostenlos)
- **Mac:** QuickTime Player (eingebaut)
- **Linux:** SimpleScreenRecorder

### Video-Bearbeitung (kostenlos)
- **DaVinci Resolve** - Professionell
- **Shotcut** - Einfach
- **OpenShot** - Anfängerfreundlich

### GIF als Fallback erstellen
Falls Video nicht lädt:
```bash
# Mit ffmpeg: Video zu GIF konvertieren
ffmpeg -i ki-integration.mp4 -vf "fps=30,scale=480:-1:flags=lanczos" ki-integration-fallback.gif
```

## 📤 Videos hinzufügen

1. **Videos erstellen** (siehe oben)
2. **In Ordner legen:** `assets/videos/`
3. **Git commit:**
   ```bash
   git add assets/videos/
   git commit -m "feat: Add showcase videos"
   git push origin master
   ```
4. **Deployment** läuft automatisch

## ⚡ Performance-Tipps

- **Video-Größe:** Max 2-5 MB pro Video
- **Komprimierung:** HandBrake oder ffmpeg
- **WebM Alternative:** Für bessere Performance
  ```html
  <source src="assets/videos/ki-integration.webm" type="video/webm">
  <source src="assets/videos/ki-integration.mp4" type="video/mp4">
  ```

## 🎯 Beispiel: Loop-Video erstellen

Mit ffmpeg:
```bash
# Aus mehreren Bildern ein Loop-Video erstellen
ffmpeg -framerate 30 -pattern_type glob -i "*.png" -c:v libx264 -pix_fmt yuv420p output.mp4

# Oder: Bestehendes Video trimmen und loopen
ffmpeg -i input.mp4 -t 10 -c copy output.mp4
```

## 🖼️ Thumbnails erstellen

Aus dem ersten Frame des Videos:
```bash
ffmpeg -i ki-integration.mp4 -ss 00:00:00 -vframes 1 ai-thumb.jpg
```

## ✅ Checkliste vor Upload

- [ ] Video ist MP4 Format
- [ ] Länge: 5-15 Sekunden
- [ ] Größe: Unter 5 MB
- [ ] Auflösung: 1280x720 (16:9)
- [ ] Kein Ton (oder muted)
- [ ] Smooth Loop
- [ ] Fallback GIF erstellt
- [ ] Thumbnail erstellt
- [ ] Im assets/videos/ Ordner

## 📱 Mobile Optimierung

Für mobile Geräte:
- Kleinere Dateien (< 2 MB)
- Niedrigere Auflösung (720p statt 1080p)
- WebM Format zusätzlich

---

**Hinweis:** Solange keine Videos vorhanden sind, zeigt die Seite das Fallback-Bild/GIF an.
