Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PowerManager

```
class PowerManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.PowerManager](PowerManager.md) |

This class lets you query and request control of aspects of the device's power state.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/os/PowerManager.OnThermalHeadroomChangedListener` Listener passed to android. |
| abstract | `https://developer.android.com/reference/kotlin/android/os/PowerManager.OnThermalStatusChangedListener` Listener passed to android. |
| | `https://developer.android.com/reference/kotlin/android/os/PowerManager.WakeLock` A wake lock is a mechanism to indicate that your application needs to have the device stay on. |
| --- | --- |
| abstract | `https://developer.android.com/reference/kotlin/android/os/PowerManager.WakeLockStateListener` A listener interface to get notified when the wakelock is enabled/disabled. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#ACQUIRE_CAUSES_WAKEUP:kotlin.Int` Wake lock flag: Turn the screen on when the wake lock is acquired. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#ACTION_DEVICE_IDLE_MODE_CHANGED:kotlin.String` Intent that is broadcast when the state of `https://developer.android.com/reference/kotlin/android/os/PowerManager#isDeviceIdleMode()` changes. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#ACTION_DEVICE_LIGHT_IDLE_MODE_CHANGED:kotlin.String` Intent that is broadcast when the state of `https://developer.android.com/reference/kotlin/android/os/PowerManager#isDeviceLightIdleMode()` changes. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#ACTION_LOW_POWER_STANDBY_ENABLED_CHANGED:kotlin.String` Intent that is broadcast when Low Power Standby is enabled or disabled. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#ACTION_LOW_POWER_STANDBY_POLICY_CHANGED:kotlin.String` Intent that is broadcast when Low Power Standby policy is changed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#ACTION_POWER_SAVE_MODE_CHANGED:kotlin.String` Intent that is broadcast when the state of `https://developer.android.com/reference/kotlin/android/os/PowerManager#isPowerSaveMode()` changes. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#FEATURE_WAKE_ON_LAN_IN_LOW_POWER_STANDBY:kotlin.String` Signals that wake-on-lan/wake-on-wlan is allowed in Low Power Standby. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#FULL_WAKE_LOCK:kotlin.Int` Wake lock level: Ensures that the screen and keyboard backlight are on at full brightness. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#LOCATION_MODE_ALL_DISABLED_WHEN_SCREEN_OFF:kotlin.Int` All location providers should be disabled when battery saver is on and the device is non-interactive. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#LOCATION_MODE_FOREGROUND_ONLY:kotlin.Int` In this mode, all the location providers will be kept available, but location fixes should only be provided to foreground apps. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#LOCATION_MODE_GPS_DISABLED_WHEN_SCREEN_OFF:kotlin.Int` In this mode, the GPS based location provider should be disabled when battery saver is on and the device is non-interactive. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#LOCATION_MODE_NO_CHANGE:kotlin.Int` Either the location providers shouldn't be affected by battery saver, or battery saver is off. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#LOCATION_MODE_THROTTLE_REQUESTS_WHEN_SCREEN_OFF:kotlin.Int` In this mode, location will not be turned off, but LocationManager will throttle all requests to providers when the device is non-interactive. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#LOW_POWER_STANDBY_ALLOWED_REASON_ONGOING_CALL:kotlin.Int` Exempts apps with ongoing calls. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#LOW_POWER_STANDBY_ALLOWED_REASON_TEMP_POWER_SAVE_ALLOWLIST:kotlin.Int` Exempts apps on the temporary powersave allowlist. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#LOW_POWER_STANDBY_ALLOWED_REASON_VOICE_INTERACTION:kotlin.Int` Exempts active Voice Interaction Sessions in Low Power Standby. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#ON_AFTER_RELEASE:kotlin.Int` Wake lock flag: When this wake lock is released, poke the user activity timer so the screen stays on for a little longer. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#PARTIAL_WAKE_LOCK:kotlin.Int` Wake lock level: Ensures that the CPU is running; the screen and keyboard backlight will be allowed to go off. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#PROXIMITY_SCREEN_OFF_WAKE_LOCK:kotlin.Int` Wake lock level: Turns the screen off when the proximity sensor activates. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#RELEASE_FLAG_WAIT_FOR_NO_PROXIMITY:kotlin.Int` Flag for android. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#SCREEN_BRIGHT_WAKE_LOCK:kotlin.Int` Wake lock level: Ensures that the screen is on at full brightness; the keyboard backlight will be allowed to go off. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#SCREEN_DIM_WAKE_LOCK:kotlin.Int` Wake lock level: Ensures that the screen is on (but may be dimmed); the keyboard backlight will be allowed to go off. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#THERMAL_STATUS_CRITICAL:kotlin.Int` Thermal status code: Platform has done everything to reduce power. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#THERMAL_STATUS_EMERGENCY:kotlin.Int` Thermal status code: Key components in platform are shutting down due to thermal condition. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#THERMAL_STATUS_LIGHT:kotlin.Int` Thermal status code: Light throttling where UX is not impacted. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#THERMAL_STATUS_MODERATE:kotlin.Int` Thermal status code: Moderate throttling where UX is not largely impacted. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#THERMAL_STATUS_NONE:kotlin.Int` Thermal status code: Not under throttling. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#THERMAL_STATUS_SEVERE:kotlin.Int` Thermal status code: Severe throttling where UX is largely impacted. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#THERMAL_STATUS_SHUTDOWN:kotlin.Int` Thermal status code: Need shutdown immediately. |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#addThermalHeadroomListener(android.os.PowerManager.OnThermalHeadroomChangedListener)(listener: https://developer.android.com/reference/kotlin/android/os/PowerManager.OnThermalHeadroomChangedListener)` This function adds a listener for thermal headroom change, listener callback will be enqueued tasks on the main thread |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#addThermalHeadroomListener(java.util.concurrent.Executor,%20android.os.PowerManager.OnThermalHeadroomChangedListener)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, listener: https://developer.android.com/reference/kotlin/android/os/PowerManager.OnThermalHeadroomChangedListener)` This function adds a listener for thermal headroom change. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#addThermalStatusListener(android.os.PowerManager.OnThermalStatusChangedListener)(listener: https://developer.android.com/reference/kotlin/android/os/PowerManager.OnThermalStatusChangedListener)` This function adds a listener for thermal status change, listener callback will be enqueued tasks on the main thread |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#addThermalStatusListener(java.util.concurrent.Executor,%20android.os.PowerManager.OnThermalStatusChangedListener)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, listener: https://developer.android.com/reference/kotlin/android/os/PowerManager.OnThermalStatusChangedListener)` This function adds a listener for thermal status change. |
| [Duration](../java.time/Duration.md)? | `https://developer.android.com/reference/kotlin/android/os/PowerManager#getBatteryDischargePrediction()()` Returns the current battery life remaining estimate. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#getCurrentThermalStatus()()` This function returns the current thermal status of the device. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#getLocationPowerSaveMode()()` Returns how location features should behave when battery saver is on. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#getThermalHeadroom(kotlin.Int)(forecastSeconds: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Provides an estimate of how much thermal headroom the device currently has before hitting severe throttling. |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!, [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!\> | `https://developer.android.com/reference/kotlin/android/os/PowerManager#getThermalHeadroomThresholds()()` Gets the thermal headroom thresholds for all available thermal throttling status above `https://developer.android.com/reference/kotlin/android/os/PowerManager#THERMAL_STATUS_NONE:kotlin.Int`. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#isAllowedInLowPowerStandby(kotlin.Int)(reason: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns true if Low Power Standby is disabled (so Low Power Standby does not restrict apps), or apps may be automatically exempt from Low Power Standby restrictions for the given reason. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#isAllowedInLowPowerStandby(kotlin.String)(feature: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns true if Low Power Standby is disabled (so Low Power Standby does not restrict apps), or apps are allowed to use a given feature during Low Power Standby. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#isBatteryDischargePredictionPersonalized()()` Returns whether the current battery life remaining estimate is personalized based on device usage history or not. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#isDeviceIdleMode()()` Returns true if the device is currently in idle mode. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#isDeviceLightIdleMode()()` Returns true if the device is currently in light idle mode. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#isExemptFromLowPowerStandby()()` Returns true if the calling package is exempt from Low Power Standby restrictions or Low Power Standby is disabled (so Low Power Standby does not restrict apps), false otherwise. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#isIgnoringBatteryOptimizations(kotlin.String)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Return whether the given application package name is on the device's power allowlist. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#isInteractive()()` Returns true if the device is in an interactive state. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#isLowPowerStandbyEnabled()()` Returns true if Low Power Standby is enabled. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#isPowerSaveMode()()` Returns true if the device is currently in power save mode. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#isRebootingUserspaceSupported()()` Returns `true` if this device supports rebooting userspace. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#isScreenOn()()` Returns true if the device is in an interactive state. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#isSustainedPerformanceModeSupported()()` This function checks if the device has implemented Sustained Performance Mode. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#isWakeLockLevelSupported(kotlin.Int)(level: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns true if the specified wake lock level is supported. |
| [PowerManager.WakeLock](../android/os/PowerManager.WakeLock.md)! | `https://developer.android.com/reference/kotlin/android/os/PowerManager#newWakeLock(kotlin.Int,%20kotlin.String)(levelAndFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, tag: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Creates a new wake lock with the specified level and flags. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#reboot(kotlin.String)(reason: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Reboot the device. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#removeThermalHeadroomListener(android.os.PowerManager.OnThermalHeadroomChangedListener)(listener: https://developer.android.com/reference/kotlin/android/os/PowerManager.OnThermalHeadroomChangedListener)` This function removes a listener for Thermal headroom change |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager#removeThermalStatusListener(android.os.PowerManager.OnThermalStatusChangedListener)(listener: https://developer.android.com/reference/kotlin/android/os/PowerManager.OnThermalStatusChangedListener)` This function removes a listener for thermal status change |
| --- | --- |

