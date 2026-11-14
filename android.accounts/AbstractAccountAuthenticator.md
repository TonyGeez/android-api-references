Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AbstractAccountAuthenticator

```
abstract class AbstractAccountAuthenticator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.accounts.AbstractAccountAuthenticator](AbstractAccountAuthenticator.md) |

Abstract base class for creating AccountAuthenticators. In order to be an authenticator one must extend this class, provide implementations for the abstract methods, and write a service that returns the result of getIBinder in the service's onBind when invoked with an intent with action `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#ACTION_AUTHENTICATOR_INTENT:kotlin.String`. This service must specify the following intent filter and metadata tags in its AndroidManifest.xml file

```kotlin
<intent-filter>
      <action android:name="android.accounts.AccountAuthenticator" />
    </intent-filter>
    <meta-data android:name="android.accounts.AccountAuthenticator"
              android:resource="@xml/authenticator" />
  
```
The `android:resource` attribute must point to a resource that looks like:

```kotlin
<account-authenticator xmlns:android="http://schemas.android.com/apk/res/android"
     android:accountType="typeOfAuthenticator"
     android:icon="@drawable/icon"
     android:smallIcon="@drawable/miniIcon"
     android:label="@string/label"
     android:accountPreferences="@xml/account_preferences"
  />
  
```
Replace the icons and labels with your own resources. The `android:accountType` attribute must be a string that uniquely identifies your authenticator and will be the same string that user will use when making calls on the AccountManager and it also corresponds to `https://developer.android.com/reference/kotlin/android/accounts/Account#type:kotlin.String` for your accounts. One user of the android:icon is the "Account \& Sync" settings page and one user of the android:smallIcon is the Contact Application's tab panels.

<br />

The preferences attribute points to a PreferenceScreen xml hierarchy that contains a list of PreferenceScreens that can be invoked to manage the authenticator. An example is:

```kotlin
<PreferenceScreen xmlns:android="http://schemas.android.com/apk/res/android">
     <PreferenceCategory android:title="@string/title_fmt" />
     <PreferenceScreen
          android:key="key1"
          android:title="@string/key1_action"
          android:summary="@string/key1_summary">
          <intent
              android:action="key1.ACTION"
              android:targetPackage="key1.package"
              android:targetClass="key1.class" />
      </PreferenceScreen>
  </PreferenceScreen>
  
```

The standard pattern for implementing any of the abstract methods is the following:

- If the supplied arguments are enough for the authenticator to fully satisfy the request then it will do so and return a `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` that contains the results.
- If the authenticator needs information from the user to satisfy the request then it will create an `https://developer.android.com/reference/kotlin/android/content/Intent.html#` to an activity that will prompt the user for the information and then carry out the request. This intent must be returned in a Bundle as key `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_INTENT:kotlin.String`.

 The activity needs to return the final result when it is complete so the Intent should contain the AccountAuthenticatorResponse as `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_AUTHENTICATOR_RESPONSE:kotlin.String`. The activity must then call onResult or onError when it is complete.
- If the authenticator cannot synchronously process the request and return a result then it may choose to return null and then use the AccountManagerResponse to send the result when it has completed the request. This asynchronous option is not available for the addAccount method, which must complete synchronously.

The following descriptions of each of the abstract authenticator methods will not describe the possible asynchronous nature of the request handling and will instead just describe the input parameters and the expected result.

When writing an activity to satisfy these requests one must pass in the AccountManagerResponse and return the result via that response when the activity finishes (or whenever else the activity author deems it is the correct time to respond).

## Summary

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/accounts/AbstractAccountAuthenticator#KEY_CUSTOM_TOKEN_EXPIRY:kotlin.String` Bundle key used for the `long` expiration time (in millis from the unix epoch) of the associated auth token. |

| Public constructors ||
|---|---|
| AbstractAccountAuthenticator <br /> |

