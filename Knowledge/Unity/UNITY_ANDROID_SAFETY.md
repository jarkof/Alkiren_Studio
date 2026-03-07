# Unity Android: AppLovin MAX & Safety SOP

## 1. Test Mode Verification
Just like native Android, Unity builds must explicitly register test devices to avoid bans.

### C# Implementation:
```csharp
using UnityEngine;
using System.Collections.Generic;

public class AdsManager : MonoBehaviour
{
    private void Start()
    {
        MaxSdkCallbacks.OnSdkInitializedEvent += (MaxSdkBase.SdkConfiguration sdkConfiguration) => {
            // AppLovin SDK is initialized, start loading ads
        };

        MaxSdk.SetSdkKey("YOUR_SDK_KEY");
        // CRITICAL: Set test device IDs before initialization
        MaxSdk.SetTestDeviceAdvertisingIds(new string[] { "YOUR_GAID_HERE" });
        MaxSdk.InitializeSdk();
    }
}
```

## 2. Platform Specific Safety
* **Build Settings**: Ensure "Development Build" is checked only for internal testing.
* **ProGuard/R8**: Always use the AppLovin provided ProGuard rules in `UserLibraries` to prevent crashing during ad display.
* **Main Thread**: Always ensure ad callbacks are handled on the main thread (Unity's `MaxSdkCallbacks` usually handles this, but verify for custom wrappers).
