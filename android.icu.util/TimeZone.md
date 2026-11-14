Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TimeZone

```
abstract class TimeZone : Cloneable, Freezable<TimeZone!>, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.util.TimeZone](TimeZone.md) |

**\[icu enhancement\]** ICU's replacement for `https://developer.android.com/reference/kotlin/java/util/TimeZone.html#`. Methods, fields, and other functionality specific to ICU are labeled '**\[icu\]**'.

`TimeZone` represents a time zone offset, and also computes daylight savings.

Typically, you get a `TimeZone` using getDefault which creates a `TimeZone` based on the time zone where the program is running. For example, for a program running in Japan, `getDefault` creates a `TimeZone` object based on Japanese Standard Time.

You can also get a `TimeZone` using getTimeZone along with a time zone ID. For instance, the time zone ID for the U.S. Pacific Time zone is "America/Los_Angeles". So, you can get a U.S. Pacific Time `TimeZone` object with:

```kotlin
TimeZone tz = TimeZone.getTimeZone("America/Los_Angeles");
  
```
You can use the getAvailableIDs method to iterate through all the supported time zone IDs, or getCanonicalID method to check if a time zone ID is supported or not. You can then choose a supported ID to get a `TimeZone`. If the time zone you want is not represented by one of the supported IDs, then you can create a custom time zone ID with the following syntax:

```kotlin
GMT[+|-]hh[[:]mm]
  
```
For example, you might specify GMT+14:00 as a custom time zone ID. The `TimeZone` that is returned when you specify a custom time zone ID uses the specified offset from GMT(=UTC) and does not observe daylight saving time. For example, you might specify GMT+14:00 as a custom time zone ID to create a TimeZone representing 14 hours ahead of GMT (with no daylight saving time). In addition, `getCanonicalID` can also be used to normalize a custom time zone ID.

For compatibility with JDK 1.1.x, some other three-letter time zone IDs (such as "PST", "CTT", "AST") are also supported. However, **their use is deprecated** because the same abbreviation is often used for multiple time zones (for example, "CST" could be U.S. "Central Standard Time" and "China Standard Time"), and the Java platform can then only recognize one of them.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/icu/util/TimeZone.SystemTimeZoneType` **\[icu\]** System time zone type constants used by filtering zones in getAvailableIDs |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/TimeZone#GENERIC_LOCATION:kotlin.Int` **\[icu\]** A style specifier for `getDisplayName()` indicating a long name derived from the timezone's fallback name, such as "United States (Los Angeles). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/TimeZone#LONG:kotlin.Int` A style specifier for `getDisplayName()` indicating a long name, such as "Pacific Standard Time. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/TimeZone#LONG_GENERIC:kotlin.Int` **\[icu\]** A style specifier for `getDisplayName()` indicating a long generic name, such as "Pacific Time. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/TimeZone#LONG_GMT:kotlin.Int` **\[icu\]** A style specifier for `getDisplayName()` indicating a long name derived from the timezone's offset, such as "GMT-08:00. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/TimeZone#SHORT:kotlin.Int` A style specifier for `getDisplayName()` indicating a short name, such as "PST. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/TimeZone#SHORT_COMMONLY_USED:kotlin.Int` **\[icu\]** A style specifier for `getDisplayName()` indicating a short name derived from the timezone's short standard or daylight timezone name ignoring commonlyUsed, such as "PDT. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/TimeZone#SHORT_GENERIC:kotlin.Int` **\[icu\]** A style specifier for `getDisplayName()` indicating a short generic name, such as "PT. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/TimeZone#SHORT_GMT:kotlin.Int` **\[icu\]** A style specifier for `getDisplayName()` indicating a short name derived from the timezone's offset, such as "-0800. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/TimeZone#TIMEZONE_ICU:kotlin.Int` **\[icu\]** A time zone implementation type indicating ICU's own TimeZone used by `getTimeZone`. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/TimeZone#TIMEZONE_JDK:kotlin.Int` **\[icu\]** A time zone implementation type indicating the `https://developer.android.com/reference/kotlin/java/util/TimeZone.html#` used by `getTimeZone`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/TimeZone#UNKNOWN_ZONE_ID:kotlin.String` **\[icu\]** The time zone ID reserved for unknown time zone. |

| Public constructors ||
|---|---|
| TimeZone Default constructor. |

| Public methods ||
|---|---|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | clone Overrides clone. |
| open [TimeZone](TimeZone.md)! | cloneAsThawed Provides for the clone operation. |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | countEquivalentIDs **\[icu\]** Returns the number of IDs in the equivalency group that includes the given ID. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Overrides equals. |
| open [TimeZone](TimeZone.md)! | freeze Freezes the object. |
| open static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | getAvailableIDs Return a new String array containing all system TimeZone IDs. |
| --- | --- |
| open static [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | getAvailableIDs **\[icu\]** Returns a set of time zone ID strings with the given filter conditions. |
| open static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | getAvailableIDs Return a new String array containing all system TimeZone IDs with the given raw offset from GMT. |
| open static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | getAvailableIDs Return a new String array containing all system TimeZone IDs associated with the given country. |
| --- | --- |
| open static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getCanonicalID **\[icu\]** Returns the canonical system time zone ID or the normalized custom time zone ID for the given time zone ID. |
| open static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getCanonicalID **\[icu\]** Returns the canonical system time zone ID or the normalized custom time zone ID for the given time zone ID. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getDSTSavings Returns the amount of time to be added to local standard time to get local wall clock time. |
| --- | --- |
| open static [TimeZone](TimeZone.md)! | getDefault Gets the default `TimeZone` for this host. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getDisplayName Returns a name of this time zone suitable for presentation to the user in the default `DISPLAY` locale. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getDisplayName Returns a name of this time zone suitable for presentation to the user in the specified locale. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getDisplayName Returns a name of this time zone suitable for presentation to the user in the default `DISPLAY` locale. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getDisplayName Returns a name of this time zone suitable for presentation to the user in the specified locale. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getDisplayName Returns a name of this time zone suitable for presentation to the user in the specified locale. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getDisplayName Returns a name of this time zone suitable for presentation to the user in the specified locale. |
| open static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getEquivalentID Returns an ID in the equivalency group that includes the given ID. |
| open static [TimeZone](TimeZone.md)! | getFrozenTimeZone Gets the `TimeZone` for the given ID. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getID Gets the ID of this time zone. |
| open static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getIDForWindowsID **\[icu\]** Converts a Windows time zone ID to an equivalent system time zone ID for a region. |
| open static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getIanaID Returns the preferred time zone ID in the IANA database for the given time zone ID. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getOffset Gets the time zone offset, for current date, modified in case of daylight savings. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getOffset Returns the offset of this time zone from UTC at the specified date. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | getOffset Returns the time zone raw and GMT offset for the given moment in time. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getRawOffset Gets unmodified offset, NOT modified in case of daylight savings. |
| open static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getRegion **\[icu\]** Returns the region code associated with the given system time zone ID. |
| open static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getTZDataVersion **\[icu\]** Returns the time zone data version currently used by ICU. |
| --- | --- |
| open static [TimeZone](TimeZone.md)! | getTimeZone Gets the `TimeZone` for the given ID. |
| open static [TimeZone](TimeZone.md)! | getTimeZone Gets the `TimeZone` for the given ID and the timezone type. |
| open static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getWindowsID **\[icu\]** Converts a system time zone ID to an equivalent Windows time zone ID. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasSameRules Returns true if this zone has the same rule and offset as another zone. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Overrides hashCode. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | inDaylightTime Queries if the given date is in daylight savings time in this time zone. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isFrozen Determines whether the object has been frozen or not. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | observesDaylightTime Queries if this time zone is in daylight saving time or will observe daylight saving time at any future time. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setID Sets the time zone ID. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setRawOffset Sets the base time zone offset to GMT. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | useDaylightTime Queries if this time zone uses daylight savings time. |

| Properties ||
|---|---|
| static [TimeZone](TimeZone.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/TimeZone#GMT_ZONE:android.icu.util.TimeZone` **\[icu\]** The immutable GMT (=UTC) time zone. |
| static [TimeZone](TimeZone.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/TimeZone#UNKNOWN_ZONE:android.icu.util.TimeZone` **\[icu\]** The immutable (frozen) "unknown" time zone. |

## Constants

### GENERIC_LOCATION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GENERIC_LOCATION: Int
```

**\[icu\]** A style specifier for `getDisplayName()` indicating a long name derived from the timezone's fallback name, such as "United States (Los Angeles)."

 Value: 7

### LONG

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LONG: Int
```

A style specifier for `getDisplayName()` indicating a long name, such as "Pacific Standard Time."

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/TimeZone#SHORT:kotlin.Int`

### LONG_GENERIC

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LONG_GENERIC: Int
```

**\[icu\]** A style specifier for `getDisplayName()` indicating a long generic name, such as "Pacific Time."

 Value: 3

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/TimeZone#SHORT_GENERIC:kotlin.Int`

### LONG_GMT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LONG_GMT: Int
```

**\[icu\]** A style specifier for `getDisplayName()` indicating a long name derived from the timezone's offset, such as "GMT-08:00."

 Value: 5

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/TimeZone#SHORT_GMT:kotlin.Int`

### SHORT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SHORT: Int
```

A style specifier for `getDisplayName()` indicating a short name, such as "PST."

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/TimeZone#LONG:kotlin.Int`

### SHORT_COMMONLY_USED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SHORT_COMMONLY_USED: Int
```

**\[icu\]** A style specifier for `getDisplayName()` indicating a short name derived from the timezone's short standard or daylight timezone name ignoring commonlyUsed, such as "PDT."

 Value: 6

### SHORT_GENERIC

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SHORT_GENERIC: Int
```

**\[icu\]** A style specifier for `getDisplayName()` indicating a short generic name, such as "PT."

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/TimeZone#LONG_GENERIC:kotlin.Int`

### SHORT_GMT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SHORT_GMT: Int
```

**\[icu\]** A style specifier for `getDisplayName()` indicating a short name derived from the timezone's offset, such as "-0800."

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/TimeZone#LONG_GMT:kotlin.Int`

### TIMEZONE_ICU

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TIMEZONE_ICU: Int
```

**\[icu\]** A time zone implementation type indicating ICU's own TimeZone used by `getTimeZone`.

 Value: 0

### TIMEZONE_JDK

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TIMEZONE_JDK: Int
```

**\[icu\]** A time zone implementation type indicating the `https://developer.android.com/reference/kotlin/java/util/TimeZone.html#` used by `getTimeZone`.

 Value: 1

### UNKNOWN_ZONE_ID

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNKNOWN_ZONE_ID: String
```

**\[icu\]** The time zone ID reserved for unknown time zone.

 Value: "Etc/Unknown"

**See Also**

- getTimeZone

## Public constructors

### TimeZone

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
TimeZone()
```

Default constructor. (For invocation by subclass constructors, typically implicit.)

## Public methods

### clone

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clone(): Any
```

Overrides clone.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html` | a clone of this instance. |

| Exceptions ||
|---|---|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the `Cloneable` interface. Subclasses that override the `clone` method can also throw this exception to indicate that an instance cannot be cloned. |

### cloneAsThawed

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun cloneAsThawed(): TimeZone!
```

Provides for the clone operation. Any clone is initially unfrozen.

### countEquivalentIDs

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun countEquivalentIDs(id: String!): Int
```

**\[icu\]** Returns the number of IDs in the equivalency group that includes the given ID. An equivalency group contains zones that have the same GMT offset and rules.

The returned count includes the given ID; it is always \>= 1 for valid IDs. The given ID must be a system time zone. If it is not, returns zero.

| Parameters ||
|---|---|
| `id` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a system time zone ID |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of zones in the equivalency group containing 'id', or zero if 'id' is not a valid system ID |

**See Also**

- getEquivalentID

### equals

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(other: Any?): Boolean
```

Overrides equals.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### freeze

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun freeze(): TimeZone!
```

Freezes the object.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/util/TimeZone#!` | the object itself. |

### getAvailableIDs

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getAvailableIDs(): Array<String!>!
```

Return a new String array containing all system TimeZone IDs. These IDs (and only these IDs) may be passed to `get()` to construct the corresponding TimeZone object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | an array of all system TimeZone IDs |

**See Also**

- getAvailableIDs

### getAvailableIDs

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getAvailableIDs(
    zoneType: TimeZone.SystemTimeZoneType!, 
    region: String!, 
    rawOffset: Int!
): MutableSet<String!>!
```

**\[icu\]** Returns a set of time zone ID strings with the given filter conditions.

**Note:** A `Set` returned by this method is immutable.

| Parameters ||
|---|---|
| `zoneType` | [TimeZone.SystemTimeZoneType](../android/icu/util/TimeZone.SystemTimeZoneType.md)!: The system time zone type. |
| `region` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The ISO 3166 two-letter country code or UN M.49 three-digit area code. When null, no filtering done by region. |
| `rawOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!: An offset from GMT in milliseconds, ignoring the effect of daylight savings time, if any. When null, no filtering done by zone offset. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | an immutable set of system time zone IDs. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/TimeZone.SystemTimeZoneType`

### getAvailableIDs

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getAvailableIDs(rawOffset: Int): Array<String!>!
```

Return a new String array containing all system TimeZone IDs with the given raw offset from GMT. These IDs may be passed to `get()` to construct the corresponding TimeZone object.

| Parameters ||
|---|---|
| `rawOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the offset in milliseconds from GMT |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | an array of IDs for system TimeZones with the given raw offset. If there are none, return a zero-length array. |

**See Also**

- getAvailableIDs

### getAvailableIDs

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getAvailableIDs(country: String!): Array<String!>!
```

Return a new String array containing all system TimeZone IDs associated with the given country. These IDs may be passed to `get()` to construct the corresponding TimeZone object.

| Parameters ||
|---|---|
| `country` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a two-letter ISO 3166 country code, or `null` to return zones not associated with any country |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | an array of IDs for system TimeZones in the given country. If there are none, return a zero-length array. |

**See Also**

- getAvailableIDs

### getCanonicalID

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getCanonicalID(id: String!): String!
```

**\[icu\]** Returns the canonical system time zone ID or the normalized custom time zone ID for the given time zone ID.

| Parameters ||
|---|---|
| `id` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The input time zone ID to be canonicalized. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The canonical system time zone ID or the custom time zone ID in normalized format for the given time zone ID. When the given time zone ID is neither a known system time zone ID nor a valid custom time zone ID, null is returned. |

### getCanonicalID

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getCanonicalID(
    id: String!, 
    isSystemID: BooleanArray!
): String!
```

**\[icu\]** Returns the canonical system time zone ID or the normalized custom time zone ID for the given time zone ID.

| Parameters ||
|---|---|
| `id` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The input time zone ID to be canonicalized. |
| `isSystemID` | [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)!: When non-null boolean array is specified and the given ID is a known system time zone ID, true is set to `isSystemID[0]` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The canonical system time zone ID or the custom time zone ID in normalized format for the given time zone ID. When the given time zone ID is neither a known system time zone ID nor a valid custom time zone ID, null is returned. |

### getDSTSavings

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDSTSavings(): Int
```

Returns the amount of time to be added to local standard time to get local wall clock time.

The default implementation always returns 3600000 milliseconds (i.e., one hour) if this time zone observes Daylight Saving Time. Otherwise, 0 (zero) is returned.

If an underlying TimeZone implementation subclass supports historical Daylight Saving Time changes, this method returns the known latest daylight saving value.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the amount of saving time in milliseconds |

### getDefault

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getDefault(): TimeZone!
```

Gets the default `TimeZone` for this host. The source of the default `TimeZone` may vary with implementation.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/util/TimeZone#!` | a default `TimeZone`. |

### getDisplayName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDisplayName(): String!
```

Returns a name of this time zone suitable for presentation to the user in the default `DISPLAY` locale. This method returns the long generic name. If the display name is not available for the locale, a fallback based on the country, city, or time zone id will be used.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the human-readable name of this time zone in the default locale. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Category`

### getDisplayName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDisplayName(locale: ULocale!): String!
```

Returns a name of this time zone suitable for presentation to the user in the specified locale. This method returns the long name, not including daylight savings. If the display name is not available for the locale, a fallback based on the country, city, or time zone id will be used.

| Parameters ||
|---|---|
| `locale` | [ULocale](ULocale.md)!: the ulocale in which to supply the display name. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the human-readable name of this time zone in the given locale or in the default ulocale if the given ulocale is not recognized. |

### getDisplayName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDisplayName(
    daylight: Boolean, 
    style: Int
): String!
```

Returns a name of this time zone suitable for presentation to the user in the default `DISPLAY` locale. If the display name is not available for the locale, then this method returns a string in the localized GMT offset format such as `GMT[+-]HH:mm`.

| Parameters ||
|---|---|
| `daylight` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): if true, return the daylight savings name. |
| `style` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the output style of the display name. Valid styles are `SHORT`, `LONG`, `SHORT_GENERIC`, `LONG_GENERIC`, `SHORT_GMT`, `LONG_GMT`, `SHORT_COMMONLY_USED` or `GENERIC_LOCATION`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the human-readable name of this time zone in the default locale. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Category`

### getDisplayName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDisplayName(
    daylight: Boolean, 
    style: Int, 
    locale: ULocale!
): String!
```

Returns a name of this time zone suitable for presentation to the user in the specified locale. If the display name is not available for the locale, then this method returns a string in the localized GMT offset format such as `GMT[+-]HH:mm`.

| Parameters ||
|---|---|
| `daylight` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): if true, return the daylight savings name. |
| `style` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the output style of the display name. Valid styles are `SHORT`, `LONG`, `SHORT_GENERIC`, `LONG_GENERIC`, `SHORT_GMT`, `LONG_GMT`, `SHORT_COMMONLY_USED` or `GENERIC_LOCATION`. |
| `locale` | [ULocale](ULocale.md)!: the locale in which to supply the display name. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the human-readable name of this time zone in the given locale or in the default locale if the given locale is not recognized. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | style is invalid. |

### getDisplayName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDisplayName(
    daylight: Boolean, 
    style: Int, 
    locale: Locale!
): String!
```

Returns a name of this time zone suitable for presentation to the user in the specified locale. If the display name is not available for the locale, then this method returns a string in the localized GMT offset format such as `GMT[+-]HH:mm`.

| Parameters ||
|---|---|
| `daylight` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): if true, return the daylight savings name. |
| `style` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the output style of the display name. Valid styles are `SHORT`, `LONG`, `SHORT_GENERIC`, `LONG_GENERIC`, `SHORT_GMT`, `LONG_GMT`, `SHORT_COMMONLY_USED` or `GENERIC_LOCATION`. |
| `locale` | [Locale](../java.util/Locale.md)!: the locale in which to supply the display name. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the human-readable name of this time zone in the given locale or in the default locale if the given locale is not recognized. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | style is invalid. |

### getDisplayName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDisplayName(locale: Locale!): String!
```