| Public methods ||
|---|---|
| abstract [Bundle](../android.os/Bundle.md)! | addAccount Adds an account of the specified accountType. |
| open [Bundle](../android.os/Bundle.md)! | addAccountFromCredentials Creates an account based on credentials provided by the authenticator instance of another user on the device, who has chosen to share the account with this user. |
| abstract [Bundle](../android.os/Bundle.md)! | confirmCredentials Checks that the user knows the credentials of an account. |
| --- | --- |
| abstract [Bundle](../android.os/Bundle.md)! | editProperties Returns a Bundle that contains the Intent of the activity that can be used to edit the properties. |
| open [Bundle](../android.os/Bundle.md)! | finishSession Finishes the session started by #startAddAccountSession or #startUpdateCredentials by installing the account to device with AccountManager, or updating the local credentials. |
| open [Bundle](../android.os/Bundle.md)! | getAccountCredentialsForCloning Returns a Bundle that contains whatever is required to clone the account on a different user. |
| --- | --- |
| open [Bundle](../android.os/Bundle.md)! | getAccountRemovalAllowed Checks if the removal of this account is allowed. |
| abstract [Bundle](../android.os/Bundle.md)! | getAuthToken Gets an authtoken for an account. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getAuthTokenLabel Ask the authenticator for a localized label for the given authTokenType. |
| --- | --- |
| [IBinder](../android.os/IBinder.md)! | getIBinder <br /> |
| abstract [Bundle](../android.os/Bundle.md)! | hasFeatures Checks if the account supports all the specified authenticator specific features. |
| open [Bundle](../android.os/Bundle.md)! | isCredentialsUpdateSuggested Checks if update of the account credentials is suggested. |
| --- | --- |
| open [Bundle](../android.os/Bundle.md)! | startAddAccountSession Starts the add account session to authenticate user to an account of the specified accountType. |
| open [Bundle](../android.os/Bundle.md)! | startUpdateCredentialsSession Asks user to re-authenticate for an account but defers updating the locally stored credentials. |
| abstract [Bundle](../android.os/Bundle.md)! | updateCredentials Update the locally stored credentials for an account. |
| --- | --- |

## Constants

### KEY_CUSTOM_TOKEN_EXPIRY

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CUSTOM_TOKEN_EXPIRY: String
```

Bundle key used for the `long` expiration time (in millis from the unix epoch) of the associated auth token.

 Value: "android.accounts.expiry"

**See Also**

- getAuthToken

## Public constructors

### AbstractAccountAuthenticator

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
AbstractAccountAuthenticator(context: Context!)
```

## Public methods

### addAccount

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun addAccount(
    response: AccountAuthenticatorResponse!, 
    accountType: String!, 
    authTokenType: String!, 
    requiredFeatures: Array<String!>!, 
    options: Bundle!
): Bundle!
```

Adds an account of the specified accountType.

| Parameters ||
|---|---|
| `response` | [AccountAuthenticatorResponse](AccountAuthenticatorResponse.md)!: to send the result back to the AccountManager, will never be null |
| `accountType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the type of account to add, will never be null |
| `authTokenType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the type of auth token to retrieve after adding the account, may be null |
| --- | --- |
| `requiredFeatures` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: a String array of authenticator-specific features that the added account must support, may be null |
| `options` | [Bundle](../android.os/Bundle.md)!: a Bundle of authenticator-specific options. It always contains `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_CALLER_PID:kotlin.String` and `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_CALLER_UID:kotlin.String` fields which will let authenticator know the identity of the caller. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#!` | a Bundle result or null if the result is to be returned via the response. The result will contain either: - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_INTENT:kotlin.String`, or - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_NAME:kotlin.String` and `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_TYPE:kotlin.String` of the account that was added, or - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ERROR_CODE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ERROR_MESSAGE:kotlin.String` to indicate an error |

| Exceptions ||
|---|---|
| `android.accounts.NetworkErrorException` | if the authenticator could not honor the request due to a network error |

### addAccountFromCredentials

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addAccountFromCredentials(
    response: AccountAuthenticatorResponse!, 
    account: Account!, 
    accountCredentials: Bundle!
): Bundle!
```

Creates an account based on credentials provided by the authenticator instance of another user on the device, who has chosen to share the account with this user.

| Parameters ||
|---|---|
| `response` | [AccountAuthenticatorResponse](AccountAuthenticatorResponse.md)!: to send the result back to the AccountManager, will never be null |
| `account` | [Account](Account.md)!: the account to clone, will never be null |
| `accountCredentials` | [Bundle](../android.os/Bundle.md)!: the Bundle containing the required credentials to create the account. Contents of the Bundle are only meaningful to the authenticator. This Bundle is provided by getAccountCredentialsForCloning. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#!` | a Bundle result or null if the result is to be returned via the response. |

| Exceptions ||
|---|---|
| `android.accounts.NetworkErrorException` | |

**See Also**

- getAccountCredentialsForCloning

