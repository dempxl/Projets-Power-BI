<div align="center">
  <img src="img/power-bi_logo.svg" alt="Power BI Logo" width="300">
</div><br>

# Power BI — Comprendre et apprendre

## Sommaire
- [Qu'est-ce que Power BI ?](#quest-ce-que-power-bi-)
- [Terminologies à retenir](#terminologies-à-retenir)
- [Pipeline d'un projet sur Power BI](#pipeline-dun-projet-sur-power-bi)
- [Alternatives à Power BI](#alternatives-à-power-bi)
- [Sources](#sources)

## Qu'est ce que Power BI ?

Power BI est un logiciel d'analyse de données d'informatique décisionnelle de Microsoft. Il permet de visualiser les données et de partager des informations au sein d'une organisation. Étant un logiciel très performant, regrouppant un ensemble de services logiciels, d'applications et d'interfaces de programmation interconnectés, il est prisé par les entreprise et est très TRÈS souvent pris en considération lors d'entretiens d'embauches. 

## Terminologies à retenir
- Tout d'abord, Power BI n'est pas qu'un seul outils mais plutôt trois
  + Power BI Desktop (Application PC) : Permet de concevoir les rapports
  + Power BI Service (Application Web) : Après avoir conçu le rapport, il faut le **publier**, Service nous permet d'écrire nos tableau de bords
  + Power BI Mobile (Application Téléphone) : Version Mobile pour consulter les tableaux de bords
- Espace de travail/workspace : conteneur pour les tableaux de bords, rapports, jeux de données et dataflow dans Power BI 
- Espace de travail **personnel** avec uniquement **nos données**
- Espace de travail **collectif** avec nos données et **celles partagées**
- Dataset/jeux de données : collections de données qu'on importe ou auquelles on se connecte.

> Les jeux de données sont associés aux espaces de travail et un même jeu de donnée peut faire partie de nombreux espaces/workspaces

- Rapport : constitué **d'une ou plusieurs pages de visualisations** comme des graphiques en courbes, des cartes etc; souvent dans un espace de travail.

- Tableau de bord : **un canevas unique qui contient zéro ou plusieurs vignettes de widgets**. Chaque vignettes épinglée à partir d'un rapport ou plusieurs. Des pages de rapport entières peuvent être épinglées à un tableau de bord. Les tableaux de bord sont souvent utilisés pour **surveiller les indicateurs clés de performance (KPI)**.

> Un tableau de bord est unique et peut contenir plusieurs rapports. **PAS L'INVERSE**

## Pipeline d'un projet sur Power BI
```mermaid
---
title : pipeline d'un projet sur Power BI
config :
  theme: dark
---

flowchart LR
A[Se connceter aux données]
B[Nettoyer les données]
C[Transformer les données]
D[Créer des visualisations]
E[Publier et partager le rapport]

A --> B
B --> C
C --> D
D --> E

```
---

## Commencer sur Power BI



---

## Alternatives à Power BI 
| Nom             | Avantages | Inconvénients |  
|-|-|-|  
| Tableau        | Référence historique, très reconnu, le plus abouti et **très demandé en entreprise visuellement** | **Licence coûteuse**, moins répendu dans les PME, courbe d'apprentissage plus longue sur les fonctionnalités avancées |  
| Metabase        | Open source et gratuit, interface simple | Beaucoup moins présent dans les entreprises, plus utilisé par les statups, moins de profondeur analytique que PBI ou Tableau               |  
| Looker Studio   | Gratuit, accessible immédiatement sans licence, très simple à prendre en main, bonne porte d'entrée pour débuter, **bien intégré à Google Analytics et Google Ads** | Moins puissant pour des modélisation de données complexes ou multi-sources, peu utilisé dans le secteur de finances, industrie, contrôle de gestion, **vue comme trop "basique" par certaines entreprises** |   

## Sources
- [Power BI : Le Guide Ultime | Tutoriel complet pour les débutants]()
