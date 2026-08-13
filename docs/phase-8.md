# Phase 8 — Haute disponibilité : Load Balancer & Availability Zones

**Statut** : ⬜ À faire
**Domaine AZ-104** : Configurer et gérer la mise en réseau virtuelle
**Coût estimé** : ~0,10 € (LB à supprimer en fin de session)
**Durée recommandée** : 2 heures

## Objectifs
- Répartir la charge entre 2 VM identiques
- Choisir Availability Set (moins cher) ou Availability Zones (plus résilient)
- Tester la tolérance de panne

## Prérequis
- Phase 3 terminée (VM opérationnelles ou à recréer x2)

## Checklist des tâches
- [ ] Choisir Availability Set (budget) ou Availability Zones (résilience max) — documenter le choix
- [ ] Créer le Load Balancer `lb-contoso-prod-euw-01` (Standard SKU) avec IP publique
- [ ] Configurer le backend pool avec les 2 VM
- [ ] Configurer une health probe HTTP (port 80)
- [ ] Installer IIS ou nginx sur chaque VM pour tester
- [ ] Simuler une panne (arrêter une VM) et observer la bascule
- [ ] Documenter le choix Availability Set vs Zones et son impact budgétaire

## ⚠️ Pièges à surveiller
- [ ] Toujours utiliser Standard SKU (Basic SKU en fin de vie)
- [ ] Standard LB exige un NSG explicite sur les VM
- [ ] Ouvrir le port 80/443 dans le NSG `snet-app` (sinon health probe "Unhealthy")
- [ ] Vérifier la disponibilité des Availability Zones dans votre région
- [ ] IP publique Standard obligatoire avec Standard LB

## Décisions techniques prises
_À compléter._

## Captures d'écran
_Voir `/screenshots/phase-8/`_

## 🧹 Nettoyage fin de session
- [ ] Supprimer le Load Balancer
- [ ] Supprimer l'IP publique
- [ ] Deallocate les VM backend
