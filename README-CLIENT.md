# Site Nunta Daniel & Anca - Versiunea 2.0

## Despre acest site

Site de invitatie pentru nunta lui Daniel si Anca, programata pentru **26 Iulie 2026** la "La Brazi", Vama, Suceava.

### Caracteristici

- Design elegant cu palette de culori sage green si gold
- Animatii fluide la scroll si tranzitii
- Slideshow hero cu 4 fotografii
- Countdown interactiv pana la data nuntii
- Galerie foto cu lightbox
- Formular RSVP complet cu:
  - Optiune pentru confirmare participare sau refuz
  - Selectie numar de invitati (1-8 persoane)
  - Alegere meniu pentru fiecare persoana (Carne, Vegetarian, Meniu de copii)
  - Mesaj optional
- Butoane directe pentru navigare Google Maps si Waze
- Design responsive (functioneaza pe telefon, tableta, desktop)
- Ecran de incarcare animat

### Sectiuni

1. **Hero** - Slideshow cu numele mirilor si data evenimentului
2. **Countdown** - Numaratoare inversa pana la ziua nuntii
3. **Locatie** - Adresa si butoane pentru navigare GPS
4. **Detalii** - Orarul evenimentului (cununie si receptie)
5. **Galerie** - Fotografii cu mirii
6. **RSVP** - Formular de confirmare prezenta
7. **Citat** - Un citat despre dragoste
8. **Footer** - Numele mirilor si data

## Cum se foloseste

### Pentru vizualizare locala

1. Deschide fisierul `index.html` in browser
2. Sau porneste un server local:
   ```
   python -m http.server 8000
   ```
   Apoi deschide http://localhost:8000

### Pentru publicare (cPanel / hosting)

Varianta recomandata este publicarea prin Git si cPanel:

1. Modifica local fisierele `index.html` si `assets/`
2. Fa commit si push in repository-ul Git
3. In cPanel, deschide `Git Version Control`
4. Intra in `Manage` -> `Pull or Deploy`
5. Apasa `Update from Remote`
6. Apasa `Deploy HEAD Commit`

Fisierul `.cpanel.yml` copiaza automat `index.html` si `assets/` in folderul subdomeniului `daniel-anca.aerdigital.ro`.

## Structura fisierelor

```
Daniel-Anca-v2/
  index.html              <- Fisierul principal al site-ului
  assets/
    images/
      horizontal/         <- Fotografiile din slideshow si galerie
        1.jpeg
        2.jpg
        3.jpeg
        4.jpeg
      additional/         <- Imagini auxiliare (logo-uri navigatie, fundal)
        googlemaps.png
        waze.png
        h_la_brazi.png
  .cpanel.yml             <- Configurare deploy Git pentru cPanel
  README-CLIENT.md        <- Acest fisier
```

## Configurari

### URL-ul Google Apps Script (RSVP)

Formularul RSVP trimite datele catre Google Sheets folosind URL-ul configurat in fisierul HTML:

```javascript
const RSVP_SCRIPT_URL = 'https://script.google.com/macros/s/AKfycbxeZJR-YNqNNe4yuw07Cf8zEx-uxat3jgddCU-nYTBV9qEnCY09JVbR47_jFrRhhMX_xQ/exec';
```

Acest URL este deja configurat si functional.

### Data nuntii

Data nuntii este setata in fisierul HTML:

```javascript
const WEDDING_DATE = new Date('2026-07-26T15:00:00');
```

## Contact

Pentru modificari sau intrebari tehnice, contacteaza dezvoltatorul.

---

Versiunea 2.0 - Aprilie 2026
