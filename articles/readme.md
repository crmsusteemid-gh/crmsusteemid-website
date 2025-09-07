# Artiklite süsteem - CRM Systems veebileht

See kaust sisaldab CRM Systems veebilehe artikleid ja blogipostitusi.

## Failide struktuur

```
articles/
├── README.md           # See juhend
├── index.json          # Artiklite nimekiri (metaandmed)
├── artikli-slug.md     # Artikli sisu (Markdown vormingus)
├── images/             # Artiklite pildid (valikuline)
└── ...                 # Rohkem artikleid
```

## Uue artikli lisamine

### 1. Loo Markdown fail
Loo uus `.md` fail artikli jaoks. Failinimi peab vastama `slug` väärtusele `index.json` failis.

**Näide:** `ai-revolutsioon-2025.md`

### 2. Uuenda index.json
Lisa uus kirje `index.json` faili. Kirje formaat:

```json
{
  "slug": "failinimi-ilma-md-laiendita",
  "title": "Artikli pealkiri",
  "excerpt": "Lühike kirjeldus artiklist (160 tähemärki)",
  "category": "Kategooria nimi",
  "date": "YYYY-MM-DD",
  "image": "pilt.jpg", // valikuline, kausta images/
  "icon": "😀",         // emoji, kui pilti pole
  "author": "Autori nimi"
}
```

### 3. Markdown vorming
Kasutage standardset Markdown vormingut:

```markdown
# Pealkiri (H1)

Sissejuhatav lõik...

## Alapealkirjad (H2)

### Väiksemad pealkirjad (H3)

**Paks tekst** ja *kaldkiri*

- Loetelu punkt 1
- Loetelu punkt 2

[Link tekst](https://www.näide.ee)
```

## Toetatud Markdown elemendid

Veebilehe JavaScript teisendab automaatselt:

✅ **Toetatud:**
- `# ## ###` - Pealkirjad (H1, H2, H3)
- `**tekst**` - Paks tekst
- `*tekst*` - Kaldkiri
- `[tekst](link)` - Lingid
- `- punkt` - Loendid
- Lõigud (topelt reavahetusega)

❌ **Ei toetata:**
- Pildid
- Tabelid
- Koodiplokid
- Komplekssed HTML elemendid

## Artiklite kuvamine

### Avalehel
- Näidatakse kuni 6 artiklit
- "Vaata rohkem" nupp laadib järgmised 6
- Placeholder kuvatakse, kui artikleid pole

### Artikli avamine
- Klõps "Loe edasi" avab modaalakna
- Markdown teisendatakse automaatselt HTML-ks
- Modaal on mobiilisõbralik

## Pildid

### Artiklite pildid
Salvesta pildid kausta `articles/images/` ja viita neile `index.json` failis:

```json
{
  "image": "images/minu-pilt.jpg"
}
```

### Soovitatud pildiformaadid
- **Suurus:** 400x200 px (2:1 suhe)
- **Formaat:** JPG, PNG, WebP
- **Failisuurus:** <100KB

## Kategooriad

Soovitatavad kategooriad:
- "AI Trendid"
- "CRM & AI" 
- "Klienditeenindus"
- "Automatiseerimine"
- "Juhtumianalüüs"
- "Uudised"

## SEO parimad praktikad

### Pealkirjad
- Kasutage selgeid ja kirjeldavaid pealkirju
- 60 tähemärki või vähem
- Sisaldagu võtmesõnu

### Kirjeldused (excerpt)
- 150-160 tähemärki
- Köitev ja informatiivne
- Kutsuge tegudele

### Sisu
- Kasutage selgeid alapealkirju (H2, H3)
- Lühikesed lõigud (3-4 lauset)
- Praktilised näited ja nõuanded

## Failide nimetamine

### Slug'id
- Kasutage ladina tähti, numbreid ja sidekriipse
- Ärge kasutage eesti täpitähti slug'ides
- Näited: `ai-tuleviku-trendid`, `crm-juhend-2025`

### Pildifailid
- Kirjeldavad nimed: `ai-trendid-2025.jpg`
- Mitte: `pilt1.jpg`, `screenshot.png`

## Testimine

### Kohalik testimine
1. Ava `index.html` brauseris
2. Vali "Artiklid" menüüst
3. Kontrolli, et artiklid laevad õigesti

### GitHub Pages
Pärast failide üleslaadimist GitHubi:
1. Oota 2-5 minutit lehema uuendumist
2. Külasta veebilehte
3. Testi artiklite laadimist

## Tõrkeotsing

### Artiklid ei kuvata
- Kontrolli `index.json` süntaksit (JSON validator)
- Veendu, et `.md` failid on õiges kaustas
- Vaata brauseri console'i veasõnumeid

### Markdown ei teisendu
- Kontrolli, et kasutad toetatud Markdown süntaksit
- Faili kodeering peab olema UTF-8

### Pildid ei kuvata
- Kontrolli failiteed `index.json` failis
- Veendu, et pildifailid on õiges kaustas

## Näidefailid

Hetkel on kaustas 3 näiteartiklit:
1. `ai-revolutsioon-2025.md` - AI trendidest
2. `crm-integratsioon-ai-ga.md` - CRM-i ja AI ühendamisest  
3. `klienditeenindus-ai-abil.md` - AI klienditeeninduses

Kasutage neid mallina uute artiklite loomisel.

---

**Küsimused?** Võtke ühendust CRM Systems meeskonnaga.