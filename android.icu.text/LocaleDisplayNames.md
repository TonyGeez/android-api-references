# LocaleDisplayNames

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LocaleDisplayNames

Kotlin| [Java](LocaleDisplayNames.md) 
| --- | --- |

```
abstract class LocaleDisplayNames
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.text.LocaleDisplayNames](LocaleDisplayNames.md) |

Returns display names of ULocales and components of ULocales. For more information on language, script, region, variant, key, and values, see [android.icu.util.ULocale](../android.icu.util/ULocale.md).

## Summary

| Nested classes ||
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [DialectHandling](../android/icu/text/LocaleDisplayNames.DialectHandling.md) Enum used in [getInstance(android.icu.util.ULocale,android.icu.text.LocaleDisplayNames.DialectHandling)](LocaleDisplayNames.md)). |
| open | [UiListItem](../android/icu/text/LocaleDisplayNames.UiListItem.md) Struct-like class used to return information for constructing a UI list, each corresponding to a locale. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [DisplayContext](DisplayContext.md)! | [getContext](LocaleDisplayNames.md))`(`type:` ` [DisplayContext.Type](../android/icu/text/DisplayContext.Type.md)!`)` Returns the current value for a specified DisplayContext. |
| abstract [LocaleDisplayNames.DialectHandling](../android/icu/text/LocaleDisplayNames.DialectHandling.md)! | [getDialectHandling](LocaleDisplayNames.md))`()` Returns the dialect handling used in the display names. |
| openstatic [LocaleDisplayNames](LocaleDisplayNames.md)! | [getInstance](LocaleDisplayNames.md))`(`locale:` ` [ULocale](../android.icu.util/ULocale.md)!`)` Convenience overload of [getInstance(android.icu.util.ULocale,android.icu.text.LocaleDisplayNames.DialectHandling)](LocaleDisplayNames.md))that specifies STANDARD dialect handling. |
| --- | --- |
| openstatic [LocaleDisplayNames](LocaleDisplayNames.md)! | [getInstance](LocaleDisplayNames.md))`(`locale:` ` [ULocale](../android.icu.util/ULocale.md)!`, `vararg` `contexts:` ` [DisplayContext](DisplayContext.md)!`)` Returns an instance of LocaleDisplayNames that returns names formatted for the provided locale, using the provided DisplayContext settings |
| openstatic [LocaleDisplayNames](LocaleDisplayNames.md)! | [getInstance](LocaleDisplayNames.md))`(`locale:` ` [ULocale](../android.icu.util/ULocale.md)!`, `dialectHandling:` ` [LocaleDisplayNames.DialectHandling](../android/icu/text/LocaleDisplayNames.DialectHandling.md)!`)` Returns an instance of LocaleDisplayNames that returns names formatted for the provided locale, using the provided dialectHandling. |
| openstatic [LocaleDisplayNames](LocaleDisplayNames.md)! | [getInstance](LocaleDisplayNames.md))`(`locale:` ` [Locale](../java.util/Locale.md)!`)` Convenience overload of [getInstance(java.util.Locale,android.icu.text.DisplayContext...)](LocaleDisplayNames.md))that specifies [DisplayContext.STANDARD_NAMES](DisplayContext.md). |
| --- | --- |
| openstatic [LocaleDisplayNames](LocaleDisplayNames.md)! | [getInstance](LocaleDisplayNames.md))`(`locale:` ` [Locale](../java.util/Locale.md)!`, `vararg` `contexts:` ` [DisplayContext](DisplayContext.md)!`)` Returns an instance of LocaleDisplayNames that returns names formatted for the provided [java.util.Locale](../java.util/Locale.md), using the provided DisplayContext settings |
| abstract [ULocale](../android.icu.util/ULocale.md)! | [getLocale](LocaleDisplayNames.md))`()` Returns the locale used to determine the display names. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [LocaleDisplayNames.UiListItem](../android/icu/text/LocaleDisplayNames.UiListItem.md)!\>! | [getUiList](LocaleDisplayNames.md))`(`localeSet:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [ULocale](../android.icu.util/ULocale.md)!>!`, `inSelf:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `collator:` ` [Comparator](../java.util/Comparator.md)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`)` Return a list of information used to construct a UI list of locale names. |
| --- | --- |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [LocaleDisplayNames.UiListItem](../android/icu/text/LocaleDisplayNames.UiListItem.md)!\>! | [getUiListCompareWholeItems](LocaleDisplayNames.md))`(`localeSet:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [ULocale](../android.icu.util/ULocale.md)!>!`, `comparator:` ` [Comparator](../java.util/Comparator.md)< [LocaleDisplayNames.UiListItem](../android/icu/text/LocaleDisplayNames.UiListItem.md)!>!`)` Return a list of information used to construct a UI list of locale names, providing more access to control the sorting. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [keyDisplayName](LocaleDisplayNames.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the display name of the provided locale key. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [keyValueDisplayName](LocaleDisplayNames.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the display name of the provided value (used with the provided key). |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [languageDisplayName](LocaleDisplayNames.md))`(`lang:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the display name of the provided language code. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [localeDisplayName](LocaleDisplayNames.md))`(`locale:` ` [ULocale](../android.icu.util/ULocale.md)!`)` Returns the display name of the provided ulocale. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [localeDisplayName](LocaleDisplayNames.md))`(`localeId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the display name of the provided locale id. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [localeDisplayName](LocaleDisplayNames.md))`(`locale:` ` [Locale](../java.util/Locale.md)!`)` Returns the display name of the provided locale. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [regionDisplayName](LocaleDisplayNames.md))`(`region:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the display name of the provided region code. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [scriptDisplayName](LocaleDisplayNames.md))`(`scriptCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the display name of the provided script code. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [scriptDisplayName](LocaleDisplayNames.md))`(`script:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the display name of the provided script code. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [variantDisplayName](LocaleDisplayNames.md))`(`variant:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the display name of the provided variant. |

