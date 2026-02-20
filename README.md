# nanobot-skill-translator

Nanobot AI skill for multi-language translation with context awareness.

## Features
- Translate text between 12+ languages
- Automatic language detection
- Context-aware conversation translation
- Tone control (formal, casual, business)
- Supports: Turkish, English, German, French, Spanish, Italian, Portuguese, Russian, Arabic, Chinese, Japanese, Korean

## Installation

1. Open your Nanobot AI Dashboard
2. Go to **Settings → Skills → Marketplace**
3. Search for "translator"
4. Click **Install**

Or install via API:
```bash
curl -X POST /api/v1/skills/marketplace/install \
  -H "Content-Type: application/json" \
  -d '{"repo": "kombalarasoftware-cmd/nanobot-skill-translator"}'
```

## Tools
| Tool | Description |
|------|-------------|
| `translate_text` | Translate text between languages |
| `detect_language` | Detect text language |
| `translate_conversation` | Translate conversation with context |
| `get_supported_languages` | List supported languages |

## License
MIT
