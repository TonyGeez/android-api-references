# AndroidCharacter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AndroidCharacter

Kotlin| [Java](AndroidCharacter.md) 
| --- | --- |

```
open class AndroidCharacter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.text.AndroidCharacter](AndroidCharacter.md) |

| **This class was deprecated in API level 26.**
|
| Use various methods from [android.icu.lang.UCharacter](../android.icu.lang/UCharacter.md), instead.

AndroidCharacter exposes some character properties that used to be not easily accessed from java.lang.Character, but are now available in ICU.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EAST_ASIAN_WIDTH_AMBIGUOUS](AndroidCharacter.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EAST_ASIAN_WIDTH_FULL_WIDTH](AndroidCharacter.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EAST_ASIAN_WIDTH_HALF_WIDTH](AndroidCharacter.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EAST_ASIAN_WIDTH_NARROW](AndroidCharacter.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EAST_ASIAN_WIDTH_NEUTRAL](AndroidCharacter.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EAST_ASIAN_WIDTH_WIDE](AndroidCharacter.md) <br /> |
| --- | --- |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------|---|
| [AndroidCharacter](AndroidCharacter.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getDirectionalities](AndroidCharacter.md))`(`src:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `dest:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Fill in the first`count`bytes of`dest`with the directionalities from the first`count`chars of`src`. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEastAsianWidth](AndroidCharacter.md))`(`input:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Calculate the East Asian Width of a character according to [Unicode TR#11](http://unicode.org/reports/tr11/). |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getEastAsianWidths](AndroidCharacter.md))`(`src:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dest:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Fill the first`count`bytes of`dest`with the East Asian Width from`count`chars of`src`starting at`start`. |
| --- | --- |
| openstatic [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getMirror](AndroidCharacter.md))`(`ch:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Return the right-to-left mirror (or the original char if none) of the specified char. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [mirror](AndroidCharacter.md))`(`text:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Replace the specified slice of`text`with the chars' right-to-left mirrors (if any), returning true if any replacements were made. |

## Constants

### EAST_ASIAN_WIDTH_AMBIGUOUS

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EAST_ASIAN_WIDTH_AMBIGUOUS: Int
```

**Deprecated:** *Deprecated in Java.* 

 Value: 1

### EAST_ASIAN_WIDTH_FULL_WIDTH

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EAST_ASIAN_WIDTH_FULL_WIDTH: Int
```

**Deprecated:** *Deprecated in Java.* 

 Value: 3

### EAST_ASIAN_WIDTH_HALF_WIDTH

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EAST_ASIAN_WIDTH_HALF_WIDTH: Int
```

**Deprecated:** *Deprecated in Java.* 

 Value: 2

### EAST_ASIAN_WIDTH_NARROW

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EAST_ASIAN_WIDTH_NARROW: Int
```

**Deprecated:** *Deprecated in Java.* 

 Value: 4

### EAST_ASIAN_WIDTH_NEUTRAL

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EAST_ASIAN_WIDTH_NEUTRAL: Int
```

**Deprecated:** *Deprecated in Java.* 

 Value: 0

### EAST_ASIAN_WIDTH_WIDE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EAST_ASIAN_WIDTH_WIDE: Int
```

**Deprecated:** *Deprecated in Java.* 

 Value: 5

## Public constructors

### AndroidCharacter

```
AndroidCharacter()
```

## Public methods

### getDirectionalities

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getDirectionalities(
    src: CharArray!, 
    dest: ByteArray!, 
    count: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Fill in the first`count`bytes of`dest`with the directionalities from the first`count`chars of`src`. This is just like Character.getDirectionality() except it is a batch operation. 

### getEastAsianWidth

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getEastAsianWidth(input: Char): Int
```

**Deprecated:** *Deprecated in Java.*

Calculate the East Asian Width of a character according to [Unicode TR#11](http://unicode.org/reports/tr11/). The return will be one of [EAST_ASIAN_WIDTH_NEUTRAL](AndroidCharacter.md), [EAST_ASIAN_WIDTH_AMBIGUOUS](AndroidCharacter.md), [EAST_ASIAN_WIDTH_HALF_WIDTH](AndroidCharacter.md), [EAST_ASIAN_WIDTH_FULL_WIDTH](AndroidCharacter.md), [EAST_ASIAN_WIDTH_NARROW](AndroidCharacter.md), or [EAST_ASIAN_WIDTH_WIDE](AndroidCharacter.md).

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------|
| `input` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):the character to measure |

| Return ||
|----------------------------------------------------------------------------|--------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the East Asian Width for input |

### getEastAsianWidths

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getEastAsianWidths(
    src: CharArray!, 
    start: Int, 
    count: Int, 
    dest: ByteArray!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Fill the first`count`bytes of`dest`with the East Asian Width from`count`chars of`src`starting at`start`. East Asian Width is calculated based on [Unicode TR#11](http://unicode.org/reports/tr11/). Each entry in`dest`will be one of [EAST_ASIAN_WIDTH_NEUTRAL](AndroidCharacter.md), [EAST_ASIAN_WIDTH_AMBIGUOUS](AndroidCharacter.md), [EAST_ASIAN_WIDTH_HALF_WIDTH](AndroidCharacter.md), [EAST_ASIAN_WIDTH_FULL_WIDTH](AndroidCharacter.md), [EAST_ASIAN_WIDTH_NARROW](AndroidCharacter.md), or [EAST_ASIAN_WIDTH_WIDE](AndroidCharacter.md).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| `src` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:character array of input to measure |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):first character in array to measure |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):maximum number of characters to measure |
| --- | --- |
| `dest` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:byte array of results for each character in src |

### getMirror

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getMirror(ch: Char): Char
```

**Deprecated:** *Deprecated in Java.*

Return the right-to-left mirror (or the original char if none) of the specified char. 

### mirror

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun mirror(
    text: CharArray!, 
    start: Int, 
    count: Int
): Boolean
```

**Deprecated:** *Deprecated in Java.*

Replace the specified slice of`text`with the chars' right-to-left mirrors (if any), returning true if any replacements were made.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:array of characters to apply mirror operation |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):first character in array to mirror |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):maximum number of characters to mirror |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if replacements were made |
