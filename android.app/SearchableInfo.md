Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SearchableInfo

Kotlin | [Java](https://developer.android.com/reference/android/app/SearchableInfo "View this page in Java")

```
class SearchableInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.SearchableInfo](https://developer.android.com/reference/kotlin/android/app/SearchableInfo#) |

Searchability meta-data for an activity. Only applications that search other applications should need to use this class. See [Searchable Configuration](https://developer.android.com/guide/topics/search/searchable-config.html) for more information about declaring searchability meta-data for your application.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/SearchableInfo#autoUrlDetect()()` Checks whether this searchable activity has auto URL detection turned on. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/SearchableInfo#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/SearchableInfo#getHintId()()` Gets the resource id of the hint text. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/SearchableInfo#getImeOptions()()` Gets the input method options specified in the searchable attributes. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/SearchableInfo#getInputType()()` Gets the input type as specified in the searchable attributes. |
| [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)! | `https://developer.android.com/reference/kotlin/android/app/SearchableInfo#getSearchActivity()()` Gets the component name of the searchable activity. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/SearchableInfo#getSettingsDescriptionId()()` Gets the resource id of the description string to use for this source in system search settings, or `0` if none has been specified. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/app/SearchableInfo#getSuggestAuthority()()` Gets the search suggestion content provider authority. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/app/SearchableInfo#getSuggestIntentAction()()` Gets the optional intent action for use with these suggestions. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/app/SearchableInfo#getSuggestIntentData()()` Gets the optional intent data for use with these suggestions. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/app/SearchableInfo#getSuggestPackage()()` Gets the name of the package where the suggestion provider lives, or `null`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/app/SearchableInfo#getSuggestPath()()` Gets the content provider path for obtaining search suggestions. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/app/SearchableInfo#getSuggestSelection()()` Gets the selection for obtaining search suggestions. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/SearchableInfo#getSuggestThreshold()()` Gets the suggestion threshold. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/SearchableInfo#getVoiceLanguageId()()` Gets the resource id of the spoken language to recognize in voice search. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/SearchableInfo#getVoiceLanguageModeId()()` Gets the resource id of the voice search language model string. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/SearchableInfo#getVoiceMaxResults()()` The maximum number of voice recognition results to return. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/SearchableInfo#getVoicePromptTextId()()` Gets the resource id of the voice prompt text string. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/SearchableInfo#getVoiceSearchEnabled()()` Checks if the searchable activity wants the voice search button to be shown. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/SearchableInfo#getVoiceSearchLaunchRecognizer()()` Checks if voice search should start in-app search. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/SearchableInfo#getVoiceSearchLaunchWebSearch()()` Checks if voice search should start web search. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/SearchableInfo#queryAfterZeroResults()()` Checks whether this searchable activity should be queried for suggestions if a prefix of the query has returned no results. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/SearchableInfo#shouldIncludeInGlobalSearch()()` Checks whether the searchable should be included in global search. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/SearchableInfo#shouldRewriteQueryFromData()()` Checks whether the text in the query field should come from the suggestion intent data. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/SearchableInfo#shouldRewriteQueryFromText()()` Checks whether the text in the query field should come from the suggestion title. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/SearchableInfo#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [SearchableInfo](https://developer.android.com/reference/kotlin/android/app/SearchableInfo#)!\> | `https://developer.android.com/reference/kotlin/android/app/SearchableInfo#CREATOR:android.os.Parcelable.Creator` Support for parcelable and aidl operations. |

## Public methods

### autoUrlDetect

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun autoUrlDetect(): Boolean
```

Checks whether this searchable activity has auto URL detection turned on.
**See Also**

- `https://developer.android.com/reference/kotlin/android/R.styleable.html#Searchable_autoUrlDetect:kotlin.Int`

### describeContents

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getHintId

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getHintId(): Int
```

Gets the resource id of the hint text. This must be read using the searchable Activity's resources.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | A resource id, or `0` if no hint was specified. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/R.styleable.html#Searchable_hint:kotlin.Int`

### getImeOptions

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getImeOptions(): Int
```

Gets the input method options specified in the searchable attributes. This will default to `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo.html#IME_ACTION_GO:kotlin.Int` if not specified (which is appropriate for a search box).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the input type |

**See Also**

- `https://developer.android.com/reference/kotlin/android/R.styleable.html#Searchable_imeOptions:kotlin.Int`

### getInputType

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getInputType(): Int
```

Gets the input type as specified in the searchable attributes. This will default to `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_CLASS_TEXT:kotlin.Int` if not specified (which is appropriate for free text input).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the input type |

**See Also**

- `https://developer.android.com/reference/kotlin/android/R.styleable.html#Searchable_inputType:kotlin.Int`

### getSearchActivity

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSearchActivity(): ComponentName!
```

Gets the component name of the searchable activity.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#!` | A component name, never `null`. |

### getSettingsDescriptionId

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSettingsDescriptionId(): Int
```

Gets the resource id of the description string to use for this source in system search settings, or `0` if none has been specified.
**See Also**

- `https://developer.android.com/reference/kotlin/android/R.styleable.html#Searchable_searchSettingsDescription:kotlin.Int`

### getSuggestAuthority

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSuggestAuthority(): String!
```

Gets the search suggestion content provider authority.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The search suggestions authority, or `null` if not set. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/R.styleable.html#Searchable_searchSuggestAuthority:kotlin.Int`

### getSuggestIntentAction

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSuggestIntentAction(): String!
```

Gets the optional intent action for use with these suggestions. This is useful if all intents will have the same action (e.g. `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_VIEW:kotlin.String`) This can be overriden in any given suggestion using the column `https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_COLUMN_INTENT_ACTION:kotlin.String`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The default intent action, or `null` if not set. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/R.styleable.html#Searchable_searchSuggestIntentAction:kotlin.Int`

### getSuggestIntentData

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSuggestIntentData(): String!
```

Gets the optional intent data for use with these suggestions. This is useful if all intents will have similar data URIs, but you'll likely need to provide a specific ID as well via the column `https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_COLUMN_INTENT_DATA_ID:kotlin.String`, which will be appended to the intent data URI. This can be overriden in any given suggestion using the column `https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_COLUMN_INTENT_DATA:kotlin.String`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The default intent data, or `null` if not set. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/R.styleable.html#Searchable_searchSuggestIntentData:kotlin.Int`

### getSuggestPackage

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSuggestPackage(): String!
```

Gets the name of the package where the suggestion provider lives, or `null`.

### getSuggestPath

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSuggestPath(): String!
```

Gets the content provider path for obtaining search suggestions.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The suggestion path, or `null` if not set. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/R.styleable.html#Searchable_searchSuggestPath:kotlin.Int`

### getSuggestSelection

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSuggestSelection(): String!
```

Gets the selection for obtaining search suggestions.
**See Also**

- `https://developer.android.com/reference/kotlin/android/R.styleable.html#Searchable_searchSuggestSelection:kotlin.Int`

### getSuggestThreshold

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSuggestThreshold(): Int
```

Gets the suggestion threshold.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The suggestion threshold, or `0` if not set. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/R.styleable.html#Searchable_searchSuggestThreshold:kotlin.Int`

### getVoiceLanguageId

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getVoiceLanguageId(): Int
```

Gets the resource id of the spoken language to recognize in voice search.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | A resource id, or `0` if no language was specified. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/R.styleable.html#Searchable_voiceLanguage:kotlin.Int`

### getVoiceLanguageModeId

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getVoiceLanguageModeId(): Int
```

Gets the resource id of the voice search language model string.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | A resource id, or `0` if no language model was specified. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/R.styleable.html#Searchable_voiceLanguageModel:kotlin.Int`

### getVoiceMaxResults

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getVoiceMaxResults(): Int
```

The maximum number of voice recognition results to return.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the max results count, if specified in the searchable activity's metadata, or `0` if not specified. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/R.styleable.html#Searchable_voiceMaxResults:kotlin.Int`

### getVoicePromptTextId

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getVoicePromptTextId(): Int
```

Gets the resource id of the voice prompt text string.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | A resource id, or `0` if no voice prompt text was specified. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/R.styleable.html#Searchable_voicePromptText:kotlin.Int`

### getVoiceSearchEnabled

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getVoiceSearchEnabled(): Boolean
```

Checks if the searchable activity wants the voice search button to be shown.
**See Also**

- `https://developer.android.com/reference/kotlin/android/R.styleable.html#Searchable_voiceSearchMode:kotlin.Int`

### getVoiceSearchLaunchRecognizer

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getVoiceSearchLaunchRecognizer(): Boolean
```

Checks if voice search should start in-app search.
**See Also**

- `https://developer.android.com/reference/kotlin/android/R.styleable.html#Searchable_voiceSearchMode:kotlin.Int`

### getVoiceSearchLaunchWebSearch

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getVoiceSearchLaunchWebSearch(): Boolean
```

Checks if voice search should start web search.
**See Also**

- `https://developer.android.com/reference/kotlin/android/R.styleable.html#Searchable_voiceSearchMode:kotlin.Int`

### queryAfterZeroResults

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun queryAfterZeroResults(): Boolean
```

Checks whether this searchable activity should be queried for suggestions if a prefix of the query has returned no results.
**See Also**

- `https://developer.android.com/reference/kotlin/android/R.styleable.html#Searchable_queryAfterZeroResults:kotlin.Int`

### shouldIncludeInGlobalSearch

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun shouldIncludeInGlobalSearch(): Boolean
```

Checks whether the searchable should be included in global search.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | The value of the `https://developer.android.com/reference/kotlin/android/R.styleable.html#Searchable_includeInGlobalSearch:kotlin.Int` attribute, or `false` if the attribute is not set. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/R.styleable.html#Searchable_includeInGlobalSearch:kotlin.Int`

### shouldRewriteQueryFromData

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun shouldRewriteQueryFromData(): Boolean
```

Checks whether the text in the query field should come from the suggestion intent data.
**See Also**

- `https://developer.android.com/reference/kotlin/android/R.styleable.html#Searchable_searchMode:kotlin.Int`

### shouldRewriteQueryFromText

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun shouldRewriteQueryFromText(): Boolean
```

Checks whether the text in the query field should come from the suggestion title.
**See Also**

- `https://developer.android.com/reference/kotlin/android/R.styleable.html#Searchable_searchMode:kotlin.Int`

### writeToParcel

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<SearchableInfo!>
```

Support for parcelable and aidl operations.