### confirmCredentials

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun confirmCredentials(
    response: AccountAuthenticatorResponse!, 
    account: Account!, 
    options: Bundle!
): Bundle!
```

Checks that the user knows the credentials of an account.

| Parameters ||
|---|---|
| `response` | [AccountAuthenticatorResponse](AccountAuthenticatorResponse.md)!: to send the result back to the AccountManager, will never be null |
| `account` | [Account](Account.md)!: the account whose credentials are to be checked, will never be null |
| `options` | [Bundle](../android.os/Bundle.md)!: a Bundle of authenticator-specific options, may be null |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#!` | a Bundle result or null if the result is to be returned via the response. The result will contain either: - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_INTENT:kotlin.String`, or - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_BOOLEAN_RESULT:kotlin.String`, true if the check succeeded, false otherwise - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ERROR_CODE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ERROR_MESSAGE:kotlin.String` to indicate an error |

| Exceptions ||
|---|---|
| `android.accounts.NetworkErrorException` | if the authenticator could not honor the request due to a network error |

### editProperties

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun editProperties(
    response: AccountAuthenticatorResponse!, 
    accountType: String!
): Bundle!
```

Returns a Bundle that contains the Intent of the activity that can be used to edit the properties. In order to indicate success the activity should call response.setResult() with a non-null Bundle.

| Parameters ||
|---|---|
| `response` | [AccountAuthenticatorResponse](AccountAuthenticatorResponse.md)!: used to set the result for the request. If the Constants.INTENT_KEY is set in the bundle then this response field is to be used for sending future results if and when the Intent is started. |
| `accountType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the AccountType whose properties are to be edited. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#!` | a Bundle containing the result or the Intent to start to continue the request. If this is null then the request is considered to still be active and the result should sent later using response. |

### finishSession

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun finishSession(
    response: AccountAuthenticatorResponse!, 
    accountType: String!, 
    sessionBundle: Bundle!
): Bundle!
```

Finishes the session started by #startAddAccountSession or #startUpdateCredentials by installing the account to device with AccountManager, or updating the local credentials. File I/O may be performed in this call.

Note: when overriding this method, startAddAccountSession and startUpdateCredentialsSession should be overridden too.

| Parameters ||
|---|---|
| `response` | [AccountAuthenticatorResponse](AccountAuthenticatorResponse.md)!: to send the result back to the AccountManager, will never be null |
| `accountType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the type of account to authenticate with, will never be null |
| `sessionBundle` | [Bundle](../android.os/Bundle.md)!: a bundle of session data created by startAddAccountSession used for adding account to device, or by startUpdateCredentialsSession used for updating local credentials. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#!` | a Bundle result or null if the result is to be returned via the response. The result will contain either: - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_INTENT:kotlin.String`, or - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_NAME:kotlin.String` and `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_TYPE:kotlin.String` of the account that was added or local credentials were updated, and optional `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_STATUS_TOKEN:kotlin.String` for checking the status of the account later, or - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ERROR_CODE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ERROR_MESSAGE:kotlin.String` to indicate an error |

| Exceptions ||
|---|---|
| `android.accounts.NetworkErrorException` | if the authenticator could not honor the request due to a network error |

**See Also**

- startAddAccountSession

### getAccountCredentialsForCloning

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAccountCredentialsForCloning(
    response: AccountAuthenticatorResponse!, 
    account: Account!
): Bundle!
```

Returns a Bundle that contains whatever is required to clone the account on a different user. The Bundle is passed to the authenticator instance in the target user via addAccountFromCredentials. The default implementation returns null, indicating that cloning is not supported.

| Parameters ||
|---|---|
| `response` | [AccountAuthenticatorResponse](AccountAuthenticatorResponse.md)!: to send the result back to the AccountManager, will never be null |
| `account` | [Account](Account.md)!: the account to clone, will never be null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#!` | a Bundle result or null if the result is to be returned via the response. |

| Exceptions ||
|---|---|
| `android.accounts.NetworkErrorException` | |

**See Also**

- addAccountFromCredentials

### getAccountRemovalAllowed

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAccountRemovalAllowed(
    response: AccountAuthenticatorResponse!, 
    account: Account!
): Bundle!
```

Checks if the removal of this account is allowed.

| Parameters ||
|---|---|
| `response` | [AccountAuthenticatorResponse](AccountAuthenticatorResponse.md)!: to send the result back to the AccountManager, will never be null |
| `account` | [Account](Account.md)!: the account to check, will never be null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#!` | a Bundle result or null if the result is to be returned via the response. The result will contain either: - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_INTENT:kotlin.String`, or - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_BOOLEAN_RESULT:kotlin.String`, true if the removal of the account is allowed, false otherwise - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ERROR_CODE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ERROR_MESSAGE:kotlin.String` to indicate an error |

| Exceptions ||
|---|---|
| `android.accounts.NetworkErrorException` | if the authenticator could not honor the request due to a network error |

### getAuthToken

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getAuthToken(
    response: AccountAuthenticatorResponse!, 
    account: Account!, 
    authTokenType: String!, 
    options: Bundle!
): Bundle!
```

