Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Entries

```
interface Entries
```

| [android.security.identity.CredentialDataResult.Entries](https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult.Entries#) |

> [!CAUTION]
> **This interface was deprecated in API level 37.2.**
>
> Use `java.security.KeyStore` with the Android hardware-backed keystore instead.

A class for representing data elements returned.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult.Entries#STATUS_NOT_IN_REQUEST_MESSAGE:kotlin.Int` The entry wasn't in the request message. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult.Entries#STATUS_NOT_REQUESTED:kotlin.Int` The entry was not requested. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult.Entries#STATUS_NO_ACCESS_CONTROL_PROFILES:kotlin.Int` The entry was not retrieved because it was configured without any access control profile. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult.Entries#STATUS_NO_SUCH_ENTRY:kotlin.Int` The entry does not exist. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult.Entries#STATUS_OK:kotlin.Int` Value was successfully retrieved. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult.Entries#STATUS_READER_AUTHENTICATION_FAILED:kotlin.Int` The entry was not retrieved because reader authentication failed. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult.Entries#STATUS_USER_AUTHENTICATION_FAILED:kotlin.Int` The entry was not retrieved because user authentication failed. |

| Public methods ||
|---|---|
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult.Entries#getEntry(kotlin.String,%20kotlin.String)(namespaceName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Gets the raw CBOR data for the value of an entry. |
| abstract [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult.Entries#getEntryNames(kotlin.String)(namespaceName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Get the names of all requested entries in a name space. |
| abstract [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult.Entries#getNamespaces()()` Gets the names of namespaces with retrieved entries. |
| --- | --- |
| abstract [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult.Entries#getRetrievedEntryNames(kotlin.String)(namespaceName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Get the names of all entries that was successfully retrieved from a name space. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult.Entries#getStatus(kotlin.String,%20kotlin.String)(namespaceName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Gets the status of an entry. |

## Constants

### STATUS_NOT_IN_REQUEST_MESSAGE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_NOT_IN_REQUEST_MESSAGE: Int
```

**Deprecated:** *Deprecated in Java.*

The entry wasn't in the request message.

 Value: 3

### STATUS_NOT_REQUESTED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_NOT_REQUESTED: Int
```

**Deprecated:** *Deprecated in Java.*

The entry was not requested.

 Value: 2

### STATUS_NO_ACCESS_CONTROL_PROFILES

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_NO_ACCESS_CONTROL_PROFILES: Int
```

**Deprecated:** *Deprecated in Java.*

The entry was not retrieved because it was configured without any access control profile.

 Value: 6

### STATUS_NO_SUCH_ENTRY

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_NO_SUCH_ENTRY: Int
```

**Deprecated:** *Deprecated in Java.*

The entry does not exist.

 Value: 1

### STATUS_OK

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_OK: Int
```

**Deprecated:** *Deprecated in Java.*

Value was successfully retrieved.

 Value: 0

### STATUS_READER_AUTHENTICATION_FAILED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_READER_AUTHENTICATION_FAILED: Int
```

**Deprecated:** *Deprecated in Java.*

The entry was not retrieved because reader authentication failed.

 Value: 5

### STATUS_USER_AUTHENTICATION_FAILED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_USER_AUTHENTICATION_FAILED: Int
```

**Deprecated:** *Deprecated in Java.*

The entry was not retrieved because user authentication failed.

 Value: 4

## Public methods

### getEntry

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getEntry(
    namespaceName: String, 
    name: String
): ByteArray?
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Gets the raw CBOR data for the value of an entry.

This should only be called on an entry for which the `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult.Entries#getStatus(kotlin.String,%20kotlin.String)` method returns `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult.Entries#STATUS_OK:kotlin.Int`.

| Parameters ||
|---|---|
| `namespaceName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the namespace name of the entry. This value cannot be `null`. |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the name of the entry to get the value for. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html?` | the raw CBOR data or `null` if no entry with the given name exists. |

### getEntryNames

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getEntryNames(namespaceName: String): MutableCollection<String!>
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Get the names of all requested entries in a name space.

This includes the name of entries that wasn't successfully retrieved.

| Parameters ||
|---|---|
| `namespaceName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the namespace name to get entries for. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | A collection of names for the given namespace or the empty collection if no entries was returned for the given name space. This value cannot be `null`. |

### getNamespaces

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getNamespaces(): MutableCollection<String!>
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Gets the names of namespaces with retrieved entries.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | collection of name of namespaces containing retrieved entries. May be empty if no data was retrieved. This value cannot be `null`. |

### getRetrievedEntryNames

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getRetrievedEntryNames(namespaceName: String): MutableCollection<String!>
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Get the names of all entries that was successfully retrieved from a name space.

This only return entries for which `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult.Entries#getStatus(kotlin.String,%20kotlin.String)` will return `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult.Entries#STATUS_OK:kotlin.Int`.

| Parameters ||
|---|---|
| `namespaceName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the namespace name to get entries for. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | The entries in the given namespace that were successfully rerieved or the empty collection if no entries was returned for the given name space. This value cannot be `null`. |

### getStatus

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getStatus(
    namespaceName: String, 
    name: String
): Int
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Gets the status of an entry.

This returns `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult.Entries#STATUS_OK:kotlin.Int` if the value was retrieved, `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult.Entries#STATUS_NO_SUCH_ENTRY:kotlin.Int` if the given entry wasn't retrieved, `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult.Entries#STATUS_NOT_REQUESTED:kotlin.Int` if it wasn't requested, `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult.Entries#STATUS_NOT_IN_REQUEST_MESSAGE:kotlin.Int` if the request message was set but the entry wasn't present in the request message, `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult.Entries#STATUS_USER_AUTHENTICATION_FAILED:kotlin.Int` if the value wasn't retrieved because the necessary user authentication wasn't performed, `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult.Entries#STATUS_READER_AUTHENTICATION_FAILED:kotlin.Int` if the supplied reader certificate chain didn't match the set of certificates the entry was provisioned with, or `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult.Entries#STATUS_NO_ACCESS_CONTROL_PROFILES:kotlin.Int` if the entry was configured without any access control profiles.

| Parameters ||
|---|---|
| `namespaceName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the namespace name of the entry. This value cannot be `null`. |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the name of the entry to get the value for. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the status indicating whether the value was retrieved and if not, why. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult.Entries#STATUS_OK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult.Entries#STATUS_NO_SUCH_ENTRY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult.Entries#STATUS_NOT_REQUESTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult.Entries#STATUS_NOT_IN_REQUEST_MESSAGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult.Entries#STATUS_USER_AUTHENTICATION_FAILED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult.Entries#STATUS_READER_AUTHENTICATION_FAILED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult.Entries#STATUS_NO_ACCESS_CONTROL_PROFILES:kotlin.Int` |
