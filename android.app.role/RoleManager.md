Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RoleManager

```
class RoleManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.role.RoleManager](../android/app/role/RoleManager.md) |

This class provides information about and manages roles.

A role is a unique name within the system associated with certain privileges. The list of available roles might change with a system app update, so apps should not make assumption about the availability of roles. Instead, they should always query if the role is available using `https://developer.android.com/reference/kotlin/android/app/role/RoleManager#isRoleAvailable(kotlin.String)` before trying to do anything with it. Some predefined role names are available as constants in this class, and a list of possibly available roles can be found in the [AndroidX Role library](../androidx/core/role/_package.md).

There can be multiple applications qualifying for a role, but only a subset of them can become role holders. To qualify for a role, an application must meet certain requirements, including defining certain components in its manifest. These requirements can be found in the AndroidX Libraries. Then the application will need user consent to become a role holder, which can be requested using `https://developer.android.com/reference/kotlin/android/app/Activity.html#startActivityForResult(android.content.Intent,%20kotlin.Int)` with the `Intent` obtained from `https://developer.android.com/reference/kotlin/android/app/role/RoleManager#createRequestRoleIntent(kotlin.String)`.

Upon becoming a role holder, the application may be granted certain privileges that are role specific. When the application loses its role, these privileges will also be revoked.

## Summary

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/role/RoleManager#ROLE_ASSISTANT:kotlin.String` The name of the assistant app role. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/role/RoleManager#ROLE_BROWSER:kotlin.String` The name of the browser role. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/role/RoleManager#ROLE_CALL_REDIRECTION:kotlin.String` The name of the call redirection role. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/role/RoleManager#ROLE_CALL_SCREENING:kotlin.String` The name of the call screening and caller id role. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/role/RoleManager#ROLE_CONTENT_SAFETY:kotlin.String` The name of the content safety role. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/role/RoleManager#ROLE_DIALER:kotlin.String` The name of the dialer role. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/role/RoleManager#ROLE_EMERGENCY:kotlin.String` The name of the emergency role |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/role/RoleManager#ROLE_HOME:kotlin.String` The name of the home role. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/role/RoleManager#ROLE_NOTES:kotlin.String` The name of the notes role. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/role/RoleManager#ROLE_REGISTERED_APP_STORE:kotlin.String` The name of the registered app store role. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/role/RoleManager#ROLE_SEARCH_ENGINE:kotlin.String` The name of the search engine role. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/role/RoleManager#ROLE_SMS:kotlin.String` The name of the SMS role. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/role/RoleManager#ROLE_WALLET:kotlin.String` The name of the Wallet role. |

| Public methods ||
|---|---|
| [Intent](../android/content/Intent.md) | `https://developer.android.com/reference/kotlin/android/app/role/RoleManager#createRequestRoleIntent(kotlin.String)(roleName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns an `Intent` suitable for passing to `https://developer.android.com/reference/kotlin/android/app/Activity.html#startActivityForResult(android.content.Intent,%20kotlin.Int)` which prompts the user to grant a role to this application. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/role/RoleManager#isRoleAvailable(kotlin.String)(roleName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Check whether a role is available in the system. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/role/RoleManager#isRoleHeld(kotlin.String)(roleName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Check whether the calling application is holding a particular role. |
| --- | --- |

## Constants

### ROLE_ASSISTANT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ROLE_ASSISTANT: String
```

The name of the assistant app role.

 Value: "android.app.role.ASSISTANT"

**See Also**

- `https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionService.html#`

### ROLE_BROWSER

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ROLE_BROWSER: String
```

The name of the browser role.

 Value: "android.app.role.BROWSER"

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_APP_BROWSER:kotlin.String`

### ROLE_CALL_REDIRECTION

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ROLE_CALL_REDIRECTION: String
```

The name of the call redirection role.

A call redirection app provides a means to re-write the phone number for an outgoing call to place the call through a call redirection service.

 Value: "android.app.role.CALL_REDIRECTION"

**See Also**

- `https://developer.android.com/reference/kotlin/android/telecom/CallRedirectionService.html#`

### ROLE_CALL_SCREENING

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ROLE_CALL_SCREENING: String
```

The name of the call screening and caller id role.

 Value: "android.app.role.CALL_SCREENING"

**See Also**

- `https://developer.android.com/reference/kotlin/android/telecom/CallScreeningService.html#`

### ROLE_CONTENT_SAFETY

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ROLE_CONTENT_SAFETY: String
```

The name of the content safety role. This role enables the ability to view and restrict content for the user.

 Value: "android.app.role.CONTENT_SAFETY"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/contentsafety/ContentSafetyManager.html#`

### ROLE_DIALER

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ROLE_DIALER: String
```

The name of the dialer role.

 Value: "android.app.role.DIALER"

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_DIAL:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/telecom/InCallService.html#`

### ROLE_EMERGENCY

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ROLE_EMERGENCY: String
```

The name of the emergency role

 Value: "android.app.role.EMERGENCY"

### ROLE_HOME

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ROLE_HOME: String
```

The name of the home role.

 Value: "android.app.role.HOME"

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_HOME:kotlin.String`

### ROLE_NOTES

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ROLE_NOTES: String
```

The name of the notes role.

 Value: "android.app.role.NOTES"

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CREATE_NOTE:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_USE_STYLUS_MODE:kotlin.String`

### ROLE_REGISTERED_APP_STORE

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ROLE_REGISTERED_APP_STORE: String
```

The name of the registered app store role. This role is managed from `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#` when a registered app store is installed or updated.

 Value: "android.app.role.REGISTERED_APP_STORE"

### ROLE_SEARCH_ENGINE

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ROLE_SEARCH_ENGINE: String
```

The name of the search engine role.

 Value: "android.app.role.SEARCH_ENGINE"

### ROLE_SMS

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ROLE_SMS: String
```

The name of the SMS role.

 Value: "android.app.role.SMS"

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_APP_MESSAGING:kotlin.String`

### ROLE_WALLET

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ROLE_WALLET: String
```

The name of the Wallet role.

 Value: "android.app.role.WALLET"

**See Also**

- `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation.html#`

## Public methods

### createRequestRoleIntent

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun createRequestRoleIntent(roleName: String): Intent
```

Returns an `Intent` suitable for passing to `https://developer.android.com/reference/kotlin/android/app/Activity.html#startActivityForResult(android.content.Intent,%20kotlin.Int)` which prompts the user to grant a role to this application.

If the role is granted, the `resultCode` will be `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_OK:kotlin.Int`, otherwise it will be `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_CANCELED:kotlin.Int`.

| Parameters ||
|---|---|
| `roleName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the name of requested role. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/Intent.html#` | the `Intent` to prompt user to grant the role. This value cannot be `null`. |

### isRoleAvailable

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isRoleAvailable(roleName: String): Boolean
```

Check whether a role is available in the system.

| Parameters ||
|---|---|
| `roleName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the name of role to checking for. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether the role is available in the system |

### isRoleHeld

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isRoleHeld(roleName: String): Boolean
```

Check whether the calling application is holding a particular role.

| Parameters ||
|---|---|
| `roleName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the name of the role to check for. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether the calling application is holding the role |
