# ChooserManager

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ChooserManager

Kotlin| [Java](https://developer.android.com/reference/android/service/chooser/ChooserManager "View this page in Java") 

```
open class ChooserManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.service.chooser.ChooserManager](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserManager#) |

Manages the creation, tracking, and retrieval of chooser sessions.

An Interactive Chooser Session allows apps to invoke the system Chooser without entirely covering app UI. Users may interact with both the app and Chooser, while bidirectional communication between the two ensures a consistent state.

### Usage Example:

```kotlin
<code>ChooserManager chooserManager = context.getSystemService(ChooserManager.class);
  if (chooserManager == null) {
      // handle the case when the interactive chooser session functionality is not supported.
  }
 
  // Construct the sharing intent
  Intent targetIntent = new Intent(Intent.ACTION_SEND);
  targetIntent.setType("text/plain");
  targetIntent.putExtra(Intent.EXTRA_TEXT, "This is a message that will be shared.");
 
  Intent chooserIntent = Intent.createChooser(targetIntent, null);
 
  // Start a new chooser session
  ChooserSession session = chooserManager.startSession(context, chooserIntent);
  ChooserSessionToken token = session.getToken();
  // Optionally, store the token int an activity saved state to re-associate with the session later
 
  // Later, to retrieve a session using a token:
  ChooserSessionToken retrievedToken = ... // obtain the stored token
  ChooserSession existingSession = chooserManager.getSession(retrievedToken);
  if (existingSession != null) {
  // Interact with the existing session
  }
  </code>
```

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [ChooserSession](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSession)? | [getSession](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserManager#getSession(android.service.chooser.ChooserSessionToken))`(`token:` ` [ChooserSessionToken](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSessionToken)`)` Returns a [ChooserSession](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSession) associated with this token or`null`if there is no active session. |
| open [ChooserSession](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSession) | [startSession](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserManager#startSession(android.content.Context,%20android.content.Intent))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`, `chooserIntent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)`)` Starts a new interactive Chooser session. |

## Public methods

### getSession

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSession(token: ChooserSessionToken): ChooserSession?
```

Returns a [ChooserSession](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSession) associated with this token or`null`if there is no active session.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `token` | [ChooserSessionToken](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSessionToken): [ChooserSessionToken](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSessionToken). This value cannot be`null`. |

**See Also**

- [android.service.chooser.ChooserSession#getToken()](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSession#getToken()) 

### startSession

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startSession(
    context: Context, 
    chooserIntent: Intent
): ChooserSession
```

Starts a new interactive Chooser session. The method is idempotent and will start Chooser only once.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `chooserIntent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#):an [Intent.ACTION_CHOOSER](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CHOOSER:kotlin.String) intent that will be used as a base for the new Chooser session. An interactive Chooser session also supports the following chooser parameters: - [Intent.EXTRA_ALTERNATE_INTENTS](https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_ALTERNATE_INTENTS:kotlin.String) - [Intent.EXTRA_INITIAL_INTENTS](https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_INITIAL_INTENTS:kotlin.String) - [Intent.EXTRA_EXCLUDE_COMPONENTS](https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_EXCLUDE_COMPONENTS:kotlin.String) - [Intent.EXTRA_REPLACEMENT_EXTRAS](https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_REPLACEMENT_EXTRAS:kotlin.String) - [Intent.EXTRA_CHOOSER_TARGETS](https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHOOSER_TARGETS:kotlin.String) - [Intent.EXTRA_CHOOSER_REFINEMENT_INTENT_SENDER](https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHOOSER_REFINEMENT_INTENT_SENDER:kotlin.String) - [Intent.EXTRA_CHOOSER_RESULT_INTENT_SENDER](https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHOOSER_RESULT_INTENT_SENDER:kotlin.String) - [Intent.EXTRA_CHOSEN_COMPONENT_INTENT_SENDER](https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHOSEN_COMPONENT_INTENT_SENDER:kotlin.String) <br /> See also [Intent.createChooser(Intent, CharSequence)](https://developer.android.com/reference/kotlin/android/content/Intent.html#createChooser(android.content.Intent,%20kotlin.CharSequence)). This value cannot be`null`. |
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#):This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------------------------------|-----------------------------|
| [ChooserSession](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSession) | This value cannot be`null`. |
