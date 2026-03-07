# Unity Publishing: Asset Store & Android Prep

## 1. Asset Store Submission
- **Package Integrity**: Ensure all scripts are under a unique namespace to avoid collisions in customer projects.
- **Dependencies**: Use Package Manager (`manifest.json`) where possible instead of raw `.unitypackage` files for external tools.
- **Testing**: Test the asset in a clean Unity project (Standard, URP, and HDRP) before submission.

## 2. Android Build Optimization
- **IL2CPP**: Always use IL2CPP for release builds to support 64-bit requirements.
- **Stripping Level**: Set "Managed Stripping Level" to "Low" or "Medium" to prevent reflection-based code (like JSON serializers) from breaking.
- **Asset Bundles/Addressables**: For larger games, use Addressables to keep the initial APK/AAB size under the 200MB Play Store limit.

## 3. Play Console Checklist (Unity)
- **AAB Format**: Always export as Android App Bundle (.aab).
- **Target SDK**: Ensure `Player Settings > Other Settings > Target API Level` is set to the latest required (API 34/35+).
- **Privacy Policy**: Link to the Alkiren Studio privacy policy in the first launch "Consent" dialog if using analytics or ads.
