Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Voice

Kotlin | [Java](Voice.md)
| --- | --- |

```
open class Voice : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.speech.tts.Voice](Voice.md) |

Characteristics and features of a Text-To-Speech Voice. Each TTS Engine can expose multiple voices for each locale, with different set of features.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/speech/tts/Voice#LATENCY_HIGH:kotlin.Int` Network based expected synthesizer latency (\~200ms) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/speech/tts/Voice#LATENCY_LOW:kotlin.Int` Low expected synthesizer latency (\~20ms) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/speech/tts/Voice#LATENCY_NORMAL:kotlin.Int` Normal expected synthesizer latency (\~50ms) |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/speech/tts/Voice#LATENCY_VERY_HIGH:kotlin.Int` Very slow network based expected synthesizer latency (\> 200ms) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/speech/tts/Voice#LATENCY_VERY_LOW:kotlin.Int` Very low expected synthesizer latency (\< 20ms) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/speech/tts/Voice#QUALITY_HIGH:kotlin.Int` High, human-like quality of speech synthesis |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/speech/tts/Voice#QUALITY_LOW:kotlin.Int` Low, not human-like quality of speech synthesis |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/speech/tts/Voice#QUALITY_NORMAL:kotlin.Int` Normal quality of speech synthesis |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/speech/tts/Voice#QUALITY_VERY_HIGH:kotlin.Int` Very high, almost human-indistinguishable quality of speech synthesis |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/speech/tts/Voice#QUALITY_VERY_LOW:kotlin.Int` Very low, but still intelligible quality of speech synthesis |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/speech/tts/Voice#Voice(kotlin.String,%20java.util.Locale,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20kotlin.collections.MutableSet)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, locale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!, quality: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, latency: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, requiresNetworkConnection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, features: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` <br /> |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/speech/tts/Voice#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/speech/tts/Voice#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/speech/tts/Voice#getFeatures()()` Returns the set of features it supports for a given voice. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/speech/tts/Voice#getLatency()()` <br /> |
| open [Locale](../java.util/Locale.md)! | `https://developer.android.com/reference/kotlin/android/speech/tts/Voice#getLocale()()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/speech/tts/Voice#getName()()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/speech/tts/Voice#getQuality()()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/speech/tts/Voice#hashCode()()` Returns a hash code value for the object. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/speech/tts/Voice#isNetworkConnectionRequired()()` <br /> |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/speech/tts/Voice#toString()()` Returns a string representation of the object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/speech/tts/Voice#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [Voice](Voice.md)!\> | `https://developer.android.com/reference/kotlin/android/speech/tts/Voice#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### LATENCY_HIGH

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LATENCY_HIGH: Int
```

Network based expected synthesizer latency (\~200ms)

 Value: 400

### LATENCY_LOW

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LATENCY_LOW: Int
```

Low expected synthesizer latency (\~20ms)

 Value: 200

### LATENCY_NORMAL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LATENCY_NORMAL: Int
```

Normal expected synthesizer latency (\~50ms)

 Value: 300

### LATENCY_VERY_HIGH

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LATENCY_VERY_HIGH: Int
```

Very slow network based expected synthesizer latency (\> 200ms)

 Value: 500

### LATENCY_VERY_LOW

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LATENCY_VERY_LOW: Int
```

Very low expected synthesizer latency (\< 20ms)

 Value: 100

### QUALITY_HIGH

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val QUALITY_HIGH: Int
```

High, human-like quality of speech synthesis

 Value: 400

### QUALITY_LOW

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val QUALITY_LOW: Int
```

Low, not human-like quality of speech synthesis

 Value: 200

### QUALITY_NORMAL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val QUALITY_NORMAL: Int
```

Normal quality of speech synthesis

 Value: 300

### QUALITY_VERY_HIGH

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val QUALITY_VERY_HIGH: Int
```

Very high, almost human-indistinguishable quality of speech synthesis

 Value: 500

### QUALITY_VERY_LOW

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val QUALITY_VERY_LOW: Int
```

Very low, but still intelligible quality of speech synthesis

 Value: 100

## Public constructors

### Voice

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Voice(
    name: String!, 
    locale: Locale!, 
    quality: Int, 
    latency: Int, 
    requiresNetworkConnection: Boolean, 
    features: MutableSet<String!>!)
```

## Public methods

### describeContents

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(other: Any?): Boolean
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
| `obj` | This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getFeatures

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFeatures(): MutableSet<String!>!
```

Returns the set of features it supports for a given voice. Features can either be framework defined, e.g. `https://developer.android.com/reference/kotlin/android/speech/tts/TextToSpeech.Engine#KEY_FEATURE_NETWORK_TIMEOUT_MS:kotlin.String` or engine specific. Engine specific keys must be prefixed by the name of the engine they are intended for. These keys can be used as parameters to `https://developer.android.com/reference/kotlin/android/speech/tts/TextToSpeech#speak(kotlin.String,%20kotlin.Int,%20java.util.HashMap)` and `https://developer.android.com/reference/kotlin/android/speech/tts/TextToSpeech#synthesizeToFile(kotlin.String,%20java.util.HashMap,%20kotlin.String)`. Features values are strings and their values must met restrictions described in their documentation.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | Set instance. May return `null` on error. |

### getLatency

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLatency(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The voice's latency (lower is better) |

**See Also**

- `https://developer.android.com/reference/kotlin/android/speech/tts/Voice#LATENCY_VERY_LOW:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/speech/tts/Voice#LATENCY_LOW:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/speech/tts/Voice#LATENCY_NORMAL:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/speech/tts/Voice#LATENCY_HIGH:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/speech/tts/Voice#LATENCY_VERY_HIGH:kotlin.Int`

### getLocale

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLocale(): Locale!
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Locale.html#!` | The voice's locale |

### getName

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getName(): String!
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | Unique voice name. |

### getQuality

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getQuality(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The voice's quality (higher is better) |

**See Also**

- `https://developer.android.com/reference/kotlin/android/speech/tts/Voice#QUALITY_VERY_HIGH:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/speech/tts/Voice#QUALITY_HIGH:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/speech/tts/Voice#QUALITY_NORMAL:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/speech/tts/Voice#QUALITY_LOW:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/speech/tts/Voice#QUALITY_VERY_LOW:kotlin.Int`

### hashCode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### isNetworkConnectionRequired

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isNetworkConnectionRequired(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Does the Voice require a network connection to work. |

### toString

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android.os/Parcel.md): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<Voice!>
```
