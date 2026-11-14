# TvInputInfo

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TvInputInfo

Kotlin| [Java](../android/media/tv/TvInputInfo.md) 
| --- | --- |

```
class TvInputInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.tv.TvInputInfo](../android/media/tv/TvInputInfo.md) |

This class is used to specify meta information of a TV input.

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/media/tv/TvInputInfo.Builder.md) A convenience builder for creating [TvInputInfo](../android/media/tv/TvInputInfo.md) objects. |

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_INPUT_ID](../android/media/tv/TvInputInfo.md) Used as a String extra field in setup intents created by [createSetupIntent()](../android/media/tv/TvInputInfo.md))to supply the ID of a specific TV input to set up. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_COMPONENT](../android/media/tv/TvInputInfo.md) TV input type: the TV input service represents a component port. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_COMPOSITE](../android/media/tv/TvInputInfo.md) TV input type: the TV input service represents a composite port. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_DISPLAY_PORT](../android/media/tv/TvInputInfo.md) TV input type: the TV input service represents a display port. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_DVI](../android/media/tv/TvInputInfo.md) TV input type: the TV input service represents a DVI port. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_HDMI](../android/media/tv/TvInputInfo.md) TV input type: the TV input service is HDMI. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_OTHER](../android/media/tv/TvInputInfo.md) TV input type: a generic hardware TV input type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_SCART](../android/media/tv/TvInputInfo.md) TV input type: the TV input service represents a SCART port. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_SVIDEO](../android/media/tv/TvInputInfo.md) TV input type: the TV input service represents a SVIDEO port. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TUNER](../android/media/tv/TvInputInfo.md) TV input type: the TV input service is a tuner which provides channels. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_VGA](../android/media/tv/TvInputInfo.md) TV input type: the TV input service represents a VGA port. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canPauseRecording](../android/media/tv/TvInputInfo.md))`()` Returns`true`if this TV input can pause recording TV programs,`false`otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canRecord](../android/media/tv/TvInputInfo.md))`()` Returns`true`if this TV input can record TV programs,`false`otherwise. |
| [Intent](../android/content/Intent.md)! | [createSettingsIntent](../android/media/tv/TvInputInfo.md))`()` Returns an intent to start the settings activity for this TV input. |
| --- | --- |
| [Intent](../android/content/Intent.md)! | [createSetupIntent](../android/media/tv/TvInputInfo.md))`()` Returns an intent to start the setup activity for this TV input. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/media/tv/TvInputInfo.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/media/tv/TvInputInfo.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| --- | --- |
| [Bundle](../android/os/Bundle.md)! | [getExtras](../android/media/tv/TvInputInfo.md))`()` Returns domain-specific extras associated with this TV input. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getId](../android/media/tv/TvInputInfo.md))`()` Returns a unique ID for this TV input. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getParentId](../android/media/tv/TvInputInfo.md))`()` Returns the parent input ID. |
| --- | --- |
| [ServiceInfo](../android/content/pm/ServiceInfo.md)! | [getServiceInfo](../android/media/tv/TvInputInfo.md))`()` Returns the information of the service that implements this TV input. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTunerCount](../android/media/tv/TvInputInfo.md))`()` Returns the number of tuners this TV input has. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](../android/media/tv/TvInputInfo.md))`()` Returns the type of this TV input. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/media/tv/TvInputInfo.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isHidden](../android/media/tv/TvInputInfo.md))`(`context:` ` [Context](../android/content/Context.md)!`)` Checks if this TV input is marked hidden by the user in the settings. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPassthroughInput](../android/media/tv/TvInputInfo.md))`()` Returns`true`if this TV input is pass-though which does not have any real channels in TvProvider. |
| --- | --- |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [loadCustomLabel](../android/media/tv/TvInputInfo.md))`(`context:` ` [Context](../android/content/Context.md)!`)` Loads the custom label set by user in settings. |
| [Drawable](../android/graphics/drawable/Drawable.md)! | [loadIcon](../android/media/tv/TvInputInfo.md))`(`context:` ` [Context](../android/content/Context.md)`)` Loads the user-displayed icon for this TV input. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [loadLabel](../android/media/tv/TvInputInfo.md))`(`context:` ` [Context](../android/content/Context.md)`)` Loads the user-displayed label for this TV input. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/media/tv/TvInputInfo.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/media/tv/TvInputInfo.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Used to package this object into a [Parcel](../android/os/Parcel.md). |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [TvInputInfo](../android/media/tv/TvInputInfo.md)!\> | [CREATOR](../android/media/tv/TvInputInfo.md) <br /> |

## Constants

### EXTRA_INPUT_ID

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_INPUT_ID: String
```

Used as a String extra field in setup intents created by [createSetupIntent()](../android/media/tv/TvInputInfo.md))to supply the ID of a specific TV input to set up. 

 Value: "android.media.tv.extra.INPUT_ID"

### TYPE_COMPONENT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_COMPONENT: Int
```

TV input type: the TV input service represents a component port. 

 Value: 1004

### TYPE_COMPOSITE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_COMPOSITE: Int
```

TV input type: the TV input service represents a composite port. 

 Value: 1001

### TYPE_DISPLAY_PORT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_DISPLAY_PORT: Int
```

TV input type: the TV input service represents a display port. 

 Value: 1008

### TYPE_DVI

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_DVI: Int
```

TV input type: the TV input service represents a DVI port. 

 Value: 1006

### TYPE_HDMI

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_HDMI: Int
```

TV input type: the TV input service is HDMI. (e.g. HDMI 1) 

 Value: 1007

### TYPE_OTHER

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_OTHER: Int
```

TV input type: a generic hardware TV input type. 

 Value: 1000

