# SipProfile

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SipProfile

Kotlin| [Java](https://developer.android.com/reference/android/net/sip/SipProfile "View this page in Java") 
| --- | --- |

```
open class SipProfile : Cloneable, Parcelable, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.sip.SipProfile](https://developer.android.com/reference/kotlin/android/net/sip/SipProfile#) |

| **This class was deprecated in API level 31.**
|
| [android.net.sip.SipManager](https://developer.android.com/reference/kotlin/android/net/sip/SipManager) and associated classes are no longer supported and should not be used as the basis of future VOIP apps.

Defines a SIP profile, including a SIP account, domain and server information.

You can create a [SipProfile](https://developer.android.com/reference/kotlin/android/net/sip/SipProfile#) using [SipProfile.Builder](https://developer.android.com/reference/kotlin/android/net/sip/SipProfile.Builder). You can also retrieve one from a [SipSession](https://developer.android.com/reference/kotlin/android/net/sip/SipSession), using [android.net.sip.SipSession#getLocalProfile](https://developer.android.com/reference/kotlin/android/net/sip/SipSession#getLocalProfile())and [SipSession.getPeerProfile](https://developer.android.com/reference/kotlin/android/net/sip/SipSession#getPeerProfile()).
|
| ### Developer Guides
|
| For more information about using SIP, read the [Session Initiation Protocol](https://developer.android.com/guide/topics/network/sip.html) developer guide.

## Summary

| Nested classes ||
|------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Builder](https://developer.android.com/reference/kotlin/android/net/sip/SipProfile.Builder) Helper class for creating a [SipProfile](https://developer.android.com/reference/kotlin/android/net/sip/SipProfile#). |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/net/sip/SipProfile#describeContents())`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAuthUserName](https://developer.android.com/reference/kotlin/android/net/sip/SipProfile#getAuthUserName())`()` Gets the username for authentication. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getAutoRegistration](https://developer.android.com/reference/kotlin/android/net/sip/SipProfile#getAutoRegistration())`()` Gets the flag of 'Auto Registration'. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayName](https://developer.android.com/reference/kotlin/android/net/sip/SipProfile#getDisplayName())`()` Gets the display name of the user. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPassword](https://developer.android.com/reference/kotlin/android/net/sip/SipProfile#getPassword())`()` Gets the password. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPort](https://developer.android.com/reference/kotlin/android/net/sip/SipProfile#getPort())`()` Gets the port number of the SIP server. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getProfileName](https://developer.android.com/reference/kotlin/android/net/sip/SipProfile#getProfileName())`()` Gets the (user-defined) name of the profile. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getProtocol](https://developer.android.com/reference/kotlin/android/net/sip/SipProfile#getProtocol())`()` Gets the protocol used to connect to the server. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getProxyAddress](https://developer.android.com/reference/kotlin/android/net/sip/SipProfile#getProxyAddress())`()` Gets the network address of the server outbound proxy. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getSendKeepAlive](https://developer.android.com/reference/kotlin/android/net/sip/SipProfile#getSendKeepAlive())`()` Gets the flag of 'Sending keep-alive'. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSipDomain](https://developer.android.com/reference/kotlin/android/net/sip/SipProfile#getSipDomain())`()` Gets the SIP domain. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getUriString](https://developer.android.com/reference/kotlin/android/net/sip/SipProfile#getUriString())`()` Gets the SIP URI string of this profile. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getUserName](https://developer.android.com/reference/kotlin/android/net/sip/SipProfile#getUserName())`()` Gets the username. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCallingUid](https://developer.android.com/reference/kotlin/android/net/sip/SipProfile#setCallingUid(kotlin.Int))`(`uid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the calling process's Uid in the sip service. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/net/sip/SipProfile#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`out:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [SipProfile](https://developer.android.com/reference/kotlin/android/net/sip/SipProfile#)!\>! | [CREATOR](https://developer.android.com/reference/kotlin/android/net/sip/SipProfile#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public methods

### describeContents

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getAuthUserName

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAuthUserName(): String!
```

**Deprecated:** *Deprecated in Java.*

Gets the username for authentication. If it is null, then the username is used in authentication instead.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the authentication username |

**See Also**

- [#getUserName](https://developer.android.com/reference/kotlin/android/net/sip/SipProfile#getUserName()) 

### getAutoRegistration

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAutoRegistration(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Gets the flag of 'Auto Registration'.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the flag of registering the profile automatically. |

### getDisplayName

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDisplayName(): String!
```

**Deprecated:** *Deprecated in Java.*

Gets the display name of the user.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the display name of the user |

### getPassword

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPassword(): String!
```

**Deprecated:** *Deprecated in Java.*

Gets the password.

| Return ||
|-----------------------------------------------------------------------------------|--------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the password |

### getPort

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPort(): Int
```

**Deprecated:** *Deprecated in Java.*

Gets the port number of the SIP server.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the port number of the SIP server |

### getProfileName

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getProfileName(): String!
```

**Deprecated:** *Deprecated in Java.*

Gets the (user-defined) name of the profile.

| Return ||
|-----------------------------------------------------------------------------------|---------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | name of the profile |

### getProtocol

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getProtocol(): String!
```

**Deprecated:** *Deprecated in Java.*

Gets the protocol used to connect to the server.

| Return ||
|-----------------------------------------------------------------------------------|--------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the protocol |

### getProxyAddress

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getProxyAddress(): String!
```

**Deprecated:** *Deprecated in Java.*

Gets the network address of the server outbound proxy.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the network address of the server outbound proxy |

### getSendKeepAlive

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSendKeepAlive(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Gets the flag of 'Sending keep-alive'.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the flag of sending SIP keep-alive messages. |

### getSipDomain

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSipDomain(): String!
```

**Deprecated:** *Deprecated in Java.*

Gets the SIP domain.

| Return ||
|-----------------------------------------------------------------------------------|----------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the SIP domain |

### getUriString

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUriString(): String!
```

**Deprecated:** *Deprecated in Java.*

Gets the SIP URI string of this profile.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the SIP URI string of this profile |

### getUserName

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUserName(): String!
```

**Deprecated:** *Deprecated in Java.*

Gets the username.

| Return ||
|-----------------------------------------------------------------------------------|--------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the username |

### setCallingUid

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCallingUid(uid: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the calling process's Uid in the sip service. 

### writeToParcel

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
    out: Parcel, 
    flags: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<SipProfile!>!
```

**Deprecated:** *Deprecated in Java.*