## Constants

### ACQUIRE_CAUSES_WAKEUP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACQUIRE_CAUSES_WAKEUP: Int
```

**Deprecated:** *Most applications should use `https://developer.android.com/reference/kotlin/android/R.attr.html#turnScreenOn:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/app/Activity.html#setTurnScreenOn(kotlin.Boolean)` instead, as this prevents the previous foreground app from being resumed first when the screen turns on.*

Wake lock flag: Turn the screen on when the wake lock is acquired.

This flag will require `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#TURN_SCREEN_ON:kotlin.String` in future releases.

Normally wake locks don't actually wake the device, they just cause the screen to remain on once it's already on. This flag will cause the device to wake up when the wake lock is acquired.

Android TV playback devices attempt to turn on the HDMI-connected TV via HDMI-CEC on any wake-up, including wake-ups triggered by wake locks.

Cannot be used with `https://developer.android.com/reference/kotlin/android/os/PowerManager#PARTIAL_WAKE_LOCK:kotlin.Int`.

 Value: 268435456

### ACTION_DEVICE_IDLE_MODE_CHANGED

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_DEVICE_IDLE_MODE_CHANGED: String
```

Intent that is broadcast when the state of `https://developer.android.com/reference/kotlin/android/os/PowerManager#isDeviceIdleMode()` changes. This broadcast is only sent to registered receivers.

 Value: "android.os.action.DEVICE_IDLE_MODE_CHANGED"

