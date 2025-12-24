# Dev Tools - Steel Evolution

Ce dossier contient tous les outils de développement custom pour accélérer le workflow.

## Structure

```
tools/
├── balance-calculator/     # Calculateur d'équilibrage
├── asset-optimizer/        # Optimiseur d'assets
├── data-validator/         # Validateur de données
├── build-scripts/          # Scripts de build
└── analytics-dashboard/    # Dashboard analytics (future)
```

## Outils Disponibles

### 1. Balance Calculator

Calcule et valide les formules d'équilibrage du jeu.

```bash
cd tools/balance-calculator
npm install
npm start
```

**Features:**
- Calcul XP par niveau
- Calcul power scaling ennemis
- Simulation drop rates
- Validation gacha pity
- Export vers CSV/JSON

### 2. Asset Optimizer

Optimise automatiquement les assets pour mobile.

```bash
cd tools/asset-optimizer
npm install
node optimize.js --input ../assets-source --output ../client/Assets
```

**Features:**
- Compression PNG/JPG
- Resize automatique
- Conversion formats
- Génération atlases
- Validation sizes

### 3. Data Validator

Valide les fichiers de données du jeu.

```bash
cd tools/data-validator
npm install
npm run validate
```

**Features:**
- Validation JSON/CSV
- Check IDs uniques
- Validation stats ranges
- Check référence integrity
- Report erreurs

### 4. Build Scripts

Scripts utilitaires pour builds automatisés.

```bash
cd tools/build-scripts
./build-android.sh
./build-ios.sh
```

**Scripts:**
- `build-android.sh` - Build APK/AAB
- `build-ios.sh` - Build IPA
- `increment-version.sh` - Bump version
- `deploy.sh` - Deploy to stores

## Prérequis

- **Node.js 18+**
- **Python 3.9+** (pour certains tools)
- **ImageMagick** (pour asset optimizer)

## Installation Globale

```bash
cd tools
npm install
```

## Usage Recommandé

### Avant chaque commit
```bash
# Valider les données
cd tools/data-validator
npm run validate

# Optimiser nouveaux assets
cd tools/asset-optimizer
npm run optimize-new
```

### Avant chaque release
```bash
# Valider tout
cd tools
npm run validate-all

# Build
cd tools/build-scripts
./build-all.sh
```

## Développer de Nouveaux Tools

Structure recommandée :
```
tools/
└── mon-tool/
    ├── package.json
    ├── README.md
    ├── src/
    │   └── index.js
    └── tests/
        └── index.test.js
```

Guidelines :
- Node.js ou Python
- CLI-friendly
- Tests unitaires
- Documentation claire
- Logs verbose (option --verbose)

## Contributing

Ajouter des tools utiles ! Voir [CONTRIBUTING.md](../CONTRIBUTING.md)

## Resources

- [Node.js](https://nodejs.org/)
- [Python](https://python.org/)
- [ImageMagick](https://imagemagick.org/)
- [Sharp](https://sharp.pixelplumbing.com/) - Image processing
