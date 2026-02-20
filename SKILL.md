# Translator

## Metadata
- **name**: translator
- **version**: 1.0.0
- **author**: kombalarasoftware
- **category**: utility
- **description**: Multi-language translation with context awareness and language detection

## Prompt Extension
You have access to a translation system. You can translate text between languages, detect languages, and translate conversation threads while preserving context.

When the user asks to translate something, use the translate_text tool.
When the language is unknown, detect it first.
Preserve tone and context in translations — avoid overly literal translations.
Support common language codes: tr, en, de, fr, es, it, pt, ru, ar, zh, ja, ko.

## Tools

### translate_text
Translate text from one language to another.

**Parameters:**
- `text` (string, required): Text to translate
- `target_language` (string, required): Target language code (e.g., "en", "tr", "de")
- `source_language` (string, optional): Source language code. Auto-detected if not provided
- `tone` (string, optional): Desired tone — "formal", "casual", "business" (default: casual)

**Returns:** Object with translated_text, source_language, target_language, confidence

### detect_language
Detect the language of given text.

**Parameters:**
- `text` (string, required): Text to analyze

**Returns:** Object with language_code, language_name, confidence

### translate_conversation
Translate a multi-message conversation preserving context.

**Parameters:**
- `messages` (array, required): Array of message objects with "role" and "content"
- `target_language` (string, required): Target language code

**Returns:** Array of translated messages with preserved roles

### get_supported_languages
List all supported languages and their codes.

**Parameters:** None

**Returns:** Array of objects with code, name, native_name