### ACTION_DEVICE_LIGHT_IDLE_MODE_CHANGED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_DEVICE_LIGHT_IDLE_MODE_CHANGED: String
```

Intent that is broadcast when the state of `https://developer.android.com/reference/kotlin/android/os/PowerManager#isDeviceLightIdleMode()` changes. This broadcast is only sent to registered receivers.

 Value: "android.os.action.LIGHT_DEVICE_IDLE_MODE_CHANGED"

### ACTION_LOW_POWER_STANDBY_ENABLED_CHANGED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_LOW_POWER_STANDBY_ENABLED_CHANGED: String
```

Intent that is broadcast when Low Power Standby is enabled or disabled. This broadcast is only sent to registered receivers and receivers holding `android.permission.MANAGE_LOW_POWER_STANDBY`.

 Value: "android.os.action.LOW_POWER_STANDBY_ENABLED_CHANGED"

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/PowerManager#isLowPowerStandbyEnabled()`

### ACTION_LOW_POWER_STANDBY_POLICY_CHANGED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_LOW_POWER_STANDBY_POLICY_CHANGED: String
```

Intent that is broadcast when Low Power Standby policy is changed. This broadcast is only sent to registered receivers and receivers holding `android.permission.MANAGE_LOW_POWER_STANDBY`.

 Value: "android.os.action.LOW_POWER_STANDBY_POLICY_CHANGED"

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/PowerManager#isExemptFromLowPowerStandby()`
- `https://developer.android.com/reference/kotlin/android/os/PowerManager#isAllowedInLowPowerStandby(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/os/PowerManager#isAllowedInLowPowerStandby(kotlin.String)`

### ACTION_POWER_SAVE_MODE_CHANGED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_POWER_SAVE_MODE_CHANGED: String
```

Intent that is broadcast when the state of `https://developer.android.com/reference/kotlin/android/os/PowerManager#isPowerSaveMode()` changes. This broadcast is only sent to registered receivers.

 Value: "android.os.action.POWER_SAVE_MODE_CHANGED"

### FEATURE_WAKE_ON_LAN_IN_LOW_POWER_STANDBY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_WAKE_ON_LAN_IN_LOW_POWER_STANDBY: String
```

Signals that wake-on-lan/wake-on-wlan is allowed in Low Power Standby.

If Low Power Standby is enabled (`https://developer.android.com/reference/kotlin/android/os/PowerManager#isLowPowerStandbyEnabled()`), wake-on-lan/wake-on-wlan may not be available while in standby. Use `https://developer.android.com/reference/kotlin/android/os/PowerManager#isAllowedInLowPowerStandby(kotlin.String)` to determine whether the device allows this feature to be used during Low Power Standby with the currently active Low Power Standby policy.

 Value: "com.android.lowpowerstandby.WAKE_ON_LAN"

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/PowerManager#isAllowedInLowPowerStandby(kotlin.String)`

### FULL_WAKE_LOCK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FULL_WAKE_LOCK: Int
```

**Deprecated:** *Most applications should use `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#FLAG_KEEP_SCREEN_ON:kotlin.Int` instead of this type of wake lock, as it will be correctly managed by the platform as the user moves between applications and doesn't require a special permission.*

Wake lock level: Ensures that the screen and keyboard backlight are on at full brightness.

If the user presses the power button, then the `https://developer.android.com/reference/kotlin/android/os/PowerManager#FULL_WAKE_LOCK:kotlin.Int` will be implicitly released by the system, causing both the screen and the CPU to be turned off. Contrast with `https://developer.android.com/reference/kotlin/android/os/PowerManager#PARTIAL_WAKE_LOCK:kotlin.Int`.

 Value: 26

### LOCATION_MODE_ALL_DISABLED_WHEN_SCREEN_OFF

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LOCATION_MODE_ALL_DISABLED_WHEN_SCREEN_OFF: Int
```

All location providers should be disabled when battery saver is on and the device is non-interactive.

 Value: 2

### LOCATION_MODE_FOREGROUND_ONLY

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LOCATION_MODE_FOREGROUND_ONLY: Int
```

In this mode, all the location providers will be kept available, but location fixes should only be provided to foreground apps.

 Value: 3

### LOCATION_MODE_GPS_DISABLED_WHEN_SCREEN_OFF

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LOCATION_MODE_GPS_DISABLED_WHEN_SCREEN_OFF: Int
```

In this mode, the GPS based location provider should be disabled when battery saver is on and the device is non-interactive.

 Value: 1

### LOCATION_MODE_NO_CHANGE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LOCATION_MODE_NO_CHANGE: Int
```

Either the location providers shouldn't be affected by battery saver, or battery saver is off.

 Value: 0

### LOCATION_MODE_THROTTLE_REQUESTS_WHEN_SCREEN_OFF

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LOCATION_MODE_THROTTLE_REQUESTS_WHEN_SCREEN_OFF: Int
```

In this mode, location will not be turned off, but LocationManager will throttle all requests to providers when the device is non-interactive.

 Value: 4

### LOW_POWER_STANDBY_ALLOWED_REASON_ONGOING_CALL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LOW_POWER_STANDBY_ALLOWED_REASON_ONGOING_CALL: Int
```

Exempts apps with ongoing calls.

