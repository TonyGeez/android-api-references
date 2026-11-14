# AutoText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AutoText

Kotlin| [Java](AutoText.md) 
| --- | --- |

```
open class AutoText
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.text.AutoText](AutoText.md) |

This class accesses a dictionary of corrections to frequent misspellings.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [get](AutoText.md))`(`src:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `view:` ` [View](../android.view/View.md)!`)` Retrieves a possible spelling correction for the specified range of text. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSize](AutoText.md))`(`view:` ` [View](../android.view/View.md)!`)` Returns the size of the auto text dictionary. |

## Public methods

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun get(
    src: CharSequence!, 
    start: Int, 
    end: Int, 
    view: View!
): String!
```

Retrieves a possible spelling correction for the specified range of text. Returns null if no correction can be found. The View is used to get the current Locale and Resources. 

### getSize

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getSize(view: View!): Int
```

Returns the size of the auto text dictionary. The return value can be zero if there is no auto correction data available for the current locale.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](../android.view/View.md)!:used to retrieve the current Locale and Resources. |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of entries in the auto text dictionary |
