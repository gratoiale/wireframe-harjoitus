# Sivu flexbox:ia käyttäen ja värjäten rivejä ja sarakkeita

## Alkutyöt: kansion luonti

Tee tätä tehtävää varten, tähän repositorioon, hakemisto `harjoitukset/flexbox-varjays`.

Lisää kaikki tämän tehtävän aikana luomasi tiedostot edellä luotuun hakemistoon.

## Tehtävä lyhyesti

Toteutetaan wireframe-versio verkkokauppa.com:in etusivusta siten, että:

* käytetään osien järjestelemiseen css:n `flexbox`-sääntöjä.
* värjätään elementit violetilla, joissa käytetään `flex-direction: row;` -sääntöä.
* värjätään elementit vihreällä, joissa käytetään `flex-direction: column;` -sääntöä.

Tehdään siis oheista muistuttava sivu, mutta käsivaraisen värjäyksen sijaan, tehdään värjäys html:llä ja css:llä.

![värjätty sivu](../kuvat/värjäys_tapa.jpg)

## Tehtävä

### Kuvakaappaus referenssisivusta

Ota [verkkokauppa.com](https://verkkokauppa.com) -sivuston etusivusta kuvakaappaus siten, että kuvassa näkyy sivun yläpalkki ja horisontaalinen tuote-esittelyosio alla olevan kuvan mukaisesti.

Tallenna tämä referenssikuva samaan kansioon tämän tehtävän html- ja css-tiedostojen kanssa.

![replikoitava näkymä verkkokauppa.com-sivustolta](../kuvat/replikoitava_sivu.jpg)

### Wireframe-sivu

Tässä tehtävässä tehdyn sivun ei tarvitse muistuttaa suoraan referenssikuvaa, vaan tuottaa verkkokauppa.com:in etusivua mallintava sivu, jossa sivun elementit on värjätty kahdella värillä, sen mukaan ovatko elementin lapsielementit järjestetty riviin vai sarakkeeseen.

![lopputulos](../kuvat/lopputulos.jpg)

#### käyttäen `flexbox`-sääntöjä

Tee sivu käyttäen `flexbox`-css-sääntöjä:

* merkitse lapsielementtejä sisältävät elementit `display: flex` -säännöllä
* määritä elementeille joko `flex-direction: row` tai `flex-direction: column`

#### värjäten elementtejä violetiksi ja vihreäksi

Jokaisella elementillä, jolla on lapsielementtejä, pitäisi päteä seuraavat asiat:

* värjää elementit, joihin on asetettu `flex-direction: row` violetiksi: `background-color: violet`.
* värjää elementit, joihin on asetettu `flex-direction: column` vihreäksi: `background-color: green`.
* lisää näille elementeille musta reunus: `border: solid 1px black`.
* lisää näille elementeille padding, jotta lapsielementtien värit eivät peitä tämän elementin taustaväriä: `padding: 14px`.

#### käytä kahta luokkaa värjäämiseksi

Koska samoja sääntöjä toistetaan tässä tehtävässä paljon, kannattaa käyttää kahta erillistä luokkaa, joilla määrittää elementeille värin ja `flex-direction`-arvon.

Tällaiset luokat voivat olla esimerkiksi seuraavat `.rivi` ja `.sarake`-luokat:

```css
.rivi {
    display: flex;
    flex-direction: row;
    background-color: violet;
    border: solid 1px black;
    padding: 7px;
}

.sarake {
    display: flex;
    flex-direction: column;
    background-color: green;
    border: solid 1px black; 
    padding: 7px;
}
```

Näitä luokkia käytetään normaalisti, kuten mitä tahansa muutakin luokkaa, lisäämällä ne html-tiedostossa luokiksi elementeille:

```html
<div class="rivi">
    <div class="sarake">sarake</div>
    <div class="sarake">sarake</div>
    <div class="sarake">sarake</div>
</div>
```

#### Jokainen elementti on joko rivi tai sarake

Tässä tehtävässä jokaiselle elementille `body`-elementin sisällä pitäisi määrittää `display: flex;`-sääntö, ja sitä vastaava väri. 

Tämä kannattaa tehdä yllä olevia `.rivi` ja `.sarake`-luokkia käyttäen.

Tällöin koko sivu värjäytyy violetiksi ja vihreäksi.