This includes apps with foreground services of type "phoneCall".

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/PowerManager#isAllowedInLowPowerStandby(kotlin.Int)`

### LOW_POWER_STANDBY_ALLOWED_REASON_TEMP_POWER_SAVE_ALLOWLIST

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LOW_POWER_STANDBY_ALLOWED_REASON_TEMP_POWER_SAVE_ALLOWLIST: Int
```

Exempts apps on the temporary powersave allowlist.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/PowerManager#isAllowedInLowPowerStandby(kotlin.Int)`

### LOW_POWER_STANDBY_ALLOWED_REASON_VOICE_INTERACTION

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LOW_POWER_STANDBY_ALLOWED_REASON_VOICE_INTERACTION: Int
```

Exempts active Voice Interaction Sessions in Low Power Standby.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/PowerManager#isAllowedInLowPowerStandby(kotlin.Int)`

### ON_AFTER_RELEASE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ON_AFTER_RELEASE: Int
```

Wake lock flag: When this wake lock is released, poke the user activity timer so the screen stays on for a little longer.

This will not turn the screen on if it is not already on.

Cannot be used with `https://developer.android.com/reference/kotlin/android/os/PowerManager#PARTIAL_WAKE_LOCK:kotlin.Int`.

 Value: 536870912

### PARTIAL_WAKE_LOCK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARTIAL_WAKE_LOCK: Int
```

Wake lock level: Ensures that the CPU is running; the screen and keyboard backlight will be allowed to go off.

If the user presses the power button, then the screen will be turned off but the CPU will be kept on until all partial wake locks have been released.

 Value: 1

### PROXIMITY_SCREEN_OFF_WAKE_LOCK

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROXIMITY_SCREEN_OFF_WAKE_LOCK: Int
```

Wake lock level: Turns the screen off when the proximity sensor activates.

If the proximity sensor detects that an object is nearby, the screen turns off immediately. Shortly after the object moves away, the screen turns on again.

A proximity wake lock does not prevent the device from falling asleep unlike `https://developer.android.com/reference/kotlin/android/os/PowerManager#FULL_WAKE_LOCK:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/os/PowerManager#SCREEN_BRIGHT_WAKE_LOCK:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/os/PowerManager#SCREEN_DIM_WAKE_LOCK:kotlin.Int`. If there is no user activity and no other wake locks are held, then the device will fall asleep (and lock) as usual. However, the device will not fall asleep while the screen has been turned off by the proximity sensor because it effectively counts as ongoing user activity.

Since not all devices have proximity sensors, use `https://developer.android.com/reference/kotlin/android/os/PowerManager#isWakeLockLevelSupported(kotlin.Int)` to determine whether this wake lock level is supported.

Cannot be used with `https://developer.android.com/reference/kotlin/android/os/PowerManager#ACQUIRE_CAUSES_WAKEUP:kotlin.Int`.

 Value: 32

### RELEASE_FLAG_WAIT_FOR_NO_PROXIMITY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RELEASE_FLAG_WAIT_FOR_NO_PROXIMITY: Int
```

Flag for android.os.PowerManager.WakeLock#release: Defer releasing a `https://developer.android.com/reference/kotlin/android/os/PowerManager#PROXIMITY_SCREEN_OFF_WAKE_LOCK:kotlin.Int` wake lock until the proximity sensor indicates that an object is not in close proximity.

 Value: 1

### SCREEN_BRIGHT_WAKE_LOCK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCREEN_BRIGHT_WAKE_LOCK: Int
```

**Deprecated:** *Most applications should use `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#FLAG_KEEP_SCREEN_ON:kotlin.Int` instead of this type of wake lock, as it will be correctly managed by the platform as the user moves between applications and doesn't require a special permission.*

Wake lock level: Ensures that the screen is on at full brightness; the keyboard backlight will be allowed to go off.

If the user presses the power button, then the `https://developer.android.com/reference/kotlin/android/os/PowerManager#SCREEN_BRIGHT_WAKE_LOCK:kotlin.Int` will be implicitly released by the system, causing both the screen and the CPU to be turned off. Contrast with `https://developer.android.com/reference/kotlin/android/os/PowerManager#PARTIAL_WAKE_LOCK:kotlin.Int`.

 Value: 10

### SCREEN_DIM_WAKE_LOCK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCREEN_DIM_WAKE_LOCK: Int
```

**Deprecated:** *Most applications should use `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#FLAG_KEEP_SCREEN_ON:kotlin.Int` instead of this type of wake lock, as it will be correctly managed by the platform as the user moves between applications and doesn't require a special permission.*

Wake lock level: Ensures that the screen is on (but may be dimmed); the keyboard backlight will be allowed to go off.

If the user presses the power button, then the `https://developer.android.com/reference/kotlin/android/os/PowerManager#SCREEN_DIM_WAKE_LOCK:kotlin.Int` will be implicitly released by the system, causing both the screen and the CPU to be turned off. Contrast with `https://developer.android.com/reference/kotlin/android/os/PowerManager#PARTIAL_WAKE_LOCK:kotlin.Int`.

 Value: 6

### THERMAL_STATUS_CRITICAL

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val THERMAL_STATUS_CRITICAL: Int
```

Thermal status code: Platform has done everything to reduce power.

 Value: 4

### THERMAL_STATUS_EMERGENCY

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val THERMAL_STATUS_EMERGENCY: Int
```

Thermal status code: Key components in platform are shutting down due to thermal condition. Device functionalities will be limited.

 Value: 5

### THERMAL_STATUS_LIGHT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val THERMAL_STATUS_LIGHT: Int
```

Thermal status code: Light throttling where UX is not impacted.

 Value: 1

### THERMAL_STATUS_MODERATE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val THERMAL_STATUS_MODERATE: Int
```

Thermal status code: Moderate throttling where UX is not largely impacted.

 Value: 2

### THERMAL_STATUS_NONE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val THERMAL_STATUS_NONE: Int
```

Thermal status code: Not under throttling.

 Value: 0

### THERMAL_STATUS_SEVERE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val THERMAL_STATUS_SEVERE: Int
```

Thermal status code: Severe throttling where UX is largely impacted.

 Value: 3

### THERMAL_STATUS_SHUTDOWN

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val THERMAL_STATUS_SHUTDOWN: Int
```

Thermal status code: Need shutdown immediately.

 Value: 6

## Public methods

### addThermalHeadroomListener

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addThermalHeadroomListener(listener: PowerManager.OnThermalHeadroomChangedListener): Unit
```

This function adds a listener for thermal headroom change, listener callback will be enqueued tasks on the main thread

| Parameters ||
|---|---|
| `listener` | [PowerManager.OnThermalHeadroomChangedListener](../android/os/PowerManager.OnThermalHeadroomChangedListener.md): listener to be added,. This value cannot be `null`. |

### addThermalHeadroomListener

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addThermalHeadroomListener(
    executor: Executor, 
    listener: PowerManager.OnThermalHeadroomChangedListener
): Unit
```

This function adds a listener for thermal headroom change.

| Parameters ||
|---|---|
| `executor` | [Executor](../java.util.concurrent/Executor.md): `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` to handle listener callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `listener` | [PowerManager.OnThermalHeadroomChangedListener](../android/os/PowerManager.OnThermalHeadroomChangedListener.md): listener to be added. This value cannot be `null`. |

### addThermalStatusListener

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addThermalStatusListener(listener: PowerManager.OnThermalStatusChangedListener): Unit
```

This function adds a listener for thermal status change, listener callback will be enqueued tasks on the main thread

| Parameters ||
|---|---|
| `listener` | [PowerManager.OnThermalStatusChangedListener](../android/os/PowerManager.OnThermalStatusChangedListener.md): listener to be added,. This value cannot be `null`. |

### addThermalStatusListener

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addThermalStatusListener(
    executor: Executor, 
    listener: PowerManager.OnThermalStatusChangedListener
): Unit
```

This function adds a listener for thermal status change.

| Parameters ||
|---|---|
| `executor` | [Executor](../java.util.concurrent/Executor.md): `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` to handle listener callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `listener` | [PowerManager.OnThermalStatusChangedListener](../android/os/PowerManager.OnThermalStatusChangedListener.md): listener to be added. This value cannot be `null`. |

### getBatteryDischargePrediction

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getBatteryDischargePrediction(): Duration?
```

Returns the current battery life remaining estimate.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Duration.html#?` | The estimated battery life remaining as a `https://developer.android.com/reference/kotlin/java/time/Duration.html#`. Will be `null` if the device is powered, charging, or an error was encountered. |

### getCurrentThermalStatus

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCurrentThermalStatus(): Int
```

This function returns the current thermal status of the device.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | thermal status as int, `https://developer.android.com/reference/kotlin/android/os/PowerManager#THERMAL_STATUS_NONE:kotlin.Int` if device in not under thermal throttling. |

### getLocationPowerSaveMode

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLocationPowerSaveMode(): Int
```

Returns how location features should behave when battery saver is on. When battery saver is off, this will always return `https://developer.android.com/reference/kotlin/android/os/PowerManager#LOCATION_MODE_NO_CHANGE:kotlin.Int`.

This API is normally only useful for components that provide location features.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/os/PowerManager#LOCATION_MODE_NO_CHANGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/PowerManager#LOCATION_MODE_GPS_DISABLED_WHEN_SCREEN_OFF:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/PowerManager#LOCATION_MODE_ALL_DISABLED_WHEN_SCREEN_OFF:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/PowerManager#LOCATION_MODE_FOREGROUND_ONLY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/PowerManager#LOCATION_MODE_THROTTLE_REQUESTS_WHEN_SCREEN_OFF:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/PowerManager#isPowerSaveMode()`
- `https://developer.android.com/reference/kotlin/android/os/PowerManager#ACTION_POWER_SAVE_MODE_CHANGED:kotlin.String`

### getThermalHeadroom

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getThermalHeadroom(forecastSeconds: Int): Float
```

Provides an estimate of how much thermal headroom the device currently has before hitting severe throttling. Note that this only attempts to track the headroom of slow-moving sensors, such as the skin temperature sensor. This means that there is no benefit to calling this function more frequently than about once per second, and attempts to call significantly more frequently may result in the function returning `NaN`.

In addition, in order to be able to provide an accurate forecast, the system does not attempt to forecast until it has multiple temperature samples from which to extrapolate. This should only take a few seconds from the time of the first call, but during this time, no forecasting will occur, and the current headroom will be returned regardless of the value of `forecastSeconds`.

The value returned is a non-negative float that represents how much of the thermal envelope is in use (or is forecasted to be in use). A value of 1.0 indicates that the device is (or will be) throttled at `https://developer.android.com/reference/kotlin/android/os/PowerManager#THERMAL_STATUS_SEVERE:kotlin.Int`. Such throttling can affect the CPU, GPU, and other subsystems. Values may exceed 1.0, but there is no implied mapping to specific thermal status levels beyond that point. This means that values greater than 1.0 may correspond to `https://developer.android.com/reference/kotlin/android/os/PowerManager#THERMAL_STATUS_SEVERE:kotlin.Int`, but may also represent heavier throttling.

