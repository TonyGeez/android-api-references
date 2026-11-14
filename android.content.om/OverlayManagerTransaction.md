Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OverlayManagerTransaction

```
class OverlayManagerTransaction : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.om.OverlayManagerTransaction](OverlayManagerTransaction.md) |

A container for a batch of requests to the OverlayManager.

An app can get an `https://developer.android.com/reference/kotlin/android/content/om/OverlayManagerTransaction#` with the specified `https://developer.android.com/reference/kotlin/android/content/om/OverlayManager` to handle the transaction. The app can register multiple overlays and unregister multiple registered overlays in one transaction commitment.

The below example is registering a `updatingOverlay` and unregistering a `deprecatedOverlay` in one transaction commitment.

```kotlin
<code>final OverlayManager overlayManager = ctx.getSystemService(OverlayManager.class);
  final OverlayManagerTransaction transaction = new OverlayManagerTransaction(overlayManager);
  transaction.registerFabricatedOverlay(updatingOverlay);
  transaction.unregisterFabricatedOverlay(deprecatedOverlay)
  transaction.commit();
  </code>
```

## Summary

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/om/OverlayManagerTransaction#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| static [OverlayManagerTransaction](OverlayManagerTransaction.md) | `https://developer.android.com/reference/kotlin/android/content/om/OverlayManagerTransaction#newInstance()()` Get an overlay manager transaction. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/om/OverlayManagerTransaction#registerFabricatedOverlay(android.content.om.FabricatedOverlay)(overlay: https://developer.android.com/reference/kotlin/android/content/om/FabricatedOverlay)` Registers the fabricated overlays with the overlay manager so it can be used to overlay the app resources in runtime. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/om/OverlayManagerTransaction#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/om/OverlayManagerTransaction#unregisterFabricatedOverlay(android.content.om.OverlayIdentifier)(overlay: https://developer.android.com/reference/kotlin/android/content/om/OverlayIdentifier)` Unregisters the registered overlays from the overlay manager. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/om/OverlayManagerTransaction#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [OverlayManagerTransaction](OverlayManagerTransaction.md)!\> | `https://developer.android.com/reference/kotlin/android/content/om/OverlayManagerTransaction#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### newInstance

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun newInstance(): OverlayManagerTransaction
```

Get an overlay manager transaction.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/om/OverlayManagerTransaction#` | a new `https://developer.android.com/reference/kotlin/android/content/om/OverlayManagerTransaction#` instance. This value cannot be `null`. |

### registerFabricatedOverlay

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun registerFabricatedOverlay(overlay: FabricatedOverlay): Unit
```

Registers the fabricated overlays with the overlay manager so it can be used to overlay the app resources in runtime.

If an overlay is re-registered the existing overlay will be replaced by the newly registered overlay. The registered overlay will be left unchanged until the target package or target overlayable is changed.

| Parameters ||
|---|---|
| `overlay` | [FabricatedOverlay](FabricatedOverlay.md): the overlay to register with the overlay manager. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | This value cannot be `null`. |

### toString

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### unregisterFabricatedOverlay

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun unregisterFabricatedOverlay(overlay: OverlayIdentifier): Unit
```

Unregisters the registered overlays from the overlay manager.

| Parameters ||
|---|---|
| `overlay` | [OverlayIdentifier](OverlayIdentifier.md): the overlay to be unregistered. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/om/OverlayManager#getOverlayInfosForTarget(kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/content/om/OverlayInfo#getOverlayIdentifier()`

### writeToParcel

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android.os/Parcel.md): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<OverlayManagerTransaction!>
```
