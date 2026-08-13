# Phase 5 — Identité & Gouvernance : Entra ID, RBAC, Azure Policy

**Statut** : ⬜ À faire
**Domaine AZ-104** : Gérer les identités et gouvernances Azure
**Coût estimé** : 0 €
**Durée recommandée** : 1 heure

## Objectifs
- Créer des utilisateurs et groupes dans Microsoft Entra ID
- Attribuer des rôles RBAC précis (pas de rôle Owner global)
- Appliquer une Azure Policy pour forcer la conformité

## Prérequis
- Phases 1 à 4 terminées

## Checklist des tâches
- [ ] Créer 2 groupes Entra ID (`Contoso-CloudAdmins`, `Contoso-NetworkTeam`) + 1 utilisateur test
- [ ] Attribuer RBAC `Contributor` sur `rg-contoso-compute` au groupe CloudAdmins
- [ ] Attribuer RBAC `Network Contributor` sur `rg-contoso-network` au groupe NetworkTeam
- [ ] Attribuer RBAC `Reader` (scope abonnement) à l'utilisateur test
- [ ] Créer/appliquer une Azure Policy restreignant les régions de déploiement (ex. westeurope uniquement)
- [ ] Appliquer un verrou `CanNotDelete` sur `rg-contoso-network`
- [ ] Documenter le principe de moindre privilège appliqué

## ⚠️ Pièges à surveiller
- [ ] Ne pas attribuer Owner par facilité — préférer Contributor/Reader/Network Contributor
- [ ] Tester une Policy en effet "Deny" prudemment (peut bloquer les déploiements suivants)
- [ ] Retirer le Resource Lock `CanNotDelete` avant le nettoyage final
- [ ] Ne pas confondre rôle RBAC (ressources) et rôle Entra ID (annuaire)

## Décisions techniques prises
_À compléter._

## Captures d'écran
_Voir `/screenshots/phase-5/`_
