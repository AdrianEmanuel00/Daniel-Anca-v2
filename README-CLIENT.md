# Site Nunta Daniel & Anca - Versiunea 2.0

## Despre acest site

Site de invitatie pentru nunta lui Daniel si Anca, programata pentru **26 Iulie 2026** la "La Brazi", Vama, Suceava.

### Caracteristici

- Design elegant cu palette de culori sage green si gold
- Animatii fluide la scroll si tranzitii
- Slideshow hero cu 4 fotografii
- Countdown interactiv pana la data nuntii
- Galerie foto cu lightbox
- Cautare interactiva pentru asezarea invitatilor la mese
- Afisare masa si invitatii de la aceeasi masa
- Butoane directe pentru navigare Google Maps si Waze
- Design responsive (functioneaza pe telefon, tableta, desktop)
- Ecran de incarcare animat

### Sectiuni

1. **Hero** - Slideshow cu numele mirilor si data evenimentului
2. **Countdown** - Numaratoare inversa pana la ziua nuntii
3. **Locatie** - Adresa si butoane pentru navigare GPS
4. **Detalii** - Orarul evenimentului (cununie si receptie)
5. **Galerie** - Fotografii cu mirii
6. **Asezare la mese** - Cautare invitat si masa
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
    data/
      seating.js          <- Lista invitatilor si mesele generate din Excel
  .cpanel.yml             <- Configurare deploy Git pentru cPanel
  README-CLIENT.md        <- Acest fisier
```

## Configurari

### Lista invitatilor

Lista pentru cautarea meselor este in `assets/data/seating.js` si este generata din fisierul Excel cu invitati.

### Data nuntii

Data nuntii este setata in fisierul HTML:

```javascript
const WEDDING_DATE = new Date('2026-07-26T15:00:00');
```

## Contact

Pentru modificari sau intrebari tehnice, contacteaza dezvoltatorul.

---

Versiunea 2.1 - Iulie 2026
