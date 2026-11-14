# Credential

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Credential

Kotlin| [Java](../android/net/wifi/hotspot2/pps/Credential.md) 
| --- | --- |

```
class Credential : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.hotspot2.pps.Credential](../android/net/wifi/hotspot2/pps/Credential.md) |

Class representing Credential subtree in the PerProviderSubscription (PPS) Management Object (MO) tree. For more info, refer to Hotspot 2.0 PPS MO defined in section 9.1 of the Hotspot 2.0 Release 2 Technical Specification. In addition to the fields in the Credential subtree, this will also maintain necessary information for the private key and certificates associated with this credential.

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [CertificateCredential](../android/net/wifi/hotspot2/pps/Credential.CertificateCredential.md) Certificate based credential. |
| | [SimCredential](../android/net/wifi/hotspot2/pps/Credential.SimCredential.md) SIM (Subscriber Identify Module) based credential. |
| | [UserCredential](../android/net/wifi/hotspot2/pps/Credential.UserCredential.md) Username-password based credential. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Credential](../android/net/wifi/hotspot2/pps/Credential.md))`()` Constructor for creating Credential with default values. |
| [Credential](../android/net/wifi/hotspot2/pps/Credential.md))`(`source:` ` [Credential](../android/net/wifi/hotspot2/pps/Credential.md)!`)` Copy constructor. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/net/wifi/hotspot2/pps/Credential.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/net/wifi/hotspot2/pps/Credential.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [X509Certificate](../java/security/cert/X509Certificate.md)! | [getCaCertificate](../android/net/wifi/hotspot2/pps/Credential.md))`()` Get the CA (Certification Authority) certificate associated with this credential. |
| --- | --- |
| [Credential.CertificateCredential](../android/net/wifi/hotspot2/pps/Credential.CertificateCredential.md)! | [getCertCredential](../android/net/wifi/hotspot2/pps/Credential.md))`()` Get the certificate credential information. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [X509Certificate](../java/security/cert/X509Certificate.md)!\>! | [getClientCertificateChain](../android/net/wifi/hotspot2/pps/Credential.md))`()` Get the client certificate chain associated with this credential. |
| [PrivateKey](../java/security/PrivateKey.md)! | [getClientPrivateKey](../android/net/wifi/hotspot2/pps/Credential.md))`()` Get the client private key associated with this credential. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimumTlsVersion](../android/net/wifi/hotspot2/pps/Credential.md))`()` Get the minimum TLS version for TLS-based EAP methods. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getRealm](../android/net/wifi/hotspot2/pps/Credential.md))`()` Get the realm associated with this credential. |
| [Credential.SimCredential](../android/net/wifi/hotspot2/pps/Credential.SimCredential.md)! | [getSimCredential](../android/net/wifi/hotspot2/pps/Credential.md))`()` Get the SIM credential information. |
| --- | --- |
| [Credential.UserCredential](../android/net/wifi/hotspot2/pps/Credential.UserCredential.md)! | [getUserCredential](../android/net/wifi/hotspot2/pps/Credential.md))`()` Get the user credential information. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/net/wifi/hotspot2/pps/Credential.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCaCertificate](../android/net/wifi/hotspot2/pps/Credential.md))`(`caCertificate:` ` [X509Certificate](../java/security/cert/X509Certificate.md)!`)` Set the CA (Certification Authority) certificate associated with this credential. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCertCredential](../android/net/wifi/hotspot2/pps/Credential.md))`(`certCredential:` ` [Credential.CertificateCredential](../android/net/wifi/hotspot2/pps/Credential.CertificateCredential.md)!`)` Set the certificate credential information. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setClientCertificateChain](../android/net/wifi/hotspot2/pps/Credential.md))`(`certificateChain:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [X509Certificate](../java/security/cert/X509Certificate.md)!>!`)` Set the client certificate chain associated with this credential. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setClientPrivateKey](../android/net/wifi/hotspot2/pps/Credential.md))`(`clientPrivateKey:` ` [PrivateKey](../java/security/PrivateKey.md)!`)` Set the client private key associated with this credential. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMinimumTlsVersion](../android/net/wifi/hotspot2/pps/Credential.md))`(`tlsVersion:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the minimum TLS version for TLS-based EAP methods. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRealm](../android/net/wifi/hotspot2/pps/Credential.md))`(`realm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the realm associated with this credential. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSimCredential](../android/net/wifi/hotspot2/pps/Credential.md))`(`simCredential:` ` [Credential.SimCredential](../android/net/wifi/hotspot2/pps/Credential.SimCredential.md)!`)` Set the SIM credential information. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setUserCredential](../android/net/wifi/hotspot2/pps/Credential.md))`(`userCredential:` ` [Credential.UserCredential](../android/net/wifi/hotspot2/pps/Credential.UserCredential.md)!`)` Set the user credential information. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/net/wifi/hotspot2/pps/Credential.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/net/wifi/hotspot2/pps/Credential.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [Credential](../android/net/wifi/hotspot2/pps/Credential.md)!\> | [CREATOR](../android/net/wifi/hotspot2/pps/Credential.md) <br /> |

## Public constructors

### Credential

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Credential()
```

Constructor for creating Credential with default values. 

### Credential

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Credential(source: Credential!)
```

Copy constructor.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| `source` | [Credential](../android/net/wifi/hotspot2/pps/Credential.md)!:The source to copy from |

## Public methods

### describeContents

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### equals

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getCaCertificate

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCaCertificate(): X509Certificate!
```

Get the CA (Certification Authority) certificate associated with this credential.

| Return ||
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [X509Certificate](../java/security/cert/X509Certificate.md)! | CA certificate associated with this credential,`null`if certificate is not set or certificate is more than one. |

### getCertCredential

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCertCredential(): Credential.CertificateCredential!
```

Get the certificate credential information.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| [Credential.CertificateCredential](../android/net/wifi/hotspot2/pps/Credential.CertificateCredential.md)! | certificate credential information |

### getClientCertificateChain

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getClientCertificateChain(): Array<X509Certificate!>!
```

Get the client certificate chain associated with this credential.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [X509Certificate](../java/security/cert/X509Certificate.md)!>! | client certificate chain associated with this credential |

### getClientPrivateKey

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getClientPrivateKey(): PrivateKey!
```

Get the client private key associated with this credential.

| Return ||
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [PrivateKey](../java/security/PrivateKey.md)! | client private key associated with this credential. |

### getMinimumTlsVersion

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMinimumTlsVersion(): Int
```

Get the minimum TLS version for TLS-based EAP methods.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the TLS version Value is [android.net.wifi.WifiEnterpriseConfig#TLS_V1_0](../android/net/wifi/WifiEnterpriseConfig.md), [android.net.wifi.WifiEnterpriseConfig#TLS_V1_1](../android/net/wifi/WifiEnterpriseConfig.md), [android.net.wifi.WifiEnterpriseConfig#TLS_V1_2](../android/net/wifi/WifiEnterpriseConfig.md), or [android.net.wifi.WifiEnterpriseConfig#TLS_V1_3](../android/net/wifi/WifiEnterpriseConfig.md) |

### getRealm

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRealm(): String!
```

Get the realm associated with this credential.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the realm associated with this credential |

### getSimCredential

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSimCredential(): Credential.SimCredential!
```

Get the SIM credential information.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| [Credential.SimCredential](../android/net/wifi/hotspot2/pps/Credential.SimCredential.md)! | SIM credential information |

### getUserCredential

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUserCredential(): Credential.UserCredential!
```

Get the user credential information.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [Credential.UserCredential](../android/net/wifi/hotspot2/pps/Credential.UserCredential.md)! | user credential information |

### hashCode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### setCaCertificate

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setCaCertificate(caCertificate: X509Certificate!): Unit
```

Set the CA (Certification Authority) certificate associated with this credential.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `caCertificate` | [X509Certificate](../java/security/cert/X509Certificate.md)!:The CA certificate to set to |

### setCertCredential

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setCertCredential(certCredential: Credential.CertificateCredential!): Unit
```

Set the certificate credential information.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `certCredential` | [Credential.CertificateCredential](../android/net/wifi/hotspot2/pps/Credential.CertificateCredential.md)!:The certificate credential to set to |

### setClientCertificateChain

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setClientCertificateChain(certificateChain: Array<X509Certificate!>!): Unit
```

Set the client certificate chain associated with this credential.

| Parameters ||
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `certificateChain` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [X509Certificate](../java/security/cert/X509Certificate.md)!\>!:The client certificate chain to set to |

### setClientPrivateKey

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setClientPrivateKey(clientPrivateKey: PrivateKey!): Unit
```

Set the client private key associated with this credential.

| Parameters ||
|--------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `clientPrivateKey` | [PrivateKey](../java/security/PrivateKey.md)!:the client private key to set to |

### setMinimumTlsVersion

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setMinimumTlsVersion(tlsVersion: Int): Unit
```

Set the minimum TLS version for TLS-based EAP methods. [android.net.wifi.WifiManager#isTlsMinimumVersionSupported()](../android/net/wifi/WifiManager.md))indicates whether or not a minimum TLS version can be set. If not supported, the minimum TLS version is always TLS v1.0.

[android.net.wifi.WifiManager#isTlsV13Supported()](../android/net/wifi/WifiManager.md))indicates whether or not TLS v1.3 is supported. If requested minimum is not supported, it will default to the maximum supported version.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tlsVersion` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the TLS version Value is [android.net.wifi.WifiEnterpriseConfig#TLS_V1_0](../android/net/wifi/WifiEnterpriseConfig.md), [android.net.wifi.WifiEnterpriseConfig#TLS_V1_1](../android/net/wifi/WifiEnterpriseConfig.md), [android.net.wifi.WifiEnterpriseConfig#TLS_V1_2](../android/net/wifi/WifiEnterpriseConfig.md), or [android.net.wifi.WifiEnterpriseConfig#TLS_V1_3](../android/net/wifi/WifiEnterpriseConfig.md) |

| Exceptions ||
|--------------------------------------|--------------------------------|
| `java.lang.IllegalArgumentException` | if the TLS version is invalid. |

### setRealm

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setRealm(realm: String!): Unit
```

Set the realm associated with this credential.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------|
| `realm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The realm to set to |

### setSimCredential

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setSimCredential(simCredential: Credential.SimCredential!): Unit
```

Set the SIM credential information.

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `simCredential` | [Credential.SimCredential](../android/net/wifi/hotspot2/pps/Credential.SimCredential.md)!:The SIM credential to set to |

### setUserCredential

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setUserCredential(userCredential: Credential.UserCredential!): Unit
```

Set the user credential information.

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `userCredential` | [Credential.UserCredential](../android/net/wifi/hotspot2/pps/Credential.UserCredential.md)!:The user credential to set to |

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android/os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<Credential!>
```
