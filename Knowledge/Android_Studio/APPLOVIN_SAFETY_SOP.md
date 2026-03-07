# AppLovin MAX: Anti-Ban & Safety Protocol

## 1. Mandatory Test Device Configuration
To prevent "Invalid Traffic" bans, every project must programmatically register the developer's Advertising ID.

### Java Implementation Snippet:
```java
// To be called in the Application class or BaseActivity before any ads load
private void initializeAppLovin() {
    AppLovinSdk.getInstance(context).setMediationProvider("max");
    AppLovinSdk.initializeSdk(context, configuration -> {
        // Safe to load ads now
    });

    // CRITICAL: Hardcode your GAID here during development
    AppLovinSdk.getInstance(context).getSettings().setTestDeviceAdvertisingIds(
        Arrays.asList("YOUR_GAID_HERE")
    );
}

```

## 2. Safety Check-list

* **Debug Failsafe**: Wrap ad loading logic in `if (!BuildConfig.DEBUG)` checks if live ads are not required during testing.
* **No Self-Clicking**: Never interact with live ads on any device associated with the developer account.
* **Test Ads Verification**: Always confirm the "Test Ad" overlay is visible before interacting with an ad during development.
