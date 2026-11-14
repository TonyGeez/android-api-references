# Tag

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Tag

Kotlin| [Java](../android/nfc/Tag.md) 
| --- | --- |

```
class Tag : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.nfc.Tag](../android/nfc/Tag.md) |

Represents an NFC tag that has been discovered.

[Tag](../android/nfc/Tag.md) is an immutable object that represents the state of a NFC tag at the time of discovery. It can be used as a handle to [TagTechnology](../android/nfc/tech/TagTechnology.md) classes to perform advanced operations, or directly queried for its ID via [getId](../android/nfc/Tag.md))and the set of technologies it contains via [getTechList](../android/nfc/Tag.md)). Arrays passed to and returned by this class are*not*cloned, so be careful not to modify them.

A new tag object is created every time a tag is discovered (comes into range), even if it is the same physical tag. If a tag is removed and then returned into range, then only the most recent tag object can be successfully used to create a [TagTechnology](../android/nfc/tech/TagTechnology.md).

### Tag Dispatch

When a tag is discovered, a [Tag](../android/nfc/Tag.md) object is created and passed to a single activity via the [NfcAdapter.EXTRA_TAG](../android/nfc/NfcAdapter.md) extra in an [android.content.Intent](../android/content/Intent.md) via android.content.Context#startActivity. A four stage dispatch is used to select the most appropriate activity to handle the tag. The Android OS executes each stage in order, and completes dispatch as soon as a single matching activity is found. If there are multiple matching activities found at any one stage then the Android activity chooser dialog is shown to allow the user to select the activity to receive the tag.

The Tag dispatch mechanism was designed to give a high probability of dispatching a tag to the correct activity without showing the user an activity chooser dialog. This is important for NFC interactions because they are very transient -- if a user has to move the Android device to choose an application then the connection will likely be broken.

#### 1. Foreground activity dispatch

A foreground activity that has called [NfcAdapter.enableForegroundDispatch()](../android/nfc/NfcAdapter.md))is given priority. See the documentation on [NfcAdapter.enableForegroundDispatch()](../android/nfc/NfcAdapter.md))for its usage.

#### 2. NDEF data dispatch

If the tag contains NDEF data the system inspects the first [NdefRecord](../android/nfc/NdefRecord.md) in the first [NdefMessage](../android/nfc/NdefMessage.md). If the record is a URI, SmartPoster, or MIME data android.content.Context#startActivity is called with [NfcAdapter.ACTION_NDEF_DISCOVERED](../android/nfc/NfcAdapter.md). For URI and SmartPoster records the URI is put into the intent's data field. For MIME records the MIME type is put in the intent's type field. This allows activities to register to be launched only when data they know how to handle is present on a tag. This is the preferred method of handling data on a tag since NDEF data can be stored on many types of tags and doesn't depend on a specific tag technology. See [NfcAdapter.ACTION_NDEF_DISCOVERED](../android/nfc/NfcAdapter.md) for more detail. If the tag does not contain NDEF data, or if no activity is registered for [NfcAdapter.ACTION_NDEF_DISCOVERED](../android/nfc/NfcAdapter.md) with a matching data URI or MIME type then dispatch moves to stage 3.

#### 3. Tag Technology dispatch

android.content.Context#startActivity is called with [NfcAdapter.ACTION_TECH_DISCOVERED](../android/nfc/NfcAdapter.md) to dispatch the tag to an activity that can handle the technologies present on the tag. Technologies are defined as sub-classes of [TagTechnology](../android/nfc/tech/TagTechnology.md), see the package [android.nfc.tech](../android/nfc/tech/_package.md). The Android OS looks for an activity that can handle one or more technologies in the tag. See [NfcAdapter.ACTION_TECH_DISCOVERED](../android/nfc/NfcAdapter.md) for more detail.

#### 4. Fall-back dispatch

If no activity has been matched then android.content.Context#startActivity is called with [NfcAdapter.ACTION_TAG_DISCOVERED](../android/nfc/NfcAdapter.md). This is intended as a fall-back mechanism. See [NfcAdapter.ACTION_TAG_DISCOVERED](../android/nfc/NfcAdapter.md).

### NFC Tag Background

An NFC tag is a passive NFC device, powered by the NFC field of this Android device while it is in range. Tag's can come in many forms, such as stickers, cards, key fobs, or even embedded in a more sophisticated device.

Tags can have a wide range of capabilities. Simple tags just offer read/write semantics, and contain some one time programmable areas to make read-only. More complex tags offer math operations and per-sector access control and authentication. The most sophisticated tags contain operating environments allowing complex interactions with the code executing on the tag. Use [TagTechnology](../android/nfc/tech/TagTechnology.md) classes to access a broad range of capabilities available in NFC tags.

<br />

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/nfc/Tag.md))`()` <br /> |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getId](../android/nfc/Tag.md))`()` Get the Tag Identifier (if it has one). |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getTechList](../android/nfc/Tag.md))`()` Get the technologies available in this tag, as fully qualified class names. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/nfc/Tag.md))`()` Human-readable description of the tag, for debugging. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/nfc/Tag.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [Tag](../android/nfc/Tag.md)!\> | [CREATOR](../android/nfc/Tag.md) <br /> |

## Public methods

### describeContents

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getId

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getId(): ByteArray!
```

Get the Tag Identifier (if it has one).

The tag identifier is a low level serial number, used for anti-collision and identification.

Most tags have a stable unique identifier (UID), but some tags will generate a random ID every time they are discovered (RID), and there are some tags with no ID at all (the byte array will be zero-sized).

The size and format of an ID is specific to the RF technology used by the tag.

This function retrieves the ID as determined at discovery time, and does not perform any further RF communication or block.

| Return ||
|------------------------------------------------------------------------------------------|------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | ID as byte array, never null |

### getTechList

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTechList(): Array<String!>!
```

Get the technologies available in this tag, as fully qualified class names.

A technology is an implementation of the [TagTechnology](../android/nfc/tech/TagTechnology.md) interface, and can be instantiated by calling the static`get(Tag)`method on the implementation with this Tag. The [TagTechnology](../android/nfc/tech/TagTechnology.md) object can then be used to perform advanced, technology-specific operations on a tag.

Android defines a mandatory set of technologies that must be correctly enumerated by all Android NFC devices, and an optional set of proprietary technologies. See [TagTechnology](../android/nfc/tech/TagTechnology.md) for more details.

The ordering of the returned array is undefined and should not be relied upon.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | an array of fully-qualified [TagTechnology](../android/nfc/tech/TagTechnology.md) class-names. |

### toString

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Human-readable description of the tag, for debugging.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android/os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<Tag!>
```
