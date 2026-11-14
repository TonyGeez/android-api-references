Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Report

```
class Report
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.hid.Report](../android/hardware/hid/Report.md) |

Represents a Human Interface Device (HID) report exchanged between a host and a HID device.

A HID report contains structured data defined by the device's report descriptor. It includes an optional report ID that distinguishes between multiple report formats supported by the same device, along with a read-only binary data payload.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/hardware/hid/Report#Report(kotlin.Int,%20java.nio.ByteBuffer)(reportId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, data: https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)` Creates a new `https://developer.android.com/reference/kotlin/android/hardware/hid/Report#` instance with a specified report ID and binary data payload. |
| `https://developer.android.com/reference/kotlin/android/hardware/hid/Report#Report(java.nio.ByteBuffer)(data: https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)` Constructor for a report that does not use report ID. |

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/hid/Report#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [ByteBuffer](../java/nio/ByteBuffer.md) | `https://developer.android.com/reference/kotlin/android/hardware/hid/Report#getData()()` Returns the data provided by the device for the report ID. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/hid/Report#getReportId()()` Accessor for the report ID. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/hid/Report#hashCode()()` Returns a hash code value for the object. |

## Public constructors

### Report

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Report(
    reportId: Int, 
    data: ByteBuffer)
```

Creates a new `https://developer.android.com/reference/kotlin/android/hardware/hid/Report#` instance with a specified report ID and binary data payload.

To prevent external modification, the provided `https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#` is copied into an internal payload buffer.

| Parameters ||
|---|---|
| `reportId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the ID for this report format, or zero if report IDs are not used. |
| `data` | [ByteBuffer](../java/nio/ByteBuffer.md): the non-null buffer containing the raw binary report payload. |

### Report

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Report(data: ByteBuffer)
```

Constructor for a report that does not use report ID.

| Parameters ||
|---|---|
| `data` | [ByteBuffer](../java/nio/ByteBuffer.md): the report data. This value cannot be `null`. |

## Public methods

### equals

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

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

### getData

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getData(): ByteBuffer
```

Returns the data provided by the device for the report ID.

The data format is specified in the device descriptor, provided by `https://developer.android.com/reference/kotlin/android/hardware/hid/HidDevice#getReportDescriptor()`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#` | the `https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#` of the raw report data. This value cannot be `null`. |

### getReportId

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getReportId(): Int
```

Accessor for the report ID.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the report ID or zero if the device does not use report IDs. |

### hashCode

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |
