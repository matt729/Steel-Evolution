# Steel Evolution

> Idle RPG Mobile - Cyberpunk Robots & AI

[![Version](https://img.shields.io/badge/version-0.1.0--dev-orange.svg)](CHANGELOG.md)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Android%20%7C%20iOS-green.svg)]()

## 📱 À Propos

**Steel Evolution** est un idle RPG mobile inspiré de Legend of Mushroom, transposé dans un univers cyberpunk post-apocalyptique. Évoluez un proto-robot à travers 5 stades transformatifs, de la rouille aux étoiles.

### 🎮 Caractéristiques Principales

- 🤖 **Évolution Unique** - Un seul héros avec 5 stades d'évolution dramatiques
- ⚙️ **Core Protocol** - Système de loot orienté élément (66% contrôle)
- 🔥 **Fusion Endgame** - Merge de builds pour meta complexe
- 💎 **Gacha Fair** - Pas de héros dans le gacha, transparent & équitable
- 🎯 **100% Auto-Battle** - Optionnel manuel pour contrôle tactique
- 📊 **F2P Friendly** - Entièrement jouable gratuitement

### 🌟 Les 5 Stades d'Évolution

1. **Proto** (1-10) - Découverte pathétique
2. **Régulier** (11-30) - Normalisation
3. **Optimisé** (31-60) - Maîtrise + Fusion débloquée
4. **Variant** (61-100) - Divergence endgame
5. **Résurgent** (100+) - Transcendance divine

## 🚀 Quick Start

### Prérequis

- **Unity 2022.3 LTS** (recommandé) ou **Flutter 3.16+**
- **Android Studio** / **Xcode**
- **Supabase** account (backend)
- **Node.js 18+** (pour outils)

### Installation

```bash
# Cloner le repository
git clone https://github.com/matt729/Steel-Evolution.git
cd Steel-Evolution

# Option A : Unity
# Ouvrir le dossier client/Unity dans Unity Hub

# Option B : Flutter
cd client/flutter
flutter pub get
flutter run
```

### Configuration Backend

```bash
cd backend/supabase
supabase init
supabase db push
```

Voir [docs/SETUP.md](docs/SETUP.md) pour instructions détaillées.

## 📚 Documentation

- 📖 [Game Design Document (GDD)](docs/GDD.md) - Design complet du jeu
- 🔧 [Technical Requirements (TRD)](docs/TRD.md) - Architecture technique
- 🔌 [API Documentation](docs/API.md) - API Supabase
- 📋 [Setup Guide](docs/SETUP.md) - Guide d'installation
- 🤝 [Contributing](CONTRIBUTING.md) - Comment contribuer

## 🗺️ Roadmap

### Phase 1 : MVP (Mois 1-2) ✅ En cours
- [x] Core combat loop
- [x] 30 stages (Chapitre 1)
- [x] Equipment system (4 slots)
- [x] Proto → Régulier évolution
- [ ] Basic UI (Hub, Battle, Character)
- [ ] Save/Load local

### Phase 2 : Alpha (Mois 3)
- [ ] 50 stages (Chapitres 1-2)
- [ ] Gacha system + pity
- [ ] Core Protocol
- [ ] 10 slots équipement
- [ ] IAP integration
- [ ] Analytics

### Phase 3 : Beta (Mois 4)
- [ ] 100 stages (5 chapitres)
- [ ] Évolution complète (5 stades)
- [ ] Events system
- [ ] Leaderboards
- [ ] Fusion system

### Phase 4 : Launch (Mois 5-6)
- [ ] Soft launch (Canada, Philippines)
- [ ] Tuning économie
- [ ] Global launch
- [ ] Live ops

Voir [Project Board](https://github.com/matt729/Steel-Evolution/projects) pour suivi détaillé.

## 🏗️ Structure du Projet

```
Steel-Evolution/
├── .github/              # GitHub Actions, templates
├── client/               # Code client (Unity/Flutter)
│   ├── Assets/          # Assets Unity
│   └── lib/             # Code Flutter
├── backend/              # Backend (Supabase, n8n)
│   ├── supabase/        # Schema, migrations, functions
│   └── n8n-workflows/   # Workflows automation
├── docs/                 # Documentation
├── assets-source/        # Assets source (PSD, AI)
└── tools/                # Dev tools
```

## 🛠️ Tech Stack

**Frontend:**
- Unity 2022.3 LTS (C#) ou Flutter 3.16+ (Dart)
- Portrait mobile-first

**Backend:**
- Supabase (PostgreSQL + Auth + Storage + Realtime)
- n8n (workflow automation)

**CI/CD:**
- GitHub Actions
- Unity Cloud Build / Codemagic

**Analytics:**
- Firebase Analytics
- Unity Analytics

**Tools:**
- Midjourney/DALL-E (asset generation)
- Notion (project management)

## 🤝 Contribuer

Les contributions sont les bienvenues ! Consultez [CONTRIBUTING.md](CONTRIBUTING.md) pour :
- Comment reporter des bugs
- Proposer des features
- Soumettre des pull requests
- Standards de code

## 📊 Métriques de Succès

**Launch (Mois 1):**
- 10K+ téléchargements
- D7 Retention: 18%+
- 4.0+ rating stores

**Stabilité (Mois 3):**
- 50K+ téléchargements
- D30 Retention: 6%+
- ARPDAU: €0.10+

**Croissance (Mois 6):**
- 200K+ téléchargements
- 5K+ DAU
- Top 100 catégorie (région)

## 📄 License

Ce projet est sous licence MIT - voir [LICENSE](LICENSE) pour détails.

## 🙏 Crédits

- **Design & Development:** Matt
- **AI Assistant:** Claude (Anthropic)
- **Inspiration:** Legend of Mushroom
- **Art Style:** Cyberpunk 2077, Megaman, Cookie Run

## 📧 Contact

- **GitHub Issues:** [Créer une issue](https://github.com/matt729/Steel-Evolution/issues)
- **Discussions:** [GitHub Discussions](https://github.com/matt729/Steel-Evolution/discussions)

---

⭐ **Star ce repo si tu aimes le projet !**

Made with ❤️ and ☕ by Matt
