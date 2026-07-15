# CV-kilder

HTML-kilderne bag de downloadbare CV-PDF'er i `assets/`:

| Kilde | Genererer |
|---|---|
| `cv-en.html` | `assets/cv-morten-lundum-noergaard.pdf` (engelsk) |
| `cv-da.html` | `assets/cv-morten-lundum-noergaard-da.pdf` (dansk) |

Designet matcher forsidens "Flow"-tema (Archivo/Inter/JetBrains Mono, blæk-blå header, lime/cyan-accenter). Fontene hentes fra Google Fonts, så filerne kræver internetforbindelse for at rendere korrekt.

## Sådan opdaterer du CV'et

1. Ret teksten i `cv-en.html` og/eller `cv-da.html`
2. Generér PDF — enten i browseren (åbn filen i Chrome → Print → "Gem som PDF", A4, marginer: Ingen, "Baggrundsgrafik" slået til) eller fra terminalen:

   ```bash
   chrome --headless --print-to-pdf=assets/cv-morten-lundum-noergaard.pdf \
     --no-pdf-header-footer --print-to-pdf-no-header cv-src/cv-en.html
   chrome --headless --print-to-pdf=assets/cv-morten-lundum-noergaard-da.pdf \
     --no-pdf-header-footer cv-src/cv-da.html
   ```

   (`chrome` kan hedde `google-chrome`, `chromium` eller `chromium-browser` afhængigt af system.)

3. Commit begge HTML- og PDF-filer

**Husk:** Indholdet skal holdes synkront på tværs af de to sprog — og telefonnummeret er bevidst udeladt, da PDF'erne kan downloades frit fra hjemmesiden.
