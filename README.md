# Contoso Cloud Migration 

> Migration Azure de bout en bout d'une PME fictive de 150 employés (Contoso Corp), de la fondation réseau à l'exploitation en production. Projet réalisé dans le cadre de la préparation à la certification **AZ-104: Microsoft Azure Administrator**.

## 🎯 Contexte métier

Contoso Corp, PME de 150 employés, migre son infrastructure on-premise vers Azure. Ce dépôt documente, phase par phase, le déploiement complet réalisé en tant qu'administrateur cloud : gouvernance, réseau, calcul, stockage, identité, sécurité, application, haute disponibilité, supervision et sauvegarde.

## 🏗️ Architecture cible

_À compléter en Phase 0 / Phase 12 : schéma global assemblé (voir `/architecture`)._

![Architecture globale](architecture/architecture-globale.png)

## 🧭 Convention de nommage

Voir [`docs/naming-convention.md`](docs/naming-convention.md) pour la convention complète appliquée à toutes les ressources du projet.

Format général : `<type>-<projet>-<env>-<region>-<instance>`
Exemple : `rg-contoso-prod-euw-01`, `vnet-contoso-prod-euw-01`

## 📋 Phases du projet

| Phase | Titre | Domaine AZ-104 | Statut | Doc |
|---|---|---|---|---|
| 0 | Cadrage & README | Gouvernance | ⬜ À faire | [phase-0.md](docs/phase-0.md) |
| 1 | Fondations (RG, naming, tags) | Gérer les identités et gouvernances Azure | ⬜ À faire | [phase-1.md](docs/phase-1.md) |
| 2 | Réseau (VNet, Subnets, NSG, Bastion) | Implémenter et gérer le stockage / réseau virtuel | ⬜ À faire | [phase-2.md](docs/phase-2.md) |
| 3 | Calcul (VM Windows/Linux) | Déployer et gérer les ressources de calcul Azure | ⬜ À faire | [phase-3.md](docs/phase-3.md) |
| 4 | Stockage | Implémenter et gérer le stockage | ⬜ À faire | [phase-4.md](docs/phase-4.md) |
| 5 | Identité & Gouvernance (Entra ID, RBAC, Policy) | Gérer les identités et gouvernances Azure | ⬜ À faire | [phase-5.md](docs/phase-5.md) |
| 6 | Sécurité (Key Vault, Private Endpoints) | Configurer et gérer la sécurité | ⬜ À faire | [phase-6.md](docs/phase-6.md) |
| 7 | Application (App Service) | Déployer et gérer les ressources de calcul Azure | ⬜ À faire | [phase-7.md](docs/phase-7.md) |
| 8 | Haute disponibilité (LB, Availability Zones) | Configurer et gérer la mise en réseau virtuelle | ⬜ À faire | [phase-8.md](docs/phase-8.md) |
| 9 | Supervision (Monitor, Log Analytics) | Superviser et sauvegarder les ressources Azure | ⬜ À faire | [phase-9.md](docs/phase-9.md) |
| 10 | Sauvegarde (Azure Backup) | Superviser et sauvegarder les ressources Azure | ⬜ À faire | [phase-10.md](docs/phase-10.md) |
| 11 | Optimisation coûts & perfs | Gérer les identités et gouvernances Azure | ⬜ À faire | [phase-11.md](docs/phase-11.md) |
| 12 | Documentation finale | Portfolio | ⬜ À faire | [phase-12.md](docs/phase-12.md) |

Légende statut : ⬜ À faire · 🟨 En cours · ✅ Terminé

## 🎓 Compétences AZ-104 couvertes

- ✅ Gérer les identités et gouvernances Azure (RG, tags, RBAC, Policy, coûts)
- ✅ Implémenter et gérer le stockage
- ✅ Déployer et gérer les ressources de calcul Azure (VM, App Service)
- ✅ Configurer et gérer la mise en réseau virtuelle (VNet, NSG, LB, Bastion, Private Endpoint)
- ✅ Superviser et sauvegarder les ressources Azure (Monitor, Log Analytics, Backup)

## 💰 Coût réel du lab

_À mettre à jour au fur et à mesure. Budget estimé si nettoyage rigoureux entre sessions : ~1 à 2 €. Voir détail dans [phase-12.md](docs/phase-12.md)._

| Phase | Coût réel constaté | Notes |
|---|---|---|
| 0 | 0 € | — |
| ... | | |

## 🔑 Décisions techniques clés

_À compléter au fil des phases (une entrée par décision d'architecture significative, avec justification)._

## 🐛 Pièges rencontrés et résolus

_À compléter avec les galères réelles rencontrées — très valorisé en entretien._

## 📁 Structure du dépôt

```
azure-migration-portfolio/
├── README.md                  # Ce fichier
├── docs/                      # Un fichier par phase + convention de nommage
│   ├── naming-convention.md
│   ├── phase-0.md ... phase-12.md
├── scripts/                   # Scripts ARM / Bicep / Terraform / CLI
├── screenshots/                # Captures d'écran par phase
│   ├── phase-0/ ... phase-12/
└── architecture/              # Schémas (.drawio, .png)
```

## 🚀 Pour aller plus loin

_À compléter en Phase 12 : ce qui serait fait avec plus de budget/temps (Azure Firewall, ExpressRoute, multi-région...)._