Gets an authtoken for an account. If not `null`, the resultant `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` will contain different sets of keys depending on whether a token was successfully issued and, if not, whether one could be issued via some `https://developer.android.com/reference/kotlin/android/app/Activity.html#`.

If a token cannot be provided without some additional activity, the Bundle should contain `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_INTENT:kotlin.String` with an associated `https://developer.android.com/reference/kotlin/android/content/Intent.html#`. On the other hand, if there is no such activity, then a Bundle containing `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ERROR_CODE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ERROR_MESSAGE:kotlin.String` should be returned.

If a token can be successfully issued, the implementation should return the `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_NAME:kotlin.String` and `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_TYPE:kotlin.String` of the account associated with the token as well as the `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_AUTHTOKEN:kotlin.String`. In addition AbstractAccountAuthenticator implementations that declare themselves `android:customTokens=true` may also provide a non-negative `https://developer.android.com/reference/kotlin/android/accounts/AbstractAccountAuthenticator#KEY_CUSTOM_TOKEN_EXPIRY:kotlin.String` long value containing the expiration timestamp of the expiration time (in millis since the unix epoch), tokens will be cached in memory based on application's packageName/signature for however long that was specified.

Implementers should assume that tokens will be cached on the basis of account and authTokenType. The system may ignore the contents of the supplied options Bundle when determining to re-use a cached token. Furthermore, implementers should assume a supplied expiration time will be treated as non-binding advice.

Finally, note that for `android:customTokens=false` authenticators, tokens are cached indefinitely until some client calls invalidateAuthToken.

| Parameters ||
|---|---|
| `response` | [AccountAuthenticatorResponse](AccountAuthenticatorResponse.md)!: to send the result back to the AccountManager, will never be null |
| `account` | [Account](Account.md)!: the account whose credentials are to be retrieved, will never be null |
| `authTokenType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the type of auth token to retrieve, will never be null |
| --- | --- |
| `options` | [Bundle](../android.os/Bundle.md)!: a Bundle of authenticator-specific options. It always contains `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_CALLER_PID:kotlin.String` and `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_CALLER_UID:kotlin.String` fields which will let authenticator know the identity of the caller. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#!` | a Bundle result or null if the result is to be returned via the response. |

| Exceptions ||
|---|---|
| `android.accounts.NetworkErrorException` | if the authenticator could not honor the request due to a network error |

### getAuthTokenLabel

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getAuthTokenLabel(authTokenType: String!): String!
```

Ask the authenticator for a localized label for the given authTokenType.

| Parameters ||
|---|---|
| `authTokenType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the authTokenType whose label is to be returned, will never be null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the localized label of the auth token type, may be null if the type isn't known |

### getIBinder

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getIBinder(): IBinder!
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/IBinder.html#!` | the IBinder for the AccountAuthenticator |

### hasFeatures

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun hasFeatures(
    response: AccountAuthenticatorResponse!, 
    account: Account!, 
    features: Array<String!>!
): Bundle!
```

Checks if the account supports all the specified authenticator specific features.

| Parameters ||
|---|---|
| `response` | [AccountAuthenticatorResponse](AccountAuthenticatorResponse.md)!: to send the result back to the AccountManager, will never be null |
| `account` | [Account](Account.md)!: the account to check, will never be null |
| `features` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: an array of features to check, will never be null |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#!` | a Bundle result or null if the result is to be returned via the response. The result will contain either: - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_INTENT:kotlin.String`, or - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_BOOLEAN_RESULT:kotlin.String`, true if the account has all the features, false otherwise - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ERROR_CODE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ERROR_MESSAGE:kotlin.String` to indicate an error |

| Exceptions ||
|---|---|
| `android.accounts.NetworkErrorException` | if the authenticator could not honor the request due to a network error |

### isCredentialsUpdateSuggested

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isCredentialsUpdateSuggested(
    response: AccountAuthenticatorResponse!, 
    account: Account!, 
    statusToken: String!
): Bundle!
```

Checks if update of the account credentials is suggested.

| Parameters ||
|---|---|
| `response` | [AccountAuthenticatorResponse](AccountAuthenticatorResponse.md)!: to send the result back to the AccountManager, will never be null. |
| `account` | [Account](Account.md)!: the account to check, will never be null |
| `statusToken` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a String of token which can be used to check the status of locally stored credentials and if update of credentials is suggested |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#!` | a Bundle result or null if the result is to be returned via the response. The result will contain either: - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_BOOLEAN_RESULT:kotlin.String`, true if update of account's credentials is suggested, false otherwise - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ERROR_CODE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ERROR_MESSAGE:kotlin.String` to indicate an error |

