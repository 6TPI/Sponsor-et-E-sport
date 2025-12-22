ToDO
Metre les image

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


