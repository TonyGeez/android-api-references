# BatteryManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BatteryManager

Kotlin| [Java](https://developer.android.com/reference/android/os/BatteryManager "View this page in Java") 

```
open class BatteryManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.os.BatteryManager](https://developer.android.com/reference/kotlin/android/os/BatteryManager#) |

The BatteryManager class contains strings and constants used for values in the [android.content.Intent#ACTION_BATTERY_CHANGED](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_BATTERY_CHANGED:kotlin.String) Intent, and provides a method for querying battery and charging properties.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_CHARGING](https://developer.android.com/reference/kotlin/android/os/BatteryManager#ACTION_CHARGING:kotlin.String) Sent when the device's battery has started charging (or has reached full charge and the device is on power). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_DISCHARGING](https://developer.android.com/reference/kotlin/android/os/BatteryManager#ACTION_DISCHARGING:kotlin.String) Sent when the device's battery may be discharging, so apps should avoid doing extraneous work that would cause it to discharge faster. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_CAPACITY_LEVEL_CRITICAL](https://developer.android.com/reference/kotlin/android/os/BatteryManager#BATTERY_CAPACITY_LEVEL_CRITICAL:kotlin.Int) Battery capacity level is critical. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_CAPACITY_LEVEL_FULL](https://developer.android.com/reference/kotlin/android/os/BatteryManager#BATTERY_CAPACITY_LEVEL_FULL:kotlin.Int) Battery capacity level is full. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_CAPACITY_LEVEL_HIGH](https://developer.android.com/reference/kotlin/android/os/BatteryManager#BATTERY_CAPACITY_LEVEL_HIGH:kotlin.Int) Battery capacity level is high. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_CAPACITY_LEVEL_LOW](https://developer.android.com/reference/kotlin/android/os/BatteryManager#BATTERY_CAPACITY_LEVEL_LOW:kotlin.Int) Battery capacity level is low. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_CAPACITY_LEVEL_NORMAL](https://developer.android.com/reference/kotlin/android/os/BatteryManager#BATTERY_CAPACITY_LEVEL_NORMAL:kotlin.Int) Battery capacity level is normal. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_CAPACITY_LEVEL_UNKNOWN](https://developer.android.com/reference/kotlin/android/os/BatteryManager#BATTERY_CAPACITY_LEVEL_UNKNOWN:kotlin.Int) Battery capacity level is unknown. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_CAPACITY_LEVEL_UNSUPPORTED](https://developer.android.com/reference/kotlin/android/os/BatteryManager#BATTERY_CAPACITY_LEVEL_UNSUPPORTED:kotlin.Int) Battery capacity level is unsupported. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_HEALTH_COLD](https://developer.android.com/reference/kotlin/android/os/BatteryManager#BATTERY_HEALTH_COLD:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_HEALTH_DEAD](https://developer.android.com/reference/kotlin/android/os/BatteryManager#BATTERY_HEALTH_DEAD:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_HEALTH_GOOD](https://developer.android.com/reference/kotlin/android/os/BatteryManager#BATTERY_HEALTH_GOOD:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_HEALTH_OVERHEAT](https://developer.android.com/reference/kotlin/android/os/BatteryManager#BATTERY_HEALTH_OVERHEAT:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_HEALTH_OVER_VOLTAGE](https://developer.android.com/reference/kotlin/android/os/BatteryManager#BATTERY_HEALTH_OVER_VOLTAGE:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_HEALTH_UNKNOWN](https://developer.android.com/reference/kotlin/android/os/BatteryManager#BATTERY_HEALTH_UNKNOWN:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_HEALTH_UNSPECIFIED_FAILURE](https://developer.android.com/reference/kotlin/android/os/BatteryManager#BATTERY_HEALTH_UNSPECIFIED_FAILURE:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_PLUGGED_AC](https://developer.android.com/reference/kotlin/android/os/BatteryManager#BATTERY_PLUGGED_AC:kotlin.Int) Power source is an AC charger. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_PLUGGED_DOCK](https://developer.android.com/reference/kotlin/android/os/BatteryManager#BATTERY_PLUGGED_DOCK:kotlin.Int) Power source is dock. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_PLUGGED_USB](https://developer.android.com/reference/kotlin/android/os/BatteryManager#BATTERY_PLUGGED_USB:kotlin.Int) Power source is a USB port. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_PLUGGED_WIRELESS](https://developer.android.com/reference/kotlin/android/os/BatteryManager#BATTERY_PLUGGED_WIRELESS:kotlin.Int) Power source is wireless. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_PROPERTY_CAPACITY](https://developer.android.com/reference/kotlin/android/os/BatteryManager#BATTERY_PROPERTY_CAPACITY:kotlin.Int) Remaining battery capacity as an integer percentage of total capacity (with no fractional part). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_PROPERTY_CHARGE_COUNTER](https://developer.android.com/reference/kotlin/android/os/BatteryManager#BATTERY_PROPERTY_CHARGE_COUNTER:kotlin.Int) Battery capacity in microampere-hours, as an integer. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_PROPERTY_CURRENT_AVERAGE](https://developer.android.com/reference/kotlin/android/os/BatteryManager#BATTERY_PROPERTY_CURRENT_AVERAGE:kotlin.Int) Average battery current in microamperes, as an integer. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_PROPERTY_CURRENT_NOW](https://developer.android.com/reference/kotlin/android/os/BatteryManager#BATTERY_PROPERTY_CURRENT_NOW:kotlin.Int) Instantaneous battery current in microamperes, as an integer. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_PROPERTY_ENERGY_COUNTER](https://developer.android.com/reference/kotlin/android/os/BatteryManager#BATTERY_PROPERTY_ENERGY_COUNTER:kotlin.Int) Battery remaining energy in nanowatt-hours, as a long integer. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_PROPERTY_STATUS](https://developer.android.com/reference/kotlin/android/os/BatteryManager#BATTERY_PROPERTY_STATUS:kotlin.Int) Battery charge status, from a BATTERY_STATUS_\* value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_STATUS_CHARGING](https://developer.android.com/reference/kotlin/android/os/BatteryManager#BATTERY_STATUS_CHARGING:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_STATUS_DISCHARGING](https://developer.android.com/reference/kotlin/android/os/BatteryManager#BATTERY_STATUS_DISCHARGING:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_STATUS_FULL](https://developer.android.com/reference/kotlin/android/os/BatteryManager#BATTERY_STATUS_FULL:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_STATUS_NOT_CHARGING](https://developer.android.com/reference/kotlin/android/os/BatteryManager#BATTERY_STATUS_NOT_CHARGING:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_STATUS_UNKNOWN](https://developer.android.com/reference/kotlin/android/os/BatteryManager#BATTERY_STATUS_UNKNOWN:kotlin.Int) <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_BATTERY_LOW](https://developer.android.com/reference/kotlin/android/os/BatteryManager#EXTRA_BATTERY_LOW:kotlin.String) Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_BATTERY_CHANGED:kotlin.String): Boolean field indicating whether the battery is currently considered to be low, that is whether a [Intent.ACTION_BATTERY_LOW](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_BATTERY_LOW:kotlin.String) broadcast has been sent. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_CAPACITY_LEVEL](https://developer.android.com/reference/kotlin/android/os/BatteryManager#EXTRA_CAPACITY_LEVEL:kotlin.String) Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_BATTERY_CHANGED:kotlin.String): Int value representing the battery's capacity level. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_CHARGING_STATUS](https://developer.android.com/reference/kotlin/android/os/BatteryManager#EXTRA_CHARGING_STATUS:kotlin.String) Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_BATTERY_CHANGED:kotlin.String): Int value representing the battery charging status. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_CYCLE_COUNT](https://developer.android.com/reference/kotlin/android/os/BatteryManager#EXTRA_CYCLE_COUNT:kotlin.String) Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_BATTERY_CHANGED:kotlin.String): Int value representing the battery charging cycle count. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_HEALTH](https://developer.android.com/reference/kotlin/android/os/BatteryManager#EXTRA_HEALTH:kotlin.String) Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_BATTERY_CHANGED:kotlin.String): integer containing the current health constant. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_ICON_SMALL](https://developer.android.com/reference/kotlin/android/os/BatteryManager#EXTRA_ICON_SMALL:kotlin.String) Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_BATTERY_CHANGED:kotlin.String): integer containing the resource ID of a small status bar icon indicating the current battery state. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_LEVEL](https://developer.android.com/reference/kotlin/android/os/BatteryManager#EXTRA_LEVEL:kotlin.String) Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_BATTERY_CHANGED:kotlin.String): integer field containing the current battery level, from 0 to [EXTRA_SCALE](https://developer.android.com/reference/kotlin/android/os/BatteryManager#EXTRA_SCALE:kotlin.String). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PLUGGED](https://developer.android.com/reference/kotlin/android/os/BatteryManager#EXTRA_PLUGGED:kotlin.String) Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_BATTERY_CHANGED:kotlin.String): integer indicating whether the device is plugged in to a power source; 0 means it is on battery, other constants are different types of power sources. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PRESENT](https://developer.android.com/reference/kotlin/android/os/BatteryManager#EXTRA_PRESENT:kotlin.String) Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_BATTERY_CHANGED:kotlin.String): boolean indicating whether a battery is present. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_SCALE](https://developer.android.com/reference/kotlin/android/os/BatteryManager#EXTRA_SCALE:kotlin.String) Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_BATTERY_CHANGED:kotlin.String): integer containing the maximum battery level. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_STATUS](https://developer.android.com/reference/kotlin/android/os/BatteryManager#EXTRA_STATUS:kotlin.String) Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_BATTERY_CHANGED:kotlin.String): integer containing the current status constant. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_TECHNOLOGY](https://developer.android.com/reference/kotlin/android/os/BatteryManager#EXTRA_TECHNOLOGY:kotlin.String) Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_BATTERY_CHANGED:kotlin.String): String describing the technology of the current battery. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_TEMPERATURE](https://developer.android.com/reference/kotlin/android/os/BatteryManager#EXTRA_TEMPERATURE:kotlin.String) Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_BATTERY_CHANGED:kotlin.String): integer containing the current battery temperature. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_VOLTAGE](https://developer.android.com/reference/kotlin/android/os/BatteryManager#EXTRA_VOLTAGE:kotlin.String) Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_BATTERY_CHANGED:kotlin.String): integer containing the current battery voltage level. |

| Public methods ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [computeChargeTimeRemaining](https://developer.android.com/reference/kotlin/android/os/BatteryManager#computeChargeTimeRemaining())`()` Compute an approximation for how much time (in milliseconds) remains until the battery is fully charged. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIntProperty](https://developer.android.com/reference/kotlin/android/os/BatteryManager#getIntProperty(kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the value of a battery property of integer type. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLongProperty](https://developer.android.com/reference/kotlin/android/os/BatteryManager#getLongProperty(kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the value of a battery property of long type If the platform does not provide the property queried, this value will be Long. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getStringProperty](https://developer.android.com/reference/kotlin/android/os/BatteryManager#getStringProperty(kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the value of a battery property of String type. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCharging](https://developer.android.com/reference/kotlin/android/os/BatteryManager#isCharging())`()` Return true if the battery is currently considered to be charging. |

## Constants

### ACTION_CHARGING

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_CHARGING: String
```

Sent when the device's battery has started charging (or has reached full charge and the device is on power). This is a good time to do work that you would like to avoid doing while on battery (that is to avoid draining the user's battery due to things they don't care enough about). This is paired with [ACTION_DISCHARGING](https://developer.android.com/reference/kotlin/android/os/BatteryManager#ACTION_DISCHARGING:kotlin.String). The current state can always be retrieved with [isCharging()](https://developer.android.com/reference/kotlin/android/os/BatteryManager#isCharging()). 

 Value: "android.os.action.CHARGING"

### ACTION_DISCHARGING

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_DISCHARGING: String
```

Sent when the device's battery may be discharging, so apps should avoid doing extraneous work that would cause it to discharge faster. This is paired with [ACTION_CHARGING](https://developer.android.com/reference/kotlin/android/os/BatteryManager#ACTION_CHARGING:kotlin.String). The current state can always be retrieved with [isCharging()](https://developer.android.com/reference/kotlin/android/os/BatteryManager#isCharging()). 

 Value: "android.os.action.DISCHARGING"

### BATTERY_CAPACITY_LEVEL_CRITICAL

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BATTERY_CAPACITY_LEVEL_CRITICAL: Int
```

Battery capacity level is critical. The Android framework has been notified to schedule a shutdown by this value. 

 Value: 1

**See Also**

- [#EXTRA_CAPACITY_LEVEL](https://developer.android.com/reference/kotlin/android/os/BatteryManager#EXTRA_CAPACITY_LEVEL:kotlin.String) 

### BATTERY_CAPACITY_LEVEL_FULL

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BATTERY_CAPACITY_LEVEL_FULL: Int
```

Battery capacity level is full. The battery is full, the battery temperature is within the normal range, and adapter power is enough to sustain running background loads. The Android framework can run background tasks without affecting the battery level or battery performance. 

 Value: 5

**See Also**

- [#EXTRA_CAPACITY_LEVEL](https://developer.android.com/reference/kotlin/android/os/BatteryManager#EXTRA_CAPACITY_LEVEL:kotlin.String) 

### BATTERY_CAPACITY_LEVEL_HIGH

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BATTERY_CAPACITY_LEVEL_HIGH: Int
```

Battery capacity level is high. Battery level is high, battery temperature is within the normal range, and adapter power is enough to charge the battery at an acceptable rate while running background loads. The Android framework can run background tasks without affecting charging or battery performance. 

 Value: 4

**See Also**

- [#EXTRA_CAPACITY_LEVEL](https://developer.android.com/reference/kotlin/android/os/BatteryManager#EXTRA_CAPACITY_LEVEL:kotlin.String) 

### BATTERY_CAPACITY_LEVEL_LOW

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BATTERY_CAPACITY_LEVEL_LOW: Int
```

Battery capacity level is low. The Android framework must limit background jobs to avoid impacting charging speed. 

 Value: 2

**See Also**

- [#EXTRA_CAPACITY_LEVEL](https://developer.android.com/reference/kotlin/android/os/BatteryManager#EXTRA_CAPACITY_LEVEL:kotlin.String) 

### BATTERY_CAPACITY_LEVEL_NORMAL

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BATTERY_CAPACITY_LEVEL_NORMAL: Int
```

Battery capacity level is normal. Battery level and charging rates are normal, battery temperature is within the normal range, and adapter power is enough to charge the battery at an acceptable rate. The Android framework can run light background tasks without affecting charging performance severely. 

 Value: 3

**See Also**

- [#EXTRA_CAPACITY_LEVEL](https://developer.android.com/reference/kotlin/android/os/BatteryManager#EXTRA_CAPACITY_LEVEL:kotlin.String) 

### BATTERY_CAPACITY_LEVEL_UNKNOWN

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BATTERY_CAPACITY_LEVEL_UNKNOWN: Int
```

Battery capacity level is unknown. 

 Value: 0

**See Also**

- [#EXTRA_CAPACITY_LEVEL](https://developer.android.com/reference/kotlin/android/os/BatteryManager#EXTRA_CAPACITY_LEVEL:kotlin.String) 

### BATTERY_CAPACITY_LEVEL_UNSUPPORTED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BATTERY_CAPACITY_LEVEL_UNSUPPORTED: Int
```

Battery capacity level is unsupported. 

 Value: -1

**See Also**

- [#EXTRA_CAPACITY_LEVEL](https://developer.android.com/reference/kotlin/android/os/BatteryManager#EXTRA_CAPACITY_LEVEL:kotlin.String) 

### BATTERY_HEALTH_COLD

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BATTERY_HEALTH_COLD: Int
```  

 Value: 7

### BATTERY_HEALTH_DEAD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BATTERY_HEALTH_DEAD: Int
```  

 Value: 4

### BATTERY_HEALTH_GOOD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BATTERY_HEALTH_GOOD: Int
```  

 Value: 2

### BATTERY_HEALTH_OVERHEAT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BATTERY_HEALTH_OVERHEAT: Int
```  

 Value: 3

### BATTERY_HEALTH_OVER_VOLTAGE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BATTERY_HEALTH_OVER_VOLTAGE: Int
```  

 Value: 5

### BATTERY_HEALTH_UNKNOWN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BATTERY_HEALTH_UNKNOWN: Int
```  

 Value: 1

### BATTERY_HEALTH_UNSPECIFIED_FAILURE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BATTERY_HEALTH_UNSPECIFIED_FAILURE: Int
```  

 Value: 6

### BATTERY_PLUGGED_AC

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BATTERY_PLUGGED_AC: Int
```

Power source is an AC charger. 

 Value: 1

### BATTERY_PLUGGED_DOCK

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BATTERY_PLUGGED_DOCK: Int
```

Power source is dock. 

 Value: 8

### BATTERY_PLUGGED_USB

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BATTERY_PLUGGED_USB: Int
```

Power source is a USB port. 

 Value: 2

### BATTERY_PLUGGED_WIRELESS

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BATTERY_PLUGGED_WIRELESS: Int
```

Power source is wireless. 

 Value: 4

### BATTERY_PROPERTY_CAPACITY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BATTERY_PROPERTY_CAPACITY: Int
```

Remaining battery capacity as an integer percentage of total capacity (with no fractional part). 

 Value: 4

### BATTERY_PROPERTY_CHARGE_COUNTER

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BATTERY_PROPERTY_CHARGE_COUNTER: Int
```

Battery capacity in microampere-hours, as an integer. 

 Value: 1

### BATTERY_PROPERTY_CURRENT_AVERAGE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BATTERY_PROPERTY_CURRENT_AVERAGE: Int
```

Average battery current in microamperes, as an integer. Positive values indicate net current entering the battery from a charge source, negative values indicate net current discharging from the battery. The time period over which the average is computed may depend on the fuel gauge hardware and its configuration. 

 Value: 3

### BATTERY_PROPERTY_CURRENT_NOW

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BATTERY_PROPERTY_CURRENT_NOW: Int
```

Instantaneous battery current in microamperes, as an integer. Positive values indicate net current entering the battery from a charge source, negative values indicate net current discharging from the battery. 

 Value: 2

### BATTERY_PROPERTY_ENERGY_COUNTER

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BATTERY_PROPERTY_ENERGY_COUNTER: Int
```

Battery remaining energy in nanowatt-hours, as a long integer. 

 Value: 5

### BATTERY_PROPERTY_STATUS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BATTERY_PROPERTY_STATUS: Int
```

Battery charge status, from a BATTERY_STATUS_\* value. 

 Value: 6

### BATTERY_STATUS_CHARGING

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BATTERY_STATUS_CHARGING: Int
```  

 Value: 2

### BATTERY_STATUS_DISCHARGING

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BATTERY_STATUS_DISCHARGING: Int
```  

 Value: 3

### BATTERY_STATUS_FULL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BATTERY_STATUS_FULL: Int
```  

 Value: 5

### BATTERY_STATUS_NOT_CHARGING

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BATTERY_STATUS_NOT_CHARGING: Int
```  

 Value: 4

### BATTERY_STATUS_UNKNOWN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BATTERY_STATUS_UNKNOWN: Int
```  

 Value: 1

### EXTRA_BATTERY_LOW

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_BATTERY_LOW: String
```

Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_BATTERY_CHANGED:kotlin.String): Boolean field indicating whether the battery is currently considered to be low, that is whether a [Intent.ACTION_BATTERY_LOW](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_BATTERY_LOW:kotlin.String) broadcast has been sent. 

 Value: "battery_low"

### EXTRA_CAPACITY_LEVEL

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_CAPACITY_LEVEL: String
```

Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_BATTERY_CHANGED:kotlin.String): Int value representing the battery's capacity level. These constants are key indicators of battery status and system capabilities, guiding power management decisions for both the system and apps. 

 Value: "android.os.extra.CAPACITY_LEVEL"

**See Also**

- [#BATTERY_CAPACITY_LEVEL_UNSUPPORTED](https://developer.android.com/reference/kotlin/android/os/BatteryManager#BATTERY_CAPACITY_LEVEL_UNSUPPORTED:kotlin.Int)
- [#BATTERY_CAPACITY_LEVEL_UNKNOWN](https://developer.android.com/reference/kotlin/android/os/BatteryManager#BATTERY_CAPACITY_LEVEL_UNKNOWN:kotlin.Int)
- [#BATTERY_CAPACITY_LEVEL_CRITICAL](https://developer.android.com/reference/kotlin/android/os/BatteryManager#BATTERY_CAPACITY_LEVEL_CRITICAL:kotlin.Int)
- [#BATTERY_CAPACITY_LEVEL_LOW](https://developer.android.com/reference/kotlin/android/os/BatteryManager#BATTERY_CAPACITY_LEVEL_LOW:kotlin.Int)
- [#BATTERY_CAPACITY_LEVEL_NORMAL](https://developer.android.com/reference/kotlin/android/os/BatteryManager#BATTERY_CAPACITY_LEVEL_NORMAL:kotlin.Int)
- [#BATTERY_CAPACITY_LEVEL_HIGH](https://developer.android.com/reference/kotlin/android/os/BatteryManager#BATTERY_CAPACITY_LEVEL_HIGH:kotlin.Int)
- [#BATTERY_CAPACITY_LEVEL_FULL](https://developer.android.com/reference/kotlin/android/os/BatteryManager#BATTERY_CAPACITY_LEVEL_FULL:kotlin.Int) 

### EXTRA_CHARGING_STATUS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_CHARGING_STATUS: String
```

Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_BATTERY_CHANGED:kotlin.String): Int value representing the battery charging status. 

 Value: "android.os.extra.CHARGING_STATUS"

### EXTRA_CYCLE_COUNT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_CYCLE_COUNT: String
```

Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_BATTERY_CHANGED:kotlin.String): Int value representing the battery charging cycle count. 

 Value: "android.os.extra.CYCLE_COUNT"

### EXTRA_HEALTH

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_HEALTH: String
```

Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_BATTERY_CHANGED:kotlin.String): integer containing the current health constant. 

 Value: "health"

### EXTRA_ICON_SMALL

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_ICON_SMALL: String
```

Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_BATTERY_CHANGED:kotlin.String): integer containing the resource ID of a small status bar icon indicating the current battery state. 

 Value: "icon-small"

### EXTRA_LEVEL

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_LEVEL: String
```

Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_BATTERY_CHANGED:kotlin.String): integer field containing the current battery level, from 0 to [EXTRA_SCALE](https://developer.android.com/reference/kotlin/android/os/BatteryManager#EXTRA_SCALE:kotlin.String). 

 Value: "level"

### EXTRA_PLUGGED

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_PLUGGED: String
```

Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_BATTERY_CHANGED:kotlin.String): integer indicating whether the device is plugged in to a power source; 0 means it is on battery, other constants are different types of power sources. 

 Value: "plugged"

### EXTRA_PRESENT

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_PRESENT: String
```

Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_BATTERY_CHANGED:kotlin.String): boolean indicating whether a battery is present. 

 Value: "present"

### EXTRA_SCALE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_SCALE: String
```

Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_BATTERY_CHANGED:kotlin.String): integer containing the maximum battery level. 

 Value: "scale"

### EXTRA_STATUS

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_STATUS: String
```

Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_BATTERY_CHANGED:kotlin.String): integer containing the current status constant. 

 Value: "status"

### EXTRA_TECHNOLOGY

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_TECHNOLOGY: String
```

Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_BATTERY_CHANGED:kotlin.String): String describing the technology of the current battery. 

 Value: "technology"

### EXTRA_TEMPERATURE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_TEMPERATURE: String
```

Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_BATTERY_CHANGED:kotlin.String): integer containing the current battery temperature. 

 Value: "temperature"

### EXTRA_VOLTAGE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_VOLTAGE: String
```

Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_BATTERY_CHANGED:kotlin.String): integer containing the current battery voltage level. 

 Value: "voltage"

## Public methods

### computeChargeTimeRemaining

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun computeChargeTimeRemaining(): Long
```

Compute an approximation for how much time (in milliseconds) remains until the battery is fully charged. Returns -1 if no time can be computed: either there is not enough current data to make a decision or the battery is currently discharging.

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | how much time is left, in milliseconds, until the battery is fully charged or -1 if the computation fails |

### getIntProperty

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIntProperty(id: Int): Int
```

Return the value of a battery property of integer type.

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):identifier of the requested property |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the property value. If the property is not supported or there is any other error, return (a) 0 if`targetSdkVersion < VERSION_CODES.P`or (b) Integer.MIN_VALUE if`targetSdkVersion >= VERSION_CODES.P`. |

### getLongProperty

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLongProperty(id: Int): Long
```

Return the value of a battery property of long type If the platform does not provide the property queried, this value will be Long.MIN_VALUE.

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):identifier of the requested property |

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the property value, or Long.MIN_VALUE if not supported. |

### getStringProperty

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStringProperty(id: Int): String?
```

Return the value of a battery property of String type. If the platform does not provide the property queried, this value will be null.

| Parameters ||
|------|------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):identifier of the requested property. |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the property value, or null if not supported. |

### isCharging

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isCharging(): Boolean
```

Return true if the battery is currently considered to be charging. This means that the device is plugged in and is supplying sufficient power that the battery level is going up (or the battery is fully charged). Changes in this state are matched by broadcasts of [ACTION_CHARGING](https://developer.android.com/reference/kotlin/android/os/BatteryManager#ACTION_CHARGING:kotlin.String) and [ACTION_DISCHARGING](https://developer.android.com/reference/kotlin/android/os/BatteryManager#ACTION_DISCHARGING:kotlin.String).
