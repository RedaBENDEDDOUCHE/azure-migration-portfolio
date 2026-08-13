# Phase 4 — Stockage : Storage Account

**Statut** : ⬜ À faire
**Domaine AZ-104** : Implémenter et gérer le stockage
**Coût estimé** : <0,05 €
**Durée recommandée** : 1 heure

## Objectifs
- Créer un compte de stockage avec le bon niveau de redondance
- Créer un conteneur Blob et un partage de fichiers
- Comprendre Hot/Cool/Archive et LRS/GRS/ZRS

## Prérequis
- Phase 1 terminée (`rg-contoso-storage-prod-euw-01`)

## Checklist des tâches
- [ ] Créer le Storage Account `stcontosoprodeuw01` (StorageV2, LRS, Hot)
- [ ] Créer 2 conteneurs Blob privés (`documents`, `backups`) + upload fichier test
- [ ] Créer un File Share `sharedconfig` (5 Go) et le monter sur la VM Windows (Phase 3)
- [ ] Générer un SAS token avec expiration 1h
- [ ] Documenter LRS vs ZRS vs GRS et le choix retenu

## ⚠️ Pièges à surveiller
- [ ] Vérifier l'unicité globale du nom de storage account
- [ ] Ne jamais laisser un conteneur en accès public par erreur
- [ ] Distinguer clé d'accès (total) vs SAS token (limité/temporaire)
- [ ] Le niveau Archive rend les données inaccessibles pendant plusieurs heures

## Décisions techniques prises
_À compléter._

## Captures d'écran
_Voir `/screenshots/phase-4/`_
