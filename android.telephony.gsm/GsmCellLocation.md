Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GsmCellLocation

Kotlin | [Java](../android/telephony/gsm/GsmCellLocation.md)
| --- | --- |

```
open class GsmCellLocation : CellLocation
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.telephony.CellLocation](../android/telephony/CellLocation.md) ||
| | ↳ | [android.telephony.gsm.GsmCellLocation](../android/telephony/gsm/GsmCellLocation.md) |

| **This class was deprecated in API level 31.**
|
| use `https://developer.android.com/reference/kotlin/android/telephony/CellIdentity.html#`.

Represents the cell location on a GSM phone.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telephony/gsm/GsmCellLocation#GsmCellLocation()()` Empty constructor. |
| `https://developer.android.com/reference/kotlin/android/telephony/gsm/GsmCellLocation#GsmCellLocation(android.os.Bundle)(bundle: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)` Initialize the object from a bundle. |

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/gsm/GsmCellLocation#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/gsm/GsmCellLocation#fillInNotifierBundle(android.os.Bundle)(m: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)` Set intent notifier Bundle based on service state |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/gsm/GsmCellLocation#getCid()()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/gsm/GsmCellLocation#getLac()()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/gsm/GsmCellLocation#getPsc()()` On a UMTS network, returns the primary scrambling code of the serving cell. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/gsm/GsmCellLocation#hashCode()()` Returns a hash code value for the object. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/gsm/GsmCellLocation#setLacAndCid(kotlin.Int,%20kotlin.Int)(lac: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, cid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the location area code and the cell id. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/gsm/GsmCellLocation#setStateInvalid()()` Invalidate this object. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/gsm/GsmCellLocation#toString()()` Returns a string representation of the object. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/telephony/CellLocation.html#` |---|---| | `https://developer.android.com/reference/kotlin/android/telephony/CellLocation.html#!` | `https://developer.android.com/reference/kotlin/android/telephony/CellLocation.html#getEmpty()()` Return a new CellLocation object representing an unknown location, or null for unknown/none phone radio types. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/telephony/CellLocation.html#requestLocationUpdate()()` Request an updated CellLocation for callers targeting SDK 30 or older. Whenever Android is aware of location changes, a callback will automatically be sent to all registrants of `https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener.html#LISTEN_CELL_LOCATION:kotlin.Int`. This API requests an additional location update for cases where power saving might cause location updates to be missed. This method is a no-op for callers targeting SDK level 31 or greater. This method is a no-op for callers that target SDK level 29 or 30 and lack `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`. This method is a no-op for callers that target SDK level 28 or below and lack `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String`. <br /> | ||

## Public constructors

### GsmCellLocation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
GsmCellLocation()
```

Empty constructor. Initializes the LAC and CID to -1.

### GsmCellLocation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
GsmCellLocation(bundle: Bundle!)
```

Initialize the object from a bundle.

## Public methods

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(other: Any?): Boolean
```

**Deprecated:** *Deprecated in Java.*

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### fillInNotifierBundle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun fillInNotifierBundle(m: Bundle!): Unit
```

**Deprecated:** *Deprecated in Java.*

Set intent notifier Bundle based on service state

| Parameters ||
|---|---|
| `m` | [Bundle](../android/os/Bundle.md)!: intent notifier Bundle |

### getCid

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCid(): Int
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | gsm cell id, -1 if unknown or invalid, 0xffff max legal value |

### getLac

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLac(): Int
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | gsm location area code, -1 if unknown, 0xffff max legal value |

### getPsc

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPsc(): Int
```

**Deprecated:** *Deprecated in Java.*

On a UMTS network, returns the primary scrambling code of the serving cell.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | primary scrambling code for UMTS, -1 if unknown or GSM |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hashCode(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### setLacAndCid

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLacAndCid(
    lac: Int, 
    cid: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Set the location area code and the cell id.

### setStateInvalid

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setStateInvalid(): Unit
```

**Deprecated:** *Deprecated in Java.*

Invalidate this object. The location area code and the cell id are set to -1.

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

**Deprecated:** *Deprecated in Java.*

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |
