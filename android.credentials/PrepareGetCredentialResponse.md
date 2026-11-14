Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PrepareGetCredentialResponse

Kotlin | [Java](PrepareGetCredentialResponse.md)
| --- | --- |

```
class PrepareGetCredentialResponse
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.credentials.PrepareGetCredentialResponse](PrepareGetCredentialResponse.md) |

A response object that prefetches user app credentials and provides metadata about them. It can then be used to issue the full credential retrieval flow via the `https://developer.android.com/reference/kotlin/android/credentials/CredentialManager#getCredential(android.content.Context,%20android.credentials.PrepareGetCredentialResponse.PendingGetCredentialHandle,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` method to perform the remaining flows such as consent collection and credential selection, to officially retrieve a credential.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/credentials/PrepareGetCredentialResponse.PendingGetCredentialHandle` A handle that represents a pending get-credential operation. |

| Public methods ||
|---|---|
| [PrepareGetCredentialResponse.PendingGetCredentialHandle](../android/credentials/PrepareGetCredentialResponse.PendingGetCredentialHandle.md) | `https://developer.android.com/reference/kotlin/android/credentials/PrepareGetCredentialResponse#getPendingGetCredentialHandle()()` Returns a handle that represents this pending get-credential operation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/credentials/PrepareGetCredentialResponse#hasAuthenticationResults()()` Returns true if the user has any candidate authentication actions (locked credential supplier), and false otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/credentials/PrepareGetCredentialResponse#hasCredentialResults(kotlin.String)(credentialType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns true if the user has any candidate credentials for the given `credentialType`, and false otherwise. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/credentials/PrepareGetCredentialResponse#hasRemoteResults()()` Returns true if the user has any candidate remote credential results, and false otherwise. |

## Public methods

### getPendingGetCredentialHandle

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPendingGetCredentialHandle(): PrepareGetCredentialResponse.PendingGetCredentialHandle
```

Returns a handle that represents this pending get-credential operation. Pass this handle to `https://developer.android.com/reference/kotlin/android/credentials/CredentialManager#getCredential(android.content.Context,%20android.credentials.PrepareGetCredentialResponse.PendingGetCredentialHandle,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` to perform the remaining flows to officially retrieve a credential.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/credentials/PrepareGetCredentialResponse.PendingGetCredentialHandle` | This value cannot be `null`. |

### hasAuthenticationResults

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasAuthenticationResults(): Boolean
```

Returns true if the user has any candidate authentication actions (locked credential supplier), and false otherwise. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CREDENTIAL_MANAGER_QUERY_CANDIDATE_CREDENTIALS:kotlin.String`

### hasCredentialResults

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasCredentialResults(credentialType: String): Boolean
```

Returns true if the user has any candidate credentials for the given `credentialType`, and false otherwise. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CREDENTIAL_MANAGER_QUERY_CANDIDATE_CREDENTIALS:kotlin.String`

| Parameters ||
|---|---|
| `credentialType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

### hasRemoteResults

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasRemoteResults(): Boolean
```

Returns true if the user has any candidate remote credential results, and false otherwise. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CREDENTIAL_MANAGER_QUERY_CANDIDATE_CREDENTIALS:kotlin.String`
