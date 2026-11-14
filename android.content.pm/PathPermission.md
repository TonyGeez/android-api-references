# PathPermission

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PathPermission

Kotlin| [Java](PathPermission.md) 
| --- | --- |

```
open class PathPermission : PatternMatcher
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.os.PatternMatcher](../android.os/PatternMatcher.md) ||
| | ↳ | [android.content.pm.PathPermission](PathPermission.md) |

Description of permissions needed to access a particular path in a [ProviderInfo](ProviderInfo.md).

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||
| From class [PatternMatcher](../android.os/PatternMatcher.md) |----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PATTERN_ADVANCED_GLOB](../android.os/PatternMatcher.md) <br /> Pattern type: the given pattern is interpreted with a regular expression-like syntax for matching against the string it is tested against. Supported tokens include dot (`.`) and sets (`[...]`) with full support for character ranges and the not (`^`) modifier. Supported modifiers include star (`*`) for zero-or-more, plus (`+`) for one-or-more and full range (`{...}`) support. This is a simple evaluation implementation in which matching is done against the pattern in real time with no backtracking support. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PATTERN_LITERAL](../android.os/PatternMatcher.md) <br /> Pattern type: the given pattern must exactly match the string it is tested against. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PATTERN_PREFIX](../android.os/PatternMatcher.md) <br /> Pattern type: the given pattern must match the beginning of the string it is tested against. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PATTERN_SIMPLE_GLOB](../android.os/PatternMatcher.md) <br /> Pattern type: the given pattern is interpreted with a simple glob syntax for matching against the string it is tested against. In this syntax, you can use the '\*' character to match against zero or more occurrences of the character immediately before. If the character before it is '.' it will match any character. The character '\\' can be used as an escape. This essentially provides only the '\*' wildcard part of a normal regexp. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PATTERN_SUFFIX](../android.os/PatternMatcher.md) <br /> Pattern type: the given pattern must match the end of the string it is tested against. <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PathPermission](PathPermission.md))`(`src:` ` [Parcel](../android.os/Parcel.md)!`)` <br /> |
| [PathPermission](PathPermission.md))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `readPermission:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `writePermission:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getReadPermission](PathPermission.md))`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getWritePermission](PathPermission.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](PathPermission.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [PatternMatcher](../android.os/PatternMatcher.md) |------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android.os/PatternMatcher.md))`()` <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPath](../android.os/PatternMatcher.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](../android.os/PatternMatcher.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [match](../android.os/PatternMatcher.md))`(`str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android.os/PatternMatcher.md))`()` <br /> | ||

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [PathPermission](PathPermission.md)!\> | [CREATOR](PathPermission.md) <br /> |

## Public constructors

### PathPermission

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PathPermission(src: Parcel!)
```  

### PathPermission

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PathPermission(
    pattern: String!, 
    type: Int, 
    readPermission: String!, 
    writePermission: String!)
```

## Public methods

### getReadPermission

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getReadPermission(): String!
```  

### getWritePermission

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWritePermission(): String!
```  

### writeToParcel

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android.os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<PathPermission!>
```