| Exceptions ||
|---|---|
| `android.accounts.NetworkErrorException` | if the authenticator could not honor the request due to a network error |

### startAddAccountSession

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startAddAccountSession(
    response: AccountAuthenticatorResponse!, 
    accountType: String!, 
    authTokenType: String!, 
    requiredFeatures: Array<String!>!, 
    options: Bundle!
): Bundle!
```

Starts the add account session to authenticate user to an account of the specified accountType. No file I/O should be performed in this call. Account should be added to device only when finishSession is called after this.

Note: when overriding this method, finishSession should be overridden too.

| Parameters ||
|---|---|
| `response` | [AccountAuthenticatorResponse](AccountAuthenticatorResponse.md)!: to send the result back to the AccountManager, will never be null |
| `accountType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the type of account to authenticate with, will never be null |
| `authTokenType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the type of auth token to retrieve after authenticating with the account, may be null |
| --- | --- |
| `requiredFeatures` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: a String array of authenticator-specific features that the account authenticated with must support, may be null |
| `options` | [Bundle](../android.os/Bundle.md)!: a Bundle of authenticator-specific options, may be null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#!` | a Bundle result or null if the result is to be returned via the response. The result will contain either: - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_INTENT:kotlin.String`, or - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_SESSION_BUNDLE:kotlin.String` for adding the account to device later, and if account is authenticated, optional `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_PASSWORD:kotlin.String` and `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_STATUS_TOKEN:kotlin.String` for checking the status of the account, or - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ERROR_CODE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ERROR_MESSAGE:kotlin.String` to indicate an error |

| Exceptions ||
|---|---|
| `android.accounts.NetworkErrorException` | if the authenticator could not honor the request due to a network error |

**See Also**

- finishSession

### startUpdateCredentialsSession

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startUpdateCredentialsSession(
    response: AccountAuthenticatorResponse!, 
    account: Account!, 
    authTokenType: String!, 
    options: Bundle!
): Bundle!
```

Asks user to re-authenticate for an account but defers updating the locally stored credentials. No file I/O should be performed in this call. Local credentials should be updated only when finishSession is called after this.

Note: when overriding this method, finishSession should be overridden too.

| Parameters ||
|---|---|
| `response` | [AccountAuthenticatorResponse](AccountAuthenticatorResponse.md)!: to send the result back to the AccountManager, will never be null |
| `account` | [Account](Account.md)!: the account whose credentials are to be updated, will never be null |
| `authTokenType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the type of auth token to retrieve after updating the credentials, may be null |
| --- | --- |
| `options` | [Bundle](../android.os/Bundle.md)!: a Bundle of authenticator-specific options, may be null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#!` | a Bundle result or null if the result is to be returned via the response. The result will contain either: - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_INTENT:kotlin.String`, or - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_SESSION_BUNDLE:kotlin.String` for updating the locally stored credentials later, and if account is re-authenticated, optional `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_PASSWORD:kotlin.String` and `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_STATUS_TOKEN:kotlin.String` for checking the status of the account later, or - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ERROR_CODE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ERROR_MESSAGE:kotlin.String` to indicate an error |

| Exceptions ||
|---|---|
| `android.accounts.NetworkErrorException` | if the authenticator could not honor the request due to a network error |

**See Also**

- finishSession

### updateCredentials

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun updateCredentials(
    response: AccountAuthenticatorResponse!, 
    account: Account!, 
    authTokenType: String!, 
    options: Bundle!
): Bundle!
```

Update the locally stored credentials for an account.

| Parameters ||
|---|---|
| `response` | [AccountAuthenticatorResponse](AccountAuthenticatorResponse.md)!: to send the result back to the AccountManager, will never be null |
| `account` | [Account](Account.md)!: the account whose credentials are to be updated, will never be null |
| `authTokenType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the type of auth token to retrieve after updating the credentials, may be null |
| --- | --- |
| `options` | [Bundle](../android.os/Bundle.md)!: a Bundle of authenticator-specific options, may be null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#!` | a Bundle result or null if the result is to be returned via the response. The result will contain either: - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_INTENT:kotlin.String`, or - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_NAME:kotlin.String` and `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ACCOUNT_TYPE:kotlin.String` of the account whose credentials were updated, or - `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ERROR_CODE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/accounts/AccountManager#KEY_ERROR_MESSAGE:kotlin.String` to indicate an error |

| Exceptions ||
|---|---|
| `android.accounts.NetworkErrorException` | if the authenticator could not honor the request due to a network error |
