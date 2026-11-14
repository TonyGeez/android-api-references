# ChooserManager

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ChooserManager

Kotlin| [Java](ChooserManager.md) 
| --- | --- |

```
open class ChooserManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.chooser.ChooserManager](ChooserManager.md) |

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
| open [ChooserSession](ChooserSession.md)? | [getSession](ChooserManager.md))`(`token:` ` [ChooserSessionToken](ChooserSessionToken.md)`)` Returns a [ChooserSession](ChooserSession.md) associated with this token or`null`if there is no active session. |
| open [ChooserSession](ChooserSession.md) | [startSession](ChooserManager.md))`(`context:` ` [Context](../android.content/Context.md)`, `chooserIntent:` ` [Intent](../android.content/Intent.md)`)` Starts a new interactive Chooser session. |

## Public methods

### getSession

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSession(token: ChooserSessionToken): ChooserSession?
```

Returns a [ChooserSession](ChooserSession.md) associated with this token or`null`if there is no active session.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `token` | [ChooserSessionToken](ChooserSessionToken.md): [ChooserSessionToken](ChooserSessionToken.md). This value cannot be`null`. |

**See Also**

- [android.service.chooser.ChooserSession#getToken()](ChooserSession.md)) 

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
| `chooserIntent` | [Intent](../android.content/Intent.md):an [Intent.ACTION_CHOOSER](../android.content/Intent.md) intent that will be used as a base for the new Chooser session. An interactive Chooser session also supports the following chooser parameters: - [Intent.EXTRA_ALTERNATE_INTENTS](../android.content/Intent.md) - [Intent.EXTRA_INITIAL_INTENTS](../android.content/Intent.md) - [Intent.EXTRA_EXCLUDE_COMPONENTS](../android.content/Intent.md) - [Intent.EXTRA_REPLACEMENT_EXTRAS](../android.content/Intent.md) - [Intent.EXTRA_CHOOSER_TARGETS](../android.content/Intent.md) - [Intent.EXTRA_CHOOSER_REFINEMENT_INTENT_SENDER](../android.content/Intent.md) - [Intent.EXTRA_CHOOSER_RESULT_INTENT_SENDER](../android.content/Intent.md) - [Intent.EXTRA_CHOSEN_COMPONENT_INTENT_SENDER](../android.content/Intent.md) <br /> See also [Intent.createChooser(Intent, CharSequence)](../android.content/Intent.md)). This value cannot be`null`. |
| `context` | [Context](../android.content/Context.md):This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------------------------------|-----------------------------|
| [ChooserSession](ChooserSession.md) | This value cannot be`null`. |
