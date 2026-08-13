# Phase 12 — Documentation finale professionnelle

**Statut** : ⬜ À faire
**Domaine AZ-104** : Portfolio (communication technique)
**Coût estimé** : 0 €
**Durée recommandée** : 2 à 3 heures — la phase la plus importante pour l'impact recruteur

## Objectifs
- Finaliser le README avec schéma global, décisions techniques et coût réel
- Préparer une présentation de 5 minutes du projet (entretien)

## Checklist des tâches
- [ ] Compléter toutes les sections du README principal (contexte, architecture, phases, coûts, décisions, pièges)
- [ ] Ajouter le schéma d'architecture final assemblé dans `/architecture`
- [ ] Préparer un pitch oral de 5 min (contexte, architecture, 3 décisions clés, 1 piège résolu, coût final)
- [ ] Publier le dépôt GitHub en public + ajouter le lien au CV/LinkedIn
- [ ] Exécuter la checklist de nettoyage final (voir README, section 🧹)

## ⚠️ Pièges à surveiller
- [ ] README pas trop long — structurer avec titres clairs et sommaire (30 sec de lecture recruteur)
- [ ] Toujours inclure un schéma visuel
- [ ] Toujours mentionner le coût réel (différenciateur pour un poste cloud)

## Checklist de nettoyage final (copiée du README)
- [ ] Retirer les Resource Locks (Phase 5) avant toute suppression
- [ ] Supprimer Azure Bastion (Phase 2)
- [ ] Supprimer le Load Balancer + IP publique (Phase 8)
- [ ] Supprimer ou downgrader l'App Service Plan en Free (Phase 7)
- [ ] Deallocate ou supprimer les VM (Phase 3)
- [ ] Désactiver la sauvegarde et purger les points de restauration (Phase 10)
- [ ] Vérifier Cost Management à J+2 pour confirmer l'absence de coût résiduel
- [ ] Supprimer les RG dans l'ordre : app → security → compute → storage → monitoring → network

## Captures d'écran
_Voir `/screenshots/phase-12/`_
