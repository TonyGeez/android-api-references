# Credential

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Credential

Kotlin| [Java](https://developer.android.com/reference/android/net/wifi/hotspot2/pps/Credential "View this page in Java") 

```
class Credential : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.net.wifi.hotspot2.pps.Credential](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential#) |

Class representing Credential subtree in the PerProviderSubscription (PPS) Management Object (MO) tree. For more info, refer to Hotspot 2.0 PPS MO defined in section 9.1 of the Hotspot 2.0 Release 2 Technical Specification. In addition to the fields in the Credential subtree, this will also maintain necessary information for the private key and certificates associated with this credential.

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [CertificateCredential](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential.CertificateCredential) Certificate based credential. |
| | [SimCredential](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential.SimCredential) SIM (Subscriber Identify Module) based credential. |
| | [UserCredential](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential.UserCredential) Username-password based credential. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Credential](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential#Credential())`()` Constructor for creating Credential with default values. |
| [Credential](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential#Credential(android.net.wifi.hotspot2.pps.Credential))`(`source:` ` [Credential](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential#)!`)` Copy constructor. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)! | [getCaCertificate](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential#getCaCertificate())`()` Get the CA (Certification Authority) certificate associated with this credential. |
| [Credential.CertificateCredential](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential.CertificateCredential)! | [getCertCredential](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential#getCertCredential())`()` Get the certificate credential information. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!\>! | [getClientCertificateChain](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential#getClientCertificateChain())`()` Get the client certificate chain associated with this credential. |
| [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey.html#)! | [getClientPrivateKey](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential#getClientPrivateKey())`()` Get the client private key associated with this credential. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimumTlsVersion](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential#getMinimumTlsVersion())`()` Get the minimum TLS version for TLS-based EAP methods. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getRealm](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential#getRealm())`()` Get the realm associated with this credential. |
| [Credential.SimCredential](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential.SimCredential)! | [getSimCredential](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential#getSimCredential())`()` Get the SIM credential information. |
| [Credential.UserCredential](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential.UserCredential)! | [getUserCredential](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential#getUserCredential())`()` Get the user credential information. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential#hashCode())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCaCertificate](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential#setCaCertificate(java.security.cert.X509Certificate))`(`caCertificate:` ` [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!`)` Set the CA (Certification Authority) certificate associated with this credential. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCertCredential](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential#setCertCredential(android.net.wifi.hotspot2.pps.Credential.CertificateCredential))`(`certCredential:` ` [Credential.CertificateCredential](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential.CertificateCredential)!`)` Set the certificate credential information. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setClientCertificateChain](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential#setClientCertificateChain(kotlin.Array))`(`certificateChain:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!>!`)` Set the client certificate chain associated with this credential. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setClientPrivateKey](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential#setClientPrivateKey(java.security.PrivateKey))`(`clientPrivateKey:` ` [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey.html#)!`)` Set the client private key associated with this credential. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMinimumTlsVersion](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential#setMinimumTlsVersion(kotlin.Int))`(`tlsVersion:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the minimum TLS version for TLS-based EAP methods. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRealm](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential#setRealm(kotlin.String))`(`realm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the realm associated with this credential. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSimCredential](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential#setSimCredential(android.net.wifi.hotspot2.pps.Credential.SimCredential))`(`simCredential:` ` [Credential.SimCredential](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential.SimCredential)!`)` Set the SIM credential information. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setUserCredential](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential#setUserCredential(android.net.wifi.hotspot2.pps.Credential.UserCredential))`(`userCredential:` ` [Credential.UserCredential](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential.UserCredential)!`)` Set the user credential information. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [Credential](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential#CREATOR:android.os.Parcelable.Creator) <br /> |

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
| `source` | [Credential](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential#)!:The source to copy from |

## Public methods

### describeContents

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

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
| [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)! | CA certificate associated with this credential,`null`if certificate is not set or certificate is more than one. |

### getCertCredential

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCertCredential(): Credential.CertificateCredential!
```

Get the certificate credential information.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| [Credential.CertificateCredential](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential.CertificateCredential)! | certificate credential information |

### getClientCertificateChain

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getClientCertificateChain(): Array<X509Certificate!>!
```

Get the client certificate chain associated with this credential.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!>! | client certificate chain associated with this credential |

### getClientPrivateKey

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getClientPrivateKey(): PrivateKey!
```

Get the client private key associated with this credential.

| Return ||
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey.html#)! | client private key associated with this credential. |

### getMinimumTlsVersion

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMinimumTlsVersion(): Int
```

Get the minimum TLS version for TLS-based EAP methods.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the TLS version Value is [android.net.wifi.WifiEnterpriseConfig#TLS_V1_0](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig.html#TLS_V1_0:kotlin.Int), [android.net.wifi.WifiEnterpriseConfig#TLS_V1_1](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig.html#TLS_V1_1:kotlin.Int), [android.net.wifi.WifiEnterpriseConfig#TLS_V1_2](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig.html#TLS_V1_2:kotlin.Int), or [android.net.wifi.WifiEnterpriseConfig#TLS_V1_3](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig.html#TLS_V1_3:kotlin.Int) |

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
| [Credential.SimCredential](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential.SimCredential)! | SIM credential information |

### getUserCredential

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUserCredential(): Credential.UserCredential!
```

Get the user credential information.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [Credential.UserCredential](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential.UserCredential)! | user credential information |

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
| `caCertificate` | [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!:The CA certificate to set to |

### setCertCredential

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setCertCredential(certCredential: Credential.CertificateCredential!): Unit
```

Set the certificate credential information.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `certCredential` | [Credential.CertificateCredential](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential.CertificateCredential)!:The certificate credential to set to |

### setClientCertificateChain

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setClientCertificateChain(certificateChain: Array<X509Certificate!>!): Unit
```

Set the client certificate chain associated with this credential.

| Parameters ||
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `certificateChain` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!\>!:The client certificate chain to set to |

### setClientPrivateKey

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setClientPrivateKey(clientPrivateKey: PrivateKey!): Unit
```

Set the client private key associated with this credential.

| Parameters ||
|--------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `clientPrivateKey` | [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey.html#)!:the client private key to set to |

### setMinimumTlsVersion

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setMinimumTlsVersion(tlsVersion: Int): Unit
```

Set the minimum TLS version for TLS-based EAP methods. [android.net.wifi.WifiManager#isTlsMinimumVersionSupported()](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.html#isTlsMinimumVersionSupported())indicates whether or not a minimum TLS version can be set. If not supported, the minimum TLS version is always TLS v1.0.

[android.net.wifi.WifiManager#isTlsV13Supported()](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.html#isTlsV13Supported())indicates whether or not TLS v1.3 is supported. If requested minimum is not supported, it will default to the maximum supported version.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tlsVersion` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the TLS version Value is [android.net.wifi.WifiEnterpriseConfig#TLS_V1_0](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig.html#TLS_V1_0:kotlin.Int), [android.net.wifi.WifiEnterpriseConfig#TLS_V1_1](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig.html#TLS_V1_1:kotlin.Int), [android.net.wifi.WifiEnterpriseConfig#TLS_V1_2](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig.html#TLS_V1_2:kotlin.Int), or [android.net.wifi.WifiEnterpriseConfig#TLS_V1_3](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig.html#TLS_V1_3:kotlin.Int) |

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
| `simCredential` | [Credential.SimCredential](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential.SimCredential)!:The SIM credential to set to |

### setUserCredential

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setUserCredential(userCredential: Credential.UserCredential!): Unit
```

Set the user credential information.

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `userCredential` | [Credential.UserCredential](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential.UserCredential)!:The user credential to set to |

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<Credential!>
```
