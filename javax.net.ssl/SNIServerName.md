# SNIServerName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SNIServerName

```
abstract class SNIServerName
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.net.ssl.SNIServerName](https://developer.android.com/reference/kotlin/javax/net/ssl/SNIServerName#) |

| Known Direct Subclasses [SNIHostName](https://developer.android.com/reference/kotlin/javax/net/ssl/SNIHostName) |-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [SNIHostName](https://developer.android.com/reference/kotlin/javax/net/ssl/SNIHostName) | Instances of this class represent a server name of type [host_name](https://developer.android.com/reference/kotlin/javax/net/ssl/StandardConstants#SNI_HOST_NAME:kotlin.Int) in a Server Name Indication (SNI) extension. | |
| --- | --- | --- | --- | --- | --- | --- |

Instances of this class represent a server name in a Server Name Indication (SNI) extension.

The SNI extension is a feature that extends the SSL/TLS protocols to indicate what server name the client is attempting to connect to during handshaking. See section 3, "Server Name Indication", of [TLS Extensions (RFC 6066)](http://www.ietf.org/rfc/rfc6066.txt).

`SNIServerName`objects are immutable. Subclasses should not provide methods that can change the state of an instance once it has been created.

## Summary

| Protected constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SNIServerName](https://developer.android.com/reference/kotlin/javax/net/ssl/SNIServerName#SNIServerName(kotlin.Int,%20kotlin.ByteArray))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `encoded:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Creates an`SNIServerName`using the specified name type and encoded value. |

| Public methods ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/javax/net/ssl/SNIServerName#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this server name. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getEncoded](https://developer.android.com/reference/kotlin/javax/net/ssl/SNIServerName#getEncoded())`()` Returns a copy of the encoded server name value of this server name. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](https://developer.android.com/reference/kotlin/javax/net/ssl/SNIServerName#getType())`()` Returns the name type of this server name. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/javax/net/ssl/SNIServerName#hashCode())`()` Returns a hash code value for this server name. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/javax/net/ssl/SNIServerName#toString())`()` Returns a string representation of this server name, including the server name type and the encoded server name value in this`SNIServerName`object. |

## Protected constructors

### SNIServerName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected SNIServerName(
    type: Int, 
    encoded: ByteArray!)
```

Creates an`SNIServerName`using the specified name type and encoded value.

Note that the`encoded`byte array is cloned to protect against subsequent modification.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the type of the server name |
| `encoded` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the encoded value of the server name |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`type`is not in the range of 0 to 255, inclusive. |
| `java.lang.NullPointerException` | if`encoded`is null |

## Public methods

### equals

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this server name.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if, and only if,`other`is of the same class of this object, and has the same name type and encoded value as this server name. |

### getEncoded

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEncoded(): ByteArray!
```

Returns a copy of the encoded server name value of this server name.

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | a copy of the encoded server name value of this server name |

### getType

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getType(): Int
```

Returns the name type of this server name.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the name type of this server name |

### hashCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Returns a hash code value for this server name.

The hash code value is generated using the name type and encoded value of this server name.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this server name. |

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a string representation of this server name, including the server name type and the encoded server name value in this`SNIServerName`object.

The exact details of the representation are unspecified and subject to change, but the following may be regarded as typical: 

```kotlin
"type=<name type>, value=<name value>"
  
```

In this class, the format of "\<name type\>" is "\[LITERAL\] (INTEGER)", where the optional "LITERAL" is the literal name, and INTEGER is the integer value of the name type. The format of "\<name value\>" is "XX:...:XX", where "XX" is the hexadecimal digit representation of a byte value. For example, a returned value of an pseudo server name may look like: 

```kotlin
"type=(31), value=77:77:77:2E:65:78:61:6D:70:6C:65:2E:63:6E"
  
```
or 

```kotlin
"type=host_name (0), value=77:77:77:2E:65:78:61:6D:70:6C:65:2E:63:6E"
  
```

Please NOTE that the exact details of the representation are unspecified and subject to change, and subclasses may override the method with their own formats.

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of this server name |
