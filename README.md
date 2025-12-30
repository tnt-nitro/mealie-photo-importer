# Mealie Photo Importer (Proof of Concept)

## 🇩🇪 Deutsch

### Idee
Mealie kann Rezepte aus **URLs** und **Bildern** anlegen,  
führt aber **keine Texterkennung (OCR)** auf Fotos durch.

Viele Rezepte liegen jedoch als **Fotos** vor:
- Kochbücher
- Rezeptzeitschriften
- handschriftliche Notizen
- abfotografierte Ausdrucke

Dieses Projekt untersucht, wie man **Rezepte aus Fotos automatisch erfassen**
und **über die Mealie API** importieren kann.

---

### Ziel
Ein externes Tool (kein Mealie-Core-Code), das:

1. ein **Foto** entgegennimmt
2. **Text per OCR** extrahiert
3. den Text **strukturiert** (Titel, Zutaten, Anleitung)
4. ein **Rezept über die Mealie API** anlegt
5. das Originalbild als **Rezeptbild** speichert

---

### Nicht-Ziele
- ❌ Kein Ersatz für Mealie
- ❌ Keine Änderungen am Mealie-Core
- ❌ Kein perfektes OCR-Ergebnis
- ❌ Keine KI-Pflicht (regelbasierte Ansätze sind erlaubt)

---

### Motivation
- Erweiterung der bestehenden Mealie-Funktionalität
- Klare Trennung zwischen Core und externem Tool
- Transparente, nachvollziehbare Implementierung
- Einladung an andere Entwickler, das Konzept zu verbessern

---

### Projektstatus
🟡 **Konzeptphase**

Noch keine Implementierung.  
Das Repository dient zunächst der:
- Dokumentation
- Strukturierung
- Planung

---

### Geplante Phasen (Roadmap – grob)

**Phase 0 – Konzept**
- Zieldefinition
- Abgrenzung
- API-Analyse

**Phase 1 – Lokales Tool**
- Dateiauswahl (Windows)
- Bild laden
- OCR-Rohtext anzeigen

**Phase 2 – Strukturierung**
- Zutaten erkennen
- Anleitung erkennen
- Titel extrahieren

**Phase 3 – Mealie-Integration**
- API-Token
- Rezept anlegen
- Bild hochladen

**Phase 4 – Qualität**
- Logging
- Fehlerfälle dokumentieren
- Beispielbilder

---

### Lizenz
MIT (vorgesehen)

---

## 🇬🇧 English

### Idea
Mealie supports creating recipes from **URLs** and **images**,  
but it **does not perform OCR** on photos.

Many recipes exist only as images:
- cookbooks
- magazines
- handwritten notes
- photographed printouts

This project explores how to **extract recipes from photos**
and **import them via the Mealie API**.

---

### Goal
An external tool (not part of Mealie core) that:

1. accepts a **photo**
2. extracts text via **OCR**
3. structures the content (title, ingredients, instructions)
4. creates a recipe via the **Mealie API**
5. attaches the original image as the recipe image

---

### Non-Goals
- ❌ Not a replacement for Mealie
- ❌ No Mealie core modifications
- ❌ No perfect OCR guarantee
- ❌ No mandatory AI usage

---

### Motivation
- Extend Mealie without touching core code
- Keep implementation transparent and understandable
- Provide a foundation others can build upon

---

### Project Status
🟡 **Concept phase**

No implementation yet.  
This repository currently focuses on:
- documentation
- structure
- planning

---

### Planned Phases (High-Level Roadmap)

**Phase 0 – Concept**
- scope definition
- API analysis

**Phase 1 – Local Tool**
- file picker (Windows)
- image loading
- raw OCR output

**Phase 2 – Structuring**
- ingredient detection
- instruction parsing
- title extraction

**Phase 3 – Mealie Integration**
- API token handling
- recipe creation
- image upload

**Phase 4 – Quality**
- logging
- error documentation
- example images

---

### License
MIT (planned)
