# Convention de nommage — Contoso Cloud Migration

Basée sur le Cloud Adoption Framework (CAF) de Microsoft.

## Règle générale

```
<type>-<projet>-<env>-<region>-<instance>
```

- **type** : préfixe abrégé du type de ressource (voir tableau)
- **projet** : `contoso`
- **env** : `prod` / `dev` / `test` (ce projet utilise `prod` par défaut, à adapter si vous dupliquez un environnement)
- **region** : code court de région (`euw` = West Europe, `eus` = East US, etc. — à adapter selon votre région)
- **instance** : numéro sur 2 chiffres (`01`, `02`...) pour permettre plusieurs instances du même type

## Tableau des préfixes par type de ressource

| Ressource | Préfixe | Exemple |
|---|---|---|
| Resource Group | `rg-` | `rg-contoso-network-prod-euw-01` |
| Virtual Network | `vnet-` | `vnet-contoso-prod-euw-01` |
| Subnet | `snet-` | `snet-app`, `snet-data`, `snet-appgw` |
| Network Security Group | `nsg-` | `nsg-app-prod-euw-01` |
| Azure Bastion | `bas-` | `bas-contoso-prod-euw-01` |
| Virtual Machine | `vm-` | `vm-contoso-web01-prod-euw` |
| Managed Disk | `disk-` | `disk-contoso-web01-osdisk` |
| Storage Account* | (voir note) | `stcontosoprodeuw01` |
| Key Vault | `kv-` | `kv-contoso-prod-euw-01` |
| App Service Plan | `asp-` | `asp-contoso-prod-euw-01` |
| App Service (Web App) | `app-` | `app-contoso-web-prod-euw-01` |
| Load Balancer | `lb-` | `lb-contoso-prod-euw-01` |
| Public IP | `pip-` | `pip-contoso-lb-prod-euw-01` |
| Availability Set | `avset-` | `avset-contoso-web` |
| Log Analytics Workspace | `law-` | `law-contoso-prod-euw-01` |
| Action Group | `ag-` | `ag-contoso-itoncall` |
| Recovery Services Vault | `rsv-` | `rsv-contoso-prod-euw-01` |
| Private Endpoint | `pe-` | `pe-contoso-kv-prod-euw-01` |
| Azure Policy (définition custom) | `pol-` | `pol-contoso-allowedregions` |

### ⚠️ Exception : Storage Account

Les noms de storage account doivent être **uniques globalement**, en **minuscules uniquement**, **sans tirets**, et **24 caractères max**. La convention standard ne s'applique donc pas directement.

Format adapté : `st<projet><env><region><instance>`
Exemple : `stcontosoprodeuw01` (19 caractères — laisse de la marge pour un suffixe si collision de nom).

## Convention de tags (appliqués à chaque groupe de ressources)

| Tag | Valeurs possibles | Exemple |
|---|---|---|
| `Environment` | `prod`, `dev`, `test` | `prod` |
| `Project` | nom du projet | `contoso-migration` |
| `Owner` | votre nom/alias | `votre-nom` |
| `CostCenter` | code arbitraire pour ce lab | `lab-az104` |

## Groupes de ressources du projet

```
rg-contoso-network-prod-euw-01
rg-contoso-compute-prod-euw-01
rg-contoso-storage-prod-euw-01
rg-contoso-security-prod-euw-01
rg-contoso-monitoring-prod-euw-01
rg-contoso-app-prod-euw-01
```

## Notes

- Toutes les ressources sont déployées dans la même région pour simplifier le peering réseau et éviter la latence inter-région.
- Les noms de subnets n'incluent pas le suffixe région/instance (ils sont scopés au VNet, donc `snet-app` suffit).
- `AzureBastionSubnet` est un nom imposé par Azure — ne pas appliquer la convention à ce sous-réseau précis.
