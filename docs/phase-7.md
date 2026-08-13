# Phase 7 — Application : Azure App Service

**Statut** : ⬜ À faire
**Domaine AZ-104** : Déployer et gérer les ressources de calcul Azure
**Coût estimé** : ~0,05 € (App Service Plan B1, à supprimer/scale down après le lab)
**Durée recommandée** : 1h30 à 2 heures

## Objectifs
- Déployer une application web PaaS
- Connecter l'application au Key Vault via Managed Identity
- Comprendre les plans App Service (Free, Basic, Standard)

## Prérequis
- Phase 6 terminée (Key Vault opérationnel)

## Checklist des tâches
- [ ] Créer l'App Service Plan `asp-contoso-prod-euw-01` en tier **B1** (pas Free)
- [ ] Déployer la Web App `app-contoso-portal-prod-euw-01`
- [ ] Activer une Managed Identity système sur la Web App
- [ ] Attribuer le rôle `Key Vault Secrets User` à cette identité sur le Key Vault
- [ ] Configurer la VNet Integration vers `snet-app`
- [ ] Lire un secret Key Vault depuis le code de l'app (SDK ou `@Microsoft.KeyVault(...)`)

## ⚠️ Pièges à surveiller
- [ ] Le tier Free (F1) ne supporte pas la VNet Integration
- [ ] Attribuer le rôle RBAC à la Managed Identity (sinon erreur 403)
- [ ] VNet Integration = trafic sortant uniquement (pas pour sécuriser l'entrant)
- [ ] Distinguer Managed Identity system-assigned vs user-assigned

## Décisions techniques prises
_À compléter._

## Captures d'écran
_Voir `/screenshots/phase-7/`_

## 🧹 Nettoyage fin de session
- [ ] Supprimer ou scale down l'App Service Plan en F1
