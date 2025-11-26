---
date: '2025-04-07T17:22:25+03:00'
draft: true
title: 'Kuinka pääset helposti eroon persikasta taustaväristä sillä yhdellä nettisivulla'
summary: 'Tässä kirjoituksessa neuvon, miten pääset melko helposti eroon persikanvärisestä taustasta tietyssä verkkosivustossa.'
description: 'Tässä kirjoituksessa neuvon, miten pääset melko helposti eroon persikanvärisestä taustasta tietyssä verkkosivustossa.'
author: Antti Koistinen
---
Itseäni on ärsyttänyt jo muutaman vuoden ajan erään usein käyttämäni verkkosivuston taustaväri. Jostain hassusta brändiuudistuksellisesta syystä eräs suomalainen uutismedia alkoi värittää teknologia- ja talousaiheisia uutisiaan kellertävällä taustavärillä.

Nyt jaksoin vihdoinkin tehdä asialle jotain, ja tee-se-itse-hengessä ajattelin jakaa nämä helpot ohjeet myös teille muille. Tässä olkaa hyvä!

### Lataa selainlisäosa **Stylus**

**Stylus**-lisäosalla pääset helposti ajamaan omia tyylitietojasi, esim. CSS-koodia, valitsemillasi verkkosivuilla. Itse käytän Firefox-selainta, ja latasin lisäosan täällä: https://addons.mozilla.org/en-US/firefox/addon/styl-us/

### Mene verkkosivullesi ja aktivoi Stylus

Avaa kaipaamasi verkkosivu, ja klikkaa Styluksen ikonia selaimessa. Valitse `Write style for: [sivuston osoite]`.

### Syötä kaipaamasi koodinpätkä avautuvaan ikkunaan

Eteesi aukeaa uusi välilehti, johon voit syöttää kaipaamasi muutokset. Tähän tarvitset hieman CSS-koodin osaamista, mutta seuraava koodi poistaa hassut persikkavärit ja korvaa ne turvallisella ja tutulla valkoisella:

```
@-moz-document domain("hs.fi") {

    :root {
        --sndp-color-brand-visio-light-powder: white !important;
        --nof-semantic-color-grayscale-100: white !important;
        /* Just in case it's re-declared multiple times */
        --sndp-color-brand-visio-light-powder: white !important;
    }

}
```

Lopuksi paina **Save** ja muutokset tulevat voimaan heti.

### Loppukaneetit ja muut huomiot

Kaikkeen internetistä löytyvään koodiin kannattaa aina suhtautua varauksella. Käytä omalla vastuullasi, siis!