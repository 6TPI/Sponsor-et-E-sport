ToDO
Metre les image

## Comment on ajoute le japonais                                                                                   
On ajoute la langue dans hugo.toml (bloc languages.ja + contentDir = "content/ja"), 
puis on crée les pages dans content/ja/ (ex : content/ja/_index.md et content/ja/posts/).   
ajout d'un fallback dans assets/css/custom.css
ajout de i18n/ja.yaml sert aux textes “fixes” du thème (ex. le footer “propulsé par…”, libellés d’interface).      

## Comment modifier le footer 
Pour enlever le power by hugo et blowfish 
soit dand hugo.toml
[params.footer]
showThemeAttribution = false
ou pour le modifier, trouver le footer dans 
Sponsor-et-E-sport\i18n\fr.yaml 



## Comment mettre le slogan 
Sponsor-et-E-sport\public\fr\index.html ( généré au build )
et
Sponsor-et-E-sport\hugo.toml 

    [languages.fr.params]
      displayName = "FR"
      author = { name = "Sponageek", image = "/img/fight.png", headline = "55 Un site e-sport vu à travers la culture Street Fighter" }
      tagline = "Sponsorise un geek."


## Comment mettre la favicon
mettre une image ou autre sur un generateur de favicon https://favicon.io/ 
Et placer le contenu du zip dans le dossier /static 
PS si il y a un bug penser a vider le cache avec ctrl+f5


## Comment mettre une video a la page d'acceuil avec le layout background 

Grace a l'id et le shortcode ci dessous 
`{{< youtubeLite id="iEM-J9mFp-w" label="Evo Street Fighter" >}}`

## Commment on définis le hugo.toml pour faire une page d'acceuil fr et une page d'acceuil anglais ? 
[params.author]
  name = "Sponageek"
  image = "/img/fight.png"   # ← TON image
  headline = "Mieux qu’un investissement en startup : sponsorise un geek."


## Comment mettre en multilangue : 
dans hugo.toml

```go
[languages]

  # ---- FRANÇAIS ----
  [languages.fr]
    languageName = "Français"
    weight = 1
    title = "Sponageek"
    contentDir = "content/fr"

    [languages.fr.params]
      displayName = "FR"
      author = { name = "Sponageek", image = "/img/fight.png", headline = "Mieux qu’un investissement en startup : sponsorise un geek." }
      tagline = "Sponsorise un geek."

    [languages.fr.params.homepage]
      layout = "background"
      homepageImage = "/img/background.svg"
      showRecent = false

  # ---- ENGLISH ----
  [languages.en]
    languageName = "English"
    weight = 2
    title = "Sponageek"
    contentDir = "content/en"

    [languages.en.params]
      displayName = "EN"
      author = { name = "Sponageek", image = "/img/fight.png", headline = "Better than a startup investment: sponsor a geek." }
      tagline = "Sponsor a geek."

    [languages.en.params.homepage]
      layout = "background"
      homepageImage = "/img/background.svg"
      showRecent = false
```

## Comment créer des articles 
Pour faire un articles, il faudrau une image en 16:9 CF les images

## Comment on ajoute les reseaux socieau a la page d'acceuil 
On créer un fichier pour chaque language du site qu'on ecrit 
Sponsor-et-E-sport\config\_default\languages.fr.toml 
Ce fichier contient les liens 

## Comment créer une table de contenue pour les documentation 
Pour cela il faut que dans le front matter de l'article il y a est 
`toc: true`

Puis dans la parametres `Sponsor-et-E-sport\config\_default\params.toml`
placer : 
```go
[article]
showTableOfContents = true
showWordCount = true
showReadingTime = true
```


