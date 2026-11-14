Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VersionInfo

```
class VersionInfo : Comparable<VersionInfo!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.util.VersionInfo](../android/icu/util/VersionInfo.md) |

Class to store version numbers of the form major.minor.milli.micro.

## Summary

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#compareTo(android.icu.util.VersionInfo)(other: https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#!)` Compares other with this VersionInfo. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Checks if this version information is equals to the argument version |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#getInstance(kotlin.Int)(major: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns an instance of VersionInfo with the argument version. |
| --- | --- |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#getInstance(kotlin.Int,%20kotlin.Int)(major: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, minor: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns an instance of VersionInfo with the argument version. |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#getInstance(kotlin.Int,%20kotlin.Int,%20kotlin.Int)(major: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, minor: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, milli: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns an instance of VersionInfo with the argument version. |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#getInstance(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(major: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, minor: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, milli: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, micro: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns an instance of VersionInfo with the argument version. |
| --- | --- |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#getInstance(kotlin.String)(version: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns an instance of VersionInfo with the argument version. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#getMajor()()` Returns the major version number |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#getMicro()()` Returns the micro version number |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#getMilli()()` Returns the milli version number |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#getMinor()()` Returns the minor version number |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#hashCode()()` Returns the hash code value for this set. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#toString()()` Returns the String representative of VersionInfo in the format of "major. |

| Properties ||
|---|---|
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#ICU_VERSION:android.icu.util.VersionInfo` ICU4J current release version |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#UCOL_BUILDER_VERSION:android.icu.util.VersionInfo` Collation builder code version. |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#UCOL_RUNTIME_VERSION:android.icu.util.VersionInfo` Collation runtime version (sort key generator, string comparisons). |
| --- | --- |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#UNICODE_10_0:android.icu.util.VersionInfo` Unicode 10. |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#UNICODE_11_0:android.icu.util.VersionInfo` Unicode 11. |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#UNICODE_12_0:android.icu.util.VersionInfo` Unicode 12. |
| --- | --- |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#UNICODE_12_1:android.icu.util.VersionInfo` Unicode 12. |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#UNICODE_13_0:android.icu.util.VersionInfo` Unicode 13. |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#UNICODE_14_0:android.icu.util.VersionInfo` Unicode 14. |
| --- | --- |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#UNICODE_15_0:android.icu.util.VersionInfo` Unicode 15. |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#UNICODE_15_1:android.icu.util.VersionInfo` Unicode 15. |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#UNICODE_16_0:android.icu.util.VersionInfo` Unicode 16. |
| --- | --- |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#UNICODE_17_0:android.icu.util.VersionInfo` Unicode 17. |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#UNICODE_1_0:android.icu.util.VersionInfo` Unicode 1. |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#UNICODE_1_0_1:android.icu.util.VersionInfo` Unicode 1. |
| --- | --- |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#UNICODE_1_1_0:android.icu.util.VersionInfo` Unicode 1. |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#UNICODE_1_1_5:android.icu.util.VersionInfo` Unicode 1. |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#UNICODE_2_0:android.icu.util.VersionInfo` Unicode 2. |
| --- | --- |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#UNICODE_2_1_2:android.icu.util.VersionInfo` Unicode 2. |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#UNICODE_2_1_5:android.icu.util.VersionInfo` Unicode 2. |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#UNICODE_2_1_8:android.icu.util.VersionInfo` Unicode 2. |
| --- | --- |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#UNICODE_2_1_9:android.icu.util.VersionInfo` Unicode 2. |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#UNICODE_3_0:android.icu.util.VersionInfo` Unicode 3. |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#UNICODE_3_0_1:android.icu.util.VersionInfo` Unicode 3. |
| --- | --- |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#UNICODE_3_1_0:android.icu.util.VersionInfo` Unicode 3. |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#UNICODE_3_1_1:android.icu.util.VersionInfo` Unicode 3. |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#UNICODE_3_2:android.icu.util.VersionInfo` Unicode 3. |
| --- | --- |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#UNICODE_4_0:android.icu.util.VersionInfo` Unicode 4. |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#UNICODE_4_0_1:android.icu.util.VersionInfo` Unicode 4. |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#UNICODE_4_1:android.icu.util.VersionInfo` Unicode 4. |
| --- | --- |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#UNICODE_5_0:android.icu.util.VersionInfo` Unicode 5. |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#UNICODE_5_1:android.icu.util.VersionInfo` Unicode 5. |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#UNICODE_5_2:android.icu.util.VersionInfo` Unicode 5. |
| --- | --- |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#UNICODE_6_0:android.icu.util.VersionInfo` Unicode 6. |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#UNICODE_6_1:android.icu.util.VersionInfo` Unicode 6. |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#UNICODE_6_2:android.icu.util.VersionInfo` Unicode 6. |
| --- | --- |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#UNICODE_6_3:android.icu.util.VersionInfo` Unicode 6. |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#UNICODE_7_0:android.icu.util.VersionInfo` Unicode 7. |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#UNICODE_8_0:android.icu.util.VersionInfo` Unicode 8. |
| --- | --- |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#UNICODE_9_0:android.icu.util.VersionInfo` Unicode 9. |

