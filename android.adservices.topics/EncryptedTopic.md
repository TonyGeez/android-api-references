Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 11](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EncryptedTopic

```
class EncryptedTopic
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.topics.EncryptedTopic](../android/adservices/topics/EncryptedTopic.md) |

> [!CAUTION]
> **This class was deprecated in API level 37.**
>
> The Rubidium (Rb) Relevance APIs, including those in android.adservices.topics, are being deprecated. Relevance APIs have no direct replacement. Developers should stop using them, as calls will be rejected in future Android releases. Please refer to official Privacy Sandbox documentation for deprecation and roadmap details: https://privacysandbox.com/news/update-on-plans-for-privacy-sandbox-technologies/

Encrypted form of `https://developer.android.com/reference/kotlin/android/adservices/topics/Topic`. This object will be used to return encrypted topic cipher text along with necessary fields required to decrypt it.

Decryption of `https://developer.android.com/reference/kotlin/android/adservices/topics/EncryptedTopic#getEncryptedTopic()` should give json string for `https://developer.android.com/reference/kotlin/android/adservices/topics/Topic`. Example of decrypted json string: `{ "taxonomy_version": 5, "model_version": 2, "topic_id": 10010 }`

Decryption of cipher text is expected to happen on the server with the corresponding algorithm and private key for the public key `https://developer.android.com/reference/kotlin/android/adservices/topics/EncryptedTopic#getKeyIdentifier()`}.

Detailed steps on decryption can be found on [Developer Guide](https://developer.android.com/design-for-safety/privacy-sandbox/guides/topics).

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/adservices/topics/EncryptedTopic#EncryptedTopic(kotlin.ByteArray,%20kotlin.String,%20kotlin.ByteArray)(encryptedTopic: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html, keyIdentifier: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, encapsulatedKey: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)` Creates encrypted version of the `https://developer.android.com/reference/kotlin/android/adservices/topics/Topic` object. |

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/topics/EncryptedTopic#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/topics/EncryptedTopic#getEncapsulatedKey()()` Returns the encapsulated key generated during HPKE setup. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/topics/EncryptedTopic#getEncryptedTopic()()` Returns encrypted bytes for the JSON version of the `https://developer.android.com/reference/kotlin/android/adservices/topics/Topic` object as cipher text. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/topics/EncryptedTopic#getKeyIdentifier()()` Returns key identifier for the used encryption key. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/topics/EncryptedTopic#hashCode()()` Returns a hash code value for the object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/topics/EncryptedTopic#toString()()` Returns a string representation of the object. |
| --- | --- |

## Public constructors

### EncryptedTopic

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 11](https://developer.android.com/sdkExtensions)

```
EncryptedTopic(
    encryptedTopic: ByteArray, 
    keyIdentifier: String, 
    encapsulatedKey: ByteArray)
```

Creates encrypted version of the `https://developer.android.com/reference/kotlin/android/adservices/topics/Topic` object.

| Parameters ||
|---|---|
| `encryptedTopic` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): byte array cipher text containing encrypted `https://developer.android.com/reference/kotlin/android/adservices/topics/Topic` json string. This value cannot be `null`. |
| `keyIdentifier` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): key used to identify the public key used for encryption. This value cannot be `null`. |
| `encapsulatedKey` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): encapsulated key generated during HPKE setup. This value cannot be `null`. |
| --- | --- |

## Public methods

### equals

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
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

### getEncapsulatedKey

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 11](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEncapsulatedKey(): ByteArray
```

**Deprecated:** *Deprecated in Java.*

Returns the encapsulated key generated during HPKE setup.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html` | This value cannot be `null`. |

### getEncryptedTopic

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 11](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEncryptedTopic(): ByteArray
```

**Deprecated:** *Deprecated in Java.*

Returns encrypted bytes for the JSON version of the `https://developer.android.com/reference/kotlin/android/adservices/topics/Topic` object as cipher text.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html` | This value cannot be `null`. |

### getKeyIdentifier

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 11](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getKeyIdentifier(): String
```

**Deprecated:** *Deprecated in Java.*

Returns key identifier for the used encryption key.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### hashCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
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

### toString

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

**Deprecated:** *Deprecated in Java.*

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |
