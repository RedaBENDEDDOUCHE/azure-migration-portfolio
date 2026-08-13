# Phase 11 — Optimisation des coûts et des performances

**Statut** : ⬜ À faire
**Domaine AZ-104** : Gérer les identités et gouvernances Azure
**Coût estimé** : 0 €
**Durée recommandée** : 1 heure

## Objectifs
- Utiliser Azure Advisor pour obtenir des recommandations
- Analyser les coûts avec Cost Management
- Redimensionner les ressources sur-provisionnées

## Prérequis
- Toutes les phases précédentes idéalement actives simultanément au moins une fois

## Checklist des tâches
- [ ] Exporter (capture) les 4 catégories de recommandations Azure Advisor
- [ ] Produire une vue "coût cumulé du projet" dans Cost Management (par RG)
- [ ] Identifier au moins 2 ressources redimensionnables/supprimables sans impact
- [ ] Appliquer au moins 1 recommandation concrète (ex. B2s → B1s, supprimer disque orphelin)
- [ ] Rédiger une synthèse Avant/Après avec delta de coût mensuel projeté

## ⚠️ Pièges à surveiller
- [ ] Azure Advisor a besoin de plusieurs jours de télémétrie — documenter honnêtement si limité
- [ ] Ne pas confondre coût réel (retard 24-48h) et coût estimé temps réel
- [ ] Vérifier les dépendances avant de supprimer une ressource recommandée (ex. disque "non attaché" = sauvegarde manuelle)

## Décisions techniques prises
_À compléter._

## Captures d'écran
_Voir `/screenshots/phase-11/`_
