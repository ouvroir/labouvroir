# Site Astro

v1 site de l'Ouvroir

## Todo

- [ ] defaultLayout pour les pages de la nav
- [ ] footer contents
- [ ] 





## Structure du site

[arborescence](./arborescence.md) (navigation du contenu)

première version en français uniquement

```
├─ dist
	└─ contient le site "buildé"
├─ node_modules
	└─ contient les nodes modules (mais .gitignore, à installer avec npm install)
├─ public
	├─ style
		└─ global.css 
	├─ ouvroir.png
	└─ favicon.ico 
├─ src
	├─ components
		├─ HeadMeta.astro 
		└─ Header.astro
	├─ layouts
	└─ pages
		├─ index.astro
		├─ fonctionnement.astro
		├─ projets.astro 
		├─ actualites.astro 
		└─ info.astro 
├─ .gitignore
	└─ node_modules
├─ package-lock.json
	└─ pour astro
└─ package.json
	└─ pour le site
	"name: astro"
	"author": "Ouvroir",
  	"license": "GNU GPL",
      "dependencies": {
        "astro": "^0.21.0"
      }
```



##### Questions/observations

- "fonctionnement" c'est trop long pour un url? 
- info ou apropos? 

### Components

#### HeadMeta

Contient les métadonnées générales pour la page (charset, favicon, title, description), OpenGraph et Twitter.

Quand on importe HeaderMeta, il faut toujours renseigner title, description et permalink pour les passer dans BaseHead

```jsx
<BaseHead title={title} description={description} permalink={permalink} />
```

Pour l'instant, les préfixes (namespaces pour [OpenGraph](https://ogp.me/)) sont dans la balise html. Peut aussi être une balise <head> dans HeadMeta pour ne pas répéter

##### Questions

- objectif: compatibilité avec [Zotero](https://www.zotero.org/support/dev/exposing_metadata#using_an_open_standard_for_exposing_metadata) (type: page web, blogue, ...)
- Quelle image par défaut pour le partage? recommandation: [carrée, 1200x1200 min](https://www.h3xed.com/web-and-internet/how-to-use-og-image-meta-tag-facebook-reddit)
- renommer MetaData? (mélangeant avec header/nav mais que je garderai pour faire le pendant de footer)

#### Header

base: contient la navbar

##### à faire pour une v2

- SkipToContent ([accessibilité](https://github.com/markteekman/accessible-astro-starter))
- MenuToggle (responsive)

```jsx
<header>
    Logo
    SkipToContent
    MenuToggle
    //LanguageSelect
    //Search
</header>
```

#### BlogPost

Publication de blogue, utilisée dans layout Actualite







## Contenus

[arborescence](./arborescence.md)

### Blog

#### Frontmatter 

**à compléter**

- title
- description
- author (individus ou Ouvroir?, si individus, on peut créer des entités [auteurs](https://github.com/withastro/astro/tree/main/examples/blog-multiple-authors) )
- publishDate
- tags: faire une liste des tags utilisés
  - lab (désigne l'Ouvroir)
  - partenariat (ciéco)
  - blog
  - event
    - date
    - place

#### tags

- affichage (et utilisation) dans BlogPostPreview 

## Dist

### Bugs

- deux balises html :octopus:

## Style

### global.css

- Choix de typo, à mettre dans HeaderMeta et dans global.css

##### Questions

- largeur maximale du contenu v1 à 980px
- définir les responsive media breakpoints
- lib d'icônes ouverts

## V2 - ajouts

- design
- accessibilité
- responsive
- [rss](https://docs.astro.build/guides/rss/)

