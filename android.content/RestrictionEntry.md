# RestrictionEntry

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RestrictionEntry

Kotlin| [Java](https://developer.android.com/reference/android/content/RestrictionEntry "View this page in Java") 

```
open class RestrictionEntry : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.content.RestrictionEntry](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#) |

Applications can expose restrictions for a restricted user on a multiuser device. The administrator can configure these restrictions that will then be applied to the restricted user. Each RestrictionsEntry is one configurable restriction.

<br />

Any application that chooses to expose such restrictions does so by implementing a receiver that handles the [Intent.ACTION_GET_RESTRICTION_ENTRIES](https://developer.android.com/reference/kotlin/android/content/Intent#ACTION_GET_RESTRICTION_ENTRIES:kotlin.String) action. The receiver then returns a result bundle that contains an entry called "restrictions", whose value is an ArrayList.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_BOOLEAN](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_BOOLEAN:kotlin.Int) Restriction of type "bool". |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_BUNDLE](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_BUNDLE:kotlin.Int) Restriction of type "bundle". |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_BUNDLE_ARRAY](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_BUNDLE_ARRAY:kotlin.Int) Restriction of type "bundle_array". |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_CHOICE](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_CHOICE:kotlin.Int) Restriction of type "choice". |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_INTEGER](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_INTEGER:kotlin.Int) Restriction of type "integer". |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_MULTI_SELECT](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_MULTI_SELECT:kotlin.Int) Restriction of type "multi-select". |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_NULL](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_NULL:kotlin.Int) Hidden restriction type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_STRING](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_STRING:kotlin.Int) Restriction of type "string". |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RestrictionEntry](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#RestrictionEntry(android.os.Parcel))`(`in:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)!`)` <br /> |
| [RestrictionEntry](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#RestrictionEntry(kotlin.Int,%20kotlin.String))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructor for specifying the type and key, with no initial value; |
| [RestrictionEntry](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#RestrictionEntry(kotlin.String,%20kotlin.Boolean))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `selectedState:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Constructor for [TYPE_BOOLEAN](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_BOOLEAN:kotlin.Int) type. |
| [RestrictionEntry](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#RestrictionEntry(kotlin.String,%20kotlin.Int))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `selectedInt:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructor for [TYPE_INTEGER](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_INTEGER:kotlin.Int) type. |
| [RestrictionEntry](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#RestrictionEntry(kotlin.String,%20kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `selectedString:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructor for [TYPE_CHOICE](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_CHOICE:kotlin.Int) type. |
| [RestrictionEntry](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#RestrictionEntry(kotlin.String,%20kotlin.Array))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `selectedStrings:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Constructor for [TYPE_MULTI_SELECT](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_MULTI_SELECT:kotlin.Int) type. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [RestrictionEntry](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#)! | [createBundleArrayEntry](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#createBundleArrayEntry(kotlin.String,%20kotlin.Array))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `restrictionEntries:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [RestrictionEntry](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#)!>!`)` Creates an entry of type [TYPE_BUNDLE_ARRAY](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_BUNDLE_ARRAY:kotlin.Int). |
| openstatic [RestrictionEntry](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#)! | [createBundleEntry](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#createBundleEntry(kotlin.String,%20kotlin.Array))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `restrictionEntries:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [RestrictionEntry](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#)!>!`)` Creates an entry of type [TYPE_BUNDLE](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_BUNDLE:kotlin.Int). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#describeContents())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getAllSelectedStrings](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#getAllSelectedStrings())`()` Returns the list of currently selected values. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getChoiceEntries](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#getChoiceEntries())`()` Returns the list of strings, set earlier, that will be presented as choices to the user. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getChoiceValues](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#getChoiceValues())`()` Returns the list of possible string values set earlier. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDescription](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#getDescription())`()` Returns the provided user-visible description of the entry, if any. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIntValue](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#getIntValue())`()` Returns the value of the entry as an integer when the type is [TYPE_INTEGER](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_INTEGER:kotlin.Int). |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getKey](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#getKey())`()` This is the unique key for the restriction entry. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [RestrictionEntry](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#)!\>! | [getRestrictions](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#getRestrictions())`()` Returns array of possible restriction entries that this entry may contain. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getSelectedState](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#getSelectedState())`()` Returns the current selected state for an entry of type [TYPE_BOOLEAN](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_BOOLEAN:kotlin.Int). |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSelectedString](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#getSelectedString())`()` Returns the currently selected string value. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getTitle](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#getTitle())`()` Returns the user-visible title for the entry, if any. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#getType())`()` Returns the type for this restriction. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#hashCode())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAllSelectedStrings](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#setAllSelectedStrings(kotlin.Array))`(`allSelectedStrings:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Sets the current list of selected values for an entry of type [TYPE_MULTI_SELECT](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_MULTI_SELECT:kotlin.Int). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setChoiceEntries](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#setChoiceEntries(android.content.Context,%20kotlin.Int))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context)!`, `stringArrayResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets a list of strings that will be presented as choices to the user. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setChoiceEntries](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#setChoiceEntries(kotlin.Array))`(`choiceEntries:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Sets a list of strings that will be presented as choices to the user. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setChoiceValues](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#setChoiceValues(android.content.Context,%20kotlin.Int))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context)!`, `stringArrayResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets a list of string values that can be selected by the user, similar to[setChoiceValues(java.lang.String[])](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#setChoiceValues(kotlin.Array)). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setChoiceValues](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#setChoiceValues(kotlin.Array))`(`choiceValues:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Sets a list of string values that can be selected by the user. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDescription](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#setDescription(kotlin.String))`(`description:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the user-visible description of the entry, as a possible sub-text for the title. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIntValue](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#setIntValue(kotlin.Int))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the integer value of the entry when the type is [TYPE_INTEGER](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_INTEGER:kotlin.Int). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRestrictions](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#setRestrictions(kotlin.Array))`(`restrictions:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [RestrictionEntry](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#)!>!`)` Sets an array of possible restriction entries, that this entry may contain. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSelectedState](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#setSelectedState(kotlin.Boolean))`(`state:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the current selected state for an entry of type [TYPE_BOOLEAN](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_BOOLEAN:kotlin.Int). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSelectedString](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#setSelectedString(kotlin.String))`(`selectedString:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the string value to use as the selected value for this restriction. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTitle](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#setTitle(kotlin.String))`(`title:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the user-visible title for the entry. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setType](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#setType(kotlin.Int))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the type for this restriction. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#toString())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [RestrictionEntry](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### TYPE_BOOLEAN

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_BOOLEAN: Int
```

Restriction of type "bool". Use this for storing a boolean value, typically presented as a checkbox in the UI. 

 Value: 1

### TYPE_BUNDLE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_BUNDLE: Int
```

Restriction of type "bundle". Use this for storing [bundles](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) of restrictions 

 Value: 7

### TYPE_BUNDLE_ARRAY

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_BUNDLE_ARRAY: Int
```

Restriction of type "bundle_array". Use this for storing arrays of [bundles](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) of restrictions 

 Value: 8

### TYPE_CHOICE

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_CHOICE: Int
```

Restriction of type "choice". Use this for storing a string value, typically presented as a single-select list. Call[setChoiceEntries(java.lang.String[])](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#setChoiceEntries(kotlin.Array))and[setChoiceValues(java.lang.String[])](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#setChoiceValues(kotlin.Array))to set the localized list entries to present to the user and the corresponding values, respectively. 

 Value: 2

### TYPE_INTEGER

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_INTEGER: Int
```

Restriction of type "integer". Use this for storing an integer value. The range of values is from [Integer.MIN_VALUE](https://developer.android.com/reference/kotlin/java/lang/Integer.html#MIN_VALUE:kotlin.Int) to [Integer.MAX_VALUE](https://developer.android.com/reference/kotlin/java/lang/Integer.html#MAX_VALUE:kotlin.Int). 

 Value: 5

### TYPE_MULTI_SELECT

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_MULTI_SELECT: Int
```

Restriction of type "multi-select". Use this for presenting a multi-select list where more than one entry can be selected, such as for choosing specific titles to allowlist. Call[setChoiceEntries(java.lang.String[])](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#setChoiceEntries(kotlin.Array))and[setChoiceValues(java.lang.String[])](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#setChoiceValues(kotlin.Array))to set the localized list entries to present to the user and the corresponding values, respectively. Use [getAllSelectedStrings()](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#getAllSelectedStrings())and[setAllSelectedStrings(java.lang.String[])](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#setAllSelectedStrings(kotlin.Array))to manipulate the selections. 

 Value: 4

### TYPE_NULL

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_NULL: Int
```

Hidden restriction type. Use this type for information that needs to be transferred across but shouldn't be presented to the user in the UI. Stores a single String value. 

 Value: 0

### TYPE_STRING

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_STRING: Int
```

Restriction of type "string". Use this for storing a string value. 

 Value: 6

**See Also**

- [#setSelectedString](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#setSelectedString(kotlin.String))
- [#getSelectedString](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#getSelectedString())

## Public constructors

### RestrictionEntry

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RestrictionEntry(in: Parcel!)
```  

### RestrictionEntry

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RestrictionEntry(
    type: Int, 
    key: String!)
```

Constructor for specifying the type and key, with no initial value;

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the restriction type. |
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the unique key for this restriction |

### RestrictionEntry

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RestrictionEntry(
    key: String!, 
    selectedState: Boolean)
```

Constructor for [TYPE_BOOLEAN](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_BOOLEAN:kotlin.Int) type.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the unique key for this restriction |
| `selectedState` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether this restriction is selected or not |

### RestrictionEntry

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RestrictionEntry(
    key: String!, 
    selectedInt: Int)
```

Constructor for [TYPE_INTEGER](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_INTEGER:kotlin.Int) type.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the unique key for this restriction |
| `selectedInt` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the integer value of the restriction |

### RestrictionEntry

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RestrictionEntry(
    key: String!, 
    selectedString: String!)
```

Constructor for [TYPE_CHOICE](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_CHOICE:kotlin.Int) type.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the unique key for this restriction |
| `selectedString` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the current value |

### RestrictionEntry

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RestrictionEntry(
    key: String!, 
    selectedStrings: Array<String!>!)
```

Constructor for [TYPE_MULTI_SELECT](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_MULTI_SELECT:kotlin.Int) type.

| Parameters ||
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the unique key for this restriction |
| `selectedStrings` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:the list of values that are currently selected |

## Public methods

### createBundleArrayEntry

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun createBundleArrayEntry(
    key: String!, 
    restrictionEntries: Array<RestrictionEntry!>!
): RestrictionEntry!
```

Creates an entry of type [TYPE_BUNDLE_ARRAY](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_BUNDLE_ARRAY:kotlin.Int).

| Parameters ||
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the unique key for this restriction |
| `restrictionEntries` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [RestrictionEntry](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#)!\>!:array of nested restriction entries. The array may only contain elements of type [bundle](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_BUNDLE:kotlin.Int). |

| Return ||
|-------------------------------------------------------------------------------------------------------|-------------------------------|
| [RestrictionEntry](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#)! | the newly created restriction |

### createBundleEntry

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun createBundleEntry(
    key: String!, 
    restrictionEntries: Array<RestrictionEntry!>!
): RestrictionEntry!
```

Creates an entry of type [TYPE_BUNDLE](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_BUNDLE:kotlin.Int).

| Parameters ||
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the unique key for this restriction |
| `restrictionEntries` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [RestrictionEntry](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#)!\>!:array of nested restriction entries. |

| Return ||
|-------------------------------------------------------------------------------------------------------|-------------------------------|
| [RestrictionEntry](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#)! | the newly created restriction |

### describeContents

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
| `o` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getAllSelectedStrings

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAllSelectedStrings(): Array<String!>!
```

Returns the list of currently selected values.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | the list of current selections, if type is [TYPE_MULTI_SELECT](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_MULTI_SELECT:kotlin.Int), null otherwise. |

### getChoiceEntries

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getChoiceEntries(): Array<String!>!
```

Returns the list of strings, set earlier, that will be presented as choices to the user.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | the list of choices presented to the user. |

### getChoiceValues

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getChoiceValues(): Array<String!>!
```

Returns the list of possible string values set earlier.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | the list of possible values. |

### getDescription

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDescription(): String!
```

Returns the provided user-visible description of the entry, if any.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the user-visible description, null if none was set earlier. |

### getIntValue

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIntValue(): Int
```

Returns the value of the entry as an integer when the type is [TYPE_INTEGER](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_INTEGER:kotlin.Int).

| Return ||
|----------------------------------------------------------------------------|---------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the integer value of the entry. |

### getKey

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKey(): String!
```

This is the unique key for the restriction entry.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the key for the restriction. |

### getRestrictions

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRestrictions(): Array<RestrictionEntry!>!
```

Returns array of possible restriction entries that this entry may contain. 

### getSelectedState

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSelectedState(): Boolean
```

Returns the current selected state for an entry of type [TYPE_BOOLEAN](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_BOOLEAN:kotlin.Int).

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the current selected state of the entry. |

### getSelectedString

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSelectedString(): String!
```

Returns the currently selected string value.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the currently selected value, which can be null for types that aren't for holding single string values. |

### getTitle

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTitle(): String!
```

Returns the user-visible title for the entry, if any.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the user-visible title for the entry, null if none was set earlier. |

### getType

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getType(): Int
```

Returns the type for this restriction.

| Return ||
|----------------------------------------------------------------------------|-------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the type for this restriction |

### hashCode

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### setAllSelectedStrings

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAllSelectedStrings(allSelectedStrings: Array<String!>!): Unit
```

Sets the current list of selected values for an entry of type [TYPE_MULTI_SELECT](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_MULTI_SELECT:kotlin.Int). These values will be persisted by the system for later use by the application.

| Parameters ||
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `allSelectedStrings` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:the current list of selected values. |

### setChoiceEntries

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setChoiceEntries(
    context: Context!, 
    stringArrayResId: Int
): Unit
```

Sets a list of strings that will be presented as choices to the user. This is similar to[setChoiceEntries(java.lang.String[])](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#setChoiceEntries(kotlin.Array)).

| Parameters ||
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context)!:the application context, used for retrieving the resources. |
| `stringArrayResId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the resource id of a string array containing the possible entries. |

### setChoiceEntries

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setChoiceEntries(choiceEntries: Array<String!>!): Unit
```

Sets a list of strings that will be presented as choices to the user. When the user selects one or more of these choices, the corresponding value from the possible values are stored as the selected strings. The size of this array must match the size of the array set in[setChoiceValues(java.lang.String[])](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#setChoiceValues(kotlin.Array)). This method is not relevant for types other than [TYPE_CHOICE](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_CHOICE:kotlin.Int), and [TYPE_MULTI_SELECT](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_MULTI_SELECT:kotlin.Int).

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `choiceEntries` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:the list of user-visible choices. |

**See Also**

- [#setChoiceValues(String[])](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#setChoiceValues(kotlin.Array)) 

### setChoiceValues

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setChoiceValues(
    context: Context!, 
    stringArrayResId: Int
): Unit
```

Sets a list of string values that can be selected by the user, similar to[setChoiceValues(java.lang.String[])](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#setChoiceValues(kotlin.Array)).

| Parameters ||
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context)!:the application context for retrieving the resources. |
| `stringArrayResId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the resource id for a string array containing the possible values. |

**See Also**

- [#setChoiceValues(String[])](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#setChoiceValues(kotlin.Array)) 

### setChoiceValues

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setChoiceValues(choiceValues: Array<String!>!): Unit
```

Sets a list of string values that can be selected by the user. If no user-visible entries are set by a call to[setChoiceEntries(java.lang.String[])](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#setChoiceEntries(kotlin.Array)), these values will be the ones shown to the user. Values will be chosen from this list as the user's selection and the selected values can be retrieved by a call to [getAllSelectedStrings()](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#getAllSelectedStrings()), or [getSelectedString()](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#getSelectedString()), depending on whether it is a multi-select type or choice type. This method is not relevant for types other than [TYPE_CHOICE](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_CHOICE:kotlin.Int), and [TYPE_MULTI_SELECT](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_MULTI_SELECT:kotlin.Int).

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `choiceValues` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:an array of Strings which will be the selected values for the user's selections. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#getChoiceValues()>
- <https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#getAllSelectedStrings()> 

### setDescription

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDescription(description: String!): Unit
```

Sets the user-visible description of the entry, as a possible sub-text for the title. You can use this to describe the entry in more detail or to display the current state of the restriction.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------|
| `description` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the user-visible description string. |

### setIntValue

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setIntValue(value: Int): Unit
```

Sets the integer value of the entry when the type is [TYPE_INTEGER](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_INTEGER:kotlin.Int).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------|
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the integer value to set. |

### setRestrictions

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setRestrictions(restrictions: Array<RestrictionEntry!>!): Unit
```

Sets an array of possible restriction entries, that this entry may contain.

This method is only relevant for types [TYPE_BUNDLE](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_BUNDLE:kotlin.Int) and [TYPE_BUNDLE_ARRAY](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_BUNDLE_ARRAY:kotlin.Int) 

### setSelectedState

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSelectedState(state: Boolean): Unit
```

Sets the current selected state for an entry of type [TYPE_BOOLEAN](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_BOOLEAN:kotlin.Int). This value will be persisted by the system for later use by the application.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------|
| `state` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the current selected state |

### setSelectedString

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSelectedString(selectedString: String!): Unit
```

Sets the string value to use as the selected value for this restriction. This value will be persisted by the system for later use by the application.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------|
| `selectedString` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the string value to select. |

### setTitle

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTitle(title: String!): Unit
```

Sets the user-visible title for the entry.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------|
| `title` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the user-visible title for the entry. |

### setType

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setType(type: Int): Unit
```

Sets the type for this restriction.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the type for this restriction. |

### toString

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<RestrictionEntry!>
```
