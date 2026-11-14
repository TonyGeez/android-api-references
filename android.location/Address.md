Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Address

Kotlin | [Java](Address.md)
| --- | --- |

```
open class Address : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.location.Address](Address.md) |

A class representing an Address, that is, a set of Strings describing a location. The address format is a simplified version of xAL (eXtensible Address Language) http://www.oasis-open.org/committees/ciq/ciq.html#6

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| Address Constructs a new Address object set to the given Locale and with all other fields initialized to null or false. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | clearLatitude Removes any latitude associated with this address. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | clearLongitude Removes any longitude associated with this address. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getAddressLine Returns a line of the address numbered by the given index (starting at 0), or null if no such line is present. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getAdminArea Returns the administrative area name of the address, for example, "CA", or null if it is unknown |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getCountryCode Returns the country code of the address, for example "US", or null if it is unknown. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getCountryName Returns the localized country name of the address, for example "Iceland", or null if it is unknown. |
| open [Bundle](../android.os/Bundle.md)! | getExtras Returns additional provider-specific information about the address as a Bundle. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getFeatureName Returns the feature name of the address, for example, "Golden Gate Bridge", or null if it is unknown |
| --- | --- |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | getLatitude Returns the latitude of the address if known. |
| open [Locale](../java.util/Locale.md)! | getLocale Returns the Locale associated with this address. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getLocality Returns the locality of the address, for example "Mountain View", or null if it is unknown. |
| --- | --- |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | getLongitude Returns the longitude of the address if known. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getMaxAddressLineIndex Returns the largest index currently in use to specify an address line. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getPhone Returns the phone number of the address if known, or null if it is unknown. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getPostalCode Returns the postal code of the address, for example "94110", or null if it is unknown. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getPremises Returns the premises of the address, or null if it is unknown. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getSubAdminArea Returns the sub-administrative area name of the address, for example, "Santa Clara County", or null if it is unknown |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getSubLocality Returns the sub-locality of the address, or null if it is unknown. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getSubThoroughfare Returns the sub-thoroughfare name of the address, which may be null. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getThoroughfare Returns the thoroughfare name of the address, for example, "1600 Ampitheater Parkway", which may be null |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getUrl Returns the public URL for the address if known, or null if it is unknown. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasLatitude Returns true if a latitude has been assigned to this Address, false otherwise. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasLongitude Returns true if a longitude has been assigned to this Address, false otherwise. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAddressLine Sets the line of the address numbered by index (starting at 0) to the given String, which may be null. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAdminArea Sets the administrative area name of the address to the given String, which may be null |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setCountryCode Sets the country code of the address to the given String, which may be null. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setCountryName Sets the country name of the address to the given String, which may be null. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setExtras Sets the extra information associated with this fix to the given Bundle. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setFeatureName Sets the feature name of the address to the given String, which may be null |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setLatitude Sets the latitude associated with this address. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setLocality Sets the locality of the address to the given String, which may be null. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setLongitude Sets the longitude associated with this address. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setPhone Sets the phone number associated with this address. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setPostalCode Sets the postal code of the address to the given String, which may be null. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setPremises Sets the premises of the address to the given String, which may be null. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setSubAdminArea Sets the sub-administrative area name of the address to the given String, which may be null |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setSubLocality Sets the sub-locality of the address to the given String, which may be null. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setSubThoroughfare Sets the sub-thoroughfare name of the address, which may be null. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setThoroughfare Sets the thoroughfare name of the address, which may be null. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setUrl Sets the public URL associated with this address. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of the object. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [Address](Address.md)!\> | `https://developer.android.com/reference/kotlin/android/location/Address#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public constructors

### Address

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Address(locale: Locale!)
```

Constructs a new Address object set to the given Locale and with all other fields initialized to null or false.

## Public methods

### clearLatitude

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clearLatitude(): Unit
```

Removes any latitude associated with this address.

### clearLongitude

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clearLongitude(): Unit
```

Removes any longitude associated with this address.

### describeContents

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of writeToParcel, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getAddressLine

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAddressLine(index: Int): String!
```

Returns a line of the address numbered by the given index (starting at 0), or null if no such line is present.

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if index \< 0 |

### getAdminArea

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAdminArea(): String!
```

Returns the administrative area name of the address, for example, "CA", or null if it is unknown

### getCountryCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCountryCode(): String!
```

Returns the country code of the address, for example "US", or null if it is unknown.

