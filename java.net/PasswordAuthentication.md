# PasswordAuthentication

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PasswordAuthentication

```
class PasswordAuthentication
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.net.PasswordAuthentication](https://developer.android.com/reference/kotlin/java/net/PasswordAuthentication#) |

The class PasswordAuthentication is a data holder that is used by Authenticator. It is simply a repository for a user name and a password.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PasswordAuthentication](https://developer.android.com/reference/kotlin/java/net/PasswordAuthentication#PasswordAuthentication(kotlin.String,%20kotlin.CharArray))`(`userName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `password:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`)` Creates a new`PasswordAuthentication`object from the given user name and password. |

| Public methods ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | [getPassword](https://developer.android.com/reference/kotlin/java/net/PasswordAuthentication#getPassword())`()` Returns the user password. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getUserName](https://developer.android.com/reference/kotlin/java/net/PasswordAuthentication#getUserName())`()` Returns the user name. |

## Public constructors

### PasswordAuthentication

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PasswordAuthentication(
    userName: String!, 
    password: CharArray!)
```

Creates a new`PasswordAuthentication`object from the given user name and password.

Note that the given user password is cloned before it is stored in the new`PasswordAuthentication`object.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------|
| `userName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the user name |
| `password` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:the user's password |

## Public methods

### getPassword

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPassword(): CharArray!
```

Returns the user password.

Note that this method returns a reference to the password. It is the caller's responsibility to zero out the password information after it is no longer needed.

| Return ||
|------------------------------------------------------------------------------------------|--------------|
| [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | the password |

### getUserName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUserName(): String!
```

Returns the user name.

| Return ||
|-----------------------------------------------------------------------------------|---------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the user name |
