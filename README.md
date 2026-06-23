# SIEM Lab - Wazuh

> Lab pratique Wazuh SIEM : installation, regles personnalisees, dashboards de securite.

![Wazuh](https://img.shields.io/badge/Wazuh-4.7-005571?style=flat-square)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Author](https://img.shields.io/badge/Author-ibramoha2-CC0000?style=flat-square)

## Architecture
```
[Agents Linux/Windows] --> [Wazuh Manager] --> [Wazuh Indexer] --> [Dashboard]
```

## Lancement rapide (Docker)
```bash
git clone https://github.com/ibramoha2/siem-lab
cd siem-lab
docker-compose up -d
# Dashboard: https://localhost:443
```

## Regles incluses

| ID | Description | Niveau |
|----|-------------|--------|
| 100001 | Brute-force SSH (>5 echecs/min) | 12 |
| 100002 | Creation de compte utilisateur | 14 |
| 100003 | Modification /etc/passwd ou /etc/shadow | 13 |
| 100004 | Connexion SSH hors horaires (22h-6h) | 8 |

**Auteur :** [@ibramoha2](https://github.com/ibramoha2) | Niger