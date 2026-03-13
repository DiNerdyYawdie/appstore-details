# appstore-details

An agent skill for Claude Code that reads your Xcode project and generates 
complete App Store Connect metadata and In-App Purchase details 
ready to copy and paste. No manual data entry needed.

Built by Di Nerd Apps LLC

## Commands

### `/appstore-details`
Reads your entire project and generates all App Store Connect metadata.

**Example output for a fitness tracking app:**
```
APP NAME (20/30):
FitTrack – Workout Logger

SUBTITLE (28/30):
Log Workouts. Track Progress.

PROMOTIONAL TEXT (156/170):
Now with custom workout templates. Build your plan once and repeat it 
every week with one tap.

DESCRIPTION (1654/4000):
FitTrack makes it simple to log every workout, track your progress over 
time, and stay consistent with your fitness goals.

Create custom workout plans from hundreds of exercises. Log sets, reps, 
weight, and rest time. View your progress with clear charts showing 
strength gains and volume over weeks and months.

Everything is stored privately on your device. No account required. 
No subscription needed to access your own data.

We use the Apple Standard License Agreement: https://www.apple.com/legal/internet-services/itunes/dev/stdeula/

WHAT'S NEW IN THIS VERSION (98/4000):
Added custom workout templates. Fixed rest timer bug on iPhone SE. 
Improved chart performance for users with large workout history.

KEYWORDS (97/100):
fitness,workout,gym,training,exercise,log,tracker,strength,sets,reps,plan

APP REVIEW NOTES (287/4000):
FitTrack stores all data locally using SwiftData. No login or account 
is required to use the app. The Pro unlock removes the 3 workout plan 
limit and unlocks advanced chart views. To test Pro: tap Upgrade on the 
Plans screen and use sandbox environment to complete the purchase.
```

---

### `/appstore-iap`
Reads your StoreKit configuration and generates IAP details for every 
product found in the project.

**Example output for a fitness app with a pro unlock:**
```
IAP #1
REFERENCE NAME (20/64):
FitTrack Pro Unlock

PRODUCT ID (36/100):
com.example.fittrack.pro.unlock

TYPE:
Non-Consumable

DISPLAY NAME (14/35):
FitTrack Pro

DESCRIPTION (51/55):
Unlock unlimited workout plans and advanced progress charts.

REVIEW NOTES (263/4000):
Unlocks Pro features including unlimited workout plans and advanced 
chart views. Free tier is limited to 3 saved plans. To test: tap 
Upgrade on the Plans screen and complete purchase in sandbox environment. 
All Pro features unlock immediately after successful purchase.

---

IAP #2
REFERENCE NAME (22/64):
Extra Storage Pack 100

PRODUCT ID (38/100):
com.example.fittrack.storage.100

TYPE:
Consumable

DISPLAY NAME (21/35):
100 Export Credits

DESCRIPTION (43/55):
Export up to 100 workouts to CSV or Apple Health.

REVIEW NOTES (198/4000):
Consumable credit pack for exporting workout data. Credits are consumed 
one per export. To test: complete a workout, tap Export on the history 
screen, and complete purchase in sandbox environment.
```

---

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
- CLAUDE.md file in your project root (recommended for best results)

## License

MIT
