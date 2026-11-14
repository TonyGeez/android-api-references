# FontRequest

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FontRequest

Kotlin| [Java](https://developer.android.com/reference/android/provider/FontRequest "View this page in Java") 
| --- | --- |

```
class FontRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.provider.FontRequest](https://developer.android.com/reference/kotlin/android/provider/FontRequest#) |

| **This class was deprecated in API level 31.**
|
| Use the androidx.core.provider.FontRequest

Information about a font request that may be sent to a Font Provider.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FontRequest](https://developer.android.com/reference/kotlin/android/provider/FontRequest#FontRequest(kotlin.String,%20kotlin.String,%20kotlin.String))`(`providerAuthority:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `providerPackage:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `query:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` <br /> |
| [FontRequest](https://developer.android.com/reference/kotlin/android/provider/FontRequest#FontRequest(kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.collections.MutableList))`(`providerAuthority:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `providerPackage:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `query:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `certificates:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!>!>`)` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!\>!\>! | [getCertificates](https://developer.android.com/reference/kotlin/android/provider/FontRequest#getCertificates())`()` Returns the list of certificate sets given for this provider. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getProviderAuthority](https://developer.android.com/reference/kotlin/android/provider/FontRequest#getProviderAuthority())`()` Returns the selected font provider's authority. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getProviderPackage](https://developer.android.com/reference/kotlin/android/provider/FontRequest#getProviderPackage())`()` Returns the selected font provider's package. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getQuery](https://developer.android.com/reference/kotlin/android/provider/FontRequest#getQuery())`()` Returns the query string. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/provider/FontRequest#toString())`()` <br /> |

## Public constructors

### FontRequest

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FontRequest(
    providerAuthority: String, 
    providerPackage: String, 
    query: String)
```

| Parameters ||
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `providerAuthority` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The authority of the Font Provider to be used for the request. This should be a system installed app. This value cannot be`null`. |
| `providerPackage` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The package for the Font Provider to be used for the request. This is used to verify the identity of the provider. This value cannot be`null`. |
| `query` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The query to be sent over to the provider. Refer to your font provider's documentation on the format of this string. This value cannot be`null`. |
| --- | --- |

### FontRequest

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FontRequest(
    providerAuthority: String, 
    providerPackage: String, 
    query: String, 
    certificates: MutableList<MutableList<ByteArray!>!>)
```

| Parameters ||
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `providerAuthority` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The authority of the Font Provider to be used for the request. This value cannot be`null`. |
| `query` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The query to be sent over to the provider. Refer to your font provider's documentation on the format of this string. This value cannot be`null`. |
| `providerPackage` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The package for the Font Provider to be used for the request. This is used to verify the identity of the provider. This value cannot be`null`. |
| --- | --- |
| `certificates` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!\>!\>:The list of sets of hashes for the certificates the provider should be signed with. This is used to verify the identity of the provider. Each set in the list represents one collection of signature hashes. Refer to your font provider's documentation for these values. This value cannot be`null`. |

## Public methods

### getCertificates

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCertificates(): MutableList<MutableList<ByteArray!>!>!
```

**Deprecated:** *Deprecated in Java.*

Returns the list of certificate sets given for this provider. This helps the system verify that the provider identified by the given authority is the one requested. 

### getProviderAuthority

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getProviderAuthority(): String!
```

**Deprecated:** *Deprecated in Java.*

Returns the selected font provider's authority. This tells the system what font provider it should request the font from. 

### getProviderPackage

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getProviderPackage(): String!
```

**Deprecated:** *Deprecated in Java.*

Returns the selected font provider's package. This helps the system verify that the provider identified by the given authority is the one requested. 

### getQuery

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getQuery(): String!
```

**Deprecated:** *Deprecated in Java.*

Returns the query string. Refer to your font provider's documentation on the format of this string. 

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
