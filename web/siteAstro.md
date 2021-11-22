# Site Astro

v1 site de l'Ouvroir

## Structure

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
		└─ HeadMeta.astro
	├─ layouts
	└─ pages
		└─ index.astro 
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



##### Questions

- utiliser [Accessible Astro Components](https://github.com/markteekman/accessible-astro-components)? Ou s'en inspirer, voir [exemple](https://github.com/markteekman/accessible-astro-starter)



### Components

#### HeaderMeta

Contient les métadonnées générales pour la page (charset, favicon, title, description), OpenGraph et Twitter.

Quand on importe HeaderMeta, il faut toujours renseigner title, description et permalink pour les passer dans BaseHead

```jsx
<BaseHead title={title} description={description} permalink={permalink} />
```



##### Questions

- Quelle image par défaut pour le partage? recommandation: [carrée, 1200x1200 min](https://www.h3xed.com/web-and-internet/how-to-use-og-image-meta-tag-facebook-reddit)
- Métadonnées générales à ajouter? 
  - author? si oui, on met "ouvroir?"
  - licence? 
- Créer un composant spécifique pour les entrées de blogue? (pour les référencer dans Zotero etc? )

#### Header

base: contient le menu

##### à gérer

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



## Contenus

[arborescence](./arborescence.md)



## Style

### global.css

- Choix de typo, à mettre dans HeaderMeta et dans global.css

##### Questions

- largeur maximale du contenu + centrer à partir de ça
- responsive media breakpoints
- lib d'icônes ouverts

