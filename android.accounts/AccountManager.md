Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AccountManager

Kotlin | [Java](https://developer.android.com/reference/android/accounts/AccountManager "View this page in Java")

```
open class AccountManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.accounts.AccountManager](https://developer.android.com/reference/kotlin/android/accounts/AccountManager#) |

This class provides access to a centralized registry of the user's online accounts. The user enters credentials (username and password) once per account, granting applications access to online resources with "one-click" approval.

Different online services have different ways of handling accounts and authentication, so the account manager uses pluggable *authenticator* modules for different *account types*. Authenticators (which may be written by third parties) handle the actual details of validating account credentials and storing account information. For example, Google, Facebook, and Microsoft Exchange each have their own authenticator.

Many servers support some notion of an *authentication token* , which can be used to authenticate a request to the server without sending the user's actual password. (Auth tokens are normally created with a separate request which does include the user's credentials.) AccountManager can generate auth tokens for applications, so the application doesn't need to handle passwords directly. Auth tokens are normally reusable and cached by AccountManager, but must be refreshed periodically. It's the responsibility of applications to *invalidate* auth tokens when they stop working so the AccountManager knows it needs to regenerate them.

Applications accessing a server normally go through these steps:

- Get an instance of AccountManager using `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#get(android.content.Context)`.
- List the available accounts using `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#getAccountsByType(kotlin.String)` or `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#getAccountsByTypeAndFeatures(kotlin.String,%20kotlin.Array,%20android.accounts.AccountManagerCallback,%20android.os.Handler)`. Normally applications will only be interested in accounts with one particular *type* , which identifies the authenticator. Account *features* are used to identify particular account subtypes and capabilities. Both the account type and features are authenticator-specific strings, and must be known by the application in coordination with its preferred authenticators.
- Select one or more of the available accounts, possibly by asking the user for their preference. If no suitable accounts are available, `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#addAccount(kotlin.String,%20kotlin.String,%20kotlin.Array,%20android.os.Bundle,%20android.app.Activity,%20android.accounts.AccountManagerCallback,%20android.os.Handler)` may be called to prompt the user to create an account of the appropriate type.
- **Important:** If the application is using a previously remembered account selection, it must make sure the account is still in the list of accounts returned by `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#getAccountsByType(kotlin.String)`. Requesting an auth token for an account no longer on the device results in an undefined failure.
- Request an auth token for the selected account(s) using one of the #getAuthToken methods or related helpers. Refer to the description of each method for exact usage and error handling details.
- Make the request using the auth token. The form of the auth token, the format of the request, and the protocol used are all specific to the service you are accessing. The application may use whatever network and protocol libraries are useful.
- **Important:** If the request fails with an authentication error, it could be that a cached auth token is stale and no longer honored by the server. The application must call `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#invalidateAuthToken(kotlin.String,%20kotlin.String)` to remove the token from the cache, otherwise requests will continue failing! After invalidating the auth token, immediately go back to the "Request an auth token" step above. If the process fails the second time, then it can be treated as a "genuine" authentication failure and the user notified or other appropriate actions taken.

Some AccountManager methods may need to interact with the user to prompt for credentials, present options, or ask the user to add an account. The caller may choose whether to allow AccountManager to directly launch the necessary user interface and wait for the user, or to return an Intent which the caller may use to launch the interface, or (in some cases) to install a notification which the user can select at any time to launch the interface. To have AccountManager launch the interface directly, the caller must supply the current foreground `https://developer.android.com/reference/kotlin/android/app/Activity.html#` context.

Many AccountManager methods take `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerCallback` and `https://developer.android.com/reference/kotlin/android/os/Handler.html#` as parameters. These methods return immediately and run asynchronously. If a callback is provided then `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerCallback#run(android.accounts.AccountManagerFuture)` will be invoked on the Handler's thread when the request completes, successfully or not. The result is retrieved by calling `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture#getResult()` on the `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture` returned by the method (and also passed to the callback). This method waits for the operation to complete (if necessary) and either returns the result or throws an exception if an error occurred during the operation. To make the request synchronously, call `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture#getResult()` immediately on receiving the future from the method; no callback need be supplied.

Requests which may block, including `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture#getResult()`, must never be called on the application's main event thread. These operations throw `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#` if they are used on the main thread.

## Summary

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#ACTION_ACCOUNT_REMOVED:kotlin.String` Action sent as a broadcast Intent by the AccountsService when any account is removed or renamed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#ACTION_AUTHENTICATOR_INTENT:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#AUTHENTICATOR_ATTRIBUTES_NAME:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#AUTHENTICATOR_META_DATA_NAME:kotlin.String` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#ERROR_CODE_BAD_ARGUMENTS:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#ERROR_CODE_BAD_AUTHENTICATION:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#ERROR_CODE_BAD_REQUEST:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#ERROR_CODE_CANCELED:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#ERROR_CODE_INVALID_RESPONSE:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#ERROR_CODE_NETWORK_ERROR:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#ERROR_CODE_REMOTE_EXCEPTION:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#ERROR_CODE_UNSUPPORTED_OPERATION:kotlin.Int` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNTS:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_AUTHENTICATOR_RESPONSE:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_MANAGER_RESPONSE:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_NAME:kotlin.String` Bundle key used for the `https://developer.android.com/reference/kotlin/java/lang/String.html#` account name in results from methods which return information about a particular account. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_SESSION_BUNDLE:kotlin.String` Bundle key used for a `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` in result from `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#startAddAccountSession(kotlin.String,%20kotlin.String,%20kotlin.Array,%20android.os.Bundle,%20android.app.Activity,%20android.accounts.AccountManagerCallback,%20android.os.Handler)` and friends which returns session data for installing an account later. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_STATUS_TOKEN:kotlin.String` Bundle key used for the `https://developer.android.com/reference/kotlin/java/lang/String.html#` account status token in result from `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#startAddAccountSession(kotlin.String,%20kotlin.String,%20kotlin.Array,%20android.os.Bundle,%20android.app.Activity,%20android.accounts.AccountManagerCallback,%20android.os.Handler)` and friends which returns information about a particular account. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_TYPE:kotlin.String` Bundle key used for the `https://developer.android.com/reference/kotlin/java/lang/String.html#` account type in results from methods which return information about a particular account. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ANDROID_PACKAGE_NAME:kotlin.String` The Android package of the caller will be set in the options bundle by the `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#` and will be passed to the AccountManagerService and to the AccountAuthenticators. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_AUTHENTICATOR_TYPES:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_AUTHTOKEN:kotlin.String` Bundle key used for the auth token value in results from #getAuthToken and friends. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_AUTH_FAILED_MESSAGE:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_AUTH_TOKEN_LABEL:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_BOOLEAN_RESULT:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_CALLER_PID:kotlin.String` The process id of caller app. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_CALLER_UID:kotlin.String` The UID of caller app. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ERROR_CODE:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ERROR_MESSAGE:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_INTENT:kotlin.String` Bundle key used for an `https://developer.android.com/reference/kotlin/android/content/Intent.html#` in results from methods that may require the caller to interact with the user. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_LAST_AUTHENTICATED_TIME:kotlin.String` Bundle key used to supply the last time the credentials of the account were authenticated successfully. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_PASSWORD:kotlin.String` Bundle key used to supply the password directly in options to `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#confirmCredentials(android.accounts.Account,%20android.os.Bundle,%20android.app.Activity,%20android.accounts.AccountManagerCallback,%20android.os.Handler)`, rather than prompting the user with the standard password prompt. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_USERDATA:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#LOGIN_ACCOUNTS_CHANGED_ACTION:kotlin.String` Action sent as a broadcast Intent by the AccountsService when accounts are added, accounts are removed, or an account's credentials (saved password, etc) are changed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#PACKAGE_NAME_KEY_LEGACY_NOT_VISIBLE:kotlin.String` Key to set default visibility for applications which don't satisfy conditions in `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#PACKAGE_NAME_KEY_LEGACY_VISIBLE:kotlin.String`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#PACKAGE_NAME_KEY_LEGACY_VISIBLE:kotlin.String` Key to set visibility for applications which satisfy one of the following conditions: - Target API level below `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int` and have deprecated `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#GET_ACCOUNTS:kotlin.String` permission. - Have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#GET_ACCOUNTS_PRIVILEGED:kotlin.String` permission. - Have the same signature as authenticator. - Have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_CONTACTS:kotlin.String` permission and account type may be associated with contacts data - (verified by `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_CONTACTS:kotlin.String` permission check for the authenticator). See `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#getAccountVisibility(android.accounts.Account,%20kotlin.String)`. <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#VISIBILITY_NOT_VISIBLE:kotlin.Int` Account is not visible to given application and only authenticator can grant visibility. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#VISIBILITY_UNDEFINED:kotlin.Int` Account visibility was not set. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#VISIBILITY_USER_MANAGED_NOT_VISIBLE:kotlin.Int` Account is not visible to given application, but user can reveal it, for example, using `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#newChooseAccountIntent(android.accounts.Account,%20kotlin.collections.MutableList,%20kotlin.Array,%20kotlin.String,%20kotlin.String,%20kotlin.Array,%20android.os.Bundle)` |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#VISIBILITY_USER_MANAGED_VISIBLE:kotlin.Int` Account is visible to given application, but user can revoke visibility. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#VISIBILITY_VISIBLE:kotlin.Int` Account is always visible to given application and only authenticator can revoke visibility. |

| Public methods ||
|---|---|
| open [AccountManagerFuture](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture)\< [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!\>! | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#addAccount(kotlin.String,%20kotlin.String,%20kotlin.Array,%20android.os.Bundle,%20android.app.Activity,%20android.accounts.AccountManagerCallback,%20android.os.Handler)(accountType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, authTokenType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, requiredFeatures: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!, addAccountOptions: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!, activity: https://developer.android.com/reference/kotlin/android/app/Activity.html#!, callback: https://developer.android.com/reference/kotlin/android/accounts/AccountManagerCallback<https://developer.android.com/reference/kotlin/android/os/Bundle.html#!>!, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#!)` Asks the user to add an account of a specified type. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#addAccountExplicitly(android.accounts.Account,%20kotlin.String,%20android.os.Bundle)(account: https://developer.android.com/reference/kotlin/android/accounts/Account!, password: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, userdata: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)` Adds an account directly to the AccountManager. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#addAccountExplicitly(android.accounts.Account,%20kotlin.String,%20android.os.Bundle,%20kotlin.collections.MutableMap)(account: https://developer.android.com/reference/kotlin/android/accounts/Account!, password: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!, visibility: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>!)` Adds an account directly to the AccountManager. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#addOnAccountsUpdatedListener(android.accounts.OnAccountsUpdateListener,%20android.os.Handler,%20kotlin.Boolean)(listener: https://developer.android.com/reference/kotlin/android/accounts/OnAccountsUpdateListener!, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#!, updateImmediately: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Adds an `https://developer.android.com/reference/kotlin/android/accounts/OnAccountsUpdateListener` to this instance of the `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#addOnAccountsUpdatedListener(android.accounts.OnAccountsUpdateListener,%20android.os.Handler,%20kotlin.Boolean,%20kotlin.Array)(listener: https://developer.android.com/reference/kotlin/android/accounts/OnAccountsUpdateListener!, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#!, updateImmediately: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, accountTypes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Adds an `https://developer.android.com/reference/kotlin/android/accounts/OnAccountsUpdateListener` to this instance of the `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#`. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#blockingGetAuthToken(android.accounts.Account,%20kotlin.String,%20kotlin.Boolean)(account: https://developer.android.com/reference/kotlin/android/accounts/Account!, authTokenType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, notifyAuthFailure: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` This convenience helper synchronously gets an auth token with `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#getAuthToken(android.accounts.Account,%20kotlin.String,%20kotlin.Boolean,%20android.accounts.AccountManagerCallback,%20android.os.Handler)`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#clearPassword(android.accounts.Account)(account: https://developer.android.com/reference/kotlin/android/accounts/Account!)` Forgets a saved password. |
| open [AccountManagerFuture](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture)\< [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!\>! | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#confirmCredentials(android.accounts.Account,%20android.os.Bundle,%20android.app.Activity,%20android.accounts.AccountManagerCallback,%20android.os.Handler)(account: https://developer.android.com/reference/kotlin/android/accounts/Account!, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!, activity: https://developer.android.com/reference/kotlin/android/app/Activity.html#!, callback: https://developer.android.com/reference/kotlin/android/accounts/AccountManagerCallback<https://developer.android.com/reference/kotlin/android/os/Bundle.html#!>!, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#!)` Confirms that the user knows the password for an account to make extra sure they are the owner of the account. |
| open [AccountManagerFuture](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture)\< [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!\>! | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#editProperties(kotlin.String,%20android.app.Activity,%20android.accounts.AccountManagerCallback,%20android.os.Handler)(accountType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, activity: https://developer.android.com/reference/kotlin/android/app/Activity.html#!, callback: https://developer.android.com/reference/kotlin/android/accounts/AccountManagerCallback<https://developer.android.com/reference/kotlin/android/os/Bundle.html#!>!, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#!)` Offers the user an opportunity to change an authenticator's settings. |
| open [AccountManagerFuture](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture)\< [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!\>! | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#finishSession(android.os.Bundle,%20android.app.Activity,%20android.accounts.AccountManagerCallback,%20android.os.Handler)(sessionBundle: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!, activity: https://developer.android.com/reference/kotlin/android/app/Activity.html#!, callback: https://developer.android.com/reference/kotlin/android/accounts/AccountManagerCallback<https://developer.android.com/reference/kotlin/android/os/Bundle.html#!>!, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#!)` Finishes the session started by `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#startAddAccountSession(kotlin.String,%20kotlin.String,%20kotlin.Array,%20android.os.Bundle,%20android.app.Activity,%20android.accounts.AccountManagerCallback,%20android.os.Handler)` or `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#startUpdateCredentialsSession(android.accounts.Account,%20kotlin.String,%20android.os.Bundle,%20android.app.Activity,%20android.accounts.AccountManagerCallback,%20android.os.Handler)`. |
| open static [AccountManager](https://developer.android.com/reference/kotlin/android/accounts/AccountManager#)! | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#get(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!)` Gets an AccountManager instance associated with a Context. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#getAccountVisibility(android.accounts.Account,%20kotlin.String)(account: https://developer.android.com/reference/kotlin/android/accounts/Account!, packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Get visibility of certain account for given application. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Account](https://developer.android.com/reference/kotlin/android/accounts/Account)!\> | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#getAccounts()()` Lists all accounts visible to the caller regardless of type. |
| open [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [Account](https://developer.android.com/reference/kotlin/android/accounts/Account)!, [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#getAccountsAndVisibilityForPackage(kotlin.String,%20kotlin.String)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, accountType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Gets all accounts of given type and their visibility for specific package. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Account](https://developer.android.com/reference/kotlin/android/accounts/Account)!\> | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#getAccountsByType(kotlin.String)(type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Lists all accounts of particular type visible to the caller. |
| open [AccountManagerFuture](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture)\< [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Account](https://developer.android.com/reference/kotlin/android/accounts/Account)!\>!\>! | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#getAccountsByTypeAndFeatures(kotlin.String,%20kotlin.Array,%20android.accounts.AccountManagerCallback,%20android.os.Handler)(type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, features: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!, callback: https://developer.android.com/reference/kotlin/android/accounts/AccountManagerCallback<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/accounts/Account!>!>!, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#!)` Lists all accounts of a type which have certain features. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Account](https://developer.android.com/reference/kotlin/android/accounts/Account)!\> | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#getAccountsByTypeForPackage(kotlin.String,%20kotlin.String)(type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns the accounts visible to the specified package in an environment where some apps are not authorized to view all accounts. |
| open [AccountManagerFuture](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture)\< [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!\>! | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#getAuthToken(android.accounts.Account,%20kotlin.String,%20android.os.Bundle,%20android.app.Activity,%20android.accounts.AccountManagerCallback,%20android.os.Handler)(account: https://developer.android.com/reference/kotlin/android/accounts/Account!, authTokenType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!, activity: https://developer.android.com/reference/kotlin/android/app/Activity.html#!, callback: https://developer.android.com/reference/kotlin/android/accounts/AccountManagerCallback<https://developer.android.com/reference/kotlin/android/os/Bundle.html#!>!, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#!)` Gets an auth token of the specified type for a particular account, prompting the user for credentials if necessary. |
| open [AccountManagerFuture](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture)\< [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!\>! | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#getAuthToken(android.accounts.Account,%20kotlin.String,%20android.os.Bundle,%20kotlin.Boolean,%20android.accounts.AccountManagerCallback,%20android.os.Handler)(account: https://developer.android.com/reference/kotlin/android/accounts/Account!, authTokenType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!, notifyAuthFailure: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, callback: https://developer.android.com/reference/kotlin/android/accounts/AccountManagerCallback<https://developer.android.com/reference/kotlin/android/os/Bundle.html#!>!, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#!)` Gets an auth token of the specified type for a particular account, optionally raising a notification if the user must enter credentials. |
| open [AccountManagerFuture](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture)\< [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!\>! | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#getAuthToken(android.accounts.Account,%20kotlin.String,%20kotlin.Boolean,%20android.accounts.AccountManagerCallback,%20android.os.Handler)(account: https://developer.android.com/reference/kotlin/android/accounts/Account!, authTokenType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, notifyAuthFailure: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, callback: https://developer.android.com/reference/kotlin/android/accounts/AccountManagerCallback<https://developer.android.com/reference/kotlin/android/os/Bundle.html#!>!, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#!)` Gets an auth token of the specified type for a particular account, optionally raising a notification if the user must enter credentials. |
| open [AccountManagerFuture](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture)\< [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!\>! | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#getAuthTokenByFeatures(kotlin.String,%20kotlin.String,%20kotlin.Array,%20android.app.Activity,%20android.os.Bundle,%20android.os.Bundle,%20android.accounts.AccountManagerCallback,%20android.os.Handler)(accountType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, authTokenType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, features: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!, activity: https://developer.android.com/reference/kotlin/android/app/Activity.html#!, addAccountOptions: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!, getAuthTokenOptions: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!, callback: https://developer.android.com/reference/kotlin/android/accounts/AccountManagerCallback<https://developer.android.com/reference/kotlin/android/os/Bundle.html#!>!, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#!)` This convenience helper combines the functionality of `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#getAccountsByTypeAndFeatures(kotlin.String,%20kotlin.Array,%20android.accounts.AccountManagerCallback,%20android.os.Handler)`, #getAuthToken, and `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#addAccount(kotlin.String,%20kotlin.String,%20kotlin.Array,%20android.os.Bundle,%20android.app.Activity,%20android.accounts.AccountManagerCallback,%20android.os.Handler)`. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [AuthenticatorDescription](https://developer.android.com/reference/kotlin/android/accounts/AuthenticatorDescription)!\>! | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#getAuthenticatorTypes()()` Lists the currently registered authenticators. |
| open [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#getPackagesAndVisibilityForAccount(android.accounts.Account)(account: https://developer.android.com/reference/kotlin/android/accounts/Account!)` Returns package names and visibility which were explicitly set for given account. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#getPassword(android.accounts.Account)(account: https://developer.android.com/reference/kotlin/android/accounts/Account!)` Gets the saved password associated with the account. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#getPreviousName(android.accounts.Account)(account: https://developer.android.com/reference/kotlin/android/accounts/Account!)` Gets the previous name associated with the account or `null`, if none. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#getUserData(android.accounts.Account,%20kotlin.String)(account: https://developer.android.com/reference/kotlin/android/accounts/Account!, key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Gets the user data named by "key" associated with the account. |
| open [AccountManagerFuture](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#hasFeatures(android.accounts.Account,%20kotlin.Array,%20android.accounts.AccountManagerCallback,%20android.os.Handler)(account: https://developer.android.com/reference/kotlin/android/accounts/Account!, features: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!, callback: https://developer.android.com/reference/kotlin/android/accounts/AccountManagerCallback<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html!>!, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#!)` Finds out whether a particular account has all the specified features. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#invalidateAuthToken(kotlin.String,%20kotlin.String)(accountType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, authToken: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Removes an auth token from the AccountManager's cache. |
| open [AccountManagerFuture](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#isCredentialsUpdateSuggested(android.accounts.Account,%20kotlin.String,%20android.accounts.AccountManagerCallback,%20android.os.Handler)(account: https://developer.android.com/reference/kotlin/android/accounts/Account!, statusToken: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, callback: https://developer.android.com/reference/kotlin/android/accounts/AccountManagerCallback<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html!>!, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#!)` Checks whether `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#updateCredentials(android.accounts.Account,%20kotlin.String,%20android.os.Bundle,%20android.app.Activity,%20android.accounts.AccountManagerCallback,%20android.os.Handler)` or `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#startUpdateCredentialsSession(android.accounts.Account,%20kotlin.String,%20android.os.Bundle,%20android.app.Activity,%20android.accounts.AccountManagerCallback,%20android.os.Handler)` should be called with respect to the specified account. |
| open static [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)! | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#newChooseAccountIntent(android.accounts.Account,%20java.util.ArrayList,%20kotlin.Array,%20kotlin.Boolean,%20kotlin.String,%20kotlin.String,%20kotlin.Array,%20android.os.Bundle)(selectedAccount: https://developer.android.com/reference/kotlin/android/accounts/Account!, allowableAccounts: https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<https://developer.android.com/reference/kotlin/android/accounts/Account!>!, allowableAccountTypes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!, alwaysPromptForAccount: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, descriptionOverrideText: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, addAccountAuthTokenType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, addAccountRequiredFeatures: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!, addAccountOptions: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)` Deprecated in favor of `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#newChooseAccountIntent(android.accounts.Account,%20kotlin.collections.MutableList,%20kotlin.Array,%20kotlin.String,%20kotlin.String,%20kotlin.Array,%20android.os.Bundle)`. |
| open static [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)! | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#newChooseAccountIntent(android.accounts.Account,%20kotlin.collections.MutableList,%20kotlin.Array,%20kotlin.String,%20kotlin.String,%20kotlin.Array,%20android.os.Bundle)(selectedAccount: https://developer.android.com/reference/kotlin/android/accounts/Account!, allowableAccounts: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/accounts/Account!>!, allowableAccountTypes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!, descriptionOverrideText: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, addAccountAuthTokenType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, addAccountRequiredFeatures: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!, addAccountOptions: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)` Returns an intent to an `https://developer.android.com/reference/kotlin/android/app/Activity.html#` that prompts the user to choose from a list of accounts. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#notifyAccountAuthenticated(android.accounts.Account)(account: https://developer.android.com/reference/kotlin/android/accounts/Account!)` Notifies the system that the account has just been authenticated. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#peekAuthToken(android.accounts.Account,%20kotlin.String)(account: https://developer.android.com/reference/kotlin/android/accounts/Account!, authTokenType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Gets an auth token from the AccountManager's cache. |
| open [AccountManagerFuture](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#removeAccount(android.accounts.Account,%20android.accounts.AccountManagerCallback,%20android.os.Handler)(account: https://developer.android.com/reference/kotlin/android/accounts/Account!, callback: https://developer.android.com/reference/kotlin/android/accounts/AccountManagerCallback<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html!>!, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#!)` Removes an account from the AccountManager. |
| open [AccountManagerFuture](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture)\< [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!\>! | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#removeAccount(android.accounts.Account,%20android.app.Activity,%20android.accounts.AccountManagerCallback,%20android.os.Handler)(account: https://developer.android.com/reference/kotlin/android/accounts/Account!, activity: https://developer.android.com/reference/kotlin/android/app/Activity.html#!, callback: https://developer.android.com/reference/kotlin/android/accounts/AccountManagerCallback<https://developer.android.com/reference/kotlin/android/os/Bundle.html#!>!, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#!)` Removes an account from the AccountManager. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#removeAccountExplicitly(android.accounts.Account)(account: https://developer.android.com/reference/kotlin/android/accounts/Account!)` Removes an account directly. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#removeOnAccountsUpdatedListener(android.accounts.OnAccountsUpdateListener)(listener: https://developer.android.com/reference/kotlin/android/accounts/OnAccountsUpdateListener!)` Removes an `https://developer.android.com/reference/kotlin/android/accounts/OnAccountsUpdateListener` previously registered with #addOnAccountsUpdatedListener. |
| open [AccountManagerFuture](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture)\< [Account](https://developer.android.com/reference/kotlin/android/accounts/Account)!\>! | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#renameAccount(android.accounts.Account,%20kotlin.String,%20android.accounts.AccountManagerCallback,%20android.os.Handler)(account: https://developer.android.com/reference/kotlin/android/accounts/Account!, newName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, callback: https://developer.android.com/reference/kotlin/android/accounts/AccountManagerCallback<https://developer.android.com/reference/kotlin/android/accounts/Account!>!, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#!)` Rename the specified `https://developer.android.com/reference/kotlin/android/accounts/Account`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#setAccountVisibility(android.accounts.Account,%20kotlin.String,%20kotlin.Int)(account: https://developer.android.com/reference/kotlin/android/accounts/Account!, packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, visibility: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set visibility value of given account to certain package. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#setAuthToken(android.accounts.Account,%20kotlin.String,%20kotlin.String)(account: https://developer.android.com/reference/kotlin/android/accounts/Account!, authTokenType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, authToken: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Adds an auth token to the AccountManager cache for an account. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#setPassword(android.accounts.Account,%20kotlin.String)(account: https://developer.android.com/reference/kotlin/android/accounts/Account!, password: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Sets or forgets a saved password. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#setUserData(android.accounts.Account,%20kotlin.String,%20kotlin.String)(account: https://developer.android.com/reference/kotlin/android/accounts/Account!, key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Sets one userdata key for an account. |
| open [AccountManagerFuture](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture)\< [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!\>! | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#startAddAccountSession(kotlin.String,%20kotlin.String,%20kotlin.Array,%20android.os.Bundle,%20android.app.Activity,%20android.accounts.AccountManagerCallback,%20android.os.Handler)(accountType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, authTokenType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, requiredFeatures: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!, activity: https://developer.android.com/reference/kotlin/android/app/Activity.html#!, callback: https://developer.android.com/reference/kotlin/android/accounts/AccountManagerCallback<https://developer.android.com/reference/kotlin/android/os/Bundle.html#!>!, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#!)` Asks the user to authenticate with an account of a specified type. |
| open [AccountManagerFuture](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture)\< [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!\>! | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#startUpdateCredentialsSession(android.accounts.Account,%20kotlin.String,%20android.os.Bundle,%20android.app.Activity,%20android.accounts.AccountManagerCallback,%20android.os.Handler)(account: https://developer.android.com/reference/kotlin/android/accounts/Account!, authTokenType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!, activity: https://developer.android.com/reference/kotlin/android/app/Activity.html#!, callback: https://developer.android.com/reference/kotlin/android/accounts/AccountManagerCallback<https://developer.android.com/reference/kotlin/android/os/Bundle.html#!>!, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#!)` Asks the user to enter a new password for the account but not updating the saved credentials for the account until `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#finishSession(android.os.Bundle,%20android.app.Activity,%20android.accounts.AccountManagerCallback,%20android.os.Handler)` is called. |
| open [AccountManagerFuture](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture)\< [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!\>! | `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#updateCredentials(android.accounts.Account,%20kotlin.String,%20android.os.Bundle,%20android.app.Activity,%20android.accounts.AccountManagerCallback,%20android.os.Handler)(account: https://developer.android.com/reference/kotlin/android/accounts/Account!, authTokenType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!, activity: https://developer.android.com/reference/kotlin/android/app/Activity.html#!, callback: https://developer.android.com/reference/kotlin/android/accounts/AccountManagerCallback<https://developer.android.com/reference/kotlin/android/os/Bundle.html#!>!, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#!)` Asks the user to enter a new password for an account, updating the saved credentials for the account. |

## Constants

### ACTION_ACCOUNT_REMOVED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_ACCOUNT_REMOVED: String
```

Action sent as a broadcast Intent by the AccountsService when any account is removed or renamed. Only applications which were able to see the account will receive the intent. Intent extra will include the following fields:

- `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_NAME:kotlin.String` - the name of the removed account
- `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_TYPE:kotlin.String` - the type of the account

<br />

 Value: "android.accounts.action.ACCOUNT_REMOVED"

### ACTION_AUTHENTICATOR_INTENT

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_AUTHENTICATOR_INTENT: String
```

 Value: "android.accounts.AccountAuthenticator"

### AUTHENTICATOR_ATTRIBUTES_NAME

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTHENTICATOR_ATTRIBUTES_NAME: String
```

 Value: "account-authenticator"

### AUTHENTICATOR_META_DATA_NAME

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTHENTICATOR_META_DATA_NAME: String
```

 Value: "android.accounts.AccountAuthenticator"

### ERROR_CODE_BAD_ARGUMENTS

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_CODE_BAD_ARGUMENTS: Int
```

 Value: 7

### ERROR_CODE_BAD_AUTHENTICATION

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_CODE_BAD_AUTHENTICATION: Int
```

 Value: 9

### ERROR_CODE_BAD_REQUEST

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_CODE_BAD_REQUEST: Int
```

 Value: 8

### ERROR_CODE_CANCELED

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_CODE_CANCELED: Int
```

 Value: 4

### ERROR_CODE_INVALID_RESPONSE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_CODE_INVALID_RESPONSE: Int
```

 Value: 5

### ERROR_CODE_NETWORK_ERROR

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_CODE_NETWORK_ERROR: Int
```

 Value: 3

### ERROR_CODE_REMOTE_EXCEPTION

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_CODE_REMOTE_EXCEPTION: Int
```

 Value: 1

### ERROR_CODE_UNSUPPORTED_OPERATION

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_CODE_UNSUPPORTED_OPERATION: Int
```

 Value: 6

### KEY_ACCOUNTS

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_ACCOUNTS: String
```

 Value: "accounts"

### KEY_ACCOUNT_AUTHENTICATOR_RESPONSE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_ACCOUNT_AUTHENTICATOR_RESPONSE: String
```

 Value: "accountAuthenticatorResponse"

### KEY_ACCOUNT_MANAGER_RESPONSE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_ACCOUNT_MANAGER_RESPONSE: String
```

 Value: "accountManagerResponse"

### KEY_ACCOUNT_NAME

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_ACCOUNT_NAME: String
```

Bundle key used for the `https://developer.android.com/reference/kotlin/java/lang/String.html#` account name in results from methods which return information about a particular account.

 Value: "authAccount"

### KEY_ACCOUNT_SESSION_BUNDLE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_ACCOUNT_SESSION_BUNDLE: String
```

Bundle key used for a `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` in result from `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#startAddAccountSession(kotlin.String,%20kotlin.String,%20kotlin.Array,%20android.os.Bundle,%20android.app.Activity,%20android.accounts.AccountManagerCallback,%20android.os.Handler)` and friends which returns session data for installing an account later.

 Value: "accountSessionBundle"

### KEY_ACCOUNT_STATUS_TOKEN

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_ACCOUNT_STATUS_TOKEN: String
```

Bundle key used for the `https://developer.android.com/reference/kotlin/java/lang/String.html#` account status token in result from `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#startAddAccountSession(kotlin.String,%20kotlin.String,%20kotlin.Array,%20android.os.Bundle,%20android.app.Activity,%20android.accounts.AccountManagerCallback,%20android.os.Handler)` and friends which returns information about a particular account.

 Value: "accountStatusToken"

### KEY_ACCOUNT_TYPE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_ACCOUNT_TYPE: String
```

Bundle key used for the `https://developer.android.com/reference/kotlin/java/lang/String.html#` account type in results from methods which return information about a particular account.

 Value: "accountType"

### KEY_ANDROID_PACKAGE_NAME

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_ANDROID_PACKAGE_NAME: String
```

The Android package of the caller will be set in the options bundle by the `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#` and will be passed to the AccountManagerService and to the AccountAuthenticators. The uid of the caller will be known by the AccountManagerService as well as the AccountAuthenticators so they will be able to verify that the package is consistent with the uid (a uid might be shared by many packages).

 Value: "androidPackageName"

### KEY_AUTHENTICATOR_TYPES

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_AUTHENTICATOR_TYPES: String
```

 Value: "authenticator_types"

### KEY_AUTHTOKEN

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_AUTHTOKEN: String
```

Bundle key used for the auth token value in results from #getAuthToken and friends.

 Value: "authtoken"

### KEY_AUTH_FAILED_MESSAGE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_AUTH_FAILED_MESSAGE: String
```

 Value: "authFailedMessage"

### KEY_AUTH_TOKEN_LABEL

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_AUTH_TOKEN_LABEL: String
```

 Value: "authTokenLabelKey"

### KEY_BOOLEAN_RESULT

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_BOOLEAN_RESULT: String
```

 Value: "booleanResult"

### KEY_CALLER_PID

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CALLER_PID: String
```

The process id of caller app.

 Value: "callerPid"

### KEY_CALLER_UID

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CALLER_UID: String
```

The UID of caller app.

 Value: "callerUid"

### KEY_ERROR_CODE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_ERROR_CODE: String
```

 Value: "errorCode"

### KEY_ERROR_MESSAGE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_ERROR_MESSAGE: String
```

 Value: "errorMessage"

### KEY_INTENT

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_INTENT: String
```

Bundle key used for an `https://developer.android.com/reference/kotlin/android/content/Intent.html#` in results from methods that may require the caller to interact with the user. The Intent can be used to start the corresponding user interface activity.

 Value: "intent"

### KEY_LAST_AUTHENTICATED_TIME

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_LAST_AUTHENTICATED_TIME: String
```

Bundle key used to supply the last time the credentials of the account were authenticated successfully. Time is specified in milliseconds since epoch. Associated time is updated on successful authentication of account on adding account, confirming credentials, or updating credentials.

 Value: "lastAuthenticatedTime"

### KEY_PASSWORD

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_PASSWORD: String
```

Bundle key used to supply the password directly in options to `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#confirmCredentials(android.accounts.Account,%20android.os.Bundle,%20android.app.Activity,%20android.accounts.AccountManagerCallback,%20android.os.Handler)`, rather than prompting the user with the standard password prompt.

 Value: "password"

### KEY_USERDATA

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_USERDATA: String
```

 Value: "userdata"

### LOGIN_ACCOUNTS_CHANGED_ACTION

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LOGIN_ACCOUNTS_CHANGED_ACTION: String
```

**Deprecated:** *use #addOnAccountsUpdatedListener to get account updates in runtime.*

Action sent as a broadcast Intent by the AccountsService when accounts are added, accounts are removed, or an account's credentials (saved password, etc) are changed.

 Value: "android.accounts.LOGIN_ACCOUNTS_CHANGED"

**See Also**

- `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#ACTION_ACCOUNT_REMOVED:kotlin.String`

### PACKAGE_NAME_KEY_LEGACY_NOT_VISIBLE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PACKAGE_NAME_KEY_LEGACY_NOT_VISIBLE: String
```

Key to set default visibility for applications which don't satisfy conditions in `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#PACKAGE_NAME_KEY_LEGACY_VISIBLE:kotlin.String`. If the value was not set by authenticator `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#VISIBILITY_USER_MANAGED_NOT_VISIBLE:kotlin.Int` is used.

 Value: "android:accounts:key_legacy_not_visible"

### PACKAGE_NAME_KEY_LEGACY_VISIBLE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PACKAGE_NAME_KEY_LEGACY_VISIBLE: String
```

Key to set visibility for applications which satisfy one of the following conditions:

- Target API level below `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int` and have deprecated `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#GET_ACCOUNTS:kotlin.String` permission.
- Have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#GET_ACCOUNTS_PRIVILEGED:kotlin.String` permission.
- Have the same signature as authenticator.
- Have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_CONTACTS:kotlin.String` permission and account type may be associated with contacts data - (verified by `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_CONTACTS:kotlin.String` permission check for the authenticator).

See `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#getAccountVisibility(android.accounts.Account,%20kotlin.String)`. If the value was not set by authenticator `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#VISIBILITY_USER_MANAGED_VISIBLE:kotlin.Int` is used.

<br />

 Value: "android:accounts:key_legacy_visible"

### VISIBILITY_NOT_VISIBLE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VISIBILITY_NOT_VISIBLE: Int
```

Account is not visible to given application and only authenticator can grant visibility.

 Value: 3

### VISIBILITY_UNDEFINED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VISIBILITY_UNDEFINED: Int
```

Account visibility was not set. Default visibility value will be used. See `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#PACKAGE_NAME_KEY_LEGACY_VISIBLE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#PACKAGE_NAME_KEY_LEGACY_NOT_VISIBLE:kotlin.String`

 Value: 0

### VISIBILITY_USER_MANAGED_NOT_VISIBLE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VISIBILITY_USER_MANAGED_NOT_VISIBLE: Int
```

Account is not visible to given application, but user can reveal it, for example, using `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#newChooseAccountIntent(android.accounts.Account,%20kotlin.collections.MutableList,%20kotlin.Array,%20kotlin.String,%20kotlin.String,%20kotlin.Array,%20android.os.Bundle)`

 Value: 4

### VISIBILITY_USER_MANAGED_VISIBLE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VISIBILITY_USER_MANAGED_VISIBLE: Int
```

Account is visible to given application, but user can revoke visibility.

 Value: 2

### VISIBILITY_VISIBLE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VISIBILITY_VISIBLE: Int
```

Account is always visible to given application and only authenticator can revoke visibility.

 Value: 1

## Public methods

### addAccount

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addAccount(
    accountType: String!, 
    authTokenType: String!, 
    requiredFeatures: Array<String!>!, 
    addAccountOptions: Bundle!, 
    activity: Activity!, 
    callback: AccountManagerCallback<Bundle!>!, 
    handler: Handler!
): AccountManagerFuture<Bundle!>!
```

Asks the user to add an account of a specified type. The authenticator for this account type processes this request with the appropriate user interface. If the user does elect to create a new account, the account name is returned.

This method may be called from any thread, but the returned `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture` must not be used on the main thread.

**NOTE:** If targeting your app to work on API level 22 and before, MANAGE_ACCOUNTS permission is needed for those platforms. See docs for this function in API level 22. 
Requires android.Manifest.permission.MANAGE_ACCOUNTS

| Parameters ||
|---|---|
| `accountType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The type of account to add; must not be null |
| `authTokenType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The type of auth token (see #getAuthToken) this account will need to be able to generate, null for none |
| `requiredFeatures` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: The features (see `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#hasFeatures(android.accounts.Account,%20kotlin.Array,%20android.accounts.AccountManagerCallback,%20android.os.Handler)`) this account must have, null for none |
| `addAccountOptions` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!: Authenticator-specific options for the request, may be null or empty |
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!: The `https://developer.android.com/reference/kotlin/android/app/Activity.html#` context to use for launching a new authenticator-defined sub-Activity to prompt the user to create an account; used only to call startActivity(); if null, the prompt will not be launched directly, but the necessary `https://developer.android.com/reference/kotlin/android/content/Intent.html#` will be returned to the caller instead |
| `callback` | [AccountManagerCallback](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerCallback)\< [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!\>!: Callback to invoke when the request completes, null for no callback |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!: `https://developer.android.com/reference/kotlin/android/os/Handler.html#` identifying the callback thread, null for the main thread |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture<https://developer.android.com/reference/kotlin/android/os/Bundle.html#!>!` | An `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture` which resolves to a Bundle with these fields if activity was specified and an account was created: - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_NAME:kotlin.String` - the name of the account created - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_TYPE:kotlin.String` - the type of the account If no activity was specified, the returned Bundle contains only `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_INTENT:kotlin.String` with the `https://developer.android.com/reference/kotlin/android/content/Intent.html#` needed to launch the actual account creation process. If an error occurred, `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture#getResult()` throws: - `https://developer.android.com/reference/kotlin/android/accounts/AuthenticatorException` if no authenticator was registered for this account type or the authenticator failed to respond - `https://developer.android.com/reference/kotlin/android/accounts/OperationCanceledException` if the operation was canceled for any reason, including the user canceling the creation process or adding accounts (of this type) has been disabled by policy - `https://developer.android.com/reference/kotlin/java/io/IOException.html#` if the authenticator experienced an I/O problem creating a new account, usually because of network trouble |

### addAccountExplicitly

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addAccountExplicitly(
    account: Account!, 
    password: String!, 
    userdata: Bundle!
): Boolean
```

Adds an account directly to the AccountManager. Normally used by sign-up wizards associated with authenticators, not directly by applications.

Calling this method does not update the last authenticated timestamp, referred by `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_LAST_AUTHENTICATED_TIME:kotlin.String`. To update it, call `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#notifyAccountAuthenticated(android.accounts.Account)` after getting success. However, if this method is called when it is triggered by addAccount() or addAccountAsUser() or similar functions, then there is no need to update timestamp manually as it is updated automatically by framework on successful completion of the mentioned functions.

It is safe to call this method from the main thread.

This method requires the caller to have a signature match with the authenticator that owns the specified account.

**NOTE:** If targeting your app to work on API level 22 and before, AUTHENTICATE_ACCOUNTS permission is needed for those platforms. See docs for this function in API level 22. 
Requires android.Manifest.permission.AUTHENTICATE_ACCOUNTS

| Parameters ||
|---|---|
| `account` | [Account](https://developer.android.com/reference/kotlin/android/accounts/Account)!: The `https://developer.android.com/reference/kotlin/android/accounts/Account` to add |
| `password` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The password to associate with the account, null for none |
| `userdata` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!: String values to use for the account's userdata, null for none |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the account was successfully added, false if the account already exists, the account is null, the user is locked, or another error occurs. |

### addAccountExplicitly

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addAccountExplicitly(
    account: Account!, 
    password: String!, 
    extras: Bundle!, 
    visibility: MutableMap<String!, Int!>!
): Boolean
```

Adds an account directly to the AccountManager. Additionally it specifies Account visibility for given list of packages.

Normally used by sign-up wizards associated with authenticators, not directly by applications.

Calling this method does not update the last authenticated timestamp, referred by `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_LAST_AUTHENTICATED_TIME:kotlin.String`. To update it, call `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#notifyAccountAuthenticated(android.accounts.Account)` after getting success.

It is safe to call this method from the main thread.

This method requires the caller to have a signature match with the authenticator that owns the specified account.

| Parameters ||
|---|---|
| `account` | [Account](https://developer.android.com/reference/kotlin/android/accounts/Account)!: The `https://developer.android.com/reference/kotlin/android/accounts/Account` to add |
| `password` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The password to associate with the account, null for none |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!: String values to use for the account's userdata, null for none |
| `visibility` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>!: Map from packageName to visibility values which will be set before account is added. See `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#getAccountVisibility(android.accounts.Account,%20kotlin.String)` for possible values. Declaring [package visibility](https://developer.android.com/reference/kotlin/training/basics/intents/package-visibility) needs for package names in the map is needed, if the caller is targeting API level 34 and above. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the account was successfully added, false if the account already exists, the account is null, or another error occurs. |

### addOnAccountsUpdatedListener

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addOnAccountsUpdatedListener(
    listener: OnAccountsUpdateListener!, 
    handler: Handler!, 
    updateImmediately: Boolean
): Unit
```

Adds an `https://developer.android.com/reference/kotlin/android/accounts/OnAccountsUpdateListener` to this instance of the `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#`. This listener will be notified whenever user or AbstractAccountAuthenticator made changes to accounts of any type related to the caller. This method is equivalent to addOnAccountsUpdatedListener(listener, handler, updateImmediately, null). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#GET_ACCOUNTS:kotlin.String`
**See Also**

- `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#addOnAccountsUpdatedListener(android.accounts.OnAccountsUpdateListener,%20android.os.Handler,%20kotlin.Boolean,%20kotlin.Array)`

### addOnAccountsUpdatedListener

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addOnAccountsUpdatedListener(
    listener: OnAccountsUpdateListener!, 
    handler: Handler!, 
    updateImmediately: Boolean, 
    accountTypes: Array<String!>!
): Unit
```

Adds an `https://developer.android.com/reference/kotlin/android/accounts/OnAccountsUpdateListener` to this instance of the `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#`. This listener will be notified whenever user or AbstractAccountAuthenticator made changes to accounts of given types related to the caller - either list of accounts returned by `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#getAccounts()` was changed, or new account was added for which user can grant access to the caller.

As long as this listener is present, the AccountManager instance will not be garbage-collected, and neither will the `https://developer.android.com/reference/kotlin/android/content/Context.html#` used to retrieve it, which may be a large Activity instance. To avoid memory leaks, you must remove this listener before then. Normally listeners are added in an Activity or Service's android.app.Activity#onCreate and removed in `https://developer.android.com/reference/kotlin/android/app/Activity.html#onDestroy()`.

It is safe to call this method from the main thread.

| Parameters ||
|---|---|
| `listener` | [OnAccountsUpdateListener](https://developer.android.com/reference/kotlin/android/accounts/OnAccountsUpdateListener)!: The listener to send notifications to |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!: `https://developer.android.com/reference/kotlin/android/os/Handler.html#` identifying the thread to use for notifications, null for the main thread |
| `updateImmediately` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If true, the listener will be invoked (on the handler thread) right away with the current account list |
| `accountTypes` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: If set, only changes to accounts of given types will be reported. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if listener is null |
| `java.lang.IllegalStateException` | if listener was already added |

### blockingGetAuthToken

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun blockingGetAuthToken(
    account: Account!, 
    authTokenType: String!, 
    notifyAuthFailure: Boolean
): String!
```

This convenience helper synchronously gets an auth token with `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#getAuthToken(android.accounts.Account,%20kotlin.String,%20kotlin.Boolean,%20android.accounts.AccountManagerCallback,%20android.os.Handler)`.

This method may block while a network request completes, and must never be made from the main thread.

**NOTE:** If targeting your app to work on API level 22 and before, USE_CREDENTIALS permission is needed for those platforms. See docs for this function in API level 22. 
Requires android.Manifest.permission.USE_CREDENTIALS

| Parameters ||
|---|---|
| `account` | [Account](https://developer.android.com/reference/kotlin/android/accounts/Account)!: The account to fetch an auth token for |
| `authTokenType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The auth token type, see #getAuthToken |
| `notifyAuthFailure` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If true, display a notification and return null if authentication fails; if false, prompt and wait for the user to re-enter correct credentials before returning |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | An auth token of the specified type for this account, or null if authentication fails or none can be fetched. |

| Exceptions ||
|---|---|
| `android.accounts.AuthenticatorException` | if the authenticator failed to respond |
| `android.accounts.OperationCanceledException` | if the request was canceled for any reason, including the user canceling a credential request |
| `java.io.IOException` | if the authenticator experienced an I/O problem creating a new auth token, usually because of network trouble |

### clearPassword

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clearPassword(account: Account!): Unit
```

Forgets a saved password. This erases the local copy of the password; it does not change the user's account password on the server. Has the same effect as setPassword(account, null) but requires fewer permissions, and may be used by applications or management interfaces to "sign out" from an account.

This method only successfully clear the account's password when the caller has the same signature as the authenticator that owns the specified account. Otherwise, this method will silently fail.

It is safe to call this method from the main thread.

**NOTE:** If targeting your app to work on API level 22 and before, MANAGE_ACCOUNTS permission is needed for those platforms. See docs for this function in API level 22. 
Requires android.Manifest.permission.MANAGE_ACCOUNTS

| Parameters ||
|---|---|
| `account` | [Account](https://developer.android.com/reference/kotlin/android/accounts/Account)!: The account whose password to clear |

### confirmCredentials

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun confirmCredentials(
    account: Account!, 
    options: Bundle!, 
    activity: Activity!, 
    callback: AccountManagerCallback<Bundle!>!, 
    handler: Handler!
): AccountManagerFuture<Bundle!>!
```

Confirms that the user knows the password for an account to make extra sure they are the owner of the account. The user-entered password can be supplied directly, otherwise the authenticator for this account type prompts the user with the appropriate interface. This method is intended for applications which want extra assurance; for example, the phone lock screen uses this to let the user unlock the phone with an account password if they forget the lock pattern.

If the user-entered password matches a saved password for this account, the request is considered valid; otherwise the authenticator verifies the password (usually by contacting the server).

This method may be called from any thread, but the returned `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture` must not be used on the main thread.

**NOTE:** If targeting your app to work on API level 22 and before, MANAGE_ACCOUNTS permission is needed for those platforms. See docs for this function in API level 22. 
Requires android.Manifest.permission.MANAGE_ACCOUNTS

| Parameters ||
|---|---|
| `account` | [Account](https://developer.android.com/reference/kotlin/android/accounts/Account)!: The account to confirm password knowledge for |
| `options` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!: Authenticator-specific options for the request; if the `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_PASSWORD:kotlin.String` string field is present, the authenticator may use it directly rather than prompting the user; may be null or empty |
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!: The `https://developer.android.com/reference/kotlin/android/app/Activity.html#` context to use for launching a new authenticator-defined sub-Activity to prompt the user to enter a password; used only to call startActivity(); if null, the prompt will not be launched directly, but the necessary `https://developer.android.com/reference/kotlin/android/content/Intent.html#` will be returned to the caller instead |
| `callback` | [AccountManagerCallback](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerCallback)\< [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!\>!: Callback to invoke when the request completes, null for no callback |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!: `https://developer.android.com/reference/kotlin/android/os/Handler.html#` identifying the callback thread, null for the main thread |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture<https://developer.android.com/reference/kotlin/android/os/Bundle.html#!>!` | An `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture` which resolves to a Bundle with these fields if activity or password was supplied and the account was successfully verified: - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_NAME:kotlin.String` - the name of the account verified - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_TYPE:kotlin.String` - the type of the account - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_BOOLEAN_RESULT:kotlin.String` - true to indicate success If no activity or password was specified, the returned Bundle contains `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_INTENT:kotlin.String` with the `https://developer.android.com/reference/kotlin/android/content/Intent.html#` needed to launch the password prompt. Also the returning Bundle may contain `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_LAST_AUTHENTICATED_TIME:kotlin.String` indicating the last time the credential was validated/created. If an error occurred,`https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture#getResult()` throws: - `https://developer.android.com/reference/kotlin/android/accounts/AuthenticatorException` if the authenticator failed to respond - `https://developer.android.com/reference/kotlin/android/accounts/OperationCanceledException` if the operation was canceled for any reason, including the user canceling the password prompt - `https://developer.android.com/reference/kotlin/java/io/IOException.html#` if the authenticator experienced an I/O problem verifying the password, usually because of network trouble |

### editProperties

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun editProperties(
    accountType: String!, 
    activity: Activity!, 
    callback: AccountManagerCallback<Bundle!>!, 
    handler: Handler!
): AccountManagerFuture<Bundle!>!
```

Offers the user an opportunity to change an authenticator's settings. These properties are for the authenticator in general, not a particular account. Not all authenticators support this method.

This method may be called from any thread, but the returned `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture` must not be used on the main thread.

This method requires the caller to have the same signature as the authenticator associated with the specified account type.

**NOTE:** If targeting your app to work on API level 22 and before, MANAGE_ACCOUNTS permission is needed for those platforms. See docs for this function in API level 22. 
Requires android.Manifest.permission.MANAGE_ACCOUNTS

| Parameters ||
|---|---|
| `accountType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The account type associated with the authenticator to adjust |
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!: The `https://developer.android.com/reference/kotlin/android/app/Activity.html#` context to use for launching a new authenticator-defined sub-Activity to adjust authenticator settings; used only to call startActivity(); if null, the settings dialog will not be launched directly, but the necessary `https://developer.android.com/reference/kotlin/android/content/Intent.html#` will be returned to the caller instead |
| `callback` | [AccountManagerCallback](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerCallback)\< [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!\>!: Callback to invoke when the request completes, null for no callback |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!: `https://developer.android.com/reference/kotlin/android/os/Handler.html#` identifying the callback thread, null for the main thread |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture<https://developer.android.com/reference/kotlin/android/os/Bundle.html#!>!` | An `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture` which resolves to a Bundle which is empty if properties were edited successfully, or if no activity was specified, contains only `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_INTENT:kotlin.String` needed to launch the authenticator's settings dialog. If an error occurred, `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture#getResult()` throws: - `https://developer.android.com/reference/kotlin/android/accounts/AuthenticatorException` if no authenticator was registered for this account type or the authenticator failed to respond - `https://developer.android.com/reference/kotlin/android/accounts/OperationCanceledException` if the operation was canceled for any reason, including the user canceling the settings dialog - `https://developer.android.com/reference/kotlin/java/io/IOException.html#` if the authenticator experienced an I/O problem updating settings, usually because of network trouble |

### finishSession

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun finishSession(
    sessionBundle: Bundle!, 
    activity: Activity!, 
    callback: AccountManagerCallback<Bundle!>!, 
    handler: Handler!
): AccountManagerFuture<Bundle!>!
```

Finishes the session started by `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#startAddAccountSession(kotlin.String,%20kotlin.String,%20kotlin.Array,%20android.os.Bundle,%20android.app.Activity,%20android.accounts.AccountManagerCallback,%20android.os.Handler)` or `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#startUpdateCredentialsSession(android.accounts.Account,%20kotlin.String,%20android.os.Bundle,%20android.app.Activity,%20android.accounts.AccountManagerCallback,%20android.os.Handler)`. This will either add the account to AccountManager or update the local credentials stored.

This method may be called from any thread, but the returned `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture` must not be used on the main thread.

| Parameters ||
|---|---|
| `sessionBundle` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!: a `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` created by `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#startAddAccountSession(kotlin.String,%20kotlin.String,%20kotlin.Array,%20android.os.Bundle,%20android.app.Activity,%20android.accounts.AccountManagerCallback,%20android.os.Handler)` or `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#startUpdateCredentialsSession(android.accounts.Account,%20kotlin.String,%20android.os.Bundle,%20android.app.Activity,%20android.accounts.AccountManagerCallback,%20android.os.Handler)` |
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!: The `https://developer.android.com/reference/kotlin/android/app/Activity.html#` context to use for launching a new authenticator-defined sub-Activity to prompt the user to create an account or reauthenticate existing account; used only to call startActivity(); if null, the prompt will not be launched directly, but the necessary `https://developer.android.com/reference/kotlin/android/content/Intent.html#` will be returned to the caller instead |
| `callback` | [AccountManagerCallback](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerCallback)\< [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!\>!: Callback to invoke when the request completes, null for no callback |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!: `https://developer.android.com/reference/kotlin/android/os/Handler.html#` identifying the callback thread, null for the main thread |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture<https://developer.android.com/reference/kotlin/android/os/Bundle.html#!>!` | An `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture` which resolves to a Bundle with these fields if an activity was supplied and an account was added to device or local credentials were updated:: - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_NAME:kotlin.String` - the name of the account created - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_TYPE:kotlin.String` - the type of the account - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_STATUS_TOKEN:kotlin.String` - optional, token to check status of the account If no activity was specified and additional information is needed from user, the returned Bundle may only contain `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_INTENT:kotlin.String` with the `https://developer.android.com/reference/kotlin/android/content/Intent.html#` needed to launch the actual account creation process. If an error occurred, `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture#getResult()` throws: - `https://developer.android.com/reference/kotlin/android/accounts/AuthenticatorException` if no authenticator was registered for this account type or the authenticator failed to respond - `https://developer.android.com/reference/kotlin/android/accounts/OperationCanceledException` if the operation was canceled for any reason, including the user canceling the creation process or adding accounts (of this type) has been disabled by policy - `https://developer.android.com/reference/kotlin/java/io/IOException.html#` if the authenticator experienced an I/O problem creating a new account, usually because of network trouble |

**See Also**

- `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#startAddAccountSession(kotlin.String,%20kotlin.String,%20kotlin.Array,%20android.os.Bundle,%20android.app.Activity,%20android.accounts.AccountManagerCallback,%20android.os.Handler)`

### get

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun get(context: Context!): AccountManager!
```

Gets an AccountManager instance associated with a Context. The `https://developer.android.com/reference/kotlin/android/content/Context.html#` will be used as long as the AccountManager is active, so make sure to use a `https://developer.android.com/reference/kotlin/android/content/Context.html#` whose lifetime is commensurate with any listeners registered to #addOnAccountsUpdatedListener or similar methods.

It is safe to call this method from the main thread.

No permission is required to call this method.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: The `https://developer.android.com/reference/kotlin/android/content/Context.html#` to use when necessary |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#!` | An `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#` instance |

### getAccountVisibility

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAccountVisibility(
    account: Account!, 
    packageName: String!
): Int
```

Get visibility of certain account for given application. Possible returned values are:

- `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#VISIBILITY_VISIBLE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#VISIBILITY_USER_MANAGED_VISIBLE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#VISIBILITY_NOT_VISIBLE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#VISIBILITY_USER_MANAGED_NOT_VISIBLE:kotlin.Int`

<br />

This method requires the caller to have a signature match with the authenticator that owns the specified account.

| Parameters ||
|---|---|
| `account` | [Account](https://developer.android.com/reference/kotlin/android/accounts/Account)!: `https://developer.android.com/reference/kotlin/android/accounts/Account` to get visibility |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Package name of the application to get account visibility |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | int Visibility of given account. For the caller targeting API level 34 and above, `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#VISIBILITY_NOT_VISIBLE:kotlin.Int` is returned if the given package is filtered by the rules of [package visibility](https://developer.android.com/reference/kotlin/training/basics/intents/package-visibility). Value is one of the following: - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#VISIBILITY_UNDEFINED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#VISIBILITY_VISIBLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#VISIBILITY_USER_MANAGED_VISIBLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#VISIBILITY_NOT_VISIBLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#VISIBILITY_USER_MANAGED_NOT_VISIBLE:kotlin.Int` |

### getAccounts

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAccounts(): Array<Account!>
```

Lists all accounts visible to the caller regardless of type. Equivalent to getAccountsByType(null). These accounts may be visible because the user granted access to the account, or the AbstractAccountAuthenticator managing the account did so or because the client shares a signature with the managing AbstractAccountAuthenticator.

**Caution:**This method returns personal and sensitive user data. If your app accesses, collects, uses, or shares personal and sensitive data, you must clearly disclose that fact to users. For apps published on Google Play, policies protecting user data require that you do the following:

- Disclose to the user how your app accesses, collects, uses, or shares personal and sensitive data. Learn more about [acceptable disclosure and consent](https://play.google.com/about/privacy-security-deception/user-data/#!#personal-sensitive).
- Provide a privacy policy that describes your use of this data on- and off-device.

To learn more, visit the [Google Play Policy regarding user data](https://play.google.com/about/privacy-security-deception/user-data).

<br />

It is safe to call this method from the main thread. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#GET_ACCOUNTS:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/accounts/Account!>` | An array of `https://developer.android.com/reference/kotlin/android/accounts/Account`, one for each account. Empty (never null) if no accounts have been added. |

### getAccountsAndVisibilityForPackage

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAccountsAndVisibilityForPackage(
    packageName: String!, 
    accountType: String!
): MutableMap<Account!, Int!>!
```

Gets all accounts of given type and their visibility for specific package. This method requires the caller to have a signature match with the authenticator that manages accountType. It is a helper method which combines calls to `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#getAccountsByType(kotlin.String)` by authenticator and `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#getAccountVisibility(android.accounts.Account,%20kotlin.String)` for every returned account.

<br />

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Package name |
| `accountType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: `https://developer.android.com/reference/kotlin/android/accounts/Account` type |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://developer.android.com/reference/kotlin/android/accounts/Account!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>!` | Map with visibility for all accounts of given type See `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#getAccountVisibility(android.accounts.Account,%20kotlin.String)` for possible values |

### getAccountsByType

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAccountsByType(type: String!): Array<Account!>
```

Lists all accounts of particular type visible to the caller. These accounts may be visible because the user granted access to the account, or the AbstractAccountAuthenticator managing the account did so or because the client shares a signature with the managing AbstractAccountAuthenticator.

The account type is a string token corresponding to the authenticator and useful domain of the account. For example, there are types corresponding to Google and Facebook. The exact string token to use will be published somewhere associated with the authenticator in question.

**Caution:**This method returns personal and sensitive user data. If your app accesses, collects, uses, or shares personal and sensitive data, you must clearly disclose that fact to users. For apps published on Google Play, policies protecting user data require that you do the following:

- Disclose to the user how your app accesses, collects, uses, or shares personal and sensitive data. Learn more about [acceptable disclosure and consent](https://play.google.com/about/privacy-security-deception/user-data/#!#personal-sensitive).
- Provide a privacy policy that describes your use of this data on- and off-device.

To learn more, visit the [Google Play Policy regarding user data](https://play.google.com/about/privacy-security-deception/user-data).

<br />

It is safe to call this method from the main thread.

Caller targeting API level `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int` and above, will get list of accounts made visible to it by user (see `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#newChooseAccountIntent(android.accounts.Account,%20kotlin.collections.MutableList,%20kotlin.Array,%20kotlin.String,%20kotlin.String,%20kotlin.Array,%20android.os.Bundle)`) or AbstractAccountAuthenticator using `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#setAccountVisibility(android.accounts.Account,%20kotlin.String,%20kotlin.Int)`. `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#GET_ACCOUNTS:kotlin.String` permission is not used.

Caller targeting API level below `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int` that have not been granted the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#GET_ACCOUNTS:kotlin.String` permission, will only see those accounts managed by AbstractAccountAuthenticators whose signature matches the client.

**NOTE:** If targeting your app to work on API level `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#LOLLIPOP_MR1:kotlin.Int` and before, `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#GET_ACCOUNTS:kotlin.String` permission is needed for those platforms, irrespective of uid or signature match. See docs for this function in API level `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#LOLLIPOP_MR1:kotlin.Int`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#GET_ACCOUNTS:kotlin.String`

| Parameters ||
|---|---|
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The type of accounts to return, null to retrieve all accounts |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/accounts/Account!>` | An array of `https://developer.android.com/reference/kotlin/android/accounts/Account`, one per matching account. Empty (never null) if no accounts of the specified type have been added. |

### getAccountsByTypeAndFeatures

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAccountsByTypeAndFeatures(
    type: String!, 
    features: Array<String!>!, 
    callback: AccountManagerCallback<Array<Account!>!>!, 
    handler: Handler!
): AccountManagerFuture<Array<Account!>!>!
```

Lists all accounts of a type which have certain features. The account type identifies the authenticator (see `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#getAccountsByType(kotlin.String)`). Account features are authenticator-specific string tokens identifying boolean account properties (see `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#hasFeatures(android.accounts.Account,%20kotlin.Array,%20android.accounts.AccountManagerCallback,%20android.os.Handler)`).

Unlike `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#getAccountsByType(kotlin.String)`, this method calls the authenticator, which may contact the server or do other work to check account features, so the method returns an `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture`.

This method may be called from any thread, but the returned `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture` must not be used on the main thread.

Caller targeting API level `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int` and above, will get list of accounts made visible to it by user (see `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#newChooseAccountIntent(android.accounts.Account,%20kotlin.collections.MutableList,%20kotlin.Array,%20kotlin.String,%20kotlin.String,%20kotlin.Array,%20android.os.Bundle)`) or AbstractAccountAuthenticator using `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#setAccountVisibility(android.accounts.Account,%20kotlin.String,%20kotlin.Int)`. `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#GET_ACCOUNTS:kotlin.String` permission is not used.

Caller targeting API level below `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int` that have not been granted the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#GET_ACCOUNTS:kotlin.String` permission, will only see those accounts managed by AbstractAccountAuthenticators whose signature matches the client.

**NOTE:** If targeting your app to work on API level `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#LOLLIPOP_MR1:kotlin.Int` and before, `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#GET_ACCOUNTS:kotlin.String` permission is needed for those platforms, irrespective of uid or signature match. See docs for this function in API level `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#LOLLIPOP_MR1:kotlin.Int`.

| Parameters ||
|---|---|
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The type of accounts to return, must not be null |
| `features` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: An array of the account features to require, may be null or empty \* |
| `callback` | [AccountManagerCallback](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerCallback)\< [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Account](https://developer.android.com/reference/kotlin/android/accounts/Account)!\>!\>!: Callback to invoke when the request completes, null for no callback |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!: `https://developer.android.com/reference/kotlin/android/os/Handler.html#` identifying the callback thread, null for the main thread |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/accounts/Account!>!>!` | An `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture` which resolves to an array of `https://developer.android.com/reference/kotlin/android/accounts/Account`, one per account of the specified type which matches the requested features. |

### getAccountsByTypeForPackage

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAccountsByTypeForPackage(
    type: String!, 
    packageName: String!
): Array<Account!>
```

Returns the accounts visible to the specified package in an environment where some apps are not authorized to view all accounts. This method can only be called by system apps and authenticators managing the type. Beginning API level `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int` it also return accounts which user can make visible to the application (see `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#VISIBILITY_USER_MANAGED_VISIBLE:kotlin.Int`).

| Parameters ||
|---|---|
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The type of accounts to return, null to retrieve all accounts |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The package name of the app for which the accounts are to be returned |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/accounts/Account!>` | An array of `https://developer.android.com/reference/kotlin/android/accounts/Account`, one per matching account. Empty (never null) if no accounts of the specified type can be accessed by the package. |

### getAuthToken

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAuthToken(
    account: Account!, 
    authTokenType: String!, 
    options: Bundle!, 
    activity: Activity!, 
    callback: AccountManagerCallback<Bundle!>!, 
    handler: Handler!
): AccountManagerFuture<Bundle!>!
```

Gets an auth token of the specified type for a particular account, prompting the user for credentials if necessary. This method is intended for applications running in the foreground where it makes sense to ask the user directly for a password.

If a previously generated auth token is cached for this account and type, then it is returned. Otherwise, if a saved password is available, it is sent to the server to generate a new auth token. Otherwise, the user is prompted to enter a password.

Some authenticators have auth token *types*, whose value is authenticator-dependent. Some services use different token types to access different functionality -- for example, Google uses different auth tokens to access Gmail and Google Calendar for the same account.

**NOTE:** If targeting your app to work on API level 22 and before, USE_CREDENTIALS permission is needed for those platforms. See docs for this function in API level 22.

This method may be called from any thread, but the returned `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture` must not be used on the main thread. 
Requires android.Manifest.permission.USE_CREDENTIALS

| Parameters ||
|---|---|
| `account` | [Account](https://developer.android.com/reference/kotlin/android/accounts/Account)!: The account to fetch an auth token for |
| `authTokenType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The auth token type, an authenticator-dependent string token, must not be null |
| `options` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!: Authenticator-specific options for the request, may be null or empty |
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!: The `https://developer.android.com/reference/kotlin/android/app/Activity.html#` context to use for launching a new authenticator-defined sub-Activity to prompt the user for a password if necessary; used only to call startActivity(); must not be null. |
| `callback` | [AccountManagerCallback](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerCallback)\< [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!\>!: Callback to invoke when the request completes, null for no callback |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!: `https://developer.android.com/reference/kotlin/android/os/Handler.html#` identifying the callback thread, null for the main thread |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture<https://developer.android.com/reference/kotlin/android/os/Bundle.html#!>!` | An `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture` which resolves to a Bundle with at least the following fields: - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_NAME:kotlin.String` - the name of the account you supplied - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_TYPE:kotlin.String` - the type of the account - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_AUTHTOKEN:kotlin.String` - the auth token you wanted (Other authenticator-specific values may be returned.) If an auth token could not be fetched, `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture#getResult()` throws: - `https://developer.android.com/reference/kotlin/android/accounts/AuthenticatorException` if the authenticator failed to respond - `https://developer.android.com/reference/kotlin/android/accounts/OperationCanceledException` if the operation is canceled for any reason, incluidng the user canceling a credential request - `https://developer.android.com/reference/kotlin/java/io/IOException.html#` if the authenticator experienced an I/O problem creating a new auth token, usually because of network trouble If the account is no longer present on the device, the return value is authenticator-dependent. The caller should verify the validity of the account before requesting an auth token. |

### getAuthToken

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAuthToken(
    account: Account!, 
    authTokenType: String!, 
    options: Bundle!, 
    notifyAuthFailure: Boolean, 
    callback: AccountManagerCallback<Bundle!>!, 
    handler: Handler!
): AccountManagerFuture<Bundle!>!
```

Gets an auth token of the specified type for a particular account, optionally raising a notification if the user must enter credentials. This method is intended for background tasks and services where the user should not be immediately interrupted with a password prompt.

If a previously generated auth token is cached for this account and type, then it is returned. Otherwise, if a saved password is available, it is sent to the server to generate a new auth token. Otherwise, an `https://developer.android.com/reference/kotlin/android/content/Intent.html#` is returned which, when started, will prompt the user for a password. If the notifyAuthFailure parameter is set, a status bar notification is also created with the same Intent, alerting the user that they need to enter a password at some point.

In that case, you may need to wait until the user responds, which could take hours or days or forever. When the user does respond and supply a new password, the account manager will broadcast the `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#LOGIN_ACCOUNTS_CHANGED_ACTION:kotlin.String` Intent and notify `https://developer.android.com/reference/kotlin/android/accounts/OnAccountsUpdateListener` which applications can use to try again.

If notifyAuthFailure is not set, it is the application's responsibility to launch the returned Intent at some point. Either way, the result from this call will not wait for user action.

Some authenticators have auth token *types*, whose value is authenticator-dependent. Some services use different token types to access different functionality -- for example, Google uses different auth tokens to access Gmail and Google Calendar for the same account.

This method may be called from any thread, but the returned `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture` must not be used on the main thread.

**NOTE:** If targeting your app to work on API level 22 and before, USE_CREDENTIALS permission is needed for those platforms. See docs for this function in API level 22. 
Requires android.Manifest.permission.USE_CREDENTIALS

| Parameters ||
|---|---|
| `account` | [Account](https://developer.android.com/reference/kotlin/android/accounts/Account)!: The account to fetch an auth token for |
| `authTokenType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The auth token type, an authenticator-dependent string token, must not be null |
| `options` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!: Authenticator-specific options for the request, may be null or empty |
| `notifyAuthFailure` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True to add a notification to prompt the user for a password if necessary, false to leave that to the caller |
| `callback` | [AccountManagerCallback](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerCallback)\< [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!\>!: Callback to invoke when the request completes, null for no callback |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!: `https://developer.android.com/reference/kotlin/android/os/Handler.html#` identifying the callback thread, null for the main thread |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture<https://developer.android.com/reference/kotlin/android/os/Bundle.html#!>!` | An `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture` which resolves to a Bundle with at least the following fields on success: - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_NAME:kotlin.String` - the name of the account you supplied - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_TYPE:kotlin.String` - the type of the account - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_AUTHTOKEN:kotlin.String` - the auth token you wanted (Other authenticator-specific values may be returned.) If the user must enter credentials, the returned Bundle contains only `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_INTENT:kotlin.String` with the `https://developer.android.com/reference/kotlin/android/content/Intent.html#` needed to launch a prompt. If an error occurred, `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture#getResult()` throws: - `https://developer.android.com/reference/kotlin/android/accounts/AuthenticatorException` if the authenticator failed to respond - `https://developer.android.com/reference/kotlin/android/accounts/OperationCanceledException` if the operation is canceled for any reason, incluidng the user canceling a credential request - `https://developer.android.com/reference/kotlin/java/io/IOException.html#` if the authenticator experienced an I/O problem creating a new auth token, usually because of network trouble If the account is no longer present on the device, the return value is authenticator-dependent. The caller should verify the validity of the account before requesting an auth token. |

### getAuthToken

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAuthToken(
    account: Account!, 
    authTokenType: String!, 
    notifyAuthFailure: Boolean, 
    callback: AccountManagerCallback<Bundle!>!, 
    handler: Handler!
): AccountManagerFuture<Bundle!>!
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#getAuthToken(android.accounts.Account,%20kotlin.String,%20android.os.Bundle,%20kotlin.Boolean,%20android.accounts.AccountManagerCallback,%20android.os.Handler)` instead*

Gets an auth token of the specified type for a particular account, optionally raising a notification if the user must enter credentials. This method is intended for background tasks and services where the user should not be immediately interrupted with a password prompt.

If a previously generated auth token is cached for this account and type, then it is returned. Otherwise, if a saved password is available, it is sent to the server to generate a new auth token. Otherwise, an `https://developer.android.com/reference/kotlin/android/content/Intent.html#` is returned which, when started, will prompt the user for a password. If the notifyAuthFailure parameter is set, a status bar notification is also created with the same Intent, alerting the user that they need to enter a password at some point.

In that case, you may need to wait until the user responds, which could take hours or days or forever. When the user does respond and supply a new password, the account manager will broadcast the `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#LOGIN_ACCOUNTS_CHANGED_ACTION:kotlin.String` Intent and notify `https://developer.android.com/reference/kotlin/android/accounts/OnAccountsUpdateListener` which applications can use to try again.

If notifyAuthFailure is not set, it is the application's responsibility to launch the returned Intent at some point. Either way, the result from this call will not wait for user action.

Some authenticators have auth token *types*, whose value is authenticator-dependent. Some services use different token types to access different functionality -- for example, Google uses different auth tokens to access Gmail and Google Calendar for the same account.

This method may be called from any thread, but the returned `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture` must not be used on the main thread. 
Requires android.Manifest.permission.USE_CREDENTIALS

| Parameters ||
|---|---|
| `account` | [Account](https://developer.android.com/reference/kotlin/android/accounts/Account)!: The account to fetch an auth token for |
| `authTokenType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The auth token type, an authenticator-dependent string token, must not be null |
| `notifyAuthFailure` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True to add a notification to prompt the user for a password if necessary, false to leave that to the caller |
| `callback` | [AccountManagerCallback](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerCallback)\< [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!\>!: Callback to invoke when the request completes, null for no callback |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!: `https://developer.android.com/reference/kotlin/android/os/Handler.html#` identifying the callback thread, null for the main thread |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture<https://developer.android.com/reference/kotlin/android/os/Bundle.html#!>!` | An `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture` which resolves to a Bundle with at least the following fields on success: - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_NAME:kotlin.String` - the name of the account you supplied - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_TYPE:kotlin.String` - the type of the account - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_AUTHTOKEN:kotlin.String` - the auth token you wanted (Other authenticator-specific values may be returned.) If the user must enter credentials, the returned Bundle contains only `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_INTENT:kotlin.String` with the `https://developer.android.com/reference/kotlin/android/content/Intent.html#` needed to launch a prompt. If an error occurred, `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture#getResult()` throws: - `https://developer.android.com/reference/kotlin/android/accounts/AuthenticatorException` if the authenticator failed to respond - `https://developer.android.com/reference/kotlin/android/accounts/OperationCanceledException` if the operation is canceled for any reason, incluidng the user canceling a credential request - `https://developer.android.com/reference/kotlin/java/io/IOException.html#` if the authenticator experienced an I/O problem creating a new auth token, usually because of network trouble If the account is no longer present on the device, the return value is authenticator-dependent. The caller should verify the validity of the account before requesting an auth token. |

### getAuthTokenByFeatures

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAuthTokenByFeatures(
    accountType: String!, 
    authTokenType: String!, 
    features: Array<String!>!, 
    activity: Activity!, 
    addAccountOptions: Bundle!, 
    getAuthTokenOptions: Bundle!, 
    callback: AccountManagerCallback<Bundle!>!, 
    handler: Handler!
): AccountManagerFuture<Bundle!>!
```

This convenience helper combines the functionality of `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#getAccountsByTypeAndFeatures(kotlin.String,%20kotlin.Array,%20android.accounts.AccountManagerCallback,%20android.os.Handler)`, #getAuthToken, and `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#addAccount(kotlin.String,%20kotlin.String,%20kotlin.Array,%20android.os.Bundle,%20android.app.Activity,%20android.accounts.AccountManagerCallback,%20android.os.Handler)`.

This method gets a list of the accounts matching specific type and feature set which are visible to the caller (see `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#getAccountsByType(kotlin.String)` for details); if there is exactly one already visible account, it is used; if there are some accounts for which user grant visibility, the user is prompted to pick one; if there are none, the user is prompted to add one. Finally, an auth token is acquired for the chosen account.

This method may be called from any thread, but the returned `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture` must not be used on the main thread.

**NOTE:** If targeting your app to work on API level 22 and before, MANAGE_ACCOUNTS permission is needed for those platforms. See docs for this function in API level 22. 
Requires android.Manifest.permission.MANAGE_ACCOUNTS

| Parameters ||
|---|---|
| `accountType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The account type required (see `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#getAccountsByType(kotlin.String)`), must not be null |
| `authTokenType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The desired auth token type (see #getAuthToken), must not be null |
| `features` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: Required features for the account (see `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#getAccountsByTypeAndFeatures(kotlin.String,%20kotlin.Array,%20android.accounts.AccountManagerCallback,%20android.os.Handler)`), may be null or empty |
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!: The `https://developer.android.com/reference/kotlin/android/app/Activity.html#` context to use for launching new sub-Activities to prompt to add an account, select an account, and/or enter a password, as necessary; used only to call startActivity(); should not be null |
| `addAccountOptions` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!: Authenticator-specific options to use for adding new accounts; may be null or empty |
| `getAuthTokenOptions` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!: Authenticator-specific options to use for getting auth tokens; may be null or empty |
| `callback` | [AccountManagerCallback](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerCallback)\< [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!\>!: Callback to invoke when the request completes, null for no callback |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!: `https://developer.android.com/reference/kotlin/android/os/Handler.html#` identifying the callback thread, null for the main thread |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture<https://developer.android.com/reference/kotlin/android/os/Bundle.html#!>!` | An `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture` which resolves to a Bundle with at least the following fields: - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_NAME:kotlin.String` - the name of the account - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_TYPE:kotlin.String` - the type of the account - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_AUTHTOKEN:kotlin.String` - the auth token you wanted If an error occurred, `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture#getResult()` throws: - `https://developer.android.com/reference/kotlin/android/accounts/AuthenticatorException` if no authenticator was registered for this account type or the authenticator failed to respond - `https://developer.android.com/reference/kotlin/android/accounts/OperationCanceledException` if the operation was canceled for any reason, including the user canceling any operation - `https://developer.android.com/reference/kotlin/java/io/IOException.html#` if the authenticator experienced an I/O problem updating settings, usually because of network trouble |

### getAuthenticatorTypes

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAuthenticatorTypes(): Array<AuthenticatorDescription!>!
```

Lists the currently registered authenticators.

It is safe to call this method from the main thread.

No permission is required to call this method.

Caller targeting API level 34 and above, the results are filtered by the rules of [package visibility](https://developer.android.com/reference/kotlin/training/basics/intents/package-visibility).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/accounts/AuthenticatorDescription!>!` | An array of `https://developer.android.com/reference/kotlin/android/accounts/AuthenticatorDescription` for every authenticator known to the AccountManager service. Empty (never null) if no authenticators are known. |

### getPackagesAndVisibilityForAccount

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPackagesAndVisibilityForAccount(account: Account!): MutableMap<String!, Int!>!
```

Returns package names and visibility which were explicitly set for given account.

This method requires the caller to have a signature match with the authenticator that owns the specified account.

| Parameters ||
|---|---|
| `account` | [Account](https://developer.android.com/reference/kotlin/android/accounts/Account)!: The account for which visibility data should be returned |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>!` | Map from package names to visibility for given account |

### getPassword

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPassword(account: Account!): String!
```

Gets the saved password associated with the account. This is intended for authenticators and related code; applications should get an auth token instead.

It is safe to call this method from the main thread.

This method requires the caller to have a signature match with the authenticator that owns the specified account.

**NOTE:** If targeting your app to work on API level `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#LOLLIPOP_MR1:kotlin.Int` and before, AUTHENTICATE_ACCOUNTS permission is needed for those platforms. See docs for this function in API level `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#LOLLIPOP_MR1:kotlin.Int`. 
Requires android.Manifest.permission.AUTHENTICATE_ACCOUNTS

| Parameters ||
|---|---|
| `account` | [Account](https://developer.android.com/reference/kotlin/android/accounts/Account)!: The account to query for a password. Must not be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The account's password, null if none or if the account doesn't exist |

### getPreviousName

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPreviousName(account: Account!): String!
```

Gets the previous name associated with the account or `null`, if none. This is intended so that clients of `https://developer.android.com/reference/kotlin/android/accounts/OnAccountsUpdateListener` can determine if an authenticator has renamed an account.

It is safe to call this method from the main thread.

| Parameters ||
|---|---|
| `account` | [Account](https://developer.android.com/reference/kotlin/android/accounts/Account)!: The account to query for a previous name. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The account's previous name, null if the account has never been renamed. |

### getUserData

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getUserData(
    account: Account!, 
    key: String!
): String!
```

Gets the user data named by "key" associated with the account. This is intended for authenticators and related code to store arbitrary metadata along with accounts. The meaning of the keys and values is up to the authenticator for the account.

It is safe to call this method from the main thread.

This method requires the caller to have a signature match with the authenticator that owns the specified account.

**NOTE:** If targeting your app to work on API level `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#LOLLIPOP_MR1:kotlin.Int` and before, AUTHENTICATE_ACCOUNTS permission is needed for those platforms. See docs for this function in API level `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#LOLLIPOP_MR1:kotlin.Int`. 
Requires android.Manifest.permission.AUTHENTICATE_ACCOUNTS

| Parameters ||
|---|---|
| `account` | [Account](https://developer.android.com/reference/kotlin/android/accounts/Account)!: The account to query for user data |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The user data, null if the account, key doesn't exist, or the user is locked |

### hasFeatures

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasFeatures(
    account: Account!, 
    features: Array<String!>!, 
    callback: AccountManagerCallback<Boolean!>!, 
    handler: Handler!
): AccountManagerFuture<Boolean!>!
```

Finds out whether a particular account has all the specified features. Account features are authenticator-specific string tokens identifying boolean account properties. For example, features are used to tell whether Google accounts have a particular service (such as Google Calendar or Google Talk) enabled. The feature names and their meanings are published somewhere associated with the authenticator in question.

This method may be called from any thread, but the returned `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture` must not be used on the main thread.

If caller target API level is below `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int`, it is required to hold the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#GET_ACCOUNTS:kotlin.String` or have a signature match with the AbstractAccountAuthenticator that manages the account.

| Parameters ||
|---|---|
| `account` | [Account](https://developer.android.com/reference/kotlin/android/accounts/Account)!: The `https://developer.android.com/reference/kotlin/android/accounts/Account` to test |
| `features` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: An array of the account features to check |
| `callback` | [AccountManagerCallback](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerCallback)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\>!: Callback to invoke when the request completes, null for no callback |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!: `https://developer.android.com/reference/kotlin/android/os/Handler.html#` identifying the callback thread, null for the main thread |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html!>!` | An `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture` which resolves to a Boolean, true if the account exists and has all of the specified features. |

### invalidateAuthToken

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun invalidateAuthToken(
    accountType: String!, 
    authToken: String!
): Unit
```

Removes an auth token from the AccountManager's cache. Does nothing if the auth token is not currently in the cache. Applications must call this method when the auth token is found to have expired or otherwise become invalid for authenticating requests. The AccountManager does not validate or expire cached auth tokens otherwise.

It is safe to call this method from the main thread.

**NOTE:** If targeting your app to work on API level 22 and before, MANAGE_ACCOUNTS or USE_CREDENTIALS permission is needed for those platforms. See docs for this function in API level 22. 
Requires android.Manifest.permission.MANAGE_ACCOUNTS or android.Manifest.permission.USE_CREDENTIALS

| Parameters ||
|---|---|
| `accountType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The account type of the auth token to invalidate, must not be null |
| `authToken` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The auth token to invalidate, may be null |

### isCredentialsUpdateSuggested

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isCredentialsUpdateSuggested(
    account: Account!, 
    statusToken: String!, 
    callback: AccountManagerCallback<Boolean!>!, 
    handler: Handler!
): AccountManagerFuture<Boolean!>!
```

Checks whether `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#updateCredentials(android.accounts.Account,%20kotlin.String,%20android.os.Bundle,%20android.app.Activity,%20android.accounts.AccountManagerCallback,%20android.os.Handler)` or `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#startUpdateCredentialsSession(android.accounts.Account,%20kotlin.String,%20android.os.Bundle,%20android.app.Activity,%20android.accounts.AccountManagerCallback,%20android.os.Handler)` should be called with respect to the specified account.

This method may be called from any thread, but the returned `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture` must not be used on the main thread.

| Parameters ||
|---|---|
| `account` | [Account](https://developer.android.com/reference/kotlin/android/accounts/Account)!: The `https://developer.android.com/reference/kotlin/android/accounts/Account` to be checked whether `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#updateCredentials(android.accounts.Account,%20kotlin.String,%20android.os.Bundle,%20android.app.Activity,%20android.accounts.AccountManagerCallback,%20android.os.Handler)` or `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#startUpdateCredentialsSession(android.accounts.Account,%20kotlin.String,%20android.os.Bundle,%20android.app.Activity,%20android.accounts.AccountManagerCallback,%20android.os.Handler)` should be called |
| `statusToken` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a String of token to check account staus |
| `callback` | [AccountManagerCallback](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerCallback)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\>!: Callback to invoke when the request completes, null for no callback |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!: `https://developer.android.com/reference/kotlin/android/os/Handler.html#` identifying the callback thread, null for the main thread |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html!>!` | An `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture` which resolves to a Boolean, true if the credentials of the account should be updated. |

### newChooseAccountIntent

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun newChooseAccountIntent(
    selectedAccount: Account!, 
    allowableAccounts: ArrayList<Account!>!, 
    allowableAccountTypes: Array<String!>!, 
    alwaysPromptForAccount: Boolean, 
    descriptionOverrideText: String!, 
    addAccountAuthTokenType: String!, 
    addAccountRequiredFeatures: Array<String!>!, 
    addAccountOptions: Bundle!
): Intent!
```

**Deprecated:** *Deprecated in Java.*

Deprecated in favor of `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#newChooseAccountIntent(android.accounts.Account,%20kotlin.collections.MutableList,%20kotlin.Array,%20kotlin.String,%20kotlin.String,%20kotlin.Array,%20android.os.Bundle)`. Returns an intent to an `https://developer.android.com/reference/kotlin/android/app/Activity.html#` that prompts the user to choose from a list of accounts. The caller will then typically start the activity by calling `startActivityForResult(intent, ...);`.

On success the activity returns a Bundle with the account name and type specified using keys `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_NAME:kotlin.String` and `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_TYPE:kotlin.String`. Chosen account is marked as `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#VISIBILITY_USER_MANAGED_VISIBLE:kotlin.Int` to the caller (see `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#setAccountVisibility(android.accounts.Account,%20kotlin.String,%20kotlin.Int)`) and will be returned to it in consequent `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#getAccountsByType(kotlin.String)`) calls.

The most common case is to call this with one account type, e.g.:

```kotlin
newChooseAccountIntent(null, null, new String[]{"com.google"}, false, null,
  null, null, null);
```

| Parameters ||
|---|---|
| `selectedAccount` | [Account](https://developer.android.com/reference/kotlin/android/accounts/Account)!: if specified, indicates that the `https://developer.android.com/reference/kotlin/android/accounts/Account` is the currently selected one, according to the caller's definition of selected. |
| `allowableAccounts` | [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)\< [Account](https://developer.android.com/reference/kotlin/android/accounts/Account)!\>!: an optional `https://developer.android.com/reference/kotlin/java/util/List.html#` of accounts that are allowed to be shown. If not specified then this field will not limit the displayed accounts. |
| `allowableAccountTypes` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: an optional string array of account types. These are used both to filter the shown accounts and to filter the list of account types that are shown when adding an account. If not specified then this field will not limit the displayed account types when adding an account. |
| `alwaysPromptForAccount` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): boolean that is ignored. |
| `descriptionOverrideText` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: if non-null this string is used as the description in the accounts chooser screen rather than the default |
| `addAccountAuthTokenType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: this string is passed as the `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#addAccount(kotlin.String,%20kotlin.String,%20kotlin.Array,%20android.os.Bundle,%20android.app.Activity,%20android.accounts.AccountManagerCallback,%20android.os.Handler)` authTokenType parameter |
| `addAccountRequiredFeatures` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: this string array is passed as the `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#addAccount(kotlin.String,%20kotlin.String,%20kotlin.Array,%20android.os.Bundle,%20android.app.Activity,%20android.accounts.AccountManagerCallback,%20android.os.Handler)` requiredFeatures parameter |
| `addAccountOptions` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!: This `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` is passed as the `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#addAccount(kotlin.String,%20kotlin.String,%20kotlin.Array,%20android.os.Bundle,%20android.app.Activity,%20android.accounts.AccountManagerCallback,%20android.os.Handler)` options parameter |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/Intent.html#!` | an `https://developer.android.com/reference/kotlin/android/content/Intent.html#` that can be used to launch the ChooseAccount activity flow. |

### newChooseAccountIntent

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun newChooseAccountIntent(
    selectedAccount: Account!, 
    allowableAccounts: MutableList<Account!>!, 
    allowableAccountTypes: Array<String!>!, 
    descriptionOverrideText: String!, 
    addAccountAuthTokenType: String!, 
    addAccountRequiredFeatures: Array<String!>!, 
    addAccountOptions: Bundle!
): Intent!
```

Returns an intent to an `https://developer.android.com/reference/kotlin/android/app/Activity.html#` that prompts the user to choose from a list of accounts. The caller will then typically start the activity by calling `startActivityForResult(intent, ...);`.

On success the activity returns a Bundle with the account name and type specified using keys `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_NAME:kotlin.String` and `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_TYPE:kotlin.String`. Chosen account is marked as `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#VISIBILITY_USER_MANAGED_VISIBLE:kotlin.Int` to the caller (see `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#setAccountVisibility(android.accounts.Account,%20kotlin.String,%20kotlin.Int)`) and will be returned to it in consequent `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#getAccountsByType(kotlin.String)`) calls.

The most common case is to call this with one account type, e.g.:

```kotlin
newChooseAccountIntent(null, null, new String[]{"com.google"}, null, null, null,
  null);
```

| Parameters ||
|---|---|
| `selectedAccount` | [Account](https://developer.android.com/reference/kotlin/android/accounts/Account)!: if specified, indicates that the `https://developer.android.com/reference/kotlin/android/accounts/Account` is the currently selected one, according to the caller's definition of selected. |
| `allowableAccounts` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Account](https://developer.android.com/reference/kotlin/android/accounts/Account)!\>!: an optional `https://developer.android.com/reference/kotlin/java/util/List.html#` of accounts that are allowed to be shown. If not specified then this field will not limit the displayed accounts. |
| `allowableAccountTypes` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: an optional string array of account types. These are used both to filter the shown accounts and to filter the list of account types that are shown when adding an account. If not specified then this field will not limit the displayed account types when adding an account. |
| `descriptionOverrideText` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: if non-null this string is used as the description in the accounts chooser screen rather than the default |
| `addAccountAuthTokenType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: this string is passed as the `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#addAccount(kotlin.String,%20kotlin.String,%20kotlin.Array,%20android.os.Bundle,%20android.app.Activity,%20android.accounts.AccountManagerCallback,%20android.os.Handler)` authTokenType parameter |
| `addAccountRequiredFeatures` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: this string array is passed as the `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#addAccount(kotlin.String,%20kotlin.String,%20kotlin.Array,%20android.os.Bundle,%20android.app.Activity,%20android.accounts.AccountManagerCallback,%20android.os.Handler)` requiredFeatures parameter |
| `addAccountOptions` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!: This `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` is passed as the `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#addAccount(kotlin.String,%20kotlin.String,%20kotlin.Array,%20android.os.Bundle,%20android.app.Activity,%20android.accounts.AccountManagerCallback,%20android.os.Handler)` options parameter |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/Intent.html#!` | an `https://developer.android.com/reference/kotlin/android/content/Intent.html#` that can be used to launch the ChooseAccount activity flow. |

### notifyAccountAuthenticated

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun notifyAccountAuthenticated(account: Account!): Boolean
```

Notifies the system that the account has just been authenticated. This information may be used by other applications to verify the account. This should be called only when the user has entered correct credentials for the account.

It is not safe to call this method from the main thread. As such, call it from another thread.

This method requires the caller to have a signature match with the authenticator that owns the specified account. 
Requires android.Manifest.permission.AUTHENTICATE_ACCOUNTS

| Parameters ||
|---|---|
| `account` | [Account](https://developer.android.com/reference/kotlin/android/accounts/Account)!: The `https://developer.android.com/reference/kotlin/android/accounts/Account` to be updated. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | boolean `true` if the authentication of the account has been successfully acknowledged. Otherwise `false`. |

### peekAuthToken

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun peekAuthToken(
    account: Account!, 
    authTokenType: String!
): String!
```

Gets an auth token from the AccountManager's cache. If no auth token is cached for this account, null will be returned -- a new auth token will not be generated, and the server will not be contacted. Intended for use by the authenticator, not directly by applications.

It is safe to call this method from the main thread.

This method requires the caller to have a signature match with the authenticator that manages the specified account.

**NOTE:** If targeting your app to work on API level 22 and before, AUTHENTICATE_ACCOUNTS permission and same UID as account's authenticator is needed for those platforms. See docs for this function in API level 22. 
Requires android.Manifest.permission.AUTHENTICATE_ACCOUNTS

| Parameters ||
|---|---|
| `account` | [Account](https://developer.android.com/reference/kotlin/android/accounts/Account)!: The account for which an auth token is to be fetched. Cannot be `null`. |
| `authTokenType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The type of auth token to fetch. Cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The cached auth token for this account and type, or null if no auth token is cached, the account does not exist, or the user is locked |

**See Also**

### removeAccount

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeAccount(
    account: Account!, 
    callback: AccountManagerCallback<Boolean!>!, 
    handler: Handler!
): AccountManagerFuture<Boolean!>!
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#removeAccount(android.accounts.Account,%20android.app.Activity,%20android.accounts.AccountManagerCallback,%20android.os.Handler)` instead*

Removes an account from the AccountManager. Does nothing if the account does not exist. Does not delete the account from the server. The authenticator may have its own policies preventing account deletion, in which case the account will not be deleted.

This method requires the caller to have a signature match with the authenticator that manages the specified account.

**NOTE:** If targeting your app to work on API level 22 and before, MANAGE_ACCOUNTS permission is needed for those platforms. See docs for this function in API level 22. 
Requires android.Manifest.permission.MANAGE_ACCOUNTS

| Parameters ||
|---|---|
| `account` | [Account](https://developer.android.com/reference/kotlin/android/accounts/Account)!: The `https://developer.android.com/reference/kotlin/android/accounts/Account` to remove |
| `callback` | [AccountManagerCallback](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerCallback)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\>!: Callback to invoke when the request completes, null for no callback |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!: `https://developer.android.com/reference/kotlin/android/os/Handler.html#` identifying the callback thread, null for the main thread |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html!>!` | An `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture` which resolves to a Boolean, true if the account has been successfully removed |

### removeAccount

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeAccount(
    account: Account!, 
    activity: Activity!, 
    callback: AccountManagerCallback<Bundle!>!, 
    handler: Handler!
): AccountManagerFuture<Bundle!>!
```

Removes an account from the AccountManager. Does nothing if the account does not exist. Does not delete the account from the server. The authenticator may have its own policies preventing account deletion, in which case the account will not be deleted.

This method may be called from any thread, but the returned `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture` must not be used on the main thread.

This method requires the caller to have a signature match with the authenticator that manages the specified account, be a profile owner or have the android.Manifest.permission#REMOVE_ACCOUNTS permission.

**NOTE:** If targeting your app to work on API level 22 and before, MANAGE_ACCOUNTS permission is needed for those platforms. See docs for this function in API level 22.

| Parameters ||
|---|---|
| `account` | [Account](https://developer.android.com/reference/kotlin/android/accounts/Account)!: The `https://developer.android.com/reference/kotlin/android/accounts/Account` to remove |
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!: The `https://developer.android.com/reference/kotlin/android/app/Activity.html#` context to use for launching a new authenticator-defined sub-Activity to prompt the user to delete an account; used only to call startActivity(); if null, the prompt will not be launched directly, but the `https://developer.android.com/reference/kotlin/android/content/Intent.html#` may be returned to the caller instead |
| `callback` | [AccountManagerCallback](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerCallback)\< [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!\>!: Callback to invoke when the request completes, null for no callback |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!: `https://developer.android.com/reference/kotlin/android/os/Handler.html#` identifying the callback thread, null for the main thread |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture<https://developer.android.com/reference/kotlin/android/os/Bundle.html#!>!` | An `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture` which resolves to a Bundle with `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_BOOLEAN_RESULT:kotlin.String` if activity was specified and an account was removed or if active. If no activity was specified, the returned Bundle contains only `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_INTENT:kotlin.String` with the `https://developer.android.com/reference/kotlin/android/content/Intent.html#` needed to launch the actual account removal process, if authenticator needs the activity launch. If an error occurred, `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture#getResult()` throws: - `https://developer.android.com/reference/kotlin/android/accounts/AuthenticatorException` if no authenticator was registered for this account type or the authenticator failed to respond - `https://developer.android.com/reference/kotlin/android/accounts/OperationCanceledException` if the operation was canceled for any reason, including the user canceling the creation process or adding accounts (of this type) has been disabled by policy |

### removeAccountExplicitly

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeAccountExplicitly(account: Account!): Boolean
```

Removes an account directly. Normally used by authenticators, not directly by applications. Does not delete the account from the server. The authenticator may have its own policies preventing account deletion, in which case the account will not be deleted.

It is safe to call this method from the main thread.

This method requires the caller to have a signature match with the authenticator that manages the specified account.

**NOTE:** If targeting your app to work on API level 22 and before, AUTHENTICATE_ACCOUNTS permission and same UID as account's authenticator is needed for those platforms. See docs for this function in API level 22. 
Requires android.Manifest.permission.AUTHENTICATE_ACCOUNTS

| Parameters ||
|---|---|
| `account` | [Account](https://developer.android.com/reference/kotlin/android/accounts/Account)!: The `https://developer.android.com/reference/kotlin/android/accounts/Account` to delete. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the account was successfully deleted, false if the account did not exist, the account is null, or another error occurs. |

### removeOnAccountsUpdatedListener

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeOnAccountsUpdatedListener(listener: OnAccountsUpdateListener!): Unit
```

Removes an `https://developer.android.com/reference/kotlin/android/accounts/OnAccountsUpdateListener` previously registered with #addOnAccountsUpdatedListener. The listener will no longer receive notifications of account changes.

It is safe to call this method from the main thread.

No permission is required to call this method.

| Parameters ||
|---|---|
| `listener` | [OnAccountsUpdateListener](https://developer.android.com/reference/kotlin/android/accounts/OnAccountsUpdateListener)!: The previously added listener to remove |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if listener is null |
| `java.lang.IllegalStateException` | if listener was not already added |

### renameAccount

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun renameAccount(
    account: Account!, 
    newName: String!, 
    callback: AccountManagerCallback<Account!>!, 
    handler: Handler!
): AccountManagerFuture<Account!>!
```

Rename the specified `https://developer.android.com/reference/kotlin/android/accounts/Account`. This is equivalent to removing the existing account and adding a new renamed account with the old account's user data.

It is safe to call this method from the main thread.

This method requires the caller to have a signature match with the authenticator that manages the specified account.

**NOTE:** If targeting your app to work on API level 22 and before, AUTHENTICATE_ACCOUNTS permission and same UID as account's authenticator is needed for those platforms. See docs for this function in API level 22. 
Requires android.Manifest.permission.AUTHENTICATE_ACCOUNTS

| Parameters ||
|---|---|
| `account` | [Account](https://developer.android.com/reference/kotlin/android/accounts/Account)!: The `https://developer.android.com/reference/kotlin/android/accounts/Account` to rename |
| `newName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: String name to be associated with the account. |
| `callback` | [AccountManagerCallback](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerCallback)\< [Account](https://developer.android.com/reference/kotlin/android/accounts/Account)!\>!: Callback to invoke when the request completes, null for no callback |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!: `https://developer.android.com/reference/kotlin/android/os/Handler.html#` identifying the callback thread, null for the main thread |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture<https://developer.android.com/reference/kotlin/android/accounts/Account!>!` | An `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture` which resolves to the Account after the name change. If successful the account's name will be the specified new name. |

### setAccountVisibility

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAccountVisibility(
    account: Account!, 
    packageName: String!, 
    visibility: Int
): Boolean
```

Set visibility value of given account to certain package. Package name must match installed application, or be equal to `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#PACKAGE_NAME_KEY_LEGACY_VISIBLE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#PACKAGE_NAME_KEY_LEGACY_NOT_VISIBLE:kotlin.String`.

Possible visibility values:

- `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#VISIBILITY_UNDEFINED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#VISIBILITY_VISIBLE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#VISIBILITY_USER_MANAGED_VISIBLE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#VISIBILITY_NOT_VISIBLE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#VISIBILITY_USER_MANAGED_NOT_VISIBLE:kotlin.Int`

This method requires the caller to have a signature match with the authenticator that owns the specified account.

| Parameters ||
|---|---|
| `account` | [Account](https://developer.android.com/reference/kotlin/android/accounts/Account)!: `https://developer.android.com/reference/kotlin/android/accounts/Account` to update visibility |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Package name of the application to modify account visibility. Declaring [package visibility](https://developer.android.com/reference/kotlin/training/basics/intents/package-visibility) needs for it is needed, if the caller is targeting API level 34 and above. |
| `visibility` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): New visibility value. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#VISIBILITY_UNDEFINED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#VISIBILITY_VISIBLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#VISIBILITY_USER_MANAGED_VISIBLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#VISIBILITY_NOT_VISIBLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#VISIBILITY_USER_MANAGED_NOT_VISIBLE:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True, if visibility value was successfully updated. |

### setAuthToken

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAuthToken(
    account: Account!, 
    authTokenType: String!, 
    authToken: String!
): Unit
```

Adds an auth token to the AccountManager cache for an account. If the account does not exist then this call has no effect. Replaces any previous auth token for this account and auth token type. Intended for use by the authenticator, not directly by applications.

It is safe to call this method from the main thread.

This method requires the caller to have a signature match with the authenticator that manages the specified account.

**NOTE:** If targeting your app to work on API level 22 and before, AUTHENTICATE_ACCOUNTS permission and same UID as account's authenticator is needed for those platforms. See docs for this function in API level 22. 
Requires android.Manifest.permission.AUTHENTICATE_ACCOUNTS

| Parameters ||
|---|---|
| `account` | [Account](https://developer.android.com/reference/kotlin/android/accounts/Account)!: The account to set an auth token for |
| `authTokenType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The type of the auth token, see {#getAuthToken} |
| `authToken` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The auth token to add to the cache |

### setPassword

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPassword(
    account: Account!, 
    password: String!
): Unit
```

Sets or forgets a saved password. This modifies the local copy of the password used to automatically authenticate the user; it does not change the user's account password on the server. Intended for use by the authenticator, not directly by applications.

Calling this method does not update the last authenticated timestamp, referred by `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_LAST_AUTHENTICATED_TIME:kotlin.String`. To update it, call `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#notifyAccountAuthenticated(android.accounts.Account)` after getting success.

It is safe to call this method from the main thread.

This method requires the caller to have a signature match with the authenticator that manages the specified account.

**NOTE:** If targeting your app to work on API level 22 and before, AUTHENTICATE_ACCOUNTS permission and same UID as account's authenticator is needed for those platforms. See docs for this function in API level 22. 
Requires android.Manifest.permission.AUTHENTICATE_ACCOUNTS

| Parameters ||
|---|---|
| `account` | [Account](https://developer.android.com/reference/kotlin/android/accounts/Account)!: The account whose password is to be set. Cannot be `null`. |
| `password` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The password to set, null to clear the password |

### setUserData

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setUserData(
    account: Account!, 
    key: String!, 
    value: String!
): Unit
```

Sets one userdata key for an account. Intended by use for the authenticator to stash state for itself, not directly by applications. The meaning of the keys and values is up to the authenticator.

It is safe to call this method from the main thread.

This method requires the caller to have a signature match with the authenticator that manages the specified account.

**NOTE:** If targeting your app to work on API level 22 and before, AUTHENTICATE_ACCOUNTS permission and same UID as account's authenticator is needed for those platforms. See docs for this function in API level 22. 
Requires android.Manifest.permission.AUTHENTICATE_ACCOUNTS

| Parameters ||
|---|---|
| `account` | [Account](https://developer.android.com/reference/kotlin/android/accounts/Account)!: Account whose user data is to be set. Must not be `null`. |
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: String user data key to set. Must not be null |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: String value to set, `null` to clear this user data key |

### startAddAccountSession

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startAddAccountSession(
    accountType: String!, 
    authTokenType: String!, 
    requiredFeatures: Array<String!>!, 
    options: Bundle!, 
    activity: Activity!, 
    callback: AccountManagerCallback<Bundle!>!, 
    handler: Handler!
): AccountManagerFuture<Bundle!>!
```

Asks the user to authenticate with an account of a specified type. The authenticator for this account type processes this request with the appropriate user interface. If the user does elect to authenticate with a new account, a bundle of session data for installing the account later is returned with optional account password and account status token.

This method may be called from any thread, but the returned `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture` must not be used on the main thread.

**NOTE:** The account will not be installed to the device by calling this api alone. #finishSession should be called after this to install the account on device.

| Parameters ||
|---|---|
| `accountType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The type of account to add; must not be null |
| `authTokenType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The type of auth token (see #getAuthToken) this account will need to be able to generate, null for none |
| `requiredFeatures` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: The features (see `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#hasFeatures(android.accounts.Account,%20kotlin.Array,%20android.accounts.AccountManagerCallback,%20android.os.Handler)`) this account must have, null for none |
| `options` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!: Authenticator-specific options for the request, may be null or empty |
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!: The `https://developer.android.com/reference/kotlin/android/app/Activity.html#` context to use for launching a new authenticator-defined sub-Activity to prompt the user to create an account; used only to call startActivity(); if null, the prompt will not be launched directly, but the necessary `https://developer.android.com/reference/kotlin/android/content/Intent.html#` will be returned to the caller instead |
| `callback` | [AccountManagerCallback](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerCallback)\< [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!\>!: Callback to invoke when the request completes, null for no callback |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!: `https://developer.android.com/reference/kotlin/android/os/Handler.html#` identifying the callback thread, null for the main thread |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture<https://developer.android.com/reference/kotlin/android/os/Bundle.html#!>!` | An `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture` which resolves to a Bundle with these fields if activity was specified and user was authenticated with an account: - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_SESSION_BUNDLE:kotlin.String` - encrypted Bundle for adding the the to the device later. - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_STATUS_TOKEN:kotlin.String` - optional, token to check status of the account If no activity was specified, the returned Bundle contains only `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_INTENT:kotlin.String` with the `https://developer.android.com/reference/kotlin/android/content/Intent.html#` needed to launch the actual account creation process. If authenticator doesn't support this method, the returned Bundle contains only `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_SESSION_BUNDLE:kotlin.String` with encrypted `options` needed to add account later. If an error occurred, `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture#getResult()` throws: - `https://developer.android.com/reference/kotlin/android/accounts/AuthenticatorException` if no authenticator was registered for this account type or the authenticator failed to respond - `https://developer.android.com/reference/kotlin/android/accounts/OperationCanceledException` if the operation was canceled for any reason, including the user canceling the creation process or adding accounts (of this type) has been disabled by policy - `https://developer.android.com/reference/kotlin/java/io/IOException.html#` if the authenticator experienced an I/O problem creating a new account, usually because of network trouble |

**See Also**

- `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#finishSession(android.os.Bundle,%20android.app.Activity,%20android.accounts.AccountManagerCallback,%20android.os.Handler)`

### startUpdateCredentialsSession

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startUpdateCredentialsSession(
    account: Account!, 
    authTokenType: String!, 
    options: Bundle!, 
    activity: Activity!, 
    callback: AccountManagerCallback<Bundle!>!, 
    handler: Handler!
): AccountManagerFuture<Bundle!>!
```

Asks the user to enter a new password for the account but not updating the saved credentials for the account until `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#finishSession(android.os.Bundle,%20android.app.Activity,%20android.accounts.AccountManagerCallback,%20android.os.Handler)` is called.

This method may be called from any thread, but the returned `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture` must not be used on the main thread.

**NOTE:** The saved credentials for the account alone will not be updated by calling this API alone. #finishSession should be called after this to update local credentials

| Parameters ||
|---|---|
| `account` | [Account](https://developer.android.com/reference/kotlin/android/accounts/Account)!: The account to update credentials for |
| `authTokenType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The credentials entered must allow an auth token of this type to be created (but no actual auth token is returned); may be null |
| `options` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!: Authenticator-specific options for the request; may be null or empty |
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!: The `https://developer.android.com/reference/kotlin/android/app/Activity.html#` context to use for launching a new authenticator-defined sub-Activity to prompt the user to enter a password; used only to call startActivity(); if null, the prompt will not be launched directly, but the necessary `https://developer.android.com/reference/kotlin/android/content/Intent.html#` will be returned to the caller instead |
| `callback` | [AccountManagerCallback](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerCallback)\< [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!\>!: Callback to invoke when the request completes, null for no callback |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!: `https://developer.android.com/reference/kotlin/android/os/Handler.html#` identifying the callback thread, null for the main thread |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture<https://developer.android.com/reference/kotlin/android/os/Bundle.html#!>!` | An `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture` which resolves to a Bundle with these fields if an activity was supplied and user was successfully re-authenticated to the account: - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_SESSION_BUNDLE:kotlin.String` - encrypted Bundle for updating the local credentials on device later. - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_STATUS_TOKEN:kotlin.String` - optional, token to check status of the account If no activity was specified, the returned Bundle contains `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_INTENT:kotlin.String` with the `https://developer.android.com/reference/kotlin/android/content/Intent.html#` needed to launch the password prompt. If an error occurred, `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture#getResult()` throws: - `https://developer.android.com/reference/kotlin/android/accounts/AuthenticatorException` if the authenticator failed to respond - `https://developer.android.com/reference/kotlin/android/accounts/OperationCanceledException` if the operation was canceled for any reason, including the user canceling the password prompt - `https://developer.android.com/reference/kotlin/java/io/IOException.html#` if the authenticator experienced an I/O problem verifying the password, usually because of network trouble |

**See Also**

- `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#finishSession(android.os.Bundle,%20android.app.Activity,%20android.accounts.AccountManagerCallback,%20android.os.Handler)`

### updateCredentials

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun updateCredentials(
    account: Account!, 
    authTokenType: String!, 
    options: Bundle!, 
    activity: Activity!, 
    callback: AccountManagerCallback<Bundle!>!, 
    handler: Handler!
): AccountManagerFuture<Bundle!>!
```

Asks the user to enter a new password for an account, updating the saved credentials for the account. Normally this happens automatically when the server rejects credentials during an auth token fetch, but this can be invoked directly to ensure we have the correct credentials stored.

This method may be called from any thread, but the returned `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture` must not be used on the main thread.

**NOTE:** If targeting your app to work on API level 22 and before, MANAGE_ACCOUNTS permission is needed for those platforms. See docs for this function in API level 22. 
Requires android.Manifest.permission.MANAGE_ACCOUNTS

| Parameters ||
|---|---|
| `account` | [Account](https://developer.android.com/reference/kotlin/android/accounts/Account)!: The account to update credentials for |
| `authTokenType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The credentials entered must allow an auth token of this type to be created (but no actual auth token is returned); may be null |
| `options` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!: Authenticator-specific options for the request; may be null or empty |
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!: The `https://developer.android.com/reference/kotlin/android/app/Activity.html#` context to use for launching a new authenticator-defined sub-Activity to prompt the user to enter a password; used only to call startActivity(); if null, the prompt will not be launched directly, but the necessary `https://developer.android.com/reference/kotlin/android/content/Intent.html#` will be returned to the caller instead |
| `callback` | [AccountManagerCallback](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerCallback)\< [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!\>!: Callback to invoke when the request completes, null for no callback |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!: `https://developer.android.com/reference/kotlin/android/os/Handler.html#` identifying the callback thread, null for the main thread |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture<https://developer.android.com/reference/kotlin/android/os/Bundle.html#!>!` | An `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture` which resolves to a Bundle with these fields if an activity was supplied and the account credentials were successfully updated: - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_NAME:kotlin.String` - the name of the account - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_TYPE:kotlin.String` - the type of the account If no activity was specified, the returned Bundle contains `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_INTENT:kotlin.String` with the `https://developer.android.com/reference/kotlin/android/content/Intent.html#` needed to launch the password prompt. If an error occurred, `https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture#getResult()` throws: - `https://developer.android.com/reference/kotlin/android/accounts/AuthenticatorException` if the authenticator failed to respond - `https://developer.android.com/reference/kotlin/android/accounts/OperationCanceledException` if the operation was canceled for any reason, including the user canceling the password prompt - `https://developer.android.com/reference/kotlin/java/io/IOException.html#` if the authenticator experienced an I/O problem verifying the password, usually because of network trouble |
