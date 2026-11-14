# BatteryManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BatteryManager

Kotlin| [Java](BatteryManager.md) 
| --- | --- |

```
open class BatteryManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.BatteryManager](BatteryManager.md) |

The BatteryManager class contains strings and constants used for values in the [android.content.Intent#ACTION_BATTERY_CHANGED](../android.content/Intent.md) Intent, and provides a method for querying battery and charging properties.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_CHARGING](BatteryManager.md) Sent when the device's battery has started charging (or has reached full charge and the device is on power). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_DISCHARGING](BatteryManager.md) Sent when the device's battery may be discharging, so apps should avoid doing extraneous work that would cause it to discharge faster. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_CAPACITY_LEVEL_CRITICAL](BatteryManager.md) Battery capacity level is critical. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_CAPACITY_LEVEL_FULL](BatteryManager.md) Battery capacity level is full. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_CAPACITY_LEVEL_HIGH](BatteryManager.md) Battery capacity level is high. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_CAPACITY_LEVEL_LOW](BatteryManager.md) Battery capacity level is low. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_CAPACITY_LEVEL_NORMAL](BatteryManager.md) Battery capacity level is normal. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_CAPACITY_LEVEL_UNKNOWN](BatteryManager.md) Battery capacity level is unknown. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_CAPACITY_LEVEL_UNSUPPORTED](BatteryManager.md) Battery capacity level is unsupported. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_HEALTH_COLD](BatteryManager.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_HEALTH_DEAD](BatteryManager.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_HEALTH_GOOD](BatteryManager.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_HEALTH_OVERHEAT](BatteryManager.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_HEALTH_OVER_VOLTAGE](BatteryManager.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_HEALTH_UNKNOWN](BatteryManager.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_HEALTH_UNSPECIFIED_FAILURE](BatteryManager.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_PLUGGED_AC](BatteryManager.md) Power source is an AC charger. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_PLUGGED_DOCK](BatteryManager.md) Power source is dock. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_PLUGGED_USB](BatteryManager.md) Power source is a USB port. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_PLUGGED_WIRELESS](BatteryManager.md) Power source is wireless. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_PROPERTY_CAPACITY](BatteryManager.md) Remaining battery capacity as an integer percentage of total capacity (with no fractional part). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_PROPERTY_CHARGE_COUNTER](BatteryManager.md) Battery capacity in microampere-hours, as an integer. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_PROPERTY_CURRENT_AVERAGE](BatteryManager.md) Average battery current in microamperes, as an integer. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_PROPERTY_CURRENT_NOW](BatteryManager.md) Instantaneous battery current in microamperes, as an integer. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_PROPERTY_ENERGY_COUNTER](BatteryManager.md) Battery remaining energy in nanowatt-hours, as a long integer. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_PROPERTY_STATUS](BatteryManager.md) Battery charge status, from a BATTERY_STATUS_\* value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_STATUS_CHARGING](BatteryManager.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_STATUS_DISCHARGING](BatteryManager.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_STATUS_FULL](BatteryManager.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_STATUS_NOT_CHARGING](BatteryManager.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BATTERY_STATUS_UNKNOWN](BatteryManager.md) <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_BATTERY_LOW](BatteryManager.md) Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](../android.content/Intent.md): Boolean field indicating whether the battery is currently considered to be low, that is whether a [Intent.ACTION_BATTERY_LOW](../android.content/Intent.md) broadcast has been sent. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_CAPACITY_LEVEL](BatteryManager.md) Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](../android.content/Intent.md): Int value representing the battery's capacity level. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_CHARGING_STATUS](BatteryManager.md) Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](../android.content/Intent.md): Int value representing the battery charging status. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_CYCLE_COUNT](BatteryManager.md) Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](../android.content/Intent.md): Int value representing the battery charging cycle count. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_HEALTH](BatteryManager.md) Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](../android.content/Intent.md): integer containing the current health constant. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_ICON_SMALL](BatteryManager.md) Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](../android.content/Intent.md): integer containing the resource ID of a small status bar icon indicating the current battery state. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_LEVEL](BatteryManager.md) Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](../android.content/Intent.md): integer field containing the current battery level, from 0 to [EXTRA_SCALE](BatteryManager.md). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PLUGGED](BatteryManager.md) Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](../android.content/Intent.md): integer indicating whether the device is plugged in to a power source; 0 means it is on battery, other constants are different types of power sources. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PRESENT](BatteryManager.md) Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](../android.content/Intent.md): boolean indicating whether a battery is present. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_SCALE](BatteryManager.md) Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](../android.content/Intent.md): integer containing the maximum battery level. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_STATUS](BatteryManager.md) Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](../android.content/Intent.md): integer containing the current status constant. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_TECHNOLOGY](BatteryManager.md) Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](../android.content/Intent.md): String describing the technology of the current battery. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_TEMPERATURE](BatteryManager.md) Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](../android.content/Intent.md): integer containing the current battery temperature. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_VOLTAGE](BatteryManager.md) Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](../android.content/Intent.md): integer containing the current battery voltage level. |
| --- | --- |

| Public methods ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [computeChargeTimeRemaining](BatteryManager.md))`()` Compute an approximation for how much time (in milliseconds) remains until the battery is fully charged. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIntProperty](BatteryManager.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the value of a battery property of integer type. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLongProperty](BatteryManager.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the value of a battery property of long type If the platform does not provide the property queried, this value will be Long. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getStringProperty](BatteryManager.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the value of a battery property of String type. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCharging](BatteryManager.md))`()` Return true if the battery is currently considered to be charging. |

## Constants

### ACTION_CHARGING

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_CHARGING: String
```

