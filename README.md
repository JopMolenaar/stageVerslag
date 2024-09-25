# Stage verslag Onetribe
## _Jop Molenaar, 500880472, CMD Amsterdam_

Functie: Front-end developer

Docentbegeleider: Anne Marleen Olthof

Bedrijfsbegeleider: Michael Post, full-stack developer

Datum: <!-- oplevering datum-->

## Inleiding
[text](text.md)
<!-- geef aan waarom je stage hebt gelopen bij dit bedrijf. Hoe ben je bij dit
bedrijf terecht gekomen? Hoe is de stage je bevallen? De inleiding moet de lezer
prikkelen om verder te lezen -->

## Omschrijving van het stage bedrijf

<!-- Plaatjes enzo -->

Onetribe is een bedrijf in de houthavens (Amsterdam) dat gefocust is op het maken van websites met een extra oog op een goede gebruikerservaring. Ze gebruiken vooral Nuxt.js en Vue.js voor hun projecten maar aangezien ze een tijd geleden zijn gefuseerd met noprotocol hebben ze ook een aantal projecten met twig en php. Aangezien ze Nuxt.js en Vue.js gebruiken  voor hun projecten zijn er weinig backend developers nodig. De organisatiestructuur bestaat uit een aantal afdelingen. Hier werken visual designers, user experience designers, veel front-end developers, een aantal backenders, contentmakers, copywriters en projectmanagers. 
Ik heb dit bedrijf gevonden door te browsen op het internet. Na wat rondgekeken te hebben op de website sprak dit bedrijf mij al erg aan. Dit komt doordat ze extra aandacht geven aan wat een website echt goed en compleet maakt. Hierbij horen bijvoorbeeld responsiveness, toegankelijkheid en performance en zagen de projecten die ze hadden gemaakt er aantrekkelijk uit. Ook is dit een groter bedrijf dan waar ik eerder stage heb gelopen en dit geeft mij de mogelijkheid om te kunnen vergelijken. Onetribe maakt ook gebruik van frameworks en dit is iets waar ik nog geen ervaring mee heb, en weet zeker dat ik daar veel van kan leren.  

## Profielschets bedrijfsbegeleider

Mijn bedrijfsbegeleider is Michael Post en is een full-stack developer bij Onetribe en personal trainer. Hij heeft CMD gestudeerd en daarnaast functies gehad als front-end developer en project manager. Hij kan mij zeker wat leren aangezien hij veel ervaring en kennis heeft in het vak en aan dezelfde (soort) projecten werkt als ik tijdens mijn stage. 

## Jouw functieomschrijving

Mijn functie die ik ga uitvoeren is front-end developer. Hierbij ga ik meewerken aan projecten op basis van Nuxt.je en Vue.js en kan ik worden gevraagd om werk te testen en aan te geven waar er verbeteringen gemaakt moeten worden of zelf te verbeteren. Deze projecten zijn voor bedrijven zoals Peakz padel. De gebruiker moet op deze websites vaak informatie kunnen vinden en bepaalde acties kunnen ondernemen waar de service voor bedoeld is zoals iets kopen of boeken. 
Het team waarin ik kom te werken zijn vooral andere developers, designers, UX’ers, en project managers.

## Werkzaamheden

<!-- wat heb je concreet gedaan. Een uitgebreide beschrijving van de
jouw werkzaamheden en van jouw gemaakte beroepsproducten. Laat afbeeldingen
zien van wat je hebt gemaakt en het proces erachter. TIP: Gebruik hierbij het logboek
dat je tijdens je stage hebt bijgehouden -->

### Werkwijzen Onetribe

Aangezien Onetribe gefuseerd is met noprotocol hebben ze nu nog meerdere werk-omgevingen en manieren voor de versie beheer. 

#### Bitbucket

Bij de projecten van Onetribe slaan ze code op op bitbucket.
Daarnaast gebruiken ze Jira voor het issue board
De bedoeling voor de versie beheer hier is dat je de branch cloned met onder andere sowieso het issue nummer. Daarna schrijf je je commits altijd in de voltooide tijd, en zet je de link van de issue uit Jira in de commit. Zo kan de reviewer makkelijk de bijbehorende issue vinden. 

#### Git flow

Bij de projecten die van noprotocol waren slaan ze code op op github.
Daarnaast gebruiken ze Jira voor het issue board.
Om de versie beheer goed inzichtelijk te houden maken ze gebruik van git flow.
Je zet feature/, hotfix/ of release/ voor de titel van je branch als je die cloned en de titel van je commit is eigenlijk vaak ook je issue nummer.
Voor de semantic release (het versienummer van je project die je automatisch kan updaten aan de hand van hoe je je commits opbouwt) moet je je commits beginnen met chore:, fix:, feature: of perf:. 
voorbeelden:

![Git flow](images/gitflow.png)

> Bron: https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow 

Ook zei Raoul dat niet iedereen zich aan de standaard van git flow houdt en vind dat je je gewoon aan de standaard moet houden en niet dingen er bij moet verzinnen die je dan eerst weer moet uitleggen. 

