# appstore-details

An agent skill that reads your Apple app project and generates 
complete App Store Connect metadata ready to copy and paste.

Built by Chad Smith — Di Nerd Apps LLC

## What It Does

Reads your entire Xcode project codebase and generates:

- App Name (30 chars)
- Subtitle (30 chars)
- Promotional Text (170 chars)
- Description (4000 chars)
- What's New in This Version (4000 chars)
- Keywords (100 chars)
- App Review Notes (4000 chars)

All fields follow Apple's guidelines, avoid rejection triggers,
and are optimized for search and conversion.

## Installing
```bash
npx skills add https://github.com/YOUR_USERNAME/appstore-details --skill appstore-details
```

## Using

Inside your Xcode project folder in Claude Code:
```
/appstore-details
```

That's it. Claude reads your project and outputs everything 
ready to paste into App Store Connect.

## Requirements

- Claude Code
- An Xcode project with a CLAUDE.md file (recommended)

## License

MIT
