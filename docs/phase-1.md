# Phase 1 — Fondations : Groupes de ressources & Gouvernance de nommage

**Statut** : ⬜ À faire
**Domaine AZ-104** : Gérer les identités et gouvernances Azure
**Coût estimé** : 0 €
**Durée recommandée** : 30 à 45 minutes

## Objectifs
- Créer la structure de groupes de ressources
- Appliquer une stratégie de tags cohérente
- Comprendre le scope abonnements/RG/ressources

## Prérequis
- Abonnement Azure (Free Tier ou PAYG avec alerte budget)
- Azure CLI ou Cloud Shell

## Checklist des tâches
- [ ] Créer les 6 groupes de ressources dans la même région (`westeurope` ou proche)
  - [ ] `rg-contoso-network-prod-euw-01`
  - [ ] `rg-contoso-compute-prod-euw-01`
  - [ ] `rg-contoso-storage-prod-euw-01`
  - [ ] `rg-contoso-security-prod-euw-01`
  - [ ] `rg-contoso-monitoring-prod-euw-01`
  - [ ] `rg-contoso-app-prod-euw-01`
- [ ] Ajouter les tags `Environment`, `Project`, `Owner`, `CostCenter` sur chacun
- [ ] Configurer une alerte de budget à 5 € (Cost Management)
- [ ] Documenter dans le README le choix de séparation par domaine vs par application

## ⚠️ Pièges à surveiller
- [ ] Tous les RG dans la même région (sinon complique le peering réseau)
- [ ] Ne pas oublier l'alerte de budget
- [ ] Ne pas confondre tag hérité (niveau RG) et tag spécifique (niveau ressource)

## Décisions techniques prises
_À compléter._

## Captures d'écran
_Voir `/screenshots/phase-1/`_
