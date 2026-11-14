# LocaleDisplayNames

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LocaleDisplayNames

Kotlin| [Java](https://developer.android.com/reference/android/icu/text/LocaleDisplayNames "View this page in Java") 

```
abstract class LocaleDisplayNames
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.icu.text.LocaleDisplayNames](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames#) |

Returns display names of ULocales and components of ULocales. For more information on language, script, region, variant, key, and values, see [android.icu.util.ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#).

## Summary

| Nested classes ||
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [DialectHandling](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames.DialectHandling) Enum used in [getInstance(android.icu.util.ULocale,android.icu.text.LocaleDisplayNames.DialectHandling)](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames#getInstance(android.icu.util.ULocale,%20android.icu.text.LocaleDisplayNames.DialectHandling)). |
| open | [UiListItem](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames.UiListItem) Struct-like class used to return information for constructing a UI list, each corresponding to a locale. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [DisplayContext](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext)! | [getContext](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames#getContext(android.icu.text.DisplayContext.Type))`(`type:` ` [DisplayContext.Type](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext.Type)!`)` Returns the current value for a specified DisplayContext. |
| abstract [LocaleDisplayNames.DialectHandling](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames.DialectHandling)! | [getDialectHandling](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames#getDialectHandling())`()` Returns the dialect handling used in the display names. |
| openstatic [LocaleDisplayNames](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames#)! | [getInstance](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames#getInstance(android.icu.util.ULocale))`(`locale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!`)` Convenience overload of [getInstance(android.icu.util.ULocale,android.icu.text.LocaleDisplayNames.DialectHandling)](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames#getInstance(android.icu.util.ULocale,%20android.icu.text.LocaleDisplayNames.DialectHandling))that specifies STANDARD dialect handling. |
| openstatic [LocaleDisplayNames](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames#)! | [getInstance](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames#getInstance(android.icu.util.ULocale,%20android.icu.text.DisplayContext))`(`locale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!`, `vararg` `contexts:` ` [DisplayContext](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext)!`)` Returns an instance of LocaleDisplayNames that returns names formatted for the provided locale, using the provided DisplayContext settings |
| openstatic [LocaleDisplayNames](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames#)! | [getInstance](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames#getInstance(android.icu.util.ULocale,%20android.icu.text.LocaleDisplayNames.DialectHandling))`(`locale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!`, `dialectHandling:` ` [LocaleDisplayNames.DialectHandling](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames.DialectHandling)!`)` Returns an instance of LocaleDisplayNames that returns names formatted for the provided locale, using the provided dialectHandling. |
| openstatic [LocaleDisplayNames](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames#)! | [getInstance](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames#getInstance(java.util.Locale))`(`locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` Convenience overload of [getInstance(java.util.Locale,android.icu.text.DisplayContext...)](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames#getInstance(java.util.Locale,%20android.icu.text.DisplayContext))that specifies [DisplayContext.STANDARD_NAMES](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext). |
| openstatic [LocaleDisplayNames](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames#)! | [getInstance](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames#getInstance(java.util.Locale,%20android.icu.text.DisplayContext))`(`locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`, `vararg` `contexts:` ` [DisplayContext](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext)!`)` Returns an instance of LocaleDisplayNames that returns names formatted for the provided [java.util.Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#), using the provided DisplayContext settings |
| abstract [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)! | [getLocale](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames#getLocale())`()` Returns the locale used to determine the display names. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [LocaleDisplayNames.UiListItem](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames.UiListItem)!\>! | [getUiList](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames#getUiList(kotlin.collections.MutableSet,%20kotlin.Boolean,%20java.util.Comparator))`(`localeSet:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!>!`, `inSelf:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `collator:` ` [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator.html#)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`)` Return a list of information used to construct a UI list of locale names. |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [LocaleDisplayNames.UiListItem](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames.UiListItem)!\>! | [getUiListCompareWholeItems](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames#getUiListCompareWholeItems(kotlin.collections.MutableSet,%20java.util.Comparator))`(`localeSet:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!>!`, `comparator:` ` [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator.html#)< [LocaleDisplayNames.UiListItem](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames.UiListItem)!>!`)` Return a list of information used to construct a UI list of locale names, providing more access to control the sorting. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [keyDisplayName](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames#keyDisplayName(kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the display name of the provided locale key. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [keyValueDisplayName](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames#keyValueDisplayName(kotlin.String,%20kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the display name of the provided value (used with the provided key). |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [languageDisplayName](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames#languageDisplayName(kotlin.String))`(`lang:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the display name of the provided language code. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [localeDisplayName](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames#localeDisplayName(android.icu.util.ULocale))`(`locale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!`)` Returns the display name of the provided ulocale. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [localeDisplayName](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames#localeDisplayName(kotlin.String))`(`localeId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the display name of the provided locale id. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [localeDisplayName](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames#localeDisplayName(java.util.Locale))`(`locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` Returns the display name of the provided locale. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [regionDisplayName](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames#regionDisplayName(kotlin.String))`(`region:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the display name of the provided region code. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [scriptDisplayName](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames#scriptDisplayName(kotlin.Int))`(`scriptCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the display name of the provided script code. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [scriptDisplayName](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames#scriptDisplayName(kotlin.String))`(`script:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the display name of the provided script code. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [variantDisplayName](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames#variantDisplayName(kotlin.String))`(`variant:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the display name of the provided variant. |

## Public methods

### getContext

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getContext(type: DisplayContext.Type!): DisplayContext!
```

Returns the current value for a specified DisplayContext.Type.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [DisplayContext.Type](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext.Type)!:the DisplayContext.Type whose value to return |

| Return ||
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [DisplayContext](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext)! | the current DisplayContext setting for the specified type |

### getDialectHandling

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDialectHandling(): LocaleDisplayNames.DialectHandling!
```

Returns the dialect handling used in the display names.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| [LocaleDisplayNames.DialectHandling](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames.DialectHandling)! | the dialect handling enum |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(locale: ULocale!): LocaleDisplayNames!
```

Convenience overload of [getInstance(android.icu.util.ULocale,android.icu.text.LocaleDisplayNames.DialectHandling)](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames#getInstance(android.icu.util.ULocale,%20android.icu.text.LocaleDisplayNames.DialectHandling))that specifies STANDARD dialect handling.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!:the display locale |

| Return ||
|------------------------------------------------------------------------------------------------------------|-------------------------------|
| [LocaleDisplayNames](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames#)! | a LocaleDisplayNames instance |

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
| `locale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!:the display locale |
| `contexts` | [DisplayContext](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext)!:one or more context settings (e.g. for dialect handling, capitalization, etc. |

| Return ||
|------------------------------------------------------------------------------------------------------------|-------------------------------|
| [LocaleDisplayNames](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames#)! | a LocaleDisplayNames instance |

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
| `locale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!:the display locale |
| `dialectHandling` | [LocaleDisplayNames.DialectHandling](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames.DialectHandling)!:how to select names for locales |

| Return ||
|------------------------------------------------------------------------------------------------------------|-------------------------------|
| [LocaleDisplayNames](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames#)! | a LocaleDisplayNames instance |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(locale: Locale!): LocaleDisplayNames!
```

Convenience overload of [getInstance(java.util.Locale,android.icu.text.DisplayContext...)](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames#getInstance(java.util.Locale,%20android.icu.text.DisplayContext))that specifies [DisplayContext.STANDARD_NAMES](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext).

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!:the display [java.util.Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#) |

| Return ||
|------------------------------------------------------------------------------------------------------------|-------------------------------|
| [LocaleDisplayNames](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames#)! | a LocaleDisplayNames instance |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(
    locale: Locale!, 
    vararg contexts: DisplayContext!
): LocaleDisplayNames!
```

Returns an instance of LocaleDisplayNames that returns names formatted for the provided [java.util.Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#), using the provided DisplayContext settings

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!:the display [java.util.Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#) |
| `contexts` | [DisplayContext](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext)!:one or more context settings (e.g. for dialect handling, capitalization, etc. |

| Return ||
|------------------------------------------------------------------------------------------------------------|-------------------------------|
| [LocaleDisplayNames](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames#)! | a LocaleDisplayNames instance |

### getLocale

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLocale(): ULocale!
```

Returns the locale used to determine the display names. This is not necessarily the same locale passed to #getInstance.

| Return ||
|-------------------------------------------------------------------------------------------|--------------------|
| [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)! | the display locale |

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
| `collator` | [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator.html#)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!:how to collate---should normally be Collator.getInstance(getDisplayLocale()) |
| `inSelf` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if true, compares the nameInSelf, otherwise the nameInDisplayLocale. Set depending on which field (displayLocale vs self) is to show up in the UI. If both are to show up in the UI, then it should be the one used for the primary sort order. |
| `localeSet` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!\>!:a list of locales to present in a UI list. The casing uses the settings in the LocaleDisplayNames instance. |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [LocaleDisplayNames.UiListItem](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames.UiListItem)!>! | an ordered list of UiListItems. |

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
| `comparator` | [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator.html#)\< [LocaleDisplayNames.UiListItem](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames.UiListItem)!\>!:how to sort the UiListItems in the result. |
| `localeSet` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!\>!:a list of locales to present in a UI list. The casing uses the settings in the LocaleDisplayNames instance. |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [LocaleDisplayNames.UiListItem](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames.UiListItem)!>! | an ordered list of UiListItems. |

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
| `locale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!:the locale whose display name to return |

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
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!:the locale whose display name to return |

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

Returns the display name of the provided script code. See [android.icu.lang.UScript](https://developer.android.com/reference/kotlin/android/icu/lang/UScript.html#) for recognized script codes.

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
