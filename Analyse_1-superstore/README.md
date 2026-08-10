# Analyse 1 — Superstore

> Fichier source : [Kaggle](https://www.kaggle.com/datasets/yesshivam007/superstore-dataset)

---

## Brief
**Contexte fictif:** *Ayant rejoint l'équipe data d'une chaine de magasins américaine, la direction commerciale veut un tableau de bord pour piloter les ventes et la rentabilité.*

**Les colonnes à observer sont:**
- `Order Date`, `Ship Date` -> dimensions temporelle
- `Region`, `State`, `City` -> dimension géographique
- `Category`, `Sub-Category`, `Product Name` -> dimension produit
- `Customer Name`, `Segment` -> dimension client
- `Sales`, `Quantity`, `Discount`, `Profit` -> mesures financières

## Étapes de travail

### Phase 1 — Préparation des données (Power Query)
- Vérifier les types de données (dates, nombres, texte)
- Créer une table Calendrier (**indispensable** pour les fonctions de Time Intelligence en DAX)
- Vérifier les doublons/valeurs manquantes

### Phase 2 — Modélisation 
- Organiser en modèle en étoile si possible (table de faits `Orders` + dimensions)
- Créer les relations entre tables

### Phase 3 — Mesures DAX à créer
- `Total Sales`, `Total Profit`, `Profit Margin %`
- `Sales YTD`, `Sales vs Previous Year`
- `Top Sub-Category by Profit`

### Phase 4 — Construction du dashboard (2-3 pages)
- Page 1 - Vue d'ensemble : KPIs (ventes, profit, marge, nb commandes), courbe d'évolution, carte géographique 
- Page 2 - Analyse produit : ventes/profit par catégorie et sous-catégorie, top/flop produits
- Page 3 - Analyse client : segments, top clients, remises vs profit (attention, c'est un point clé du dataset — la relation discount/profit révèle souvent des pertes cachées)

---