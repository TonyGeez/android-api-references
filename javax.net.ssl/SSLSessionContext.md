# SSLSessionContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SSLSessionContext

```
interface SSLSessionContext
```

| [javax.net.ssl.SSLSessionContext](SSLSessionContext.md) |

A represents a set of`SSLSession`s associated with a single entity. For example, it could be associated with a server or client who participates in many sessions concurrently.

Not all environments will contain session contexts.

There are`SSLSessionContext`parameters that affect how sessions are stored:

- Sessions can be set to expire after a specified time limit.
- The number of sessions that can be stored in context can be limited.

A session can be retrieved based on its session id, and all session id's in a`SSLSessionContext`can be listed.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Enumeration](../java.util/Enumeration.md)\< [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!\>! | [getIds](SSLSessionContext.md))`()` Returns an Enumeration of all session id's grouped under this`SSLSessionContext`. |
| abstract [SSLSession](SSLSession.md)! | [getSession](SSLSessionContext.md))`(`sessionId:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Returns the`SSLSession`bound to the specified session id. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSessionCacheSize](SSLSessionContext.md))`()` Returns the size of the cache used for storing`SSLSession`objects grouped under this`SSLSessionContext`. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSessionTimeout](SSLSessionContext.md))`()` Returns the timeout limit of`SSLSession`objects grouped under this`SSLSessionContext`. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSessionCacheSize](SSLSessionContext.md))`(`size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the size of the cache used for storing`SSLSession`objects grouped under this`SSLSessionContext`. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSessionTimeout](SSLSessionContext.md))`(`seconds:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the timeout limit for`SSLSession`objects grouped under this`SSLSessionContext`. |
| --- | --- |

## Public methods

### getIds

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getIds(): Enumeration<ByteArray!>!
```

Returns an Enumeration of all session id's grouped under this`SSLSessionContext`.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| [Enumeration](../java.util/Enumeration.md)< [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!>! | an enumeration of all the Session id's |

### getSession

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSession(sessionId: ByteArray!): SSLSession!
```

Returns the`SSLSession`bound to the specified session id.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------|
| `sessionId` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the Session identifier |

| Return ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [SSLSession](SSLSession.md)! | the`SSLSession`or null if the specified session id does not refer to a valid SSLSession. |

| Exceptions ||
|----------------------------------|-----------------------|
| `java.lang.NullPointerException` | if`sessionId`is null. |

### getSessionCacheSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSessionCacheSize(): Int
```

Returns the size of the cache used for storing`SSLSession`objects grouped under this`SSLSessionContext`.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | size of the session cache; zero means there is no size limit. |

**See Also**

- [#setSessionCacheSize](SSLSessionContext.md)) 

### getSessionTimeout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSessionTimeout(): Int
```

Returns the timeout limit of`SSLSession`objects grouped under this`SSLSessionContext`.

If the timeout limit is set to 't' seconds, a session exceeds the timeout limit 't' seconds after its creation time. When the timeout limit is exceeded for a session, the`SSLSession`object is invalidated and future connections cannot resume or rejoin the session. A check for sessions exceeding the timeout limit is made immediately whenever the timeout limit is changed for this`SSLSessionContext`.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the session timeout limit in seconds; zero means there is no limit. |

**See Also**

- [#setSessionTimeout](SSLSessionContext.md)) 

### setSessionCacheSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setSessionCacheSize(size: Int): Unit
```

Sets the size of the cache used for storing`SSLSession`objects grouped under this`SSLSessionContext`.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new session cache size limit; zero means there is no limit. |

| Exceptions ||
|--------------------------------------|--------------------------------|
| `java.lang.IllegalArgumentException` | if the specified size is`< 0`. |

**See Also**

- [#getSessionCacheSize](SSLSessionContext.md)) 

### setSessionTimeout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setSessionTimeout(seconds: Int): Unit
```

Sets the timeout limit for`SSLSession`objects grouped under this`SSLSessionContext`.

If the timeout limit is set to 't' seconds, a session exceeds the timeout limit 't' seconds after its creation time. When the timeout limit is exceeded for a session, the`SSLSession`object is invalidated and future connections cannot resume or rejoin the session. A check for sessions exceeding the timeout is made immediately whenever the timeout limit is changed for this`SSLSessionContext`.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `seconds` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new session timeout limit in seconds; zero means there is no limit. |

| Exceptions ||
|--------------------------------------|-----------------------------------|
| `java.lang.IllegalArgumentException` | if the timeout specified is`< 0`. |

**See Also**

- [#getSessionTimeout](SSLSessionContext.md))
