# ClipData

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ClipData

Kotlin| [Java](ClipData.md) 
| --- | --- |

```
open class ClipData : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.ClipData](ClipData.md) |

Representation of a clipped data on the clipboard.

ClipData is a complex type containing one or more Item instances, each of which can hold one or more representations of an item of data. For display to the user, it also has a label.

A ClipData contains a [ClipDescription](ClipDescription.md), which describes important meta-data about the clip. In particular, its [getDescription().getMimeType(int)](ClipDescription.md))must return correct MIME type(s) describing the data in the clip. For help in correctly constructing a clip with the correct MIME type, use [newPlainText(java.lang.CharSequence,java.lang.CharSequence)](ClipData.md)), [newUri(android.content.ContentResolver,java.lang.CharSequence,android.net.Uri)](ClipData.md)), and [newIntent(java.lang.CharSequence,android.content.Intent)](ClipData.md)).

Each Item instance can be one of three main classes of data: a simple CharSequence of text, a single Intent object, or a Uri. See [Item](../android/content/ClipData.Item.md) for more details.
|
| ### Developer Guides
|
| For more information about using the clipboard framework, read the [Copy and Paste](https://developer.android.com/guide/topics/clipboard/copy-paste.html) developer guide.

### Implementing Paste or Drop

To implement a paste or drop of a ClipData object into an application, the application must correctly interpret the data for its use. If the [Item](../android/content/ClipData.Item.md) it contains is simple text or an Intent, there is little to be done: text can only be interpreted as text, and an Intent will typically be used for creating shortcuts (such as placing icons on the home screen) or other actions.

If all you want is the textual representation of the clipped data, you can use the convenience method [Item.coerceToText](../android/content/ClipData.Item.md)). In this case there is generally no need to worry about the MIME types reported by [getDescription().getMimeType(int)](ClipDescription.md)), since any clip item can always be converted to a string.

More complicated exchanges will be done through URIs, in particular "content:" URIs. A content URI allows the recipient of a ClipData item to interact closely with the ContentProvider holding the data in order to negotiate the transfer of that data. The clip must also be filled in with the available MIME types; [newUri(android.content.ContentResolver,java.lang.CharSequence,android.net.Uri)](ClipData.md))will take care of correctly doing this.

For example, here is the paste function of a simple NotePad application. When retrieving the data from the clipboard, it can do either two things: if the clipboard contains a URI reference to an existing note, it copies the entire structure of the note into a new note; otherwise, it simply coerces the clip into text and uses that as the new note's contents.

In many cases an application can paste various types of streams of data. For example, an e-mail application may want to allow the user to paste an image or other binary data as an attachment. This is accomplished through the ContentResolver [ContentResolver.getStreamTypes(Uri, String)](ContentResolver.md))and [ContentResolver.openTypedAssetFileDescriptor(Uri, String, android.os.Bundle)](ContentResolver.md))methods. These allow a client to discover the type(s) of data that a particular content URI can make available as a stream and retrieve the stream of data.

For example, the implementation of [Item.coerceToText](../android/content/ClipData.Item.md))itself uses this to try to retrieve a URI clip as a stream of text:

### Implementing Copy or Drag

To be the source of a clip, the application must construct a ClipData object that any recipient can interpret best for their context. If the clip is to contain a simple text, Intent, or URI, this is easy: an [Item](../android/content/ClipData.Item.md) containing the appropriate data type can be constructed and used.

More complicated data types require the implementation of support in a ContentProvider for describing and generating the data for the recipient. A common scenario is one where an application places on the clipboard the content: URI of an object that the user has copied, with the data at that URI consisting of a complicated structure that only other applications with direct knowledge of the structure can use.

For applications that do not have intrinsic knowledge of the data structure, the content provider holding it can make the data available as an arbitrary number of types of data streams. This is done by implementing the ContentProvider [ContentProvider.getStreamTypes(Uri, String)](ContentProvider.md))and [ContentProvider.openTypedAssetFile(Uri, String, android.os.Bundle)](ContentProvider.md))methods.

Going back to our simple NotePad application, this is the implementation it may have to convert a single note URI (consisting of a title and the note text) into a stream of plain text data.

The copy operation in our NotePad application is now just a simple matter of making a clip containing the URI of the note being copied:

Note if a paste operation needs this clip as text (for example to paste into an editor), then [Item.coerceToText(Context)](../android/content/ClipData.Item.md))will ask the content provider for the clip URI as text and successfully paste the entire note.

## Summary

| Nested classes ||
|------|----------------------------------------------------------------------------------------------------------------------------------|
| open | [Item](../android/content/ClipData.Item.md) Description of a single item in a ClipData. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ClipData](ClipData.md))`(`other:` ` [ClipData](ClipData.md)!`)` Create a new clip that is a copy of another clip. |
| [ClipData](ClipData.md))`(`description:` ` [ClipDescription](ClipDescription.md)!`, `item:` ` [ClipData.Item](../android/content/ClipData.Item.md)!`)` Create a new clip. |
| [ClipData](ClipData.md))`(`label:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `mimeTypes:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `item:` ` [ClipData.Item](../android/content/ClipData.Item.md)!`)` Create a new clip. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addItem](ClipData.md))`(`item:` ` [ClipData.Item](../android/content/ClipData.Item.md)!`)` Add a new Item to the overall ClipData container. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addItem](ClipData.md))`(`resolver:` ` [ContentResolver](ContentResolver.md)!`, `item:` ` [ClipData.Item](../android/content/ClipData.Item.md)!`)` Add a new Item to the overall ClipData container. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](ClipData.md))`()` <br /> |
| --- | --- |
| open [ClipDescription](ClipDescription.md)! | [getDescription](ClipData.md))`()` Return the [ClipDescription](ClipDescription.md) associated with this data, describing what it contains. |
| open [ClipData.Item](../android/content/ClipData.Item.md)! | [getItemAt](ClipData.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return a single item inside of the clip data. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getItemCount](ClipData.md))`()` Return the number of items in the clip data. |
| --- | --- |
| openstatic [ClipData](ClipData.md)! | [newHtmlText](ClipData.md))`(`label:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `htmlText:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a new ClipData holding data of the type [ClipDescription.MIMETYPE_TEXT_HTML](ClipDescription.md). |
| openstatic [ClipData](ClipData.md)! | [newIntent](ClipData.md))`(`label:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `intent:` ` [Intent](Intent.md)!`)` Create a new ClipData holding an Intent with MIME type [ClipDescription.MIMETYPE_TEXT_INTENT](ClipDescription.md). |
| openstatic [ClipData](ClipData.md)! | [newPlainText](ClipData.md))`(`label:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Create a new ClipData holding data of the type [ClipDescription.MIMETYPE_TEXT_PLAIN](ClipDescription.md). |
| --- | --- |
| openstatic [ClipData](ClipData.md)! | [newRawUri](ClipData.md))`(`label:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `uri:` ` [Uri](../android.net/Uri.md)!`)` Create a new ClipData holding an URI with MIME type [ClipDescription.MIMETYPE_TEXT_URILIST](ClipDescription.md). |
| openstatic [ClipData](ClipData.md)! | [newUri](ClipData.md))`(`resolver:` ` [ContentResolver](ContentResolver.md)!`, `label:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `uri:` ` [Uri](../android.net/Uri.md)!`)` Create a new ClipData holding a URI. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](ClipData.md))`()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](ClipData.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [ClipData](ClipData.md)!\> | [CREATOR](ClipData.md) <br /> |

## Public constructors

### ClipData

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ClipData(other: ClipData!)
```

Create a new clip that is a copy of another clip. This does a deep-copy of all items in the clip.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------|
| `other` | [ClipData](ClipData.md)!:The existing ClipData that is to be copied. |

### ClipData

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ClipData(
    description: ClipDescription!, 
    item: ClipData.Item!)
```

Create a new clip.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `description` | [ClipDescription](ClipDescription.md)!:The ClipDescription describing the clip contents. |
| `item` | [ClipData.Item](../android/content/ClipData.Item.md)!:The contents of the first item in the clip. |

### ClipData

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ClipData(
    label: CharSequence!, 
    mimeTypes: Array<String!>!, 
    item: ClipData.Item!)
```

Create a new clip.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `label` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:Label to show to the user describing this clip. |
| `mimeTypes` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:An array of MIME types this data is available as. |
| `item` | [ClipData.Item](../android/content/ClipData.Item.md)!:The contents of the first item in the clip. |
| --- | --- |

## Public methods

### addItem

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addItem(item: ClipData.Item!): Unit
```

Add a new Item to the overall ClipData container.

This method will*not* update the list of available MIME types in the [ClipDescription](ClipDescription.md). It should be used only when adding items which do not add new MIME types to this clip. If this is not the case, use [addItem(android.content.ContentResolver,android.content.ClipData.Item)](ClipData.md))or call[ClipData(java.lang.CharSequence,java.lang.String[],android.content.ClipData.Item)](https://developer.android.com/reference/kotlin/android/content/ClipData#ClipData(kotlin.CharSequence,%20kotlin.Array,%20android.content.ClipData.Item))with a complete list of MIME types.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------|
| `item` | [ClipData.Item](../android/content/ClipData.Item.md)!:Item to be added. |

### addItem

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addItem(
    resolver: ContentResolver!, 
    item: ClipData.Item!
): Unit
```

Add a new Item to the overall ClipData container.

Unlike [addItem(android.content.ClipData.Item)](ClipData.md)), this method will update the list of available MIME types in the [ClipDescription](ClipDescription.md).

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `resolver` | [ContentResolver](ContentResolver.md)!:ContentResolver used to get information about the URI possibly contained in the item. |
| `item` | [ClipData.Item](../android/content/ClipData.Item.md)!:Item to be added. |

### describeContents

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### getDescription

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDescription(): ClipDescription!
```

Return the [ClipDescription](ClipDescription.md) associated with this data, describing what it contains. 

### getItemAt

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getItemAt(index: Int): ClipData.Item!
```

Return a single item inside of the clip data. The index can range from 0 to [getItemCount()](ClipData.md))-1. 

### getItemCount

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getItemCount(): Int
```

Return the number of items in the clip data. 

### newHtmlText

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newHtmlText(
    label: CharSequence!, 
    text: CharSequence!, 
    htmlText: String!
): ClipData!
```

Create a new ClipData holding data of the type [ClipDescription.MIMETYPE_TEXT_HTML](ClipDescription.md).

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `label` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:User-visible label for the clip data. |
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:The text of clip as plain text, for receivers that don't handle HTML. This is required. |
| `htmlText` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The actual HTML text in the clip. |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------------|-------------------------------------------------------|
| [ClipData](ClipData.md)! | Returns a new ClipData containing the specified data. |

### newIntent

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newIntent(
    label: CharSequence!, 
    intent: Intent!
): ClipData!
```

Create a new ClipData holding an Intent with MIME type [ClipDescription.MIMETYPE_TEXT_INTENT](ClipDescription.md).

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `label` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:User-visible label for the clip data. |
| `intent` | [Intent](Intent.md)!:The actual Intent in the clip. |

| Return ||
|---------------------------------------------------------------------------------------|-------------------------------------------------------|
| [ClipData](ClipData.md)! | Returns a new ClipData containing the specified data. |

### newPlainText

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newPlainText(
    label: CharSequence!, 
    text: CharSequence!
): ClipData!
```

Create a new ClipData holding data of the type [ClipDescription.MIMETYPE_TEXT_PLAIN](ClipDescription.md).

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------|
| `label` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:User-visible label for the clip data. |
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:The actual text in the clip. |

| Return ||
|---------------------------------------------------------------------------------------|-------------------------------------------------------|
| [ClipData](ClipData.md)! | Returns a new ClipData containing the specified data. |

### newRawUri

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newRawUri(
    label: CharSequence!, 
    uri: Uri!
): ClipData!
```

Create a new ClipData holding an URI with MIME type [ClipDescription.MIMETYPE_TEXT_URILIST](ClipDescription.md). Unlike [newUri(android.content.ContentResolver,java.lang.CharSequence,android.net.Uri)](ClipData.md)), nothing is inferred about the URI -- if it is a content: URI holding a bitmap, the reported type will still be uri-list. Use this with care!

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------|
| `label` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:User-visible label for the clip data. |
| `uri` | [Uri](../android.net/Uri.md)!:The URI in the clip. |

| Return ||
|---------------------------------------------------------------------------------------|-------------------------------------------------------|
| [ClipData](ClipData.md)! | Returns a new ClipData containing the specified data. |

### newUri

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newUri(
    resolver: ContentResolver!, 
    label: CharSequence!, 
    uri: Uri!
): ClipData!
```

Create a new ClipData holding a URI. If the URI is a content: URI, this will query the content provider for the MIME type of its data and use that as the MIME type. Otherwise, it will use the MIME type [ClipDescription.MIMETYPE_TEXT_URILIST](ClipDescription.md).

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `resolver` | [ContentResolver](ContentResolver.md)!:ContentResolver used to get information about the URI. |
| `label` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:User-visible label for the clip data. |
| `uri` | [Uri](../android.net/Uri.md)!:The URI in the clip. |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------------|-------------------------------------------------------|
| [ClipData](ClipData.md)! | Returns a new ClipData containing the specified data. |

### toString

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android.os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<ClipData!>
```