A value of 0.0 corresponds to a fixed distance from 1.0, but does not correspond to any particular thermal status or temperature. Values on (0.0, 1.0\] may be expected to scale linearly with temperature, though temperature changes over time are typically not linear. Negative values will be clamped to 0.0 before returning.

| Parameters ||
|---|---|
| `forecastSeconds` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): how many seconds in the future to forecast. Given that device conditions may change at any time, forecasts from further in the future will likely be less accurate than forecasts in the near future. Value is between 0 and 60 inclusive |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | a value greater than or equal to 0.0 where 1.0 indicates the SEVERE throttling threshold, as described above. Returns NaN if the device does not support this functionality. Value is 0.0f or greater |

### getThermalHeadroomThresholds

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getThermalHeadroomThresholds(): MutableMap<Int!, Float!>
```

Gets the thermal headroom thresholds for all available thermal throttling status above `https://developer.android.com/reference/kotlin/android/os/PowerManager#THERMAL_STATUS_NONE:kotlin.Int`.

A thermal status key in the returned map is only set if the device manufacturer has the corresponding threshold defined for at least one of its sensors. If it's set, one should expect to see that from `https://developer.android.com/reference/kotlin/android/os/PowerManager#getCurrentThermalStatus()` or `https://developer.android.com/reference/kotlin/android/os/PowerManager.OnThermalStatusChangedListener#onThermalStatusChanged(kotlin.Int)`.

The headroom threshold is used to interpret the possible thermal throttling status based on the headroom prediction. For example, if the headroom threshold for `https://developer.android.com/reference/kotlin/android/os/PowerManager#THERMAL_STATUS_LIGHT:kotlin.Int` is 0.7, and a headroom prediction in 10s returns 0.75 (or `getThermalHeadroom(10)=0.75`), one can expect that in 10 seconds the system could be in lightly throttled state if the workload remains the same. The app can consider taking actions according to the nearest throttling status the difference between the headroom and the threshold.

For new devices it's guaranteed to have a single sensor, but for older devices with multiple sensors reporting different threshold values, the minimum threshold is taken to be conservative on predictions. Thus, when reading real-time headroom, it's not guaranteed that a real-time value of 0.75 (or `getThermalHeadroom(0)`=0.75) exceeding the threshold of 0.7 above will always come with lightly throttled state (or `getCurrentThermalStatus()=THERMAL_STATUS_LIGHT`) but it can be lower (or `getCurrentThermalStatus()=THERMAL_STATUS_NONE`). While it's always guaranteed that the device won't be throttled heavier than the unmet threshold's state, so a real-time headroom of 0.75 will never come with `https://developer.android.com/reference/kotlin/android/os/PowerManager#THERMAL_STATUS_MODERATE:kotlin.Int` but lower, and 0.65 will never come with `https://developer.android.com/reference/kotlin/android/os/PowerManager#THERMAL_STATUS_LIGHT:kotlin.Int` but `https://developer.android.com/reference/kotlin/android/os/PowerManager#THERMAL_STATUS_NONE:kotlin.Int`.

Starting at `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES#BAKLAVA:kotlin.Int` the returned map of thresholds can change between calls to this function, one could use the new `https://developer.android.com/reference/kotlin/android/os/PowerManager#addThermalHeadroomListener(java.util.concurrent.Executor,%20android.os.PowerManager.OnThermalHeadroomChangedListener)` API to register a listener and get callback for changes to thresholds.

<br />

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html!>` | map from each thermal status to its thermal headroom. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the thermal service is not ready |
| `java.lang.UnsupportedOperationException` | if the feature is not enabled |

### isAllowedInLowPowerStandby

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isAllowedInLowPowerStandby(reason: Int): Boolean
```

Returns true if Low Power Standby is disabled (so Low Power Standby does not restrict apps), or apps may be automatically exempt from Low Power Standby restrictions for the given reason. The system may exempt apps from Low Power Standby restrictions when using allowed features. For example, if `https://developer.android.com/reference/kotlin/android/os/PowerManager#LOW_POWER_STANDBY_ALLOWED_REASON_VOICE_INTERACTION:kotlin.Int` is allowed, then apps with active voice interaction sessions are exempt from restrictions.

| Parameters ||
|---|---|
| `reason` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/PowerManager#LOW_POWER_STANDBY_ALLOWED_REASON_VOICE_INTERACTION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/PowerManager#LOW_POWER_STANDBY_ALLOWED_REASON_TEMP_POWER_SAVE_ALLOWLIST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/PowerManager#LOW_POWER_STANDBY_ALLOWED_REASON_ONGOING_CALL:kotlin.Int` |

### isAllowedInLowPowerStandby

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isAllowedInLowPowerStandby(feature: String): Boolean
```

Returns true if Low Power Standby is disabled (so Low Power Standby does not restrict apps), or apps are allowed to use a given feature during Low Power Standby.

| Parameters ||
|---|---|
| `feature` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

### isBatteryDischargePredictionPersonalized

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isBatteryDischargePredictionPersonalized(): Boolean
```

Returns whether the current battery life remaining estimate is personalized based on device usage history or not. This value does not take a device's powered or charging state into account.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | A boolean indicating if the current discharge estimate is personalized based on historical device usage or not. |

