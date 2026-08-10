# Analyse 2 — Prix du carburant en France

> Fichier source : [data.gouv](https://www.data.gouv.fr/datasets/prix-des-carburants-en-france-flux-quotidien-1)

---

## Brief
**Contexte fictif** : *Ayant rejoins le département Data d'EnerFrance, un réseau de stations-service, la direction commerciale veut un outil de veille concurrentielle et de pilotage des prix pour comparer ses tarifs à ceux du marché, région par région.*

**Objectif business** : identifier où l'entreprise est trop chère ou trop peu compétitive par rapport aux moyennes régionales/nationales, et suivre l'évolution des prix dans le temps.

**Les colonnes à observer sont:**
- Identifiant et adresse du point de vente, latitude/longitude
- `Ville`, `Département`, `Région`
- Enseigne/marque de la station
- Type de carburant (`Gazole`, `SP95`, `SP98`, `E10`, `E85`, `GPLc`)
- Prix par carburant, date/heure de relevé
- Services proposés (station 24h/24, lavage, etc.)

## Étapes de travail

### Phase 1 — Préparation des données (Power Query)
- Nettoyer les prix aberrants (valeurs à 0 ou nulles = carburant non disponible ce jour-là)
- Convertir les dates correctement (attention au format JJ/MM/AAAA)
- Créer une table Calendrier pour l'intelligence temporelle
Optionnel : créer une colonne "Marque" simplifiée si les enseignes sont trop détaillées

### Phase 2 — Modélisation 
- Table de faits : relevés de prix
- Dimensions : Région/Département/Ville, Carburant, Calendrier
- Modèle en étoile

### Phase 3 — Mesures DAX à créer
- `Prix Moyen`, `Prix Min`, `Prix Max` par carburant
- `Écart` vs `Moyenne Nationale`
- `Évolution du prix sur 30 jours` (fonction DATEADD)
- `Nombre de stations par région`

### Phase 4 — Construction du dashboard (2-3 pages)
- Page 1 – Vue d'ensemble : carte de France des prix par région, KPIs (prix moyen national par carburant), tendance sur les 30 derniers jours
- Page 2 – Analyse géographique : classement des départements les moins chers/plus chers, comparaison Gazole vs SP95/SP98
- Page 3 – Analyse par enseigne : positionnement des grandes marques (Total, Leclerc, Intermarché...) les unes par rapport aux autres

---