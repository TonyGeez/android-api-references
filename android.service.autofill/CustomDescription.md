# CustomDescription

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CustomDescription

Kotlin| [Java](CustomDescription.md) 
| --- | --- |

```
class CustomDescription : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.autofill.CustomDescription](CustomDescription.md) |

Defines a custom description for the autofill save UI.

This is useful when the autofill service needs to show a detailed view of what would be saved; for example, when the screen contains a credit card, it could display a logo of the credit card bank, the last four digits of the credit card number, and its expiration number.

A custom description is made of 2 parts:

- A [presentation template](../android.widget/RemoteViews.md) containing children views.
- [Transformations](Transformation.md) to populate the children views.

For the credit card example mentioned above, the (simplified) template would be: 

```kotlin
<LinearLayout>
    <ImageView android:id="@+id/templateccLogo"/>
    <TextView android:id="@+id/templateCcNumber"/>
    <TextView android:id="@+id/templateExpDate"/>
  </LinearLayout>
  
```

Which in code translates to: 

```kotlin
CustomDescription.Builder buider = new Builder(new RemoteViews(pgkName, R.layout.cc_template);
  
```

Then the value of each of the 3 children would be changed at runtime based on the the value of the screen fields and the [Transformations](Transformation.md): 

```kotlin
// Image child - different logo for each bank, based on credit card prefix
  builder.addChild(R.id.templateccLogo,
    new ImageTransformation.Builder(ccNumberId)
      .addOption(Pattern.compile("^4815.*$"), R.drawable.ic_credit_card_logo1)
      .addOption(Pattern.compile("^1623.*$"), R.drawable.ic_credit_card_logo2)
      .addOption(Pattern.compile("^42.*$"), R.drawable.ic_credit_card_logo3)
      .build();
  // Masked credit card number (as .....LAST_4_DIGITS)
  builder.addChild(R.id.templateCcNumber, new CharSequenceTransformation
      .Builder(ccNumberId, Pattern.compile("^.*(\\d\\d\\d\\d)$"), "...$1")
      .build();
  // Expiration date as MM / YYYY:
  builder.addChild(R.id.templateExpDate, new CharSequenceTransformation
      .Builder(ccExpMonthId, Pattern.compile("^(\\d\\d)$"), "Exp: $1")
      .addField(ccExpYearId, Pattern.compile("^(\\d\\d)$"), "/$1")
      .build();
  
```

See [ImageTransformation](ImageTransformation.md), [CharSequenceTransformation](CharSequenceTransformation.md) for more info about these transformations.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/service/autofill/CustomDescription.Builder.md) Builder for [CustomDescription](CustomDescription.md) objects. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](CustomDescription.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](CustomDescription.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](CustomDescription.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [CustomDescription](CustomDescription.md)!\> | [CREATOR](CustomDescription.md) <br /> |

## Public methods

### describeContents

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### toString

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
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

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<CustomDescription!>
```
