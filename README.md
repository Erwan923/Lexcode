<p align="center">
  <img src="logo.png" width="200" alt="Lexcode Logo"/>
</p>

<h1 align="center">
  <span style="color: #FF0000; font-family: 'Blender Pro', 'Orbitron', sans-serif; text-shadow: 0 0 5px #FF0000, 0 0 10px #FF0000; letter-spacing: 3px; font-weight: bold;">
    LEXCODE
  </span>
</h1>

<div align="center">
  <strong>Automatisation de scans de sécurité avec Ansible</strong><br>
  <img src="https://img.shields.io/badge/python-3.9+-blue.svg"/>
  <img src="https://img.shields.io/badge/license-MIT-green.svg"/>
  <img src="https://img.shields.io/badge/security-scanning-red.svg"/>
</div>


## À propos
Lexcode automatise les scans de sécurité en orchestrant des outils de scans de vulnérabilités via Ansible, avec génération de rapports intelligents.

## Installation
```bash
git clone https://github.com/Erwan923/Lexcode.git
cd Lexcode
pip install -r requirement.txt
```

## Utilisation

### Scans Rapides
```bash
# Scan basique
lexcode 192.168.1.100

# Scan web
lexcode example.com --type web

# Scan avec tags
lexcode 192.168.1.100 --tags ssl http
```

### Types de Scans
- `basic` - Scan Nmap standard
- `web` - Vulnérabilités web
- `passive` - Reconnaissance sans interaction
- `infrastructure` - Analyse complète
- `rustscan` - Scan rapide (RustScan)
- `trivy` - Analyse de conteneurs
- `light` - Scan léger

### Options Principales
```bash
lexcode --help              # Afficher l'aide
lexcode --list-tags         # Lister les tags disponibles
lexcode <target> --ai-report # Générer un rapport IA
lexcode --gui               # Lancer l'interface web
```

## Rapports
Les résultats sont disponibles en XML, JSON, Markdown et HTML avec une analyse IA optionnelle.

## Architecture
```
├── API REST (FastAPI)
├── Core (Parser, Scanner)
├── Rapports (XML/JSON/MD/HTML)
└── Templates de Scan (Markdown)
```

## Contribution
Les contributions sont les bienvenues. Voir [CONTRIBUTING.md](CONTRIBUTING.md) pour plus d'informations.

## Licence
MIT
