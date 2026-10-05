# LO-tools

Minimalistische GitHub Pages-homepage met eenvoudige adminpagina.

## Bestanden
- `index.html` — publieke homepage
- `admin.html` — beheer: toevoegen, bewerken, verwijderen, verbergen, uitlichten en volgorde wijzigen
- `tools.json` — gegevensbron voor de homepage

## Lokaal testen
Door browserbeveiliging werkt `fetch('tools.json')` niet altijd wanneer je `index.html` rechtstreeks dubbelklikt. Start daarom in deze map een kleine lokale webserver, bijvoorbeeld op Mac:

```bash
python3 -m http.server 8000
```

Open daarna `http://localhost:8000` en `http://localhost:8000/admin.html`.

Alle beheerfuncties kunnen lokaal als concept getest worden. **Publiceren** werkt pas wanneer de bestanden in een GitHub-repository staan en je de GitHub-koppeling invult.

## GitHub publiceren
Maak een repository (bijvoorbeeld `lo-tools`), upload deze drie bestanden en activeer GitHub Pages voor de `main` branch/root.

Voor de adminpagina maak je een fine-grained GitHub personal access token dat uitsluitend toegang heeft tot deze repository en alleen `Contents: Read and write` krijgt. Vul gebruikersnaam, repository en token in op `admin.html`. Het token wordt niet lokaal opgeslagen.

> Een geheime URL naar `admin.html` is geen echte beveiliging. Zonder het GitHub-token kan iemand echter niets naar de repository publiceren.


## Admin
De beheerpagina staat in `beheer-k7m4x9q2.html`. De GitHub-token wordt na de eerste invoer lokaal in de browser opgeslagen (localStorage) en niet in de repository.
