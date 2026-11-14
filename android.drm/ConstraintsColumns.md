# DrmStore.ConstraintsColumns

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ConstraintsColumns

Kotlin| [Java](https://developer.android.com/reference/android/drm/DrmStore.ConstraintsColumns "View this page in Java") 
| --- | --- |

```
interface ConstraintsColumns
```

| [android.drm.DrmStore.ConstraintsColumns](https://developer.android.com/reference/kotlin/android/drm/DrmStore.ConstraintsColumns#) |

| **This interface was deprecated in API level 30.**
|
| Deprecated in Java.

Interface definition for the columns that represent DRM constraints. android.drm.DrmManagerClient#getConstraints can be called by an application to find out the contraints on the [actions](https://developer.android.com/reference/kotlin/android/drm/DrmStore.Action) that can be performed on right-protected content. The constants defined in this interface represent three most common types of constraints: count-based, date-based, and duration-based. Two or more constraints can be used at the same time to represent more sophisticated constraints. In addition, user-defined constraint, [extended metadata](https://developer.android.com/reference/kotlin/android/drm/DrmStore.ConstraintsColumns#EXTENDED_METADATA:kotlin.String), can be used if these three types of constraints are not sufficient.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTENDED_METADATA](https://developer.android.com/reference/kotlin/android/drm/DrmStore.ConstraintsColumns#EXTENDED_METADATA:kotlin.String) This is a user-defined constraint. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LICENSE_AVAILABLE_TIME](https://developer.android.com/reference/kotlin/android/drm/DrmStore.ConstraintsColumns#LICENSE_AVAILABLE_TIME:kotlin.String) This is a duration-based constaint. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LICENSE_EXPIRY_TIME](https://developer.android.com/reference/kotlin/android/drm/DrmStore.ConstraintsColumns#LICENSE_EXPIRY_TIME:kotlin.String) This is a date-based constaint. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LICENSE_START_TIME](https://developer.android.com/reference/kotlin/android/drm/DrmStore.ConstraintsColumns#LICENSE_START_TIME:kotlin.String) This is a date-based constraint. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MAX_REPEAT_COUNT](https://developer.android.com/reference/kotlin/android/drm/DrmStore.ConstraintsColumns#MAX_REPEAT_COUNT:kotlin.String) This is a count-based constraint. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [REMAINING_REPEAT_COUNT](https://developer.android.com/reference/kotlin/android/drm/DrmStore.ConstraintsColumns#REMAINING_REPEAT_COUNT:kotlin.String) This is a count-based constraint. |
| --- | --- |

## Constants

### EXTENDED_METADATA

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTENDED_METADATA: String
```

**Deprecated:** *Deprecated in Java.*

This is a user-defined constraint. It represents the additional constraint using extended metadata.

Type: TEXT 

 Value: "extended_metadata"

### LICENSE_AVAILABLE_TIME

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LICENSE_AVAILABLE_TIME: String
```

**Deprecated:** *Deprecated in Java.*

This is a duration-based constaint. It represents the available time left before the license expires.

Type: TEXT 

 Value: "license_available_time"

### LICENSE_EXPIRY_TIME

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LICENSE_EXPIRY_TIME: String
```

**Deprecated:** *Deprecated in Java.*

This is a date-based constaint. It represents the time after which an [action](https://developer.android.com/reference/kotlin/android/drm/DrmStore.Action) can not be performed on the rights-protected content.

Type: TEXT 

 Value: "license_expiry_time"

### LICENSE_START_TIME

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LICENSE_START_TIME: String
```

**Deprecated:** *Deprecated in Java.*

This is a date-based constraint. It represents the time before which an [action](https://developer.android.com/reference/kotlin/android/drm/DrmStore.Action) can be performed on the rights-protected content.

Type: TEXT 

 Value: "license_start_time"

### MAX_REPEAT_COUNT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAX_REPEAT_COUNT: String
```

**Deprecated:** *Deprecated in Java.*

This is a count-based constraint. It represents the maximum repeat count that can be performed on an [action](https://developer.android.com/reference/kotlin/android/drm/DrmStore.Action).

Type: INTEGER 

 Value: "max_repeat_count"

### REMAINING_REPEAT_COUNT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REMAINING_REPEAT_COUNT: String
```

**Deprecated:** *Deprecated in Java.*

This is a count-based constraint. It represents the remaining repeat count that can be performed on an [action](https://developer.android.com/reference/kotlin/android/drm/DrmStore.Action).

Type: INTEGER 

 Value: "remaining_repeat_count"
