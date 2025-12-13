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