## Public methods

### getContext

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getContext(type: DisplayContext.Type!): DisplayContext!
```

Returns the current value for a specified DisplayContext.Type.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [DisplayContext.Type](../android/icu/text/DisplayContext.Type.md)!:the DisplayContext.Type whose value to return |

| Return ||
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [DisplayContext](DisplayContext.md)! | the current DisplayContext setting for the specified type |

### getDialectHandling

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDialectHandling(): LocaleDisplayNames.DialectHandling!
```

Returns the dialect handling used in the display names.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| [LocaleDisplayNames.DialectHandling](../android/icu/text/LocaleDisplayNames.DialectHandling.md)! | the dialect handling enum |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(locale: ULocale!): LocaleDisplayNames!
```

Convenience overload of [getInstance(android.icu.util.ULocale,android.icu.text.LocaleDisplayNames.DialectHandling)](LocaleDisplayNames.md))that specifies STANDARD dialect handling.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](../android.icu.util/ULocale.md)!:the display locale |

| Return ||
|------------------------------------------------------------------------------------------------------------|-------------------------------|
| [LocaleDisplayNames](LocaleDisplayNames.md)! | a LocaleDisplayNames instance |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(
    locale: ULocale!, 
    vararg contexts: DisplayContext!
): LocaleDisplayNames!
```

Returns an instance of LocaleDisplayNames that returns names formatted for the provided locale, using the provided DisplayContext settings

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](../android.icu.util/ULocale.md)!:the display locale |
| `contexts` | [DisplayContext](DisplayContext.md)!:one or more context settings (e.g. for dialect handling, capitalization, etc. |

| Return ||
|------------------------------------------------------------------------------------------------------------|-------------------------------|
| [LocaleDisplayNames](LocaleDisplayNames.md)! | a LocaleDisplayNames instance |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(
    locale: ULocale!, 
    dialectHandling: LocaleDisplayNames.DialectHandling!
): LocaleDisplayNames!
```

Returns an instance of LocaleDisplayNames that returns names formatted for the provided locale, using the provided dialectHandling.

| Parameters ||
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](../android.icu.util/ULocale.md)!:the display locale |
| `dialectHandling` | [LocaleDisplayNames.DialectHandling](../android/icu/text/LocaleDisplayNames.DialectHandling.md)!:how to select names for locales |

| Return ||
|------------------------------------------------------------------------------------------------------------|-------------------------------|
| [LocaleDisplayNames](LocaleDisplayNames.md)! | a LocaleDisplayNames instance |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(locale: Locale!): LocaleDisplayNames!
```

Convenience overload of [getInstance(java.util.Locale,android.icu.text.DisplayContext...)](LocaleDisplayNames.md))that specifies [DisplayContext.STANDARD_NAMES](DisplayContext.md).

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](../java.util/Locale.md)!:the display [java.util.Locale](../java.util/Locale.md) |

| Return ||
|------------------------------------------------------------------------------------------------------------|-------------------------------|
| [LocaleDisplayNames](LocaleDisplayNames.md)! | a LocaleDisplayNames instance |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(
    locale: Locale!, 
    vararg contexts: DisplayContext!
): LocaleDisplayNames!
```

Returns an instance of LocaleDisplayNames that returns names formatted for the provided [java.util.Locale](../java.util/Locale.md), using the provided DisplayContext settings

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](../java.util/Locale.md)!:the display [java.util.Locale](../java.util/Locale.md) |
| `contexts` | [DisplayContext](DisplayContext.md)!:one or more context settings (e.g. for dialect handling, capitalization, etc. |

| Return ||
|------------------------------------------------------------------------------------------------------------|-------------------------------|
| [LocaleDisplayNames](LocaleDisplayNames.md)! | a LocaleDisplayNames instance |

### getLocale

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLocale(): ULocale!
```

