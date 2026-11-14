# javax.security.auth.callback

# javax.security.auth.callback

## Interfaces

| [Callback](Callback.md) | Implementations of this interface are passed to a `CallbackHandler`, allowing underlying security services the ability to interact with a calling application to retrieve specific authentication data such as usernames and passwords, or to display certain information, such as error and warning messages. |
| --- | --- |
| [CallbackHandler](CallbackHandler.md) | An application implements a `CallbackHandler` and passes it to underlying security services so that they may interact with the application to retrieve specific authentication data, such as usernames and passwords, or to display certain information, such as error and warning messages. |

## Classes

| [PasswordCallback](PasswordCallback.md) | Underlying security services instantiate and pass a `PasswordCallback` to the `handle` method of a `CallbackHandler` to retrieve password information. |
| --- | --- |

## Exceptions

| [UnsupportedCallbackException](UnsupportedCallbackException.md) | Signals that a `CallbackHandler` does not recognize a particular `Callback`. |
| --- | --- |
