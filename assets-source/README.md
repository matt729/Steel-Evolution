# Assets Source - Steel Evolution

Ce dossier contient tous les **assets source** (non-optimisés) utilisés pour créer les assets finaux du jeu.

## ⚠️ Important

Les fichiers dans ce dossier sont **volumineux** et utilisent **Git LFS** (Large File Storage).

## Structure

```
assets-source/
├── characters/
│   ├── proto/          # Proto stage designs
│   ├── regulier/       # Régulier stage designs
│   ├── optimise/       # Optimisé stage designs
│   ├── variant/        # Variant stage designs
│   └── resurgent/      # Résurgent stage designs
├── equipment/
│   ├── cpu/
│   ├── gpu/
│   ├── ram/
│   └── [autres slots]/
├── enemies/
│   ├── chapter-1/
│   ├── chapter-2/
│   └── [autres chapitres]/
├── ui/
│   ├── buttons/
│   ├── backgrounds/
│   ├── icons/
│   └── hud/
└── prompts/
    ├── midjourney/     # Prompts Midjourney
    ├── dalle/          # Prompts DALL-E
    └── stable-diffusion/
```

## Types de Fichiers

### Source Files (Haute Résolution)
- **PSD** (Photoshop) - Layers éditables
- **AI** (Illustrator) - Vectors éditables
- **Sketch** - Design files
- **Figma** - UI/UX designs

### Exports pour le Jeu
Les assets source sont optimisés puis exportés vers `client/Assets/` ou `client/lib/assets/`

## Workflow Asset

1. **Créer** - Design dans Photoshop/Illustrator
2. **Optimiser** - Réduire taille, convertir format
3. **Exporter** - Vers dossier client
4. **Commiter** - Source + Export

## Git LFS Setup

```bash
# Installer Git LFS
git lfs install

# Tracker les gros fichiers
git lfs track "*.psd"
git lfs track "*.ai"
git lfs track "*.sketch"
```

## Guidelines

### Characters
- Résolution: 512x512px minimum (source)
- Export: 256x256px pour game (optimisé)
- Format: PNG transparent
- Style: Chibi cyberpunk

### Equipment
- Résolution: 256x256px minimum (source)
- Export: 128x128px pour game
- Format: PNG transparent
- Style: Cohérent avec characters

### UI
- Résolution: 2x ou 3x (Retina)
- Export: Multiple resolutions (@1x, @2x, @3x)
- Format: PNG ou WebP

## Prompts IA

Le dossier `prompts/` contient tous les prompts utilisés pour générer les assets avec :
- Midjourney
- DALL-E 3
- Stable Diffusion

Format : Markdown avec metadata (settings, seed, etc.)

## Naming Convention

```
[type]_[name]_[variant]_[resolution].ext

Exemples :
char_proto001_idle_512.psd
equip_cpu_legendary_256.ai
ui_button_primary_2x.sketch
```

## Compression & Optimization

Avant export vers client :
- **PNG** : TinyPNG ou pngquant
- **JPG** : Quality 85-90%
- **WebP** : Quality 80% (pour backgrounds)

Tools recommandés :
- [TinyPNG](https://tinypng.com/)
- [ImageOptim](https://imageoptim.com/)
- [Squoosh](https://squoosh.app/)