Sent when the device's battery has started charging (or has reached full charge and the device is on power). This is a good time to do work that you would like to avoid doing while on battery (that is to avoid draining the user's battery due to things they don't care enough about). This is paired with [ACTION_DISCHARGING](BatteryManager.md). The current state can always be retrieved with [isCharging()](BatteryManager.md)). 

 Value: "android.os.action.CHARGING"

### ACTION_DISCHARGING

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_DISCHARGING: String
```

Sent when the device's battery may be discharging, so apps should avoid doing extraneous work that would cause it to discharge faster. This is paired with [ACTION_CHARGING](BatteryManager.md). The current state can always be retrieved with [isCharging()](BatteryManager.md)). 

 Value: "android.os.action.DISCHARGING"

### BATTERY_CAPACITY_LEVEL_CRITICAL

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BATTERY_CAPACITY_LEVEL_CRITICAL: Int
```

Battery capacity level is critical. The Android framework has been notified to schedule a shutdown by this value. 

 Value: 1

**See Also**

- [#EXTRA_CAPACITY_LEVEL](BatteryManager.md) 

### BATTERY_CAPACITY_LEVEL_FULL

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BATTERY_CAPACITY_LEVEL_FULL: Int
```

Battery capacity level is full. The battery is full, the battery temperature is within the normal range, and adapter power is enough to sustain running background loads. The Android framework can run background tasks without affecting the battery level or battery performance. 

 Value: 5

**See Also**

- [#EXTRA_CAPACITY_LEVEL](BatteryManager.md) 

### BATTERY_CAPACITY_LEVEL_HIGH

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BATTERY_CAPACITY_LEVEL_HIGH: Int
```

Battery capacity level is high. Battery level is high, battery temperature is within the normal range, and adapter power is enough to charge the battery at an acceptable rate while running background loads. The Android framework can run background tasks without affecting charging or battery performance. 

 Value: 4

**See Also**

- [#EXTRA_CAPACITY_LEVEL](BatteryManager.md) 

### BATTERY_CAPACITY_LEVEL_LOW

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BATTERY_CAPACITY_LEVEL_LOW: Int
```

Battery capacity level is low. The Android framework must limit background jobs to avoid impacting charging speed. 

 Value: 2

**See Also**

- [#EXTRA_CAPACITY_LEVEL](BatteryManager.md) 

### BATTERY_CAPACITY_LEVEL_NORMAL

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BATTERY_CAPACITY_LEVEL_NORMAL: Int
```

Battery capacity level is normal. Battery level and charging rates are normal, battery temperature is within the normal range, and adapter power is enough to charge the battery at an acceptable rate. The Android framework can run light background tasks without affecting charging performance severely. 

 Value: 3

**See Also**

- [#EXTRA_CAPACITY_LEVEL](BatteryManager.md) 

### BATTERY_CAPACITY_LEVEL_UNKNOWN

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BATTERY_CAPACITY_LEVEL_UNKNOWN: Int
```

Battery capacity level is unknown. 

 Value: 0

**See Also**

- [#EXTRA_CAPACITY_LEVEL](BatteryManager.md) 

### BATTERY_CAPACITY_LEVEL_UNSUPPORTED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BATTERY_CAPACITY_LEVEL_UNSUPPORTED: Int
```

Battery capacity level is unsupported. 

 Value: -1

**See Also**

- [#EXTRA_CAPACITY_LEVEL](BatteryManager.md) 

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

Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](../android.content/Intent.md): Boolean field indicating whether the battery is currently considered to be low, that is whether a [Intent.ACTION_BATTERY_LOW](../android.content/Intent.md) broadcast has been sent. 

 Value: "battery_low"

### EXTRA_CAPACITY_LEVEL

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_CAPACITY_LEVEL: String
```

Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](../android.content/Intent.md): Int value representing the battery's capacity level. These constants are key indicators of battery status and system capabilities, guiding power management decisions for both the system and apps. 

 Value: "android.os.extra.CAPACITY_LEVEL"

**See Also**

- [#BATTERY_CAPACITY_LEVEL_UNSUPPORTED](BatteryManager.md)
- [#BATTERY_CAPACITY_LEVEL_UNKNOWN](BatteryManager.md)
- [#BATTERY_CAPACITY_LEVEL_CRITICAL](BatteryManager.md)
- [#BATTERY_CAPACITY_LEVEL_LOW](BatteryManager.md)
- [#BATTERY_CAPACITY_LEVEL_NORMAL](BatteryManager.md)
- [#BATTERY_CAPACITY_LEVEL_HIGH](BatteryManager.md)
- [#BATTERY_CAPACITY_LEVEL_FULL](BatteryManager.md) 

### EXTRA_CHARGING_STATUS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_CHARGING_STATUS: String
```

Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](../android.content/Intent.md): Int value representing the battery charging status. 

 Value: "android.os.extra.CHARGING_STATUS"

### EXTRA_CYCLE_COUNT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_CYCLE_COUNT: String
```

Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](../android.content/Intent.md): Int value representing the battery charging cycle count. 

 Value: "android.os.extra.CYCLE_COUNT"

### EXTRA_HEALTH

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_HEALTH: String
```

Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](../android.content/Intent.md): integer containing the current health constant. 

 Value: "health"

### EXTRA_ICON_SMALL

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_ICON_SMALL: String
```

Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](../android.content/Intent.md): integer containing the resource ID of a small status bar icon indicating the current battery state. 

 Value: "icon-small"

### EXTRA_LEVEL

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_LEVEL: String
```

Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](../android.content/Intent.md): integer field containing the current battery level, from 0 to [EXTRA_SCALE](BatteryManager.md). 

 Value: "level"

