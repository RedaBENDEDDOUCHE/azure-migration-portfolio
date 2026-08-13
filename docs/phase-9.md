# Phase 9 — Supervision : Azure Monitor & Log Analytics

**Statut** : ⬜ À faire
**Domaine AZ-104** : Superviser et sauvegarder les ressources Azure
**Coût estimé** : 0 € (sous 5 Go/mois gratuits)
**Durée recommandée** : 1h30 à 2 heures

## Objectifs
- Centraliser logs et métriques dans un workspace Log Analytics
- Créer des alertes proactives
- Construire un dashboard de supervision

## Prérequis
- Phase 3 (VM) et idéalement Phase 7 (App Service) terminées

## Checklist des tâches
- [ ] Créer le Log Analytics Workspace `law-contoso-prod-euw-01`
- [ ] Installer l'agent Azure Monitor sur les VM (Windows et Linux)
- [ ] Activer les diagnostic settings de l'App Service vers le workspace
- [ ] Créer 3 règles d'alerte + Action Group `ag-contoso-itoncall` (email)
  - [ ] CPU > 80% pendant 5 min
  - [ ] Disque libre < 10%
  - [ ] App Service HTTP 5xx > 10 en 5 min
- [ ] Écrire 2 requêtes KQL (top 10 erreurs, VM avec CPU moyen le plus élevé)
- [ ] Construire un dashboard avec au moins 4 tuiles
- [ ] Déclencher volontairement une alerte (stress CPU) pour vérifier la notification

## ⚠️ Pièges à surveiller
- [ ] Associer l'agent à un Data Collection Rule (DCR), sinon aucune donnée ne remonte
- [ ] Fenêtre d'évaluation d'alerte pas trop courte (faux positifs)
- [ ] Filtrer les catégories de logs ingérées (sinon facture qui explose)
- [ ] Distinguer rétention gratuite (31 jours) et rétention étendue (payante)

## Décisions techniques prises
_À compléter._

## Captures d'écran
_Voir `/screenshots/phase-9/`_
