# In-App Purchase Field Rules

## Reference Name
- Maximum 64 characters
- Internal only — users never see this
- Use a clear descriptive name for your own reference
- Format: App Name + Feature/Theme + Type
- Example: Cipher Noir Theme Pack, Ludi Beach Board Unlock

## Product ID
- Maximum 100 characters
- Must be unique across all your apps globally
- Cannot be changed after submission
- Cannot be reused even if deleted
- Use reverse domain format: com.bundleid.productname
- Lowercase only, dots and hyphens allowed
- No spaces, no special characters
- Example: com.dinerdapps.cipher.theme.noir

## Type — Choose One
- Consumable: purchased multiple times (coins, credits)
- Non-Consumable: purchased once, permanent (themes, unlocks)
- Auto-Renewable Subscription: recurring billing
- Non-Renewing Subscription: fixed duration, manual renewal

## Display Name
- Maximum 35 characters
- Users see this in the purchase sheet
- Be clear and descriptive
- No emoji, no special characters
- Should match what the paywall calls it

## Description
- Maximum 55 characters
- Users see this in the purchase sheet
- One clear sentence about what they get
- No emoji, no special characters
- Focus on the benefit not the feature

## Review Notes
- Maximum 4000 characters per IAP product
- Explain what the IAP unlocks
- Describe exactly how to test it in sandbox
- List any conditions needed to trigger the purchase flow
- If multiple IAPs exist, write separate notes for each
- Be specific — vague notes slow down review
