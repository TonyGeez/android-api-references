# Callback

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Callback

```
interface Callback
```

| [javax.security.auth.callback.Callback](Callback.md) |

| Known Direct Subclasses [PasswordCallback](PasswordCallback.md) |------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------| | [PasswordCallback](PasswordCallback.md) | Underlying security services instantiate and pass a`PasswordCallback`to the`handle`method of a`CallbackHandler`to retrieve password information. | |
| --- | --- | --- | --- | --- | --- | --- |

Implementations of this interface are passed to a`CallbackHandler`, allowing underlying security services the ability to interact with a calling application to retrieve specific authentication data such as usernames and passwords, or to display certain information, such as error and warning messages.

`Callback`implementations do not retrieve or display the information requested by underlying security services.`Callback`implementations simply provide the means to pass such requests to applications, and for applications, if appropriate, to return requested information back to the underlying security services.

## Summary
