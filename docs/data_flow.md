# Minimaler Datenfluss | Minimal Data Flow

## Deutsch

**Quelle:**  

- Foto (PC / Smartphone)  
- URL (Rezept-Webseite)  
- ZIP / HTML / JSON  

**Verarbeitung:**  

- Optional: Vorverarbeitung (z. B. externes OCR oder Parsing)  
- Übergabe an Mealie API  

**Ziel:**  

- POST /api/recipes/create/image  
- POST /api/recipes/create/url  
- POST /api/recipes  

**Ergebnis:**  

- Rezept ist in Mealie gespeichert  
- Bilder und Metadaten sind zugeordnet  

---

## English

**Source:**  

- Photo (PC / smartphone)  
- URL (recipe website)  
- ZIP / HTML / JSON  

**Processing:**  

- Optional preprocessing (e.g. external OCR or parsing)  
- Hand-off to Mealie API  

**Target:**  

- POST /api/recipes/create/image  
- POST /api/recipes/create/url  
- POST /api/recipes  

**Result:**  

- Recipe is stored in Mealie  
- Images and metadata are associated