Returns a name of this time zone suitable for presentation to the user in the specified locale. This method returns the long generic name. If the display name is not available for the locale, a fallback based on the country, city, or time zone id will be used.

| Parameters ||
|---|---|
| `locale` | [Locale](../java.util/Locale.md)!: the locale in which to supply the display name. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the human-readable name of this time zone in the given locale or in the default locale if the given locale is not recognized. |

### getEquivalentID

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getEquivalentID(
    id: String!, 
    index: Int
): String!
```

Returns an ID in the equivalency group that includes the given ID. An equivalency group contains zones that have the same GMT offset and rules.

The given index must be in the range 0..n-1, where n is the value returned by `countEquivalentIDs(id)`. For some value of 'index', the returned value will be equal to the given id. If the given id is not a valid system time zone, or if 'index' is out of range, then returns an empty string.

| Parameters ||
|---|---|
| `id` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a system time zone ID |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a value from 0 to n-1, where n is the value returned by `countEquivalentIDs(id)` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the ID of the index-th zone in the equivalency group containing 'id', or an empty string if 'id' is not a valid system ID or 'index' is out of range |

**See Also**

- countEquivalentIDs

### getFrozenTimeZone

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getFrozenTimeZone(ID: String!): TimeZone!
```

Gets the `TimeZone` for the given ID. The instance of `TimeZone` returned by this method is immutable. Any methods mutate the instance(setID, setRawOffset) will throw `UnsupportedOperationException` upon its invocation.

