# appstore-details

An agent skill that reads your Apple app project and generates 
complete App Store Connect metadata and In-App Purchase details 
ready to copy and paste.

Built by Chad Smith — Di Nerd Apps LLC

## Commands

### `/appstore-details`
Generates complete App Store Connect metadata:

- App Name (30 chars)
- Subtitle (30 chars)
- Promotional Text (170 chars)
- Description (4000 chars)
- What's New in This Version (4000 chars)
- Keywords (100 chars)
- App Review Notes (4000 chars)

### `/appstore-iap`
Generates In-App Purchase details for every IAP found in the project:

- Reference Name (64 chars)
- Product ID (100 chars)
- Type (Consumable / Non-Consumable / Subscription)
- Display Name (35 chars)
- Description (55 chars)
- Review Notes (4000 chars)

Outputs one block per IAP found in your codebase automatically.

## Installing
```bash
npx skills add https://github.com/DiNerdyYawdie/appstore-details --skill appstore-details
```

## Using

Navigate to your Xcode project folder in Claude Code then run either command:
```
/appstore-details
```
```
/appstore-iap
```

Claude reads your entire project codebase and outputs everything 
ready to paste into App Store Connect. No manual data entry needed.

## Requirements

- Claude Code
- An Xcode project
- CLAUDE.md file in your project root (recommended)

## License

MIT