### getCountryName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCountryName(): String!
```

Returns the localized country name of the address, for example "Iceland", or null if it is unknown.

### getExtras

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getExtras(): Bundle!
```

Returns additional provider-specific information about the address as a Bundle. The keys and values are determined by the provider. If no additional information is available, null is returned.

### getFeatureName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFeatureName(): String!
```

Returns the feature name of the address, for example, "Golden Gate Bridge", or null if it is unknown

### getLatitude

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLatitude(): Double
```

Returns the latitude of the address if known.

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this Address has not been assigned a latitude. |

### getLocale

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLocale(): Locale!
```

Returns the Locale associated with this address.

### getLocality

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLocality(): String!
```

Returns the locality of the address, for example "Mountain View", or null if it is unknown.

### getLongitude

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLongitude(): Double
```

Returns the longitude of the address if known.

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this Address has not been assigned a longitude. |

### getMaxAddressLineIndex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMaxAddressLineIndex(): Int
```

Returns the largest index currently in use to specify an address line. If no address lines are specified, -1 is returned.

### getPhone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPhone(): String!
```

Returns the phone number of the address if known, or null if it is unknown.

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this Address has not been assigned a phone number. |

### getPostalCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPostalCode(): String!
```

Returns the postal code of the address, for example "94110", or null if it is unknown.

### getPremises

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPremises(): String!
```

Returns the premises of the address, or null if it is unknown.

### getSubAdminArea

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSubAdminArea(): String!
```

Returns the sub-administrative area name of the address, for example, "Santa Clara County", or null if it is unknown

### getSubLocality

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSubLocality(): String!
```

Returns the sub-locality of the address, or null if it is unknown. For example, this may correspond to the neighborhood of the locality.

### getSubThoroughfare

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSubThoroughfare(): String!
```

Returns the sub-thoroughfare name of the address, which may be null. This may correspond to the street number of the address.

### getThoroughfare

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getThoroughfare(): String!
```

Returns the thoroughfare name of the address, for example, "1600 Ampitheater Parkway", which may be null

### getUrl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getUrl(): String!
```

Returns the public URL for the address if known, or null if it is unknown.

### hasLatitude

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasLatitude(): Boolean
```

Returns true if a latitude has been assigned to this Address, false otherwise.

### hasLongitude

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasLongitude(): Boolean
```

Returns true if a longitude has been assigned to this Address, false otherwise.

### setAddressLine

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAddressLine(
    index: Int, 
    line: String!
): Unit
```

Sets the line of the address numbered by index (starting at 0) to the given String, which may be null.

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if index \< 0 |

### setAdminArea

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAdminArea(adminArea: String!): Unit
```

Sets the administrative area name of the address to the given String, which may be null

### setCountryCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setCountryCode(countryCode: String!): Unit
```

Sets the country code of the address to the given String, which may be null.

### setCountryName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setCountryName(countryName: String!): Unit
```

Sets the country name of the address to the given String, which may be null.

### setExtras

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setExtras(extras: Bundle!): Unit
```

Sets the extra information associated with this fix to the given Bundle.

### setFeatureName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFeatureName(featureName: String!): Unit
```

Sets the feature name of the address to the given String, which may be null

### setLatitude

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLatitude(latitude: Double): Unit
```

Sets the latitude associated with this address.

### setLocality

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLocality(locality: String!): Unit
```

Sets the locality of the address to the given String, which may be null.

### setLongitude

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLongitude(longitude: Double): Unit
```

Sets the longitude associated with this address.

### setPhone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPhone(phone: String!): Unit
```

Sets the phone number associated with this address.

### setPostalCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPostalCode(postalCode: String!): Unit
```

Sets the postal code of the address to the given String, which may be null.

### setPremises

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPremises(premises: String!): Unit
```

Sets the premises of the address to the given String, which may be null.

### setSubAdminArea

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSubAdminArea(subAdminArea: String!): Unit
```

Sets the sub-administrative area name of the address to the given String, which may be null

### setSubLocality

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSubLocality(sublocality: String!): Unit
```

Sets the sub-locality of the address to the given String, which may be null.

### setSubThoroughfare

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSubThoroughfare(subthoroughfare: String!): Unit
```

Sets the sub-thoroughfare name of the address, which may be null.

### setThoroughfare

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setThoroughfare(thoroughfare: String!): Unit
```

Sets the thoroughfare name of the address, which may be null.

### setUrl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setUrl(Url: String!): Unit
```

Sets the public URL associated with this address.

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun writeToParcel(
    parcel: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<Address!>
```
