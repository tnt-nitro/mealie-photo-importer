# Mealie API – Relevante Endpoints | Relevant Endpoints

Dieses Dokument beschreibt die für das Projekt relevanten Mealie-API-Endpoints
und deren Zweck.

This document describes the Mealie API endpoints that are relevant for this project
and their purpose.

---

## POST Endpoints

### POST /api/recipes

**Zweck (DE):**  
Erstellt ein neues Rezept aus strukturierten Daten (JSON), ohne automatische Analyse.

**Typischer Einsatz:**  

- Eigener Importer  
- Manuell vorbereitete Rezeptdaten  
- Ziel-Endpoint nach Vorverarbeitung (z. B. externes OCR)

**Purpose (EN):**  
Creates a new recipe from structured data (JSON) without automatic parsing.

**Typical use:**  

- Custom importer  
- Manually prepared recipe data  
- Target endpoint after preprocessing (e.g. external OCR)

---

### POST /api/recipes/create/image

**Zweck (DE):**  
Erstellt ein neues Rezept aus einem Bild (Foto eines Rezepts).  
OCR und Parsing erfolgen automatisch.

**Typischer Einsatz:**  

- Rezeptfoto vom Smartphone oder PC  
- Schneller Import ohne manuelle Dateneingabe

**Purpose (EN):**  
Creates a new recipe from an image (photo of a recipe).  
OCR and parsing are performed automatically.

**Typical use:**  

- Recipe photo from smartphone or computer  
- Quick import without manual data entry

---

### POST /api/recipes/create/html-or-json

**Zweck (DE):**  
Erstellt ein Rezept aus HTML- oder JSON-Daten (z. B. aus exportierten Webseiten).

**Typischer Einsatz:**  

- Import aus bestehenden Rezept-Webseiten  
- Verarbeitung bereits strukturierter Daten

**Purpose (EN):**  
Creates a recipe from HTML or JSON data (e.g. exported from recipe websites).

**Typical use:**  

- Import from existing recipe websites  
- Processing already structured data

---

### POST /api/recipes/create/url

**Zweck (DE):**  
Erstellt ein Rezept durch Scraping einer einzelnen Rezept-URL.

**Typischer Einsatz:**  

- Import eines einzelnen Online-Rezepts  
- Direkte Übernahme aus dem Web

**Purpose (EN):**  
Creates a recipe by scraping a single recipe URL.

**Typical use:**  

- Import of a single online recipe  
- Direct web-based recipe import

---

### POST /api/recipes/create/url/bulk

**Zweck (DE):**  
Erstellt mehrere Rezepte durch Scraping mehrerer URLs in einem Durchlauf.

**Typischer Einsatz:**  

- Massenimport aus Lesezeichen oder Listen  
- Migration bestehender Rezeptsammlungen

**Purpose (EN):**  
Creates multiple recipes by scraping several URLs in one run.

**Typical use:**  

- Bulk import from bookmarks or lists  
- Migration of existing recipe collections

---

### POST /api/recipes/create/zip

**Zweck (DE):**  
Importiert mehrere Rezepte aus einem ZIP-Archiv.

**Typischer Einsatz:**  

- Backup-Import  
- Migration aus anderen Systemen

**Purpose (EN):**  
Imports multiple recipes from a ZIP archive.

**Typical use:**  

- Backup import  
- Migration from other systems

---

## Optional / Gut zu haben | Optional / Nice to have

### POST /api/recipes/{slug}/image

**Zweck (DE):**  
Fügt einem bestehenden Rezept nachträglich ein Bild hinzu oder ersetzt es.

**Purpose (EN):**  
Adds or replaces an image for an existing recipe.

---

### POST /api/recipes/{slug}/assets

**Zweck (DE):**  
Hängt zusätzliche Dateien (Assets) an ein bestehendes Rezept an.

**Purpose (EN):**  
Attaches additional files (assets) to an existing recipe.

---

## Randfall | Edge case

### POST /api/recipes/test-scrape-url

**Zweck (DE):**  
Testet, ob eine URL erfolgreich gescraped werden kann,  
ohne ein Rezept anzulegen.

**Purpose (EN):**  
Tests whether a URL can be scraped successfully  
without creating a recipe.

## GET Endpoints

### GET /api/recipes

**Zweck (DE):**  
Ruft eine Liste aller Rezepte ab (inkl. Filter-, Such- und Paginierungsoptionen).

**Typischer Einsatz:**  

- Übersicht aller Rezepte  
- Prüfen, ob ein Rezept bereits existiert  
- Synchronisations- und Abgleichslogik

**Purpose (EN):**  
Retrieves a list of all recipes (including filtering, search, and pagination options).

**Typical use:**  

- Overview of all recipes  
- Check if a recipe already exists  
- Synchronization and comparison logic

---

### GET /api/recipes/{slug}

**Zweck (DE):**  
Ruft die vollständigen Daten eines einzelnen Rezepts anhand des Slugs ab.

**Typischer Einsatz:**  

- Detailansicht eines Rezepts  
- Weiterverarbeitung oder Export  
- Validierung nach Import

**Purpose (EN):**  
Retrieves the full data of a single recipe identified by its slug.

**Typical use:**  

- Detailed recipe view  
- Further processing or export  
- Validation after import

---

### GET /api/recipes/{slug}/image

**Zweck (DE):**  
Ruft das Hauptbild eines Rezepts ab.

**Typischer Einsatz:**  

- Anzeige oder Download des Rezeptbildes  
- Prüfung, ob ein Bild vorhanden ist

**Purpose (EN):**  
Retrieves the main image of a recipe.

**Typical use:**  

- Display or download recipe image  
- Check whether an image exists

---

### GET /api/recipes/{slug}/assets

**Zweck (DE):**  
Ruft alle zugehörigen Assets (Anhänge) eines Rezepts ab.

**Typischer Einsatz:**  

- Auflisten zusätzlicher Dateien  
- Export oder Backup von Rezeptanhängen

**Purpose (EN):**  
Retrieves all assets (attachments) associated with a recipe.

**Typical use:**  

- List additional files  
- Export or backup recipe attachments
