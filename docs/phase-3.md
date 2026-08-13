# Phase 3 — Calcul : Machines Virtuelles Windows & Linux

**Statut** : ⬜ À faire
**Domaine AZ-104** : Déployer et gérer les ressources de calcul Azure
**Coût estimé** : ~0,15 €
**Durée recommandée** : 1h30 à 2 heures

## Objectifs
- Déployer des VM dans les bons subnets
- Comprendre les tailles de VM et le rapport coût/performance
- Se connecter en toute sécurité via Bastion (pas d'IP publique)

## Prérequis
- Phase 2 terminée (VNet + subnets + Bastion opérationnels)

## Checklist des tâches
- [ ] Déployer VM Windows Server (`vm-contoso-web01-prod-euw`, Standard_B2s) dans `snet-app`
- [ ] Déployer VM Linux Ubuntu (`vm-contoso-web02-prod-euw`, Standard_B1s) dans `snet-app`
- [ ] Désactiver l'IP publique à la création
- [ ] Se connecter aux deux VM via Bastion et vérifier la connectivité
- [ ] Deallocate (pas juste Stop) les deux VM en fin de session
- [ ] Documenter le choix de taille de VM (cas d'usage, budget)

## ⚠️ Pièges à surveiller
- [ ] "Stop" OS ≠ "Stop (Deallocate)" Azure — seul le deallocate arrête la facturation
- [ ] Le disque managé est facturé même VM arrêtée
- [ ] Ne pas perdre le mot de passe/clé SSH configuré à la création
- [ ] Éviter les tailles Dv5 par défaut, préférer B-series pour un lab

## Décisions techniques prises
_À compléter._

## Captures d'écran
_Voir `/screenshots/phase-3/`_

## 🧹 Nettoyage fin de session
- [ ] Deallocate VM Windows
- [ ] Deallocate VM Linux