Returns the locale used to determine the display names. This is not necessarily the same locale passed to #getInstance.

| Return ||
|-------------------------------------------------------------------------------------------|--------------------|
| [ULocale](../android.icu.util/ULocale.md)! | the display locale |

### getUiList

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUiList(
    localeSet: MutableSet<ULocale!>!, 
    inSelf: Boolean, 
    collator: Comparator<Any!>!
): MutableList<LocaleDisplayNames.UiListItem!>!
```

Return a list of information used to construct a UI list of locale names.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `collator` | [Comparator](../java.util/Comparator.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!:how to collate---should normally be Collator.getInstance(getDisplayLocale()) |
| `inSelf` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if true, compares the nameInSelf, otherwise the nameInDisplayLocale. Set depending on which field (displayLocale vs self) is to show up in the UI. If both are to show up in the UI, then it should be the one used for the primary sort order. |
| `localeSet` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [ULocale](../android.icu.util/ULocale.md)!\>!:a list of locales to present in a UI list. The casing uses the settings in the LocaleDisplayNames instance. |
| --- | --- |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [LocaleDisplayNames.UiListItem](../android/icu/text/LocaleDisplayNames.UiListItem.md)!>! | an ordered list of UiListItems. |

| Exceptions ||
|---------------------------------------------|---------------------------------------------------|
| `android.icu.util.IllformedLocaleException` | if any of the locales in localeSet are malformed. |

### getUiListCompareWholeItems

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getUiListCompareWholeItems(
    localeSet: MutableSet<ULocale!>!, 
    comparator: Comparator<LocaleDisplayNames.UiListItem!>!
): MutableList<LocaleDisplayNames.UiListItem!>!
```

Return a list of information used to construct a UI list of locale names, providing more access to control the sorting. Normally use getUiList instead.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `comparator` | [Comparator](../java.util/Comparator.md)\< [LocaleDisplayNames.UiListItem](../android/icu/text/LocaleDisplayNames.UiListItem.md)!\>!:how to sort the UiListItems in the result. |
| `localeSet` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [ULocale](../android.icu.util/ULocale.md)!\>!:a list of locales to present in a UI list. The casing uses the settings in the LocaleDisplayNames instance. |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [LocaleDisplayNames.UiListItem](../android/icu/text/LocaleDisplayNames.UiListItem.md)!>! | an ordered list of UiListItems. |

| Exceptions ||
|---------------------------------------------|---------------------------------------------------|
| `android.icu.util.IllformedLocaleException` | if any of the locales in localeSet are malformed. |

### keyDisplayName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun keyDisplayName(key: String!): String!
```

Returns the display name of the provided locale key.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the locale key name |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the display name of the provided locale key |

### keyValueDisplayName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun keyValueDisplayName(
    key: String!, 
    value: String!
): String!
```

Returns the display name of the provided value (used with the provided key).

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the locale key name |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the locale key's value |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the display name of the provided value |

### languageDisplayName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun languageDisplayName(lang: String!): String!
```

Returns the display name of the provided language code.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------|
| `lang` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the language code |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the display name of the provided language code |

### localeDisplayName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun localeDisplayName(locale: ULocale!): String!
```

Returns the display name of the provided ulocale. When no display names are available for all or portions of the original locale ID, those portions may be used directly (possibly in a more canonical form) as part of the returned display name.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](../android.icu.util/ULocale.md)!:the locale whose display name to return |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the display name of the provided locale |

### localeDisplayName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun localeDisplayName(localeId: String!): String!
```

Returns the display name of the provided locale id. When no display names are available for all or portions of the original locale ID, those portions may be used directly (possibly in a more canonical form) as part of the returned display name.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `localeId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the id of the locale whose display name to return |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the display name of the provided locale |

### localeDisplayName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun localeDisplayName(locale: Locale!): String!
```

Returns the display name of the provided locale. When no display names are available for all or portions of the original locale ID, those portions may be used directly (possibly in a more canonical form) as part of the returned display name.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](../java.util/Locale.md)!:the locale whose display name to return |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the display name of the provided locale |

### regionDisplayName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun regionDisplayName(region: String!): String!
```

Returns the display name of the provided region code.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------|
| `region` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the region code |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the display name of the provided region code |

### scriptDisplayName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun scriptDisplayName(scriptCode: Int): String!
```

Returns the display name of the provided script code. See [android.icu.lang.UScript](../android.icu.lang/UScript.md) for recognized script codes.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------|
| `scriptCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the script code number |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the display name of the provided script code |

### scriptDisplayName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun scriptDisplayName(script: String!): String!
```

Returns the display name of the provided script code.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------|
| `script` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the script code |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the display name of the provided script code |

### variantDisplayName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun variantDisplayName(variant: String!): String!
```

Returns the display name of the provided variant.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------|
| `variant` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the variant string |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the display name of the provided variant |