### TYPE_SCART

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_SCART: Int
```

TV input type: the TV input service represents a SCART port. 

 Value: 1003

### TYPE_SVIDEO

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_SVIDEO: Int
```

TV input type: the TV input service represents a SVIDEO port. 

 Value: 1002

### TYPE_TUNER

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TUNER: Int
```

TV input type: the TV input service is a tuner which provides channels. 

 Value: 0

### TYPE_VGA

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_VGA: Int
```

TV input type: the TV input service represents a VGA port. 

 Value: 1005

## Public methods

### canPauseRecording

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun canPauseRecording(): Boolean
```

Returns`true`if this TV input can pause recording TV programs,`false`otherwise. 

### canRecord

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun canRecord(): Boolean
```

Returns`true`if this TV input can record TV programs,`false`otherwise. 

### createSettingsIntent

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun createSettingsIntent(): Intent!
```

**Deprecated:** *Use [createSetupIntent()](../android/media/tv/TvInputInfo.md))instead. Settings activity is deprecated. Use setup activity instead to provide settings.*

Returns an intent to start the settings activity for this TV input. 

### createSetupIntent

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun createSetupIntent(): Intent!
```

Returns an intent to start the setup activity for this TV input. 

### describeContents

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### equals

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getExtras

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getExtras(): Bundle!
```

Returns domain-specific extras associated with this TV input. 

### getId

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getId(): String!
```

Returns a unique ID for this TV input. The ID is generated from the package and class name implementing the TV input service. 

### getParentId

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getParentId(): String!
```

Returns the parent input ID.

A TV input may have a parent input if the TV input is actually a logical representation of a device behind the hardware port represented by the parent input. For example, a HDMI CEC logical device, connected to a HDMI port, appears as another TV input. In this case, the parent input of this logical device is the HDMI port.

Applications may group inputs by parent input ID to provide an easier access to inputs sharing the same physical port. In the example of HDMI CEC, logical HDMI CEC devices behind the same HDMI port have the same parent ID, which is the ID representing the port. Thus applications can group the hardware HDMI port and the logical HDMI CEC devices behind it together using this method.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the ID of the parent input, if exists. Returns`null`if the parent input is not specified. |

### getServiceInfo

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getServiceInfo(): ServiceInfo!
```

Returns the information of the service that implements this TV input. 

### getTunerCount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTunerCount(): Int
```

Returns the number of tuners this TV input has.

This method is valid only for inputs of type [TYPE_TUNER](../android/media/tv/TvInputInfo.md). For inputs of other types, it returns 0.

Tuners correspond to physical/logical resources that allow reception of TV signal. Having*N* tuners means that the TV input is capable of receiving*N*different channels concurrently. 

### getType

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getType(): Int
```

Returns the type of this TV input.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.tv.TvInputInfo#TYPE_TUNER](../android/media/tv/TvInputInfo.md), [android.media.tv.TvInputInfo#TYPE_OTHER](../android/media/tv/TvInputInfo.md), [android.media.tv.TvInputInfo#TYPE_COMPOSITE](../android/media/tv/TvInputInfo.md), [android.media.tv.TvInputInfo#TYPE_SVIDEO](../android/media/tv/TvInputInfo.md), [android.media.tv.TvInputInfo#TYPE_SCART](../android/media/tv/TvInputInfo.md), [android.media.tv.TvInputInfo#TYPE_COMPONENT](../android/media/tv/TvInputInfo.md), [android.media.tv.TvInputInfo#TYPE_VGA](../android/media/tv/TvInputInfo.md), [android.media.tv.TvInputInfo#TYPE_DVI](../android/media/tv/TvInputInfo.md), [android.media.tv.TvInputInfo#TYPE_HDMI](../android/media/tv/TvInputInfo.md), or [android.media.tv.TvInputInfo#TYPE_DISPLAY_PORT](../android/media/tv/TvInputInfo.md) |

### hashCode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isHidden

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isHidden(context: Context!): Boolean
```

Checks if this TV input is marked hidden by the user in the settings.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:Supplies a [Context](../android/content/Context.md) used to check if this TV input is hidden. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the user marked this TV input hidden in settings.`false`otherwise. |

### isPassthroughInput

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isPassthroughInput(): Boolean
```

Returns`true`if this TV input is pass-though which does not have any real channels in TvProvider.`false`otherwise. 
**See Also**

- [android.media.tv.TvContract#buildChannelUriForPassthroughInput(String)](../android/media/tv/TvContract.md)) 

### loadCustomLabel

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun loadCustomLabel(context: Context!): CharSequence!
```

Loads the custom label set by user in settings.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:Supplies a [Context](../android/content/Context.md) used to load the custom label. |

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | a CharSequence containing the TV input's custom label.`null`if there is no custom label. |

### loadIcon

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun loadIcon(context: Context): Drawable!
```

Loads the user-displayed icon for this TV input.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md):Supplies a [Context](../android/content/Context.md) used to load the icon. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Drawable](../android/graphics/drawable/Drawable.md)! | a Drawable containing the TV input's icon. If the TV input does not have an icon, application's icon is returned. If it's unavailable too,`null`is returned. |

### loadLabel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun loadLabel(context: Context): CharSequence!
```

Loads the user-displayed label for this TV input.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md):Supplies a [Context](../android/content/Context.md) used to load the label. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | a CharSequence containing the TV input's label. If the TV input does not have a label, its name is returned. |

### toString

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Used to package this object into a [Parcel](../android/os/Parcel.md).

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android/os/Parcel.md):The [Parcel](../android/os/Parcel.md) to be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The flags used for parceling. |

## Properties

### CREATOR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<TvInputInfo!>
```