## Public methods

### compareTo

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun compareTo(other: VersionInfo!): Int
```

Compares other with this VersionInfo.

| Parameters ||
|---|---|
| `o` | the object to be compared. |
| `other` | [VersionInfo](../android/icu/util/VersionInfo.md)!: VersionInfo to be compared |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | 0 if the argument is a VersionInfo object that has version information equals to this object. Less than 0 if the argument is a VersionInfo object that has version information greater than this object. Greater than 0 if the argument is a VersionInfo object that has version information less than this object. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |
| `java.lang.NullPointerException` | if the specified object is null |

### equals

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Checks if this version information is equals to the argument version

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |
| `other` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: object to be compared |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if other is equals to this object's version information, false otherwise |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getInstance(major: Int): VersionInfo!
```

Returns an instance of VersionInfo with the argument version. Equivalent to getInstance(major, 0, 0, 0).

| Parameters ||
|---|---|
| `major` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): major version, non-negative number \<= 255. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | when either arguments are negative or \> 255 |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getInstance(
    major: Int, 
    minor: Int
): VersionInfo!
```

Returns an instance of VersionInfo with the argument version. Equivalent to getInstance(major, minor, 0, 0).

| Parameters ||
|---|---|
| `major` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): major version, non-negative number \<= 255. |
| `minor` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): minor version, non-negative number \<= 255. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | when either arguments are negative or \> 255 |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getInstance(
    major: Int, 
    minor: Int, 
    milli: Int
): VersionInfo!
```

Returns an instance of VersionInfo with the argument version. Equivalent to getInstance(major, minor, milli, 0).

| Parameters ||
|---|---|
| `major` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): major version, non-negative number \<= 255. |
| `minor` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): minor version, non-negative number \<= 255. |
| `milli` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): milli version, non-negative number \<= 255. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | when either arguments are negative or \> 255 |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getInstance(
    major: Int, 
    minor: Int, 
    milli: Int, 
    micro: Int
): VersionInfo!
```

Returns an instance of VersionInfo with the argument version.

| Parameters ||
|---|---|
| `major` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): major version, non-negative number \<= 255. |
| `minor` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): minor version, non-negative number \<= 255. |
| `milli` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): milli version, non-negative number \<= 255. |
| --- | --- |
| `micro` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): micro version, non-negative number \<= 255. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | when either arguments are negative or \> 255 |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getInstance(version: String!): VersionInfo!
```

Returns an instance of VersionInfo with the argument version.

| Parameters ||
|---|---|
| `version` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: version String in the format of "major.minor.milli.micro" or "major.minor.milli" or "major.minor" or "major", where major, minor, milli, micro are non-negative numbers \<= 255. If the trailing version numbers are not specified they are taken as 0s. E.g. Version "3.1" is equivalent to "3.1.0.0". |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo#!` | an instance of VersionInfo with the argument version. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | when the argument version is not in the right format |

### getMajor

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMajor(): Int
```

Returns the major version number

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the major version number |

### getMicro

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMicro(): Int
```

Returns the micro version number

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the micro version number |

### getMilli

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMilli(): Int
```

Returns the milli version number

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the milli version number |

### getMinor

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMinor(): Int
```

Returns the minor version number

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the minor version number |

### hashCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns the hash code value for this set.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the hash code value for this set. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Object.html#hashCode()`

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns the String representative of VersionInfo in the format of "major.minor.milli.micro"

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | String representative of VersionInfo |

## Properties

### ICU_VERSION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ICU_VERSION: VersionInfo!
```

ICU4J current release version

### UCOL_BUILDER_VERSION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UCOL_BUILDER_VERSION: VersionInfo!
```

