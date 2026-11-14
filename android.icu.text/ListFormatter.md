# ListFormatter

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ListFormatter

Kotlin| [Java](ListFormatter.md) 
| --- | --- |

```
class ListFormatter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.text.ListFormatter](ListFormatter.md) |

Immutable class for formatting a list, using data from CLDR (or supplied separately). The class is not subclassable.

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [FormattedList](../android/icu/text/ListFormatter.FormattedList.md) An immutable class containing the result of a list formatting operation. |
| | [Type](../android/icu/text/ListFormatter.Type.md) Type of meaning expressed by the list. |
| | [Width](../android/icu/text/ListFormatter.Width.md) Verbosity level of the list patterns. |
| --- | --- |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](ListFormatter.md))`(`vararg` `items:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Format a list of objects. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](ListFormatter.md))`(`items:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<*>!`)` Format a collection of objects. |
| [ListFormatter.FormattedList](../android/icu/text/ListFormatter.FormattedList.md)! | [formatToValue](ListFormatter.md))`(`vararg` `items:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Format a list of objects to a FormattedList. |
| --- | --- |
| [ListFormatter.FormattedList](../android/icu/text/ListFormatter.FormattedList.md)! | [formatToValue](ListFormatter.md))`(`items:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<*>!`)` Format a collection of objects to a FormattedList. |
| static [ListFormatter](ListFormatter.md)! | [getInstance](ListFormatter.md))`()` Create a list formatter that is appropriate for the default FORMAT locale. |
| static [ListFormatter](ListFormatter.md)! | [getInstance](ListFormatter.md))`(`locale:` ` [ULocale](../android.icu.util/ULocale.md)!`)` Create a list formatter that is appropriate for a locale. |
| --- | --- |
| static [ListFormatter](ListFormatter.md)! | [getInstance](ListFormatter.md))`(`locale:` ` [ULocale](../android.icu.util/ULocale.md)!`, `type:` ` [ListFormatter.Type](../android/icu/text/ListFormatter.Type.md)!`, `width:` ` [ListFormatter.Width](../android/icu/text/ListFormatter.Width.md)!`)` Create a list formatter that is appropriate for a locale. |
| static [ListFormatter](ListFormatter.md)! | [getInstance](ListFormatter.md))`(`locale:` ` [Locale](../java.util/Locale.md)!`)` Create a list formatter that is appropriate for a locale. |
| static [ListFormatter](ListFormatter.md)! | [getInstance](ListFormatter.md))`(`locale:` ` [Locale](../java.util/Locale.md)!`, `type:` ` [ListFormatter.Type](../android/icu/text/ListFormatter.Type.md)!`, `width:` ` [ListFormatter.Width](../android/icu/text/ListFormatter.Width.md)!`)` Create a list formatter that is appropriate for a locale. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPatternForNumItems](ListFormatter.md))`(`count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the pattern to use for a particular item count. |

## Public methods

### format

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun format(vararg items: Any!): String!
```

Format a list of objects.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------|
| `items` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:items to format. The toString() method is called on each. |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | items formatted into a string |

### format

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun format(items: MutableCollection<*>!): String!
```

Format a collection of objects. The toString() method is called on each.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `items` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<\*\>!:items to format. The toString() method is called on each. |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | items formatted into a string |

### formatToValue

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun formatToValue(vararg items: Any!): ListFormatter.FormattedList!
```

Format a list of objects to a FormattedList. You can access the offsets of each element from the FormattedList.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------|
| `items` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:items to format. The toString() method is called on each. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| [ListFormatter.FormattedList](../android/icu/text/ListFormatter.FormattedList.md)! | items formatted into a FormattedList |

### formatToValue

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun formatToValue(items: MutableCollection<*>!): ListFormatter.FormattedList!
```

Format a collection of objects to a FormattedList. You can access the offsets of each element from the FormattedList.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `items` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<\*\>!:items to format. The toString() method is called on each. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| [ListFormatter.FormattedList](../android/icu/text/ListFormatter.FormattedList.md)! | items formatted into a FormattedList |

### getInstance

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(): ListFormatter!
```

Create a list formatter that is appropriate for the default FORMAT locale.

| Return ||
|--------------------------------------------------------------------------------------------------|---------------|
| [ListFormatter](ListFormatter.md)! | ListFormatter |

### getInstance

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(locale: ULocale!): ListFormatter!
```

Create a list formatter that is appropriate for a locale.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](../android.icu.util/ULocale.md)!:the locale in question. |

| Return ||
|--------------------------------------------------------------------------------------------------|---------------|
| [ListFormatter](ListFormatter.md)! | ListFormatter |

### getInstance

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(
    locale: ULocale!, 
    type: ListFormatter.Type!, 
    width: ListFormatter.Width!
): ListFormatter!
```

Create a list formatter that is appropriate for a locale.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](../android.icu.util/ULocale.md)!:the locale in question. |

| Return ||
|--------------------------------------------------------------------------------------------------|---------------|
| [ListFormatter](ListFormatter.md)! | ListFormatter |

### getInstance

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(locale: Locale!): ListFormatter!
```

Create a list formatter that is appropriate for a locale.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](../java.util/Locale.md)!:the locale in question. |

| Return ||
|--------------------------------------------------------------------------------------------------|---------------|
| [ListFormatter](ListFormatter.md)! | ListFormatter |

### getInstance

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(
    locale: Locale!, 
    type: ListFormatter.Type!, 
    width: ListFormatter.Width!
): ListFormatter!
```

Create a list formatter that is appropriate for a locale.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](../java.util/Locale.md)!:the locale in question. |

| Return ||
|--------------------------------------------------------------------------------------------------|---------------|
| [ListFormatter](ListFormatter.md)! | ListFormatter |

### getPatternForNumItems

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPatternForNumItems(count: Int): String!
```

Returns the pattern to use for a particular item count.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------|
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the item count. |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the pattern with {0}, {1}, {2}, etc. For English, getPatternForNumItems(3) == "{0}, {1}, and {2}" |

| Exceptions ||
|--------------------------------------|------------------------------|
| `java.lang.IllegalArgumentException` | when count is 0 or negative. |
