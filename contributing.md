# Comment contribuer

Heureux d'apprendre que vous voulez contribuer à la [base de connaissances](https://lp-dev-cloud.github.io/kb2021/) 2021 des étudiants [LP CDTL, parcours cloud](https://www.iut-larochelle.fr/formations/departement-informatique/licence-professionnelle-developpeur-cloud/).

N'hésitez pas à faire des commits, ajouter des commentaire, et proposer des pull requests, dans les branches du projet !

## Règles de branches
Normalisation du nommage des branches :
[prefix]\_[matiere]_[nom]

3 éléments :
* [prefix] : Cours / Projet-Individuel / Projet-Groupe / Github
* [matière] : HarmoProg / HarmoBDD / GPI / DevOps / UX
* [nom] : TP / TD / Nom des membres d’un groupe (pour projets), thème ex. : TD1 agile

Règle UpperCammelCase pour les noms
on mets des _ pour séparer les 3 différents éléments du nom
on mets des - à la place des espaces dans un élément

*Exemples :*
* Cours_gpi_td1-agile
* Cours_HarmoProg_tp1-python
* Projet-Groupe_HarmoProg_Denis-Erwann



## Faire des commits 
### Titres et commentaires

```bash
git commit -m "📝:gitmoji correspondant au contenu: un commentaire qui représente la modification”
```

Les commits doivent se faire **en anglais** dans les branches relatives aux modifications. Attention: ne pas faire de commit et de fusion directement dans la branche *main*.

Les gitmojis permettent d'annoncer le contenu d'un commit
* ♻️ : review
* 🚀 : complete
* 📝 : update doc
* 🚧 : In progress
* ✨ : new pages/docs
* 🐛 : fix bug or grammar (use everytime)

## Pull requests
A la fin des commits, vous pouvez [soummetre une PR](https://github.com/LP-Dev-Cloud/kb2021/pull/new/main) pour révision et merge sur *main*

## Règles de code

* Indentation : usage des **tabulations**, pas d’espaces

### Markdown

```md
# Titres 1
## Titres 2
### Titres 3

*italique*
**gras**
* Une puce de liste
```


## Nommage des fichiers
Dans le dossier [/kb2021](https://github.com/LP-Dev-Cloud/kb2021/tree/main/kb2021) dossiers, fichiers :
matière / chapitre *ou* thème *ou* langage / TP0.md