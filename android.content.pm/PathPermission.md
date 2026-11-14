# PathPermission

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PathPermission

Kotlin| [Java](https://developer.android.com/reference/android/content/pm/PathPermission "View this page in Java") 

```
open class PathPermission : PatternMatcher
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.os.PatternMatcher](https://developer.android.com/reference/kotlin/android/os/PatternMatcher.html#) ||
| | ↳ | [android.content.pm.PathPermission](https://developer.android.com/reference/kotlin/android/content/pm/PathPermission#) |

Description of permissions needed to access a particular path in a [ProviderInfo](https://developer.android.com/reference/kotlin/android/content/pm/ProviderInfo).

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||
| From class [PatternMatcher](https://developer.android.com/reference/kotlin/android/os/PatternMatcher.html#) |----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PATTERN_ADVANCED_GLOB](https://developer.android.com/reference/kotlin/android/os/PatternMatcher.html#PATTERN_ADVANCED_GLOB:kotlin.Int) <br /> Pattern type: the given pattern is interpreted with a regular expression-like syntax for matching against the string it is tested against. Supported tokens include dot (`.`) and sets (`[...]`) with full support for character ranges and the not (`^`) modifier. Supported modifiers include star (`*`) for zero-or-more, plus (`+`) for one-or-more and full range (`{...}`) support. This is a simple evaluation implementation in which matching is done against the pattern in real time with no backtracking support. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PATTERN_LITERAL](https://developer.android.com/reference/kotlin/android/os/PatternMatcher.html#PATTERN_LITERAL:kotlin.Int) <br /> Pattern type: the given pattern must exactly match the string it is tested against. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PATTERN_PREFIX](https://developer.android.com/reference/kotlin/android/os/PatternMatcher.html#PATTERN_PREFIX:kotlin.Int) <br /> Pattern type: the given pattern must match the beginning of the string it is tested against. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PATTERN_SIMPLE_GLOB](https://developer.android.com/reference/kotlin/android/os/PatternMatcher.html#PATTERN_SIMPLE_GLOB:kotlin.Int) <br /> Pattern type: the given pattern is interpreted with a simple glob syntax for matching against the string it is tested against. In this syntax, you can use the '\*' character to match against zero or more occurrences of the character immediately before. If the character before it is '.' it will match any character. The character '\\' can be used as an escape. This essentially provides only the '\*' wildcard part of a normal regexp. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PATTERN_SUFFIX](https://developer.android.com/reference/kotlin/android/os/PatternMatcher.html#PATTERN_SUFFIX:kotlin.Int) <br /> Pattern type: the given pattern must match the end of the string it is tested against. <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PathPermission](https://developer.android.com/reference/kotlin/android/content/pm/PathPermission#PathPermission(android.os.Parcel))`(`src:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)!`)` <br /> |
| [PathPermission](https://developer.android.com/reference/kotlin/android/content/pm/PathPermission#PathPermission(kotlin.String,%20kotlin.Int,%20kotlin.String,%20kotlin.String))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `readPermission:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `writePermission:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getReadPermission](https://developer.android.com/reference/kotlin/android/content/pm/PathPermission#getReadPermission())`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getWritePermission](https://developer.android.com/reference/kotlin/android/content/pm/PathPermission#getWritePermission())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/content/pm/PathPermission#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Inherited functions ||
|---|---|
| From class [PatternMatcher](https://developer.android.com/reference/kotlin/android/os/PatternMatcher.html#) |------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/os/PatternMatcher.html#describeContents())`()` <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPath](https://developer.android.com/reference/kotlin/android/os/PatternMatcher.html#getPath())`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](https://developer.android.com/reference/kotlin/android/os/PatternMatcher.html#getType())`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [match](https://developer.android.com/reference/kotlin/android/os/PatternMatcher.html#match(kotlin.String))`(`str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/os/PatternMatcher.html#toString())`()` <br /> | ||

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [PathPermission](https://developer.android.com/reference/kotlin/android/content/pm/PathPermission#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/content/pm/PathPermission#CREATOR:android.os.Parcelable.Creator) <br /> |

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<PathPermission!>
```
