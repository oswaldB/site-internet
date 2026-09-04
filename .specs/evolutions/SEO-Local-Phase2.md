# Fiche Évolution - SEO Local (Phase 2)

**Date de création :** 2026-09-04  
**Priorité :** Moyenne (après lancement du site)  
**Effort estimé :** 3-5 jours

---

## Contexte

Cette fiche regroupe les recommandations SEO local identifiées lors de la création de la maquette de la page d'Accueil, mais qui seront implémentées dans un second temps pour ne pas retarder le lancement initial.

---

## Recommandations

### 1. Pages landing par ville

**Objectif :** Maximiser la visibilité sur les requêtes locales spécifiques à chaque commune des Alpes-Maritimes.

**Villes prioritaires (à confirmer selon le trafic) :**
- Nice
- Cannes
- Antibes
- Grasse
- Menton
- Le Cannet
- Cagnes-sur-Mer
- Vallauris
- Mougins
- Saint-Laurent-du-Var

**Structure de chaque page :**
- URL : /diagnostic-immobilier-[ville]
- H1 unique : *"Diagnostic immobilier à [Ville] : expert local, intervention sous 48h"*
- Contenu spécifique :
  - Marché immobilier local (prix au m², typologie des biens)
  - Spécificités architecturales (ancien, contemporain, etc.)
  - Risques locaux (inondation, termites, radon, etc.)
  - Témoignages clients de la commune
  - Photos locales
- Maillage interne vers la page Accueil et Prestations
- Formulaire pré-rempli avec la commune

**Effort :** 2-3 jours pour les 10 premières villes (contenu + intégration)

---

### 2. Schema.org enrichi

**Objectif :** Améliorer l'affichage dans les résultats Google (rich snippets).

**Ajouts prévus :**

**a) hasOfferCatalog :**
`json
"hasOfferCatalog": {
  "@type": "OfferCatalog",
  "name": "Diagnostics Immobiliers",
  "itemListElement": [
    {"@type": "Offer", "itemOffered": {"@type": "Service", "name": "DPE"}},
    {"@type": "Offer", "itemOffered": {"@type": "Service", "name": "Amiante"}},
    ...
  ]
}
`

**b) ggregateRating :**
`json
"aggregateRating": {
  "@type": "AggregateRating",
  "ratingValue": "4.6",
  "reviewCount": "127",
  "bestRating": "5",
  "worstRating": "1"
}
`
*(À synchroniser avec Immodvisor pour des données à jour)*

**c) reaServed étendu :**
`json
"areaServed": [
  {"@type": "City", "name": "Nice"},
  {"@type": "City", "name": "Cannes"},
  ...
]
`

**Effort :** 1/2 journée (développement + validation Google Rich Results Test)

---

### 3. Blog local (Phase 2)

**Objectif :** Cibler des requêtes longues traîne et établir l'autorité éditoriale d'ADTI.

**Exemples d'articles :**

| Titre | Requête ciblée | Priorité |
|-------|----------------|----------|
| "Obligation diagnostic immobilier vente appartement ancien Nice" | Diagnostic immobilier vente Nice ancien | Haute |
| "Prix DPE Cannes 2026 : tarif et délais" | Prix DPE Cannes | Haute |
| "Amiante avant travaux : obligations à Cannes et dans le 06" | Amiante avant travaux Cannes | Moyenne |
| "DPE tertiaire Nice : quelles entreprises sont concernées ?" | DPE tertiaire Nice | Moyenne |
| "Termites Alpes-Maritimes : communes concernées en 2026" | Termites 06 communes | Moyenne |
| "Audit énergétique copropriété Nice : guide complet" | Audit énergétique copropriété Nice | Basse |

**Fréquence de publication :** 2 articles/mois minimum  
**Longueur :** 800-1 500 mots par article  
**Optimisation :** Maillage interne vers pages Prestations et Contact, balises meta personnalisées

**Effort :** 1-2 jours/mois (rédaction + intégration)

---

## KPIs à suivre

- Positions SEO sur les requêtes locales (Nice, Cannes, etc.)
- Trafic organique par ville (Google Analytics)
- Taux de conversion par page landing (formulaire soumis / visites)
- Impressions et clics dans Google Search Console (filtre : requêtes avec nom de ville)

---

## Prérequis techniques

- CMS permettant la création facile de nouvelles pages
- Modèle de page landing réutilisable
- Intégration Google Search Console
- Possibilité d'ajouter du contenu dynamique (Schema.org)

---

## Notes

- Ne pas lancer ces actions avant d'avoir 3 mois de données sur le site principal
- Prioriser les villes selon le trafic organique existant et le nombre de clients actuels
- Le blog peut être démarré en parallèle des pages villes si ressources disponibles