### EXTRA_PLUGGED

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_PLUGGED: String
```

Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](../android.content/Intent.md): integer indicating whether the device is plugged in to a power source; 0 means it is on battery, other constants are different types of power sources. 

 Value: "plugged"

### EXTRA_PRESENT

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_PRESENT: String
```

Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](../android.content/Intent.md): boolean indicating whether a battery is present. 

 Value: "present"

### EXTRA_SCALE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_SCALE: String
```

Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](../android.content/Intent.md): integer containing the maximum battery level. 

 Value: "scale"

### EXTRA_STATUS

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_STATUS: String
```

Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](../android.content/Intent.md): integer containing the current status constant. 

 Value: "status"

### EXTRA_TECHNOLOGY

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_TECHNOLOGY: String
```

Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](../android.content/Intent.md): String describing the technology of the current battery. 

 Value: "technology"

### EXTRA_TEMPERATURE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_TEMPERATURE: String
```

Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](../android.content/Intent.md): integer containing the current battery temperature. 

 Value: "temperature"

### EXTRA_VOLTAGE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_VOLTAGE: String
```

Extra for [android.content.Intent#ACTION_BATTERY_CHANGED](../android.content/Intent.md): integer containing the current battery voltage level. 

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

Return true if the battery is currently considered to be charging. This means that the device is plugged in and is supplying sufficient power that the battery level is going up (or the battery is fully charged). Changes in this state are matched by broadcasts of [ACTION_CHARGING](BatteryManager.md) and [ACTION_DISCHARGING](BatteryManager.md).
