Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextClassification

Kotlin | [Java](https://developer.android.com/reference/android/view/textclassifier/TextClassification "View this page in Java")

```
class TextClassification : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.view.textclassifier.TextClassification](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassification#) |

Information for generating a widget to handle classified text.

A TextClassification object contains icons, labels, onClickListeners and intents that may be used to build a widget that can be used to act on classified text. There is the concept of a *primary action* and other *secondary actions*.

e.g. building a view that, when clicked, shares the classified text with the preferred app:

```kotlin
<code>// Called preferably outside the UiThread.
    TextClassification classification = textClassifier.classifyText(allText, 10, 25);
 
    // Called on the UiThread.
    Button button = new Button(context);
    button.setCompoundDrawablesWithIntrinsicBounds(classification.getIcon(), null, null, null);
    button.setText(classification.getLabel());
    button.setOnClickListener(v -&gt; classification.getActions().get(0).getActionIntent().send());
  </code>
```

e.g. starting an action mode with menu items that can handle the classified text:

```kotlin
<code>// Called preferably outside the UiThread.
    final TextClassification classification = textClassifier.classifyText(allText, 10, 25);
 
    // Called on the UiThread.
    view.startActionMode(new ActionMode.Callback() {
 
        public boolean onCreateActionMode(ActionMode mode, Menu menu) {
            for (int i = 0; i &lt; classification.getActions().size(); ++i) {
               RemoteAction action = classification.getActions().get(i);
               menu.add(Menu.NONE, i, 20, action.getTitle())
                  .setIcon(action.getIcon());
            }
            return true;
        }
 
        public boolean onActionItemClicked(ActionMode mode, MenuItem item) {
            classification.getActions().get(item.getItemId()).getActionIntent().send();
            return true;
        }
 
        ...
    });
  </code>
```

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassification.Builder` Builder for building `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassification#` objects. |
| | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassification.Request` A request object for generating TextClassification. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassification#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [RemoteAction](https://developer.android.com/reference/kotlin/android/app/RemoteAction.html#)!\>! | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassification#getActions()()` Returns a list of actions that may be performed on the text. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassification#getConfidenceScore(kotlin.String)(entity: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns the confidence score for the specified entity. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassification#getEntity(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the entity at the specified index. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassification#getEntityCount()()` Returns the number of entities found in the classified text. |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassification#getExtras()()` Returns the extended data. |
| [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)? | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassification#getIcon()()` Returns an icon that may be rendered on a widget used to act on the classified text. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassification#getId()()` Returns the id, if one exists, for this object. |
| [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)? | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassification#getIntent()()` Returns an intent that may be fired to act on the classified text. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassification#getLabel()()` Returns a label that may be rendered on a widget used to act on the classified text. |
| [View.OnClickListener](https://developer.android.com/reference/kotlin/android/view/View.OnClickListener.html#)? | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassification#getOnClickListener()()` Returns the OnClickListener that may be triggered to act on the classified text. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassification#getText()()` Gets the classified text. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassification#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassification#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [TextClassification](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassification#)!\> | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassification#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public methods

### describeContents

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getActions

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getActions(): MutableList<RemoteAction!>!
```

Returns a list of actions that may be performed on the text. The list is ordered based on the likelihood that a user will use the action, with the most likely action appearing first.

### getConfidenceScore

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getConfidenceScore(entity: String!): Float
```

Returns the confidence score for the specified entity. The value ranges from 0 (low confidence) to 1 (high confidence). 0 indicates that the entity was not found for the classified text.

| Parameters ||
|---|---|
| `entity` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_UNKNOWN:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_OTHER:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_EMAIL:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_PHONE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_ADDRESS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_URL:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_DATE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_DATE_TIME:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_FLIGHT_NUMBER:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_OTP:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_SMS_RETRIEVER_OTP:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_SMS_WEB_OTP:kotlin.String` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | Value is between 0.0f and 1.0f inclusive |

### getEntity

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEntity(index: Int): String
```

Returns the entity at the specified index. Entities are ordered from high confidence to low confidence.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_UNKNOWN:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_OTHER:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_EMAIL:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_PHONE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_ADDRESS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_URL:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_DATE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_DATE_TIME:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_FLIGHT_NUMBER:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_OTP:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_SMS_RETRIEVER_OTP:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_SMS_WEB_OTP:kotlin.String` |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if the specified index is out of range. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassification#getEntityCount()`

### getEntityCount

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEntityCount(): Int
```

Returns the number of entities found in the classified text.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is 0 or greater |

### getExtras

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getExtras(): Bundle
```

Returns the extended data.

**NOTE:**Do not modify this bundle.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` | This value cannot be `null`. |

### getIcon

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getIcon(): Drawable?
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassification#getActions()` instead.*

Returns an icon that may be rendered on a widget used to act on the classified text.

**NOTE:** This field is not parcelable and only represents the icon of the first `https://developer.android.com/reference/kotlin/android/app/RemoteAction.html#` (if one exists) when this object is read from a parcel.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?` | This value may be `null`. |

### getId

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getId(): String?
```

Returns the id, if one exists, for this object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | This value may be `null`. |

### getIntent

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getIntent(): Intent?
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassification#getActions()` instead.*

Returns an intent that may be fired to act on the classified text.

**NOTE:**This field is not parcelled and will always return null when this object is read from a parcel.

### getLabel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLabel(): CharSequence?
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassification#getActions()` instead.*

Returns a label that may be rendered on a widget used to act on the classified text.

**NOTE:** This field is not parcelable and only represents the label of the first `https://developer.android.com/reference/kotlin/android/app/RemoteAction.html#` (if one exists) when this object is read from a parcel.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | This value may be `null`. |

### getOnClickListener

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getOnClickListener(): View.OnClickListener?
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassification#getActions()` instead.*

Returns the OnClickListener that may be triggered to act on the classified text.

**NOTE:** This field is not parcelable and only represents the first `https://developer.android.com/reference/kotlin/android/app/RemoteAction.html#` (if one exists) when this object is read from a parcel.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/View.OnClickListener.html#?` | This value may be `null`. |

### getText

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getText(): String?
```

Gets the classified text.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | This value may be `null`. |

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<TextClassification!>
```