| Parameters ||
|---|---|
| `ID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the ID for a `TimeZone`, such as "America/Los_Angeles", or a custom ID such as "GMT-8:00". Note that the support of abbreviations, such as "PST", is for JDK 1.1.x compatibility only and full names should be used. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/util/TimeZone#!` | the specified `TimeZone`, or the UNKNOWN_ZONE if the given ID cannot be understood. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/TimeZone#UNKNOWN_ZONE:android.icu.util.TimeZone`

### getID

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getID(): String!
```

Gets the ID of this time zone.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the ID of this time zone. |

### getIDForWindowsID

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getIDForWindowsID(
    winid: String!, 
    region: String!
): String!
```

**\[icu\]** Converts a Windows time zone ID to an equivalent system time zone ID for a region. For example, system time zone ID "America/Los_Angeles" is returned for input Windows ID "Pacific Standard Time" and region "US" (or `null`), "America/Vancouver" is returned for the same Windows ID "Pacific Standard Time" and region "CA".

Not all Windows time zones can be mapped to system time zones. When the input Windows time zone ID is unknown or unmappable to a system time zone, then this method returns `null`.

This implementation utilizes [Zone-Tzid mapping data](http://unicode.org/cldr/charts/supplemental/zone_tzid.html). The mapping data is updated time to time. To get the latest changes, please read the ICU user guide section [Updating the Time Zone Data](https://unicode-org.github.io/icu/userguide/datetime/timezone#updating-the-time-zone-data).

| Parameters ||
|---|---|
| `winid` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: A Windows time zone ID |
| `region` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: A region code, or `null` if no regional preference. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | A system time zone ID mapped from the input Windows time zone ID, or `null` when the input ID is unknown or unmappable. |

**See Also**

- getWindowsID

### getIanaID

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getIanaID(id: String!): String!
```

Returns the preferred time zone ID in the IANA database for the given time zone ID. There are two types of preferred IDs. The first type is the one defined in zone.tab file, such as "America/Los_Angeles". The second types is the one defined for zones not associated with a specific region, but not defined with "Link" syntax, such as "Etc/GMT+10".

Note: For most of system time zone IDs, this method returns an ID same as getCanonicalID. getCanonicalID is based on canonical time zone IDs defined in Unicode CLDR. These canonical time zone IDs in CLDR were based on very old version of the time zone database. In the IANA time zone database, some IDs were updated since then. This API returns a newer time zone ID. For example, CLDR defines "Asia/Calcutta" as the canonical time zone ID. This method returns "Asia/Kolkata" instead.

"Etc/Unknown" is a special time zone ID defined by CLDR. There are no corresponding zones in the IANA time zone database. when the input is "Etc/Unknown", this method returns "Etc/Unknown", but it really means no mappings available. Caller of this method should interpret "Etc/Unknown" as an error.

| Parameters ||
|---|---|
| `id` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The input time zone ID. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The preferred time zone ID in the IANA time zone database, or `https://developer.android.com/reference/kotlin/android/icu/util/TimeZone#UNKNOWN_ZONE_ID:kotlin.String` if the input ID is not a system ID. |

**See Also**

- getCanonicalID

### getOffset

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getOffset(
    era: Int, 
    year: Int, 
    month: Int, 
    day: Int, 
    dayOfWeek: Int, 
    milliseconds: Int
): Int
```

Gets the time zone offset, for current date, modified in case of daylight savings. This is the offset to add *to* UTC to get local time.

| Parameters ||
|---|---|
| `era` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the era of the given date. |
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the year in the given date. |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the month in the given date. Month is 0-based. e.g., 0 for January. |
| --- | --- |
| `day` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the day-in-month of the given date. |
| `dayOfWeek` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the day-of-week of the given date. |
| `milliseconds` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the millis in day in *standard* local time. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the offset to add *to* GMT to get local time. |

### getOffset

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOffset(date: Long): Int
```

Returns the offset of this time zone from UTC at the specified date. If Daylight Saving Time is in effect at the specified date, the offset value is adjusted with the amount of daylight saving.

| Parameters ||
|---|---|
| `date` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the date represented in milliseconds since January 1, 1970 00:00:00 GMT |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the amount of time in milliseconds to add to UTC to get local time. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#ZONE_OFFSET:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DST_OFFSET:kotlin.Int`
- getOffset

### getOffset

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOffset(
    date: Long, 
    local: Boolean, 
    offsets: IntArray!
): Unit
```

Returns the time zone raw and GMT offset for the given moment in time. Upon return, local-millis = GMT-millis + rawOffset + dstOffset. All computations are performed in the proleptic Gregorian calendar. The default implementation in the TimeZone class delegates to the 8-argument getOffset().

| Parameters ||
|---|---|
| `date` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): moment in time for which to return offsets, in units of milliseconds from January 1, 1970 0:00 GMT, either GMT time or local wall time, depending on `local`. |
| `local` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): if true, `date` is local wall time; otherwise it is in GMT time. |
| `offsets` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: output parameter to receive the raw offset, that is, the offset not including DST adjustments, in offsets\[0\], and the DST offset, that is, the offset to be added to `rawOffset` to obtain the total offset between local and GMT time, in offsets\[1\]. If DST is not in effect, the DST offset is zero; otherwise it is a positive value, typically one hour. |
| --- | --- |

### getRawOffset

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getRawOffset(): Int
```

Gets unmodified offset, NOT modified in case of daylight savings. This is the offset to add *to* UTC to get local time.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the unmodified offset to add *to* UTC to get local time. |

### getRegion

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getRegion(id: String!): String!
```

**\[icu\]** Returns the region code associated with the given system time zone ID. The region code is either ISO 3166 2-letter country code or UN M.49 3-digit area code. When the time zone is not associated with a specific location, for example - "Etc/UTC", "EST5EDT", then this method returns "001" (UN M.49 area code for World).

| Parameters ||
|---|---|
| `id` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the system time zone ID. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the region code associated with the given system time zone ID. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `id` is not a known system ID. |

**See Also**

- getAvailableIDs

### getTZDataVersion

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getTZDataVersion(): String!
```

**\[icu\]** Returns the time zone data version currently used by ICU.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the version string, such as "2007f" |

| Exceptions ||
|---|---|
| `java.util.MissingResourceException` | if ICU time zone resource bundle is missing or the version information is not available. |

### getTimeZone

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getTimeZone(ID: String!): TimeZone!
```

Gets the `TimeZone` for the given ID.

| Parameters ||
|---|---|
| `ID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the ID for a `TimeZone`, such as "America/Los_Angeles", or a custom ID such as "GMT-8:00". Note that the support of abbreviations, such as "PST", is for JDK 1.1.x compatibility only and full names should be used. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/util/TimeZone#!` | the specified `TimeZone`, or a mutable clone of the UNKNOWN_ZONE if the given ID cannot be understood or if the given ID is "Etc/Unknown". |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/TimeZone#UNKNOWN_ZONE:android.icu.util.TimeZone`

### getTimeZone

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getTimeZone(
    ID: String!, 
    type: Int
): TimeZone!
```

Gets the `TimeZone` for the given ID and the timezone type.

| Parameters ||
|---|---|
| `ID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the ID for a `TimeZone`, such as "America/Los_Angeles", or a custom ID such as "GMT-8:00". Note that the support of abbreviations, such as "PST", is for JDK 1.1.x compatibility only and full names should be used. |
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Time zone type, either `TIMEZONE_ICU` or `TIMEZONE_JDK`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/util/TimeZone#!` | the specified `TimeZone`, or a mutable clone of the UNKNOWN_ZONE if the given ID cannot be understood or if the given ID is "Etc/Unknown". |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/TimeZone#UNKNOWN_ZONE:android.icu.util.TimeZone`

### getWindowsID

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getWindowsID(id: String!): String!
```

**\[icu\]** Converts a system time zone ID to an equivalent Windows time zone ID. For example, Windows time zone ID "Pacific Standard Time" is returned for input "America/Los_Angeles".

There are system time zones that cannot be mapped to Windows zones. When the input system time zone ID is unknown or unmappable to a Windows time zone, then this method returns `null`.

This implementation utilizes [Zone-Tzid mapping data](http://unicode.org/cldr/charts/supplemental/zone_tzid.html). The mapping data is updated time to time. To get the latest changes, please read the ICU user guide section [Updating the Time Zone Data](https://unicode-org.github.io/icu/userguide/datetime/timezone#updating-the-time-zone-data).

| Parameters ||
|---|---|
| `id` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: A system time zone ID |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | A Windows time zone ID mapped from the input system time zone ID, or `null` when the input ID is unknown or unmappable. |

**See Also**

- getIDForWindowsID

### hasSameRules

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasSameRules(other: TimeZone!): Boolean
```

Returns true if this zone has the same rule and offset as another zone. That is, if this zone differs only in ID, if at all. Returns false if the other zone is null.

| Parameters ||
|---|---|
| `other` | [TimeZone](TimeZone.md)!: the `TimeZone` object to be compared with |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the other zone is not null and is the same as this one, with the possible exception of the ID |

### hashCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hashCode(): Int
```

Overrides hashCode.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### inDaylightTime

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun inDaylightTime(date: Date!): Boolean
```

Queries if the given date is in daylight savings time in this time zone.

| Parameters ||
|---|---|
| `date` | [Date](../java.util/Date.md)!: the given Date. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the given date is in daylight savings time, false, otherwise. |

### isFrozen

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isFrozen(): Boolean
```

Determines whether the object has been frozen or not.

### observesDaylightTime

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun observesDaylightTime(): Boolean
```

Queries if this time zone is in daylight saving time or will observe daylight saving time at any future time.

The default implementation in this class returns `true` if useDaylightTime or inDaylightTime returns `true`.

**Note:** This method was added for `https://developer.android.com/reference/kotlin/java/util/TimeZone.html#` compatibility support. The useDaylightTime method only checks the last known rule(s), therefore it may return false even the zone observes daylight saving time currently. `https://developer.android.com/reference/kotlin/java/util/TimeZone.html#` added `observesDaylightTime()` to resolve the issue. In ICU, useDaylightTime works differently. The ICU implementation checks if the zone uses daylight saving time in the current calendar year. Therefore, it will never return `false` if daylight saving time is currently used.

ICU's TimeZone subclass implementations override this method to support the same behavior with observesDaylightTime. Unlike useDaylightTime, the implementation does not take past daylight saving time into account, so that this method may return `false` even when useDaylightTime returns `true`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this time zone is in daylight saving time or will observe daylight saving time at any future time. |

**See Also**

- useDaylightTime

### setID

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setID(ID: String!): Unit
```

Sets the time zone ID. This does not change any other data in the time zone object.

| Parameters ||
|---|---|
| `ID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the new time zone ID. |

### setRawOffset

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setRawOffset(offsetMillis: Int): Unit
```

Sets the base time zone offset to GMT. This is the offset to add *to* UTC to get local time.

| Parameters ||
|---|---|
| `offsetMillis` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the given base time zone offset to GMT. |

### useDaylightTime

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun useDaylightTime(): Boolean
```

Queries if this time zone uses daylight savings time.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this time zone uses daylight savings time, false, otherwise. **Note:** The default implementation of ICU TimeZone uses the tz database, which supports historic rule changes, for system time zones. With the implementation, there are time zones that used daylight savings time in the past, but no longer used currently. For example, Asia/Tokyo has never used daylight savings time since 1951. Most clients would expect that this method to return `false` for such case. The default implementation of this method returns `true` when the time zone uses daylight savings time in the current (Gregorian) calendar year. |

## Properties

### GMT_ZONE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GMT_ZONE: TimeZone!
```

**\[icu\]** The immutable GMT (=UTC) time zone. Its ID is "Etc/GMT".

### UNKNOWN_ZONE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNKNOWN_ZONE: TimeZone!
```

**\[icu\]** The immutable (frozen) "unknown" time zone. It behaves like the GMT/UTC time zone but has the UNKNOWN_ZONE_ID = "Etc/Unknown". getTimeZone returns a mutable clone of this time zone if the input ID is not recognized.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/TimeZone#UNKNOWN_ZONE_ID:kotlin.String`
- getTimeZone
