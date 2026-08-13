# Phase 2 — Infrastructure réseau : VNet, Subnets, NSG, Bastion

**Statut** : ⬜ À faire
**Domaine AZ-104** : Implémenter et gérer la mise en réseau virtuelle
**Coût estimé** : ~0,40-0,50 € (Bastion à l'heure — à supprimer en fin de session)
**Durée recommandée** : 1h30 à 2 heures

## Objectifs
- Concevoir un plan d'adressage IP cohérent
- Segmenter le réseau avec des sous-réseaux dédiés
- Sécuriser l'accès admin via Azure Bastion (sans IP publique sur les VM)

## Prérequis
- Phase 1 terminée (`rg-contoso-network-prod-euw-01`)

## Checklist des tâches
- [ ] Créer le VNet `vnet-contoso-prod-euw-01` (10.0.0.0/16)
- [ ] Créer les 4 sous-réseaux
  - [ ] `snet-app` 10.0.1.0/24
  - [ ] `snet-data` 10.0.2.0/24
  - [ ] `snet-appgw` 10.0.3.0/24
  - [ ] `AzureBastionSubnet` 10.0.255.0/27 (nom imposé, ne pas modifier)
- [ ] Créer NSG-app (HTTP/HTTPS entrant, RDP/SSH uniquement depuis Bastion)
- [ ] Créer NSG-data (trafic uniquement depuis snet-app)
- [ ] Déployer Azure Bastion sur `AzureBastionSubnet`
- [ ] Documenter le plan d'adressage IP (table CIDR) dans le README

## ⚠️ Pièges à surveiller
- [ ] `AzureBastionSubnet` doit faire au minimum /26 recommandé
- [ ] Vérifier si les règles NSG s'appliquent au niveau subnet et/ou NIC
- [ ] **Supprimer Azure Bastion en fin de session** (facturé à l'heure même sans connexion)
- [ ] Espacer les priorités de règles NSG (100, 200, 300...)

## Décisions techniques prises
_À compléter._

## Captures d'écran
_Voir `/screenshots/phase-2/`_

## 🧹 Nettoyage fin de session
- [ ] Supprimer Azure Bastion
- [ ] Supprimer l'IP publique du Bastion
