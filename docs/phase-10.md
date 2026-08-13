# Phase 10 — Sauvegarde : Azure Backup

**Statut** : ⬜ À faire
**Domaine AZ-104** : Superviser et sauvegarder les ressources Azure
**Coût estimé** : ~0,20 €
**Durée recommandée** : 1h30

## Objectifs
- Configurer un Recovery Services Vault
- Définir une politique de sauvegarde
- Effectuer une restauration de test

## Prérequis
- Phase 3 terminée (VM existante, redémarrée si deallocate)

## Checklist des tâches
- [ ] Créer le Recovery Services Vault `rsv-contoso-prod-euw-01`
- [ ] Créer une politique de sauvegarde personnalisée (quotidienne, rétention 7 jours pour le lab)
- [ ] Activer la sauvegarde sur la VM Windows (Phase 3)
- [ ] Déclencher une sauvegarde manuelle immédiate
- [ ] Simuler un incident (modifier un fichier) puis restaurer depuis le point de sauvegarde
- [ ] Documenter le RPO et RTO obtenus

## ⚠️ Pièges à surveiller
- [ ] Prévoir 20-30 min pour la première sauvegarde
- [ ] Éviter une rétention trop longue par défaut (coût de stockage)
- [ ] Le soft-delete du Recovery Services Vault empêche une suppression immédiate
- [ ] Préférer restaurer vers une VM séparée plutôt qu'écraser l'originale

## Décisions techniques prises
_À compléter._

## Captures d'écran
_Voir `/screenshots/phase-10/`_

## 🧹 Nettoyage fin de session (si fin de projet)
- [ ] Désactiver la sauvegarde
- [ ] Supprimer les points de restauration
