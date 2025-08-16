---
layout: default
title: Docs
permalink: /docs
---

# Docs / Документация (client-side)

Ниже — краткий гид по структуре проекта и Polytone.  
Для детальной доки см. репозиторий Polytone.

## Project layout
```text
assets/davidparticles/
  polytone/
    custom_particles/      # JSON-логика частиц
    block_modifiers/       # эмиттеры по блокам
    biome_modifiers/       # туман/цвета/ambient по биомам
    fluid_modifiers/       # цвета/туман во флюидах
    dimension_modifiers/   # цвета и колормэпы в измерениях
    particle_modifiers/    # общие правки частиц
    colormaps/             # PNG + JSON оси/формулы
  particles/               # vanilla id → texture
  textures/                # PNG спрайты эффектов
  models/                  # JSON модели
```

## Polytone quick links
- **Custom Particles** — initializer, ticker, render, emitters, `liquid_affinity`
- **Block/Biome Modifiers** — ambient particles & sounds
- **Colormaps** — JSON + PNG, `x_axis`/`y_axis`, `default_color`
- **Math DSL** — `rand()`, `gaussian()`, `TIME`, `DX/DY/DZ`, `DISTANCE_SQUARED`

**Rules we follow**
- `rand()` и `gaussian()` без аргументов, масштабирование умножением.
- Только валидные `rotation_mode`: `none | face_camera | movement | movement_aligned`.
- В `particle_emitters`: только `chance`, `particle`, `x`, `y`, `z` (выражения).
- `TIME` вместо `GAMETIME`; `DISTANCE_SQUARED` вместо `DISTANCE_TO_PLAYER`.