### isDeviceIdleMode

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isDeviceIdleMode(): Boolean
```

Returns true if the device is currently in idle mode. This happens when a device has been sitting unused and unmoving for a sufficiently long period of time, so that it decides to go into a lower power-use state. This may involve things like turning off network access to apps. You can monitor for changes to this state with `https://developer.android.com/reference/kotlin/android/os/PowerManager#ACTION_DEVICE_IDLE_MODE_CHANGED:kotlin.String`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if currently in active device idle mode, else false. This is when idle mode restrictions are being actively applied; it will return false if the device is in a long-term idle mode but currently running a maintenance window where restrictions have been lifted. |

### isDeviceLightIdleMode

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isDeviceLightIdleMode(): Boolean
```

Returns true if the device is currently in light idle mode. This happens when a device has had its screen off for a short time, switching it into a batching mode where we execute jobs, syncs, networking on a batching schedule. You can monitor for changes to this state with `https://developer.android.com/reference/kotlin/android/os/PowerManager#ACTION_DEVICE_LIGHT_IDLE_MODE_CHANGED:kotlin.String`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if currently in active device light idle mode, else false. This is when light idle mode restrictions are being actively applied; it will return false if the device is in a long-term idle mode but currently running a maintenance window where restrictions have been lifted. |

### isExemptFromLowPowerStandby

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isExemptFromLowPowerStandby(): Boolean
```

Returns true if the calling package is exempt from Low Power Standby restrictions or Low Power Standby is disabled (so Low Power Standby does not restrict apps), false otherwise.

### isIgnoringBatteryOptimizations

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isIgnoringBatteryOptimizations(packageName: String!): Boolean
```

Return whether the given application package name is on the device's power allowlist. Apps can be placed on the allowlist through the settings UI invoked by `https://developer.android.com/reference/kotlin/android/provider/Settings.html#ACTION_IGNORE_BATTERY_OPTIMIZATION_SETTINGS:kotlin.String`.

Being on the power allowlist means that the system will not apply most power saving features to the app. Guardrails for extreme cases may still be applied.

### isInteractive

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isInteractive(): Boolean
```

Returns true if the device is in an interactive state.

When this method returns true, the device is awake and ready to interact with the user (although this is not a guarantee that the user is actively interacting with the device just this moment). The main screen is usually turned on while in this state. Certain features, such as the proximity sensor, may temporarily turn off the screen while still leaving the device in an interactive state. Note in particular that the device is still considered to be interactive while dreaming (since dreams can be interactive) but not when it is dozing or asleep.

When this method returns false, the device is dozing or asleep and must be awoken before it will become ready to interact with the user again. The main screen is usually turned off while in this state. Certain features, such as "ambient mode" may cause the main screen to remain on (albeit in a low power state) to display system-provided content while the device dozes.

The system will send a `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_SCREEN_ON:kotlin.String` or `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_SCREEN_OFF:kotlin.String` broadcast whenever the interactive state of the device changes. For historical reasons, the names of these broadcasts refer to the power state of the screen but they are actually sent in response to changes in the overall interactive state of the device, as described by this method.

Services may use the non-interactive state as a hint to conserve power since the user is not present.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the device is in an interactive state. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_SCREEN_ON:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_SCREEN_OFF:kotlin.String`

### isLowPowerStandbyEnabled

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isLowPowerStandbyEnabled(): Boolean
```

Returns true if Low Power Standby is enabled.

When Low Power Standby is enabled, apps (including apps running foreground services) are subject to additional restrictions while the device is non-interactive, outside of device idle maintenance windows: Their network access is disabled, and any wakelocks they hold are ignored.

When Low Power Standby is enabled or disabled, a Intent with action `https://developer.android.com/reference/kotlin/android/os/PowerManager#ACTION_LOW_POWER_STANDBY_ENABLED_CHANGED:kotlin.String` is broadcast to registered receivers.

### isPowerSaveMode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isPowerSaveMode(): Boolean
```

Returns true if the device is currently in power save mode. When in this mode, applications should reduce their functionality in order to conserve battery as much as possible. You can monitor for changes to this state with `https://developer.android.com/reference/kotlin/android/os/PowerManager#ACTION_POWER_SAVE_MODE_CHANGED:kotlin.String`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if currently in low power mode, else false. |

### isRebootingUserspaceSupported

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isRebootingUserspaceSupported(): Boolean
```

**Deprecated:** *userspace reboot is deprecated, this method always returns `false`.*

Returns `true` if this device supports rebooting userspace.

### isScreenOn

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isScreenOn(): Boolean
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/os/PowerManager#isInteractive()` instead.*

Returns true if the device is in an interactive state.

For historical reasons, the name of this method refers to the power state of the screen but it actually describes the overall interactive state of the device. This method has been replaced by `https://developer.android.com/reference/kotlin/android/os/PowerManager#isInteractive()`.

The value returned by this method only indicates whether the device is in an interactive state which may have nothing to do with the screen being on or off. To determine the actual state of the screen, use `https://developer.android.com/reference/kotlin/android/view/Display.html#getState()`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the device is in an interactive state. |

### isSustainedPerformanceModeSupported

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isSustainedPerformanceModeSupported(): Boolean
```

This function checks if the device has implemented Sustained Performance Mode. This needs to be checked only once and is constant for a particular device/release. Sustained Performance Mode is intended to provide a consistent level of performance for prolonged amount of time. Applications should check if the device supports this mode, before using `https://developer.android.com/reference/kotlin/android/view/Window.html#setSustainedPerformanceMode(kotlin.Boolean)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns True if the device supports it, false otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/Window.html#setSustainedPerformanceMode(kotlin.Boolean)`

