# TvInputInfo

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TvInputInfo

Kotlin| [Java](https://developer.android.com/reference/android/media/tv/TvInputInfo "View this page in Java") 
| --- | --- |

```
class TvInputInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.tv.TvInputInfo](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#) |

This class is used to specify meta information of a TV input.

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo.Builder) A convenience builder for creating [TvInputInfo](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#) objects. |

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_INPUT_ID](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#EXTRA_INPUT_ID:kotlin.String) Used as a String extra field in setup intents created by [createSetupIntent()](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#createSetupIntent())to supply the ID of a specific TV input to set up. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_COMPONENT](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#TYPE_COMPONENT:kotlin.Int) TV input type: the TV input service represents a component port. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_COMPOSITE](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#TYPE_COMPOSITE:kotlin.Int) TV input type: the TV input service represents a composite port. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_DISPLAY_PORT](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#TYPE_DISPLAY_PORT:kotlin.Int) TV input type: the TV input service represents a display port. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_DVI](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#TYPE_DVI:kotlin.Int) TV input type: the TV input service represents a DVI port. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_HDMI](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#TYPE_HDMI:kotlin.Int) TV input type: the TV input service is HDMI. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_OTHER](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#TYPE_OTHER:kotlin.Int) TV input type: a generic hardware TV input type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_SCART](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#TYPE_SCART:kotlin.Int) TV input type: the TV input service represents a SCART port. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_SVIDEO](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#TYPE_SVIDEO:kotlin.Int) TV input type: the TV input service represents a SVIDEO port. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TUNER](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#TYPE_TUNER:kotlin.Int) TV input type: the TV input service is a tuner which provides channels. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_VGA](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#TYPE_VGA:kotlin.Int) TV input type: the TV input service represents a VGA port. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canPauseRecording](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#canPauseRecording())`()` Returns`true`if this TV input can pause recording TV programs,`false`otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canRecord](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#canRecord())`()` Returns`true`if this TV input can record TV programs,`false`otherwise. |
| [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)! | [createSettingsIntent](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#createSettingsIntent())`()` Returns an intent to start the settings activity for this TV input. |
| --- | --- |
| [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)! | [createSetupIntent](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#createSetupIntent())`()` Returns an intent to start the setup activity for this TV input. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| --- | --- |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | [getExtras](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#getExtras())`()` Returns domain-specific extras associated with this TV input. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getId](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#getId())`()` Returns a unique ID for this TV input. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getParentId](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#getParentId())`()` Returns the parent input ID. |
| --- | --- |
| [ServiceInfo](https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo.html#)! | [getServiceInfo](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#getServiceInfo())`()` Returns the information of the service that implements this TV input. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTunerCount](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#getTunerCount())`()` Returns the number of tuners this TV input has. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#getType())`()` Returns the type of this TV input. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#hashCode())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isHidden](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#isHidden(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` Checks if this TV input is marked hidden by the user in the settings. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPassthroughInput](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#isPassthroughInput())`()` Returns`true`if this TV input is pass-though which does not have any real channels in TvProvider. |
| --- | --- |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [loadCustomLabel](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#loadCustomLabel(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` Loads the custom label set by user in settings. |
| [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)! | [loadIcon](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#loadIcon(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`)` Loads the user-displayed icon for this TV input. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [loadLabel](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#loadLabel(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`)` Loads the user-displayed label for this TV input. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Used to package this object into a [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#). |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [TvInputInfo](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### EXTRA_INPUT_ID

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_INPUT_ID: String
```

Used as a String extra field in setup intents created by [createSetupIntent()](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#createSetupIntent())to supply the ID of a specific TV input to set up. 

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

**Deprecated:** *Use [createSetupIntent()](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#createSetupIntent())instead. Settings activity is deprecated. Use setup activity instead to provide settings.*

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

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

This method is valid only for inputs of type [TYPE_TUNER](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#TYPE_TUNER:kotlin.Int). For inputs of other types, it returns 0.

Tuners correspond to physical/logical resources that allow reception of TV signal. Having*N* tuners means that the TV input is capable of receiving*N*different channels concurrently. 

### getType

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getType(): Int
```

Returns the type of this TV input.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.tv.TvInputInfo#TYPE_TUNER](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#TYPE_TUNER:kotlin.Int), [android.media.tv.TvInputInfo#TYPE_OTHER](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#TYPE_OTHER:kotlin.Int), [android.media.tv.TvInputInfo#TYPE_COMPOSITE](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#TYPE_COMPOSITE:kotlin.Int), [android.media.tv.TvInputInfo#TYPE_SVIDEO](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#TYPE_SVIDEO:kotlin.Int), [android.media.tv.TvInputInfo#TYPE_SCART](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#TYPE_SCART:kotlin.Int), [android.media.tv.TvInputInfo#TYPE_COMPONENT](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#TYPE_COMPONENT:kotlin.Int), [android.media.tv.TvInputInfo#TYPE_VGA](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#TYPE_VGA:kotlin.Int), [android.media.tv.TvInputInfo#TYPE_DVI](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#TYPE_DVI:kotlin.Int), [android.media.tv.TvInputInfo#TYPE_HDMI](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#TYPE_HDMI:kotlin.Int), or [android.media.tv.TvInputInfo#TYPE_DISPLAY_PORT](https://developer.android.com/reference/kotlin/android/media/tv/TvInputInfo#TYPE_DISPLAY_PORT:kotlin.Int) |

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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:Supplies a [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#) used to check if this TV input is hidden. |

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

- [android.media.tv.TvContract#buildChannelUriForPassthroughInput(String)](https://developer.android.com/reference/kotlin/android/media/tv/TvContract#buildChannelUriForPassthroughInput(kotlin.String)) 

### loadCustomLabel

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun loadCustomLabel(context: Context!): CharSequence!
```

Loads the custom label set by user in settings.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:Supplies a [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#) used to load the custom label. |

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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#):Supplies a [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#) used to load the icon. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)! | a Drawable containing the TV input's icon. If the TV input does not have an icon, application's icon is returned. If it's unavailable too,`null`is returned. |

### loadLabel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun loadLabel(context: Context): CharSequence!
```

Loads the user-displayed label for this TV input.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#):Supplies a [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#) used to load the label. This value cannot be`null`. |

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

Used to package this object into a [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#).

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#) to be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The flags used for parceling. |

## Properties

### CREATOR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<TvInputInfo!>
```
