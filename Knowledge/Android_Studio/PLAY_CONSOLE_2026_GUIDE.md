# Google Play Console: 2026 Publishing Requirements

## 1. The 14-Day Testing Rule
For new personal developer accounts, Google requires a "Closed Testing" phase:
- **Requirement**: Minimum of 20 testers (recommend 25 to be safe).
- **Duration**: Testers must be opted-in for 14 consecutive days.
- **Action**: Do not plan "Instant Launches." Factor in a 3-week lead time for every app.

## 2. Target API Compliance
- **Annual Requirement**: All updates and new apps must target the latest Android API (currently API 35/36) by August 31st each year.
- **Maintenance**: Perform a "Fleet Update" annually to bump `targetSdk` across all Alkiren Studio apps to prevent removal from the store.

## 3. Data Safety & Privacy
- **Disclosure**: Even if AppLovin is the only 3rd party, you MUST disclose "Device or other IDs" collection in the Data Safety form.
- **Privacy Policy**: Every app requires a hosted Privacy Policy URL. (Recommended: Use a dedicated Alkiren Studio GitHub Pages site).
