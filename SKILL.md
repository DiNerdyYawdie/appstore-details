---
name: appstore-details
description: Reads the project codebase and generates complete App Store Connect metadata including name, subtitle, promotional text, description, keywords, what's new, and app review notes. Use when preparing an app for App Store submission.
license: MIT
metadata:
  author: Di Nerd Apps LLC
  version: "1.0"
---

Generate complete App Store Connect metadata by reading the project codebase.

## Process
1. Read CLAUDE.md for app name, platform, and feature overview
2. Read all Swift files to understand features, screens, and functionality
3. Read StoreService.swift or similar for IAP and subscription details
4. Read Models.swift for data structures and feature scope
5. Apply all rules from references/metadata.md
6. Apply keyword strategy from references/keywords.md
7. Apply copywriting rules from references/copywriting.md
8. Apply rejection rules from references/rejection.md
9. Output all fields formatted and ready to paste into App Store Connect

## Output Format
Output every field clearly labeled with current character count vs maximum.
Never exceed character limits.
Never use emojis in any field.
Always include the EULA line in description.
Always write in plain English, no markdown formatting in output fields.

Output in this exact format:

---
APP NAME (X/30):
[name here]

SUBTITLE (X/30):
[subtitle here]

PROMOTIONAL TEXT (X/170):
[promotional text here]

DESCRIPTION (X/4000):
[description here]

WHAT'S NEW IN THIS VERSION (X/4000):
[what's new here]

KEYWORDS (X/100):
[keywords here]

APP REVIEW NOTES (X/4000):
[review notes here]
---

## Core Rules
- Never use emojis anywhere
- Never exceed character limits — staying under is fine
- Use only the best details, not filler to hit the max
- Always end description with: We use the Apple Standard License Agreement: https://www.apple.com/legal/internet-services/itunes/dev/stdeula/
- Write in plain, clear English
- No markdown formatting inside output fields
- No bullet points using - or * inside output fields, use plain text paragraphs instead
- App Review Notes should reflect the latest code changes found in the project
