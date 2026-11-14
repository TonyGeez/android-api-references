# NumberRangeFormatterSettings

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NumberRangeFormatterSettings

Kotlin| [Java](https://developer.android.com/reference/android/icu/number/NumberRangeFormatterSettings "View this page in Java") 

```
abstract class NumberRangeFormatterSettings<T : NumberRangeFormatterSettings<*>!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.icu.number.NumberRangeFormatterSettings](https://developer.android.com/reference/kotlin/android/icu/number/NumberRangeFormatterSettings#) |

| Known Direct Subclasses [LocalizedNumberRangeFormatter](https://developer.android.com/reference/kotlin/android/icu/number/LocalizedNumberRangeFormatter), [UnlocalizedNumberRangeFormatter](https://developer.android.com/reference/kotlin/android/icu/number/UnlocalizedNumberRangeFormatter) |--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------| | [LocalizedNumberRangeFormatter](https://developer.android.com/reference/kotlin/android/icu/number/LocalizedNumberRangeFormatter) | A NumberRangeFormatter that has a locale associated with it; this means . | | [UnlocalizedNumberRangeFormatter](https://developer.android.com/reference/kotlin/android/icu/number/UnlocalizedNumberRangeFormatter) | A NumberRangeFormatter that does not yet have a locale. | |

An abstract base class for specifying settings related to number formatting. This class is implemented by [UnlocalizedNumberRangeFormatter](https://developer.android.com/reference/kotlin/android/icu/number/UnlocalizedNumberRangeFormatter) and [LocalizedNumberRangeFormatter](https://developer.android.com/reference/kotlin/android/icu/number/LocalizedNumberRangeFormatter). This class is not intended for public subclassing.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openT | [collapse](https://developer.android.com/reference/kotlin/android/icu/number/NumberRangeFormatterSettings#collapse(android.icu.number.NumberRangeFormatter.RangeCollapse))`(`collapse:` ` [NumberRangeFormatter.RangeCollapse](https://developer.android.com/reference/kotlin/android/icu/number/NumberRangeFormatter.RangeCollapse)!`)` Sets the aggressiveness of "collapsing" fields across the range separator. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/icu/number/NumberRangeFormatterSettings#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/icu/number/NumberRangeFormatterSettings#hashCode())`()` Returns a hash code value for the object. |
| openT | [identityFallback](https://developer.android.com/reference/kotlin/android/icu/number/NumberRangeFormatterSettings#identityFallback(android.icu.number.NumberRangeFormatter.RangeIdentityFallback))`(`identityFallback:` ` [NumberRangeFormatter.RangeIdentityFallback](https://developer.android.com/reference/kotlin/android/icu/number/NumberRangeFormatter.RangeIdentityFallback)!`)` Sets the behavior when the two sides of the range are the same. |
| openT | [numberFormatterBoth](https://developer.android.com/reference/kotlin/android/icu/number/NumberRangeFormatterSettings#numberFormatterBoth(android.icu.number.UnlocalizedNumberFormatter))`(`formatter:` ` [UnlocalizedNumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/UnlocalizedNumberFormatter)!`)` Sets the NumberFormatter instance to use for the numbers in the range. |
| openT | [numberFormatterFirst](https://developer.android.com/reference/kotlin/android/icu/number/NumberRangeFormatterSettings#numberFormatterFirst(android.icu.number.UnlocalizedNumberFormatter))`(`formatterFirst:` ` [UnlocalizedNumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/UnlocalizedNumberFormatter)!`)` Sets the NumberFormatter instance to use for the first number in the range. |
| openT | [numberFormatterSecond](https://developer.android.com/reference/kotlin/android/icu/number/NumberRangeFormatterSettings#numberFormatterSecond(android.icu.number.UnlocalizedNumberFormatter))`(`formatterSecond:` ` [UnlocalizedNumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/UnlocalizedNumberFormatter)!`)` Sets the NumberFormatter instances to use for the second number in the range. |

## Public methods

### collapse

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun collapse(collapse: NumberRangeFormatter.RangeCollapse!): T
```

Sets the aggressiveness of "collapsing" fields across the range separator. Possible values:

- ALL: "3-5K miles"
- UNIT: "3K - 5K miles"
- NONE: "3K miles - 5K miles"
- AUTO: usually UNIT or NONE, depending on the locale and formatter settings

<br />

The default value is AUTO.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `collapse` | [NumberRangeFormatter.RangeCollapse](https://developer.android.com/reference/kotlin/android/icu/number/NumberRangeFormatter.RangeCollapse)!:The collapsing strategy to use for this range. |

| Return ||
|---|-------------------|
| T | The fluent chain. |

**See Also**

- [android.icu.number.NumberRangeFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberRangeFormatter) 

### equals

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### hashCode

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by [java.util.HashMap](https://developer.android.com/reference/kotlin/java/util/HashMap.html#).

The general contract of`hashCode`is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the`hashCode`method must consistently return the same integer, provided no information used in`equals`comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the [equals](https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any))method, then calling the`hashCode`method on each of the two objects must produce the same integer result.
- It is*not* required that if two objects are unequal according to the [equals](https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any))method, then calling the`hashCode`method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### identityFallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun identityFallback(identityFallback: NumberRangeFormatter.RangeIdentityFallback!): T
```

Sets the behavior when the two sides of the range are the same. This could happen if the same two numbers are passed to the formatRange function, or if different numbers are passed to the function but they become the same after rounding rules are applied. Possible values:

- SINGLE_VALUE: "5 miles"
- APPROXIMATELY_OR_SINGLE_VALUE: "\~5 miles" or "5 miles", depending on whether the number was the same before rounding was applied
- APPROXIMATELY: "\~5 miles"
- RANGE: "5-5 miles" (with collapse=UNIT)

<br />

The default value is APPROXIMATELY.

| Parameters ||
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `identityFallback` | [NumberRangeFormatter.RangeIdentityFallback](https://developer.android.com/reference/kotlin/android/icu/number/NumberRangeFormatter.RangeIdentityFallback)!:The strategy to use when formatting two numbers that end up being the same. |

| Return ||
|---|-------------------|
| T | The fluent chain. |

**See Also**

- [android.icu.number.NumberRangeFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberRangeFormatter) 

### numberFormatterBoth

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun numberFormatterBoth(formatter: UnlocalizedNumberFormatter!): T
```

Sets the NumberFormatter instance to use for the numbers in the range. The same formatter is applied to both sides of the range.

The NumberFormatter instances must not have a locale applied yet; the locale specified on the NumberRangeFormatter will be used.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `formatter` | [UnlocalizedNumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/UnlocalizedNumberFormatter)!:The formatter to use for both numbers in the range. |

| Return ||
|---|-------------------|
| T | The fluent chain. |

**See Also**

- [android.icu.number.NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter)
- [android.icu.number.NumberRangeFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberRangeFormatter) 

### numberFormatterFirst

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun numberFormatterFirst(formatterFirst: UnlocalizedNumberFormatter!): T
```

Sets the NumberFormatter instance to use for the first number in the range.

The NumberFormatter instance must not have a locale applied yet; the locale specified on the NumberRangeFormatter will be used.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `formatterFirst` | [UnlocalizedNumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/UnlocalizedNumberFormatter)!:The formatter to use for the first number in the range. |

| Return ||
|---|-------------------|
| T | The fluent chain. |

**See Also**

- [android.icu.number.NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter)
- [android.icu.number.NumberRangeFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberRangeFormatter) 

### numberFormatterSecond

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun numberFormatterSecond(formatterSecond: UnlocalizedNumberFormatter!): T
```

Sets the NumberFormatter instances to use for the second number in the range.

The NumberFormatter instance must not have a locale applied yet; the locale specified on the NumberRangeFormatter will be used.

| Parameters ||
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `formatterSecond` | [UnlocalizedNumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/UnlocalizedNumberFormatter)!:The formatter to use for the second number in the range. |

| Return ||
|---|-------------------|
| T | The fluent chain. |

**See Also**

- [android.icu.number.NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter)
- [android.icu.number.NumberRangeFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberRangeFormatter)
