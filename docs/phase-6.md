# Phase 6 — Sécurité : Key Vault & Private Endpoints

**Statut** : ⬜ À faire
**Domaine AZ-104** : Configurer et gérer la sécurité
**Coût estimé** : ~0,05 €
**Durée recommandée** : 1h30

## Objectifs
- Centraliser les secrets dans Key Vault
- Isoler l'accès réseau avec un Private Endpoint
- Comprendre Access Policies vs RBAC

## Prérequis
- Phases 2 (réseau) et 5 (RBAC) terminées

## Checklist des tâches
- [ ] Créer le Key Vault `kv-contoso-prod-euw-01` avec accès public désactivé
- [ ] Ajouter 2 secrets (mot de passe, chaîne de connexion factices)
- [ ] Créer un Private Endpoint dans `snet-data` vers le Key Vault
- [ ] Configurer la Private DNS Zone `privatelink.vaultcore.azure.net` et la lier au VNet
- [ ] Tester l'accès depuis la VM (Phase 3) via le réseau privé uniquement
- [ ] Documenter pourquoi Private Endpoint > règle de pare-feu IP publique

## ⚠️ Pièges à surveiller
- [ ] Lier la Private DNS Zone au VNet (sinon résolution de nom échoue)
- [ ] Ne pas laisser l'accès public activé "pour tester"
- [ ] Utiliser le modèle RBAC (recommandé) plutôt qu'Access Policies (historique)
- [ ] Soft-delete Key Vault activé par défaut (rétention 7-90 jours) — impact sur nettoyage/réutilisation du nom

## Décisions techniques prises
_À compléter._

## Captures d'écran
_Voir `/screenshots/phase-6/`_
