# Contributing to ChoralLib i18n

Thank you for your interest in contributing to ChoralLib translations! This document provides guidelines for contributing translations to the project.

## Table of Contents

- [Getting Started](#getting-started)
- [Types of Contributions](#types-of-contributions)
- [File Structure](#file-structure)
- [Translation Guidelines](#translation-guidelines)
- [Pull Request Process](#pull-request-process)
- [Code of Conduct](#code-of-conduct)

## Getting Started

1. Fork this repository
2. Clone your fork locally
3. Create a new branch for your contribution
4. Make your changes
5. Submit a pull request

## Types of Contributions

### 1. Correcting Existing Translations

If you find an error or want to improve an existing translation:

- Open an issue using the **Translation Correction** template, or
- Submit a pull request directly with your fix

### 2. Adding Missing Translations

If you notice untranslated strings in an existing language:

- Check if an issue already exists for the missing translations
- Open an issue using the **Missing Translation** template, or
- Submit a pull request with the translations

### 3. Adding a New Language

If you want to add support for a new language:

1. Open an issue using the **New Language Request** template first
2. Wait for approval from maintainers
3. Copy the base language file (usually `en.json`) as your starting point
4. Translate all strings
5. Submit a pull request

## File Structure

```
i18n/
├── en.json      # English (base language)
├── ja.json      # Japanese
├── de.json      # German
├── fr.json      # French
└── ...          # Other languages
```

Each language file should:
- Use the ISO 639-1 language code as the filename (e.g., `en.json`, `ja.json`, `de.json`)
- Maintain the same key structure as the base English file
- Be valid JSON format

## Translation Guidelines

### General Principles

1. **Accuracy**: Translations should accurately convey the meaning of the original text
2. **Consistency**: Use consistent terminology throughout the translation
3. **Context**: Consider the context in which the text will appear (UI elements, error messages, etc.)
4. **Naturalness**: Translations should sound natural to native speakers

### Technical Requirements

1. **Do not translate**:
   - Translation keys (the left side of JSON key-value pairs)
   - Variable placeholders (e.g., `{{count}}`, `{name}`)
   - HTML tags if present
   - Technical terms that are commonly used in English in the target language

2. **Preserve formatting**:
   - Keep line breaks (`\n`) where they appear
   - Maintain punctuation appropriate for the target language
   - Preserve any special characters or escape sequences

3. **Handle pluralization**:
   - Follow the pluralization rules of the target language
   - Ensure all plural forms are provided where applicable

### Example

```json
{
  "welcome": {
    "title": "Welcome to ChoralLib",
    "message": "You have {{count}} new notifications"
  }
}
```

Translated to Japanese:
```json
{
  "welcome": {
    "title": "ChoralLibへようこそ",
    "message": "{{count}}件の新しい通知があります"
  }
}
```

## Pull Request Process

### Before Submitting

1. **Validate JSON**: Ensure your file is valid JSON (no syntax errors)
2. **Check completeness**: All keys from the base file should be present
3. **Test locally**: If possible, test your translations in the application
4. **Review your changes**: Double-check for typos and grammatical errors

### PR Requirements

1. **Branch naming**: Use descriptive branch names
   - For corrections: `fix/[lang]-[brief-description]` (e.g., `fix/ja-typo-in-welcome`)
   - For new translations: `add/[lang]` (e.g., `add/ko`)
   - For missing strings: `translate/[lang]-[feature]` (e.g., `translate/de-settings-page`)

2. **Commit messages**: Write clear, descriptive commit messages
   - Good: `fix(ja): correct typo in navigation menu`
   - Good: `feat(ko): add Korean translation`
   - Bad: `update translations`

3. **PR description**: Include:
   - What was changed and why
   - Reference to related issues (if any)
   - Any notes for reviewers

### Review Process

1. A maintainer will review your PR
2. You may be asked to make changes or clarifications
3. Once approved, your PR will be merged
4. Your contribution will be acknowledged in the project

## Quality Checklist

Before submitting, please verify:

- [ ] JSON file is valid (use a JSON validator)
- [ ] All keys from the base language file are present
- [ ] No translation keys were modified
- [ ] Variable placeholders are preserved (e.g., `{{variable}}`)
- [ ] No broken escape sequences
- [ ] Translations are appropriate for the context
- [ ] No machine translation without human review

## Code of Conduct

- Be respectful and constructive in all interactions
- Welcome newcomers and help them contribute
- Focus on what is best for the community
- Show empathy towards other community members

## Questions?

If you have any questions about contributing, feel free to:
- Open an issue with the **Question** label
- Contact the maintainers

Thank you for helping make ChoralLib accessible to more users around the world!