Collation builder code version. When this is different, the same tailoring might result in assigning different collation elements to code points. This value may change in subsequent releases of ICU.

### UCOL_RUNTIME_VERSION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UCOL_RUNTIME_VERSION: VersionInfo!
```

Collation runtime version (sort key generator, string comparisons). If the version is different, sort keys for the same string could be different. This value may change in subsequent releases of ICU.

### UNICODE_10_0

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNICODE_10_0: VersionInfo!
```

Unicode 10.0 version

### UNICODE_11_0

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNICODE_11_0: VersionInfo!
```

Unicode 11.0 version

### UNICODE_12_0

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNICODE_12_0: VersionInfo!
```

Unicode 12.0 version

### UNICODE_12_1

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNICODE_12_1: VersionInfo!
```

Unicode 12.1 version

### UNICODE_13_0

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNICODE_13_0: VersionInfo!
```

Unicode 13.0 version

### UNICODE_14_0

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNICODE_14_0: VersionInfo!
```

Unicode 14.0 version

### UNICODE_15_0

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNICODE_15_0: VersionInfo!
```

Unicode 15.0 version

### UNICODE_15_1

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNICODE_15_1: VersionInfo!
```

Unicode 15.1 version

### UNICODE_16_0

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNICODE_16_0: VersionInfo!
```

Unicode 16.0 version

### UNICODE_17_0

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNICODE_17_0: VersionInfo!
```

Unicode 17.0 version

### UNICODE_1_0

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNICODE_1_0: VersionInfo!
```

Unicode 1.0 version

### UNICODE_1_0_1

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNICODE_1_0_1: VersionInfo!
```

Unicode 1.0.1 version

### UNICODE_1_1_0

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNICODE_1_1_0: VersionInfo!
```

Unicode 1.1.0 version

### UNICODE_1_1_5

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNICODE_1_1_5: VersionInfo!
```

Unicode 1.1.5 version

### UNICODE_2_0

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNICODE_2_0: VersionInfo!
```

Unicode 2.0 version

### UNICODE_2_1_2

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNICODE_2_1_2: VersionInfo!
```

Unicode 2.1.2 version

### UNICODE_2_1_5

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNICODE_2_1_5: VersionInfo!
```

Unicode 2.1.5 version

### UNICODE_2_1_8

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNICODE_2_1_8: VersionInfo!
```

Unicode 2.1.8 version

### UNICODE_2_1_9

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNICODE_2_1_9: VersionInfo!
```

Unicode 2.1.9 version

### UNICODE_3_0

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNICODE_3_0: VersionInfo!
```

Unicode 3.0 version

### UNICODE_3_0_1

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNICODE_3_0_1: VersionInfo!
```

Unicode 3.0.1 version

### UNICODE_3_1_0

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNICODE_3_1_0: VersionInfo!
```

Unicode 3.1.0 version

### UNICODE_3_1_1

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNICODE_3_1_1: VersionInfo!
```

Unicode 3.1.1 version

### UNICODE_3_2

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNICODE_3_2: VersionInfo!
```

Unicode 3.2 version

### UNICODE_4_0

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNICODE_4_0: VersionInfo!
```

Unicode 4.0 version

### UNICODE_4_0_1

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNICODE_4_0_1: VersionInfo!
```

Unicode 4.0.1 version

### UNICODE_4_1

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNICODE_4_1: VersionInfo!
```

Unicode 4.1 version

### UNICODE_5_0

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNICODE_5_0: VersionInfo!
```

Unicode 5.0 version

### UNICODE_5_1

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNICODE_5_1: VersionInfo!
```

Unicode 5.1 version

### UNICODE_5_2

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNICODE_5_2: VersionInfo!
```

Unicode 5.2 version

### UNICODE_6_0

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNICODE_6_0: VersionInfo!
```

Unicode 6.0 version

### UNICODE_6_1

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNICODE_6_1: VersionInfo!
```

Unicode 6.1 version

### UNICODE_6_2

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNICODE_6_2: VersionInfo!
```

Unicode 6.2 version

### UNICODE_6_3

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNICODE_6_3: VersionInfo!
```

Unicode 6.3 version

### UNICODE_7_0

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNICODE_7_0: VersionInfo!
```

Unicode 7.0 version

### UNICODE_8_0

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNICODE_8_0: VersionInfo!
```

Unicode 8.0 version

### UNICODE_9_0

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNICODE_9_0: VersionInfo!
```

Unicode 9.0 version
