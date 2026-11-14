# WebViewDatabase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WebViewDatabase

Kotlin| [Java](../android/webkit/WebViewDatabase.md) 
| --- | --- |

```
abstract class WebViewDatabase
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.webkit.WebViewDatabase](../android/webkit/WebViewDatabase.md) |

This class allows developers to determine whether any WebView used in the application has stored any of the following types of browsing data and to clear any such stored data for all WebViews in the application.

- Username/password pairs for web forms
- HTTP authentication username/password pairs
- Data entered into text fields (e.g. for autocomplete suggestions)

<br />

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------|---|
| [WebViewDatabase](../android/webkit/WebViewDatabase.md))`()` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearFormData](../android/webkit/WebViewDatabase.md))`()` Clears any saved data for web forms. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearHttpAuthUsernamePassword](../android/webkit/WebViewDatabase.md))`()` Clears any saved credentials for HTTP authentication. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearUsernamePassword](../android/webkit/WebViewDatabase.md))`()` Clears any saved username/password pairs for web forms. |
| --- | --- |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | [getHttpAuthUsernamePassword](../android/webkit/WebViewDatabase.md))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `realm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves HTTP authentication credentials for a given host and realm from the [WebViewDatabase](../android/webkit/WebViewDatabase.md) instance. |
| openstatic [WebViewDatabase](../android/webkit/WebViewDatabase.md)! | [getInstance](../android/webkit/WebViewDatabase.md))`(`context:` ` [Context](../android/content/Context.md)!`)` <br /> |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasFormData](../android/webkit/WebViewDatabase.md))`()` Gets whether there is any saved data for web forms. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasHttpAuthUsernamePassword](../android/webkit/WebViewDatabase.md))`()` Gets whether there are any saved credentials for HTTP authentication. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasUsernamePassword](../android/webkit/WebViewDatabase.md))`()` Gets whether there are any saved username/password pairs for web forms. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHttpAuthUsernamePassword](../android/webkit/WebViewDatabase.md))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `realm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `username:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `password:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Stores HTTP authentication credentials for a given host and realm to the [WebViewDatabase](../android/webkit/WebViewDatabase.md) instance. |
| --- | --- |

## Public constructors

### WebViewDatabase

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
WebViewDatabase()
```

**Deprecated:** *This class should not be constructed by applications, use [getInstance(android.content.Context)](../android/webkit/WebViewDatabase.md))instead to fetch the singleton instance.*

## Public methods

### clearFormData

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun clearFormData(): Unit
```

**Deprecated:** *Deprecated in Java.*

Clears any saved data for web forms. 
**See Also**

- [#hasFormData](../android/webkit/WebViewDatabase.md)) 

### clearHttpAuthUsernamePassword

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun clearHttpAuthUsernamePassword(): Unit
```

Clears any saved credentials for HTTP authentication. This method only clears the username and password stored in WebViewDatabase instance. The username and password are not read from the [WebViewDatabase](../android/webkit/WebViewDatabase.md) during [WebViewClient.onReceivedHttpAuthRequest](../android/webkit/WebViewClient.md)). It is up to the app to do this or not.

The username and password used for http authentication might be cached in the network stack itself, and are not cleared when this method is called. WebView does not provide a special mechanism to clear HTTP authentication for implementing client logout. The client logout mechanism should be implemented by the Web site designer (such as server sending a HTTP 401 for invalidating credentials). 
**See Also**

- [#getHttpAuthUsernamePassword](../android/webkit/WebViewDatabase.md))
- [#setHttpAuthUsernamePassword](../android/webkit/WebViewDatabase.md))
- [#hasHttpAuthUsernamePassword](../android/webkit/WebViewDatabase.md)) 

### clearUsernamePassword

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun clearUsernamePassword(): Unit
```

**Deprecated:** *Saving passwords in WebView will not be supported in future versions.*

Clears any saved username/password pairs for web forms. Note that these are unrelated to HTTP authentication credentials. 
**See Also**

- [android.webkit.WebView#savePassword](../android/webkit/WebView.md))
- [#hasUsernamePassword](../android/webkit/WebViewDatabase.md)) 

### getHttpAuthUsernamePassword

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getHttpAuthUsernamePassword(
    host: String!, 
    realm: String!
): Array<String!>?
```

Retrieves HTTP authentication credentials for a given host and realm from the [WebViewDatabase](../android/webkit/WebViewDatabase.md) instance.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------|
| `host` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the host to which the credentials apply |
| `realm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the realm to which the credentials apply |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>? | the credentials as a String array, if found. The first element is the username and the second element is the password.`null`if no credentials are found. |

**See Also**

- [#setHttpAuthUsernamePassword](../android/webkit/WebViewDatabase.md))
- [#hasHttpAuthUsernamePassword](../android/webkit/WebViewDatabase.md))
- [#clearHttpAuthUsernamePassword](../android/webkit/WebViewDatabase.md)) 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(context: Context!): WebViewDatabase!
```  

### hasFormData

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun hasFormData(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Gets whether there is any saved data for web forms.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether there is any saved data for web forms |

**See Also**

- [#clearFormData](../android/webkit/WebViewDatabase.md)) 

### hasHttpAuthUsernamePassword

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun hasHttpAuthUsernamePassword(): Boolean
```

Gets whether there are any saved credentials for HTTP authentication.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether there are any saved credentials |

**See Also**

- [#getHttpAuthUsernamePassword](../android/webkit/WebViewDatabase.md))
- [#setHttpAuthUsernamePassword](../android/webkit/WebViewDatabase.md))
- [#clearHttpAuthUsernamePassword](../android/webkit/WebViewDatabase.md)) 

### hasUsernamePassword

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun hasUsernamePassword(): Boolean
```

**Deprecated:** *Saving passwords in WebView will not be supported in future versions.*

Gets whether there are any saved username/password pairs for web forms. Note that these are unrelated to HTTP authentication credentials.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if there are any saved username/password pairs |

**See Also**

- [android.webkit.WebView#savePassword](../android/webkit/WebView.md))
- [#clearUsernamePassword](../android/webkit/WebViewDatabase.md)) 

### setHttpAuthUsernamePassword

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setHttpAuthUsernamePassword(
    host: String!, 
    realm: String!, 
    username: String!, 
    password: String!
): Unit
```

Stores HTTP authentication credentials for a given host and realm to the [WebViewDatabase](../android/webkit/WebViewDatabase.md) instance.

To use HTTP authentication, the embedder application has to implement [WebViewClient.onReceivedHttpAuthRequest](../android/webkit/WebViewClient.md)), and call [HttpAuthHandler.proceed](../android/webkit/HttpAuthHandler.md))with the correct username and password.

The embedder app can get the username and password any way it chooses, and does not have to use [WebViewDatabase](../android/webkit/WebViewDatabase.md).

Notes:
- [WebViewDatabase](../android/webkit/WebViewDatabase.md) is provided only as a convenience to store and retrieve http authentication credentials. WebView does not read from it during HTTP authentication.
- WebView does not provide a special mechanism to clear HTTP authentication credentials for implementing client logout. The client logout mechanism should be implemented by the Web site designer (such as server sending a HTTP 401 for invalidating credentials).

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------|
| `host` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the host to which the credentials apply |
| `realm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the realm to which the credentials apply |
| `username` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the username |
| --- | --- |
| `password` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the password |

**See Also**

- [#getHttpAuthUsernamePassword](../android/webkit/WebViewDatabase.md))
- [#hasHttpAuthUsernamePassword](../android/webkit/WebViewDatabase.md))
- [#clearHttpAuthUsernamePassword](../android/webkit/WebViewDatabase.md))
