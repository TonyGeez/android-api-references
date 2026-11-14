# PasswordCallback

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PasswordCallback

```
open class PasswordCallback : Callback, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.security.auth.callback.PasswordCallback](PasswordCallback.md) |

Underlying security services instantiate and pass a`PasswordCallback`to the`handle`method of a`CallbackHandler`to retrieve password information.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PasswordCallback](PasswordCallback.md))`(`prompt:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `echoOn:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Construct a`PasswordCallback`with a prompt and a boolean specifying whether the password should be displayed as it is being typed. |

| Public methods ||
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearPassword](PasswordCallback.md))`()` Clear the retrieved password. |
| open [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | [getPassword](PasswordCallback.md))`()` Get the retrieved password. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPrompt](PasswordCallback.md))`()` Get the prompt. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEchoOn](PasswordCallback.md))`()` Return whether the password should be displayed as it is being typed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPassword](PasswordCallback.md))`(`password:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`)` Set the retrieved password. |

## Public constructors

### PasswordCallback

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PasswordCallback(
    prompt: String!, 
    echoOn: Boolean)
```

Construct a`PasswordCallback`with a prompt and a boolean specifying whether the password should be displayed as it is being typed.

<br />

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `prompt` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the prompt used to request the password. <br /> |
| `echoOn` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the password should be displayed as it is being typed. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`prompt`is null or if`prompt`has a length of 0. |

## Public methods

### clearPassword

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clearPassword(): Unit
```

Clear the retrieved password. 

### getPassword

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPassword(): CharArray!
```

Get the retrieved password.

This method returns a copy of the retrieved password.

<br />

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------------------|
| [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | the retrieved password, which may be null. |

**See Also**

- [#setPassword](PasswordCallback.md)) 

### getPrompt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPrompt(): String!
```

Get the prompt.

<br />

| Return ||
|-----------------------------------------------------------------------------------|-------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the prompt. |

### isEchoOn

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isEchoOn(): Boolean
```

Return whether the password should be displayed as it is being typed.

<br />

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the whether the password should be displayed as it is being typed. |

### setPassword

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPassword(password: CharArray!): Unit
```

Set the retrieved password.

This method makes a copy of the input*password*before storing it.

<br />

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `password` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:the retrieved password, which may be null. |

**See Also**

- [#getPassword](PasswordCallback.md))