### isWakeLockLevelSupported

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isWakeLockLevelSupported(level: Int): Boolean
```

Returns true if the specified wake lock level is supported.

| Parameters ||
|---|---|
| `level` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The wake lock level to check. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the specified wake lock level is supported. |

### newWakeLock

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun newWakeLock(
    levelAndFlags: Int, 
    tag: String!
): PowerManager.WakeLock!
```

Creates a new wake lock with the specified level and flags.

The `levelAndFlags` parameter specifies a wake lock level and optional flags combined using the logical OR operator.

The wake lock levels are: `https://developer.android.com/reference/kotlin/android/os/PowerManager#PARTIAL_WAKE_LOCK:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/os/PowerManager#FULL_WAKE_LOCK:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/os/PowerManager#SCREEN_DIM_WAKE_LOCK:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/os/PowerManager#SCREEN_BRIGHT_WAKE_LOCK:kotlin.Int`. Exactly one wake lock level must be specified as part of the `levelAndFlags` parameter.

The wake lock flags are: `https://developer.android.com/reference/kotlin/android/os/PowerManager#ACQUIRE_CAUSES_WAKEUP:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/os/PowerManager#ON_AFTER_RELEASE:kotlin.Int`. Multiple flags can be combined as part of the `levelAndFlags` parameters.

Call `https://developer.android.com/reference/kotlin/android/os/PowerManager.WakeLock#acquire()` on the object to acquire the wake lock, and android.os.PowerManager.WakeLock#release when you are done.

{@samplecode \* PowerManager pm = mContext.getSystemService(PowerManager.class); \* PowerManager.WakeLock wl = pm.newWakeLock( \* PowerManager.SCREEN_DIM_WAKE_LOCK \* | PowerManager.ON_AFTER_RELEASE, \* TAG); \* wl.acquire(); \* // ... do work... \* wl.release(); \* }
| --- | --- |

Although a wake lock can be created without special permissions, the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WAKE_LOCK:kotlin.String` permission is required to actually acquire or release the wake lock that is returned.

**Device battery life will be significantly affected by the use of this API.** Do not acquire `https://developer.android.com/reference/kotlin/android/os/PowerManager.WakeLock`s unless you really need them, use the minimum levels possible, and be sure to release them as soon as possible.

If using this to keep the screen on, you should strongly consider using `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#FLAG_KEEP_SCREEN_ON:kotlin.Int` instead. This window flag will be correctly managed by the platform as the user moves between applications and doesn't require a special permission. Additionally using the flag will keep only the appropriate screen on in a multi-display scenario while using a wake lock will keep every screen powered on.

Recommended naming conventions for tags to make debugging easier:

- use a unique prefix delimited by a colon for your app/library (e.g. gmail:mytag) to make it easier to understand where the wake locks comes from. This namespace will also avoid collision for tags inside your app coming from different libraries which will make debugging easier.
- use constants (e.g. do not include timestamps in the tag) to make it easier for tools to aggregate similar wake locks. When collecting debugging data, the platform only monitors a finite number of tags, using constants will help tools to provide better debugging data.
- avoid using Class#getName() or similar method since this class name can be transformed by java optimizer and obfuscator tools.
- avoid wrapping the tag or a prefix to avoid collision with wake lock tags from the platform (e.g. \*alarm\*).
- never include personally identifiable information for privacy reasons.

<br />

| Parameters ||
|---|---|
| `levelAndFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Combination of wake lock level and flag values defining the requested behavior of the WakeLock. |
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Your class name (or other tag) for debugging purposes. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/PowerManager.WakeLock#acquire()`
- `https://developer.android.com/reference/kotlin/android/os/PowerManager.WakeLock#release()`
- `https://developer.android.com/reference/kotlin/android/os/PowerManager#PARTIAL_WAKE_LOCK:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/os/PowerManager#FULL_WAKE_LOCK:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/os/PowerManager#SCREEN_DIM_WAKE_LOCK:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/os/PowerManager#SCREEN_BRIGHT_WAKE_LOCK:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/os/PowerManager#PROXIMITY_SCREEN_OFF_WAKE_LOCK:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/os/PowerManager#ACQUIRE_CAUSES_WAKEUP:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/os/PowerManager#ON_AFTER_RELEASE:kotlin.Int`

### reboot

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun reboot(reason: String?): Unit
```

Reboot the device. Will not return if the reboot is successful.

Requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#REBOOT:kotlin.String` permission.

If the `reason` string contains ",quiescent", then the screen stays off during reboot and is not turned on again until the user triggers the device to wake up (for example, by pressing the power key). This behavior applies to Android TV devices launched on Android 11 (API level 30) or higher.
. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#REBOOT:kotlin.String`

| Parameters ||
|---|---|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: code to pass to the kernel (e.g., "recovery") to request special boot modes, or null. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if userspace reboot was requested on a device that doesn't support it. |

### removeThermalHeadroomListener

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeThermalHeadroomListener(listener: PowerManager.OnThermalHeadroomChangedListener): Unit
```

This function removes a listener for Thermal headroom change

| Parameters ||
|---|---|
| `listener` | [PowerManager.OnThermalHeadroomChangedListener](../android/os/PowerManager.OnThermalHeadroomChangedListener.md): listener to be removed. This value cannot be `null`. |

### removeThermalStatusListener

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeThermalStatusListener(listener: PowerManager.OnThermalStatusChangedListener): Unit
```

This function removes a listener for thermal status change

| Parameters ||
|---|---|
| `listener` | [PowerManager.OnThermalStatusChangedListener](../android/os/PowerManager.OnThermalStatusChangedListener.md): listener to be removed. This value cannot be `null`. |