```
## Branches / GIT

### Git Flow - Branch Naming
For branch naming, we use the 'git flow' standard to manage our branches. In short that means only the following branches should exist:
- master
- develop
- feature/PROJECT-xxx-short-description

And (not used that often):
- release/release-version
- hotfix/short-description

See the confluence page for more information: [Branch Naming](https://noprotocol.atlassian.net/wiki/spaces/DEV/pages/1877868545/Git+Branch+Naming)

### Semantic Release - Commit Message Format
To write decent commit messages, you should follow the semantic release standards. This involves using a specific format for your commit messages:

`<type>(<scope>): <description>`

Where:
- `<type>` is one of: perf (major release), feat (minor release), fix (patch release), chore (no significance)
- `<scope>` is optional and represents the module affected
- `<description>` is a short summary of the change

Examples:
feat(auth): add login functionality
fix(api): resolve null pointer in user service

This format helps automate versioning and changelog generation based on commit messages.

[See here for more info](https://github.com/semantic-release/semantic-release?tab=readme-ov-file#how-does-it-work)
```

### Vue.js/Nuxt.js Onetribe

## Leerdoelen

## Observatieopdrachten

## Analyse feedbackformulieren 

## Reflectie

## Bijlagen






<!-- [![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger) -->
<!-- 
> Placeholder for
> quotes


```
code samples
```

```sh
sh code samples
yo
```

| Tables | xx |
| ------ | ------ |
| And | [plugins/dropbox/README.md][many more] |
| GitHub | [plugins/github/README.md][PlGh] | 
 -->

<!-- images -->
<!-- etc etc -->



<!-- 
<template>
  <picture 
    v-if="image"
    class="picture__image" 
    :class="[
      {'transparent' : image.extension === 'png'}
    ]"
  >
    <source
      v-for="(imgMobileWebSrcset, index) in reverseArray(combinedProperties.mobile_web_srcset)"
      :key="index"
      :media="imgMobileWebSrcset.media" 
      :srcset="imgMobileWebSrcset.links"
      type="image/webp"
    >
    <source
      v-for="(imgMobileSrcset, index) in reverseArray(combinedProperties.mobile_srcset)"
      :key="index"
      :media="imgMobileSrcset.media" 
      :srcset="imgMobileSrcset.links"
      type="image/jpg"
    >
    
    <source
      v-for="(imgWebSrcset, index) in reverseArray(combinedProperties.web_srcset)"
      :key="index"
      :media="imgWebSrcset.media" 
      :srcset="imgWebSrcset.links"
      type="image/webp"
    >
    <source
      v-for="(imgSrcset, index) in reverseArray(combinedProperties.srcset)"
      :key="index"
      :media="imgSrcset.media" 
      :srcset="imgSrcset.links"
      type="image/jpg"
    >
    

    <img
      :class="[ 'm-0','object-cover', combinedProperties.class, combinedProperties.aspectRatio ]"
      :src="image.url"
      :title="image.title"
      :alt="combinedProperties.customAlt ?? image.title"
      :width="combinedProperties.width ?? image.width"
      :height="combinedProperties.height ?? image.height"
      :loading="combinedProperties.loading ?? 'lazy'"
      :style="[objectPositionStyle]"
      decoding="async"
    >
  </picture>
</template>

<script setup>
/* eslint-disable @typescript-eslint/no-unused-vars */
const props = defineProps({
  image: {
    type: Object,
    requird: true,
    default: () => {}
  },
  properties: {
    type: Object,
    default: () => ({
      focalPoint: [0.5, 0.5],
      mobile_srcset: [],
      mobile_web_srcset: [],
      srcset: [],
      web_srcset: [],
      class: null,
      aspectRatio: "aspect-auto",
      customAlt: null,
      width: null,
      height: null,
      loading: "lazy",
    })
  },
});
/* eslint-enable @typescript-eslint/no-unused-vars */

const focalPoint = props.properties.focalPoint ?? props.image.focalPoint ?? [0.5, 0.5];
const objectPositionArray = focalPoint.map(position => (Math.round(position * 100)) + "%")
const objectPositionStyle = `object-position: ${objectPositionArray[0]} ${objectPositionArray[1]}`;

const getImageData = (testString) => {
  return Object.keys(props.image)
  .filter(key => testString.test(key))
  .map(key => {
    const size = key.match(testString)[1];
    return {
      media: `(min-width: ${size}px)`,
      links: props.image[key]
    };
  });
};

const srcset = getImageData(/^w(\d+)$/);
const web_srcset = getImageData(/^webp_(\d+)$/);
const mobile_srcset = getImageData(/^mobile_w(\d+)$/);
const mobile_web_srcset = getImageData(/^mobile_webp_(\d+)$/);
const aspectRatio = props.properties.aspectRatio ?? props.image.aspectRatio ?? "aspect-auto";

const combinedProperties = computed(() => {
  return {
    ...props.properties,
    ...props.image,
    aspectRatio,
    srcset,
    web_srcset,
    mobile_srcset,
    mobile_web_srcset,
  }
});

function reverseArray(arr) {
  if (Array.isArray(arr) && arr.length > 0) {
    arr.reverse();
  }
  return arr;
}

</script> -->


