# Studio Director — Orquestación de Producción Audiovisual

## Propósito

Este repositorio es el núcleo de operaciones para producción de video y audio. Claude actúa como **Director de Arte Cinematográfico** en todos los proyectos que se gestionen aquí.

Para iniciar cualquier proyecto audiovisual, usar el skill `/video-director`.

## Herramientas conectadas

| Herramienta  | Uso                              | Estado       |
|--------------|----------------------------------|--------------|
| ElevenLabs   | Generación de voiceover/TTS      | ✅ Activo     |
| FFmpeg       | Montaje, exportación, conversión | ✅ Disponible |
| Higgsfield   | Generación de video con IA       | 🔜 Fase 2    |
| Airtable     | Tracking de proyectos y assets   | 🔜 Fase 3    |

## Variables de entorno requeridas

```bash
# Fase 1 — Ya disponible
ELEVENLABS_API_KEY=...
VOICE_ID=...                    # Voice ID por defecto para español

# Fase 2 — Configurar cuando tengas cuenta Higgsfield
HIGGSFIELD_API_KEY=...

# Fase 3 — Configurar con base Airtable creada
AIRTABLE_TOKEN=...
AIRTABLE_BASE_ID=...
```

## Estructura del repositorio

```
studio-director/
├── CLAUDE.md               ← Este archivo (contexto para Claude)
├── .claude/
│   └── settings.json       ← Permisos del proyecto
├── config/
│   └── tools.json          ← Configuración de APIs y presets
├── projects/               ← Un JSON por proyecto activo
│   └── {project_id}.json
├── assets/
│   ├── audio/              ← MP3/WAV generados por ElevenLabs
│   │   └── {project_id}/
│   ├── video/              ← MP4 generados por Higgsfield
│   │   └── {project_id}/
│   └── output/             ← Videos finales ensamblados
│       └── {project_id}/
└── templates/
    └── airtable-schema.json ← Diseño de base para importar
```

## Convención de nombrado

- Proyectos: `{fecha_yyyymmdd}_{tipo}_{plataforma}` — ej. `20260522_reel_instagram`
- Assets de escena: `scene_{n}_{descriptor}.{ext}` — ej. `scene_01_hero_cta.mp3`
- Outputs: `draft_v{n}.mp4`, `final_v{n}.mp4`

## Idioma de producción

Los prompts de generación (Higgsfield) se construyen en inglés para máxima compatibilidad con los modelos de IA. Los guiones y narraciones pueden estar en español — ElevenLabs con `eleven_multilingual_v2` soporta español nativo.
