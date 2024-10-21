# BEM-harjoitus

1. Kopioi jonkin aiemman harjoituksen valmis palautuksesi uuteen kansioon `harjoitukset/bem-harjoitus/`.
2. Muokkaa html- ja css-tiedostoissa luokkien nimet käyttämään BEM-syntaksia.

## BEM-syntaksi

BEM on css:n yhteydessä käytetty luokkien nimeämistapa. Sen ideana on helpottaa luokkien nimien määrittämistä, ja tehdä nimistä järjestelmällisempiä.

BEM-syntaksi löytyy osoitteesta [getbem.com](https://getbem.com/naming/).

### Block, Element, Modifier

BEM koostuu kolmesta eri nimen osasta:

* block
* element
* modifier

```html
<div>
  <div></div>
  <div></div>
</div>
```

#### Block

Block on itsenäinen elementti, jolla ei ole järkevää yksiselitteistä vanhempaa elementtiä.

Tällainen saattaa olla esimerksi uutissivustolla `div`-joka pitää sisällään uutisotsikon.

Tällaiselle elementille annetaan nimeksi BEM:ssä jokin kuvaava nimi, esim. `.uutisotsikko`.

#### Element

Element on jokin html-elementti, joka esiintyy aina toisen html-elementin lapsena. 

Uutisotsikon yhteydessä tämä voi olla esim. uutisotsikon aika tai teksti.

Tällöin näitä esitetään muodossa:

* `.uutisotsikko__aika`
* `.uutisotsikko__teksti`

#### Modifier

Modifier-määreellä määritetään html-elementin erikoistapausta. Esimerkiksi punaista tai sinistä versiota samasta elementistä.

Tällöin elementin nimi voi olla:

* `.uutisotsikko__aika--punainen`
* `.uutisotsikko__aika--sininen`

### BEM-versio aiemmasta html:stä

```html
<div class="uutisotsikko">
  <div class="uutisotsikko__aika uutisotsikko__aika--punainen">12min</div>
  <div class="uutisotsikko__teksti">Lorem ipsum dolor sit</div>
</div>
```
