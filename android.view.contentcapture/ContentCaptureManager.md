# ContentCaptureManager

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ContentCaptureManager

Kotlin| [Java](https://developer.android.com/reference/android/view/contentcapture/ContentCaptureManager "View this page in Java") 
| --- | --- |

```
class ContentCaptureManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.contentcapture.ContentCaptureManager](https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureManager#) |

Provides additional ways for apps to integrate with the content capture subsystem.

Content capture provides real-time, continuous capture of application activity, display and events to an intelligence service that is provided by the Android system. The intelligence service then uses that info to mediate and speed user journey through different apps. For example, when the user receives a restaurant address in a chat app and switches to a map app to search for that restaurant, the intelligence service could offer an autofill dialog to let the user automatically select its address.

Content capture was designed with two major concerns in mind: privacy and performance.

- **Privacy:** the intelligence service is a trusted component provided that is provided by the device manufacturer and that cannot be changed by the user (although the user can globaly disable content capture using the Android Settings app). This service can only use the data for in-device machine learning, which is enforced both by process isolation and [CDD requirements](https://source.android.com/compatibility/cdd).
- **Performance:** content capture is highly optimized to minimize its impact in the app jankiness and overall device system health. For example, its only enabled on apps (or even specific activities from an app) that were explicitly allowlisted by the intelligence service, and it buffers the events so they are sent in a batch to the service (see [isContentCaptureEnabled()](https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureManager#isContentCaptureEnabled())for other cases when its disabled).

In fact, before using this manager, the app developer should check if it's available. Example: 

```kotlin
<code>
   ContentCaptureManager mgr = context.getSystemService(ContentCaptureManager.class);
   if (mgr != null &amp;&amp; mgr.isContentCaptureEnabled()) {
     // ...
   }
   </code>
```

App developers usually don't need to explicitly interact with content capture, except when the app:

- Can define a contextual [android.content.LocusId](https://developer.android.com/reference/kotlin/android/content/LocusId.html#) to identify unique state (such as a conversation between 2 chat users).
- Can have multiple view hierarchies with different contextual meaning (for example, a browser app with multiple tabs, each representing a different URL).
- Contains custom views (that extend View directly and are not provided by the standard Android SDK.
- Contains views that provide their own virtual hierarchy (like a web browser that render the HTML elements using a Canvas).

The main integration point with content capture is the [ContentCaptureSession](https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession). A "main" session is automatically created by the Android System when content capture is enabled for the activity and its used by the standard Android views to notify the content capture service of events such as views being added, views been removed, and text changed by user input. The session could have a [ContentCaptureContext](https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureContext) to provide more contextual info about it, such as the locus associated with the view hierarchy (see [android.content.LocusId](https://developer.android.com/reference/kotlin/android/content/LocusId.html#) for more info about locus). By default, the main session doesn't have a`ContentCaptureContext`, but you can change it after its created. Example: 

```kotlin
<code>
  protected void onCreate(Bundle savedInstanceState) {
    // Initialize view structure
    ContentCaptureSession session = rootView.getContentCaptureSession();
    if (session != null) {
      session.setContentCaptureContext(ContentCaptureContext.forLocusId("chat_UserA_UserB"));
    }
  }
  </code>
```

If your activity contains view hierarchies with a different contextual meaning, you should created child sessions for each view hierarchy root. For example, if your activity is a browser, you could use the main session for the main URL being rendered, then child sessions for each`IFRAME`: 

```kotlin
<code>
  ContentCaptureSession mMainSession;
 
  protected void onCreate(Bundle savedInstanceState) {
     // Initialize view structure...
     mMainSession = rootView.getContentCaptureSession();
     if (mMainSession != null) {
       mMainSession.setContentCaptureContext(
           ContentCaptureContext.forLocusId("https://example.com"));
     }
  }
 
  private void loadIFrame(View iframeRootView, String url) {
    if (mMainSession != null) {
       ContentCaptureSession iFrameSession = mMainSession.newChild(
           ContentCaptureContext.forLocusId(url));
       }
       iframeRootView.setContentCaptureSession(iFrameSession);
    }
    // Load iframe...
  }
  </code>
```

If your activity has custom views (i.e., views that extend [View](https://developer.android.com/reference/kotlin/android/view/View.html#) directly and provide just one logical view, not a virtual tree hiearchy) and it provides content that's relevant for content capture (as of [Android Q](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int), the only relevant content is text), then your view implementation should:

- Set it as important for content capture.
- Fill [ViewStructure](https://developer.android.com/reference/kotlin/android/view/ViewStructure.html#) used for content capture.
- Notify the [ContentCaptureSession](https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession) when the text is changed by user input.

Here's an example of the relevant methods for an`EditText`-like view: 

```kotlin
<code>
  public class MyEditText extends View {
 
  public MyEditText(...) {
    if (getImportantForContentCapture() == IMPORTANT_FOR_CONTENT_CAPTURE_AUTO) {
      setImportantForContentCapture(IMPORTANT_FOR_CONTENT_CAPTURE_YES);
    }
  }
 
  public void onProvideContentCaptureStructure(@NonNull ViewStructure structure, int flags) {
    super.onProvideContentCaptureStructure(structure, flags);
 
    structure.setText(getText(), getSelectionStart(), getSelectionEnd());
    structure.setHint(getHint());
    structure.setInputType(getInputType());
    // set other properties like setTextIdEntry(), setTextLines(), setTextStyle(),
    // setMinTextEms(), setMaxTextEms(), setMaxTextLength()
  }
 
  private void onTextChanged() {
    if (isLaidOut() &amp;&amp; isImportantForContentCapture() &amp;&amp; isTextEditable()) {
      ContentCaptureManager mgr = mContext.getSystemService(ContentCaptureManager.class);
      if (cm != null &amp;&amp; cm.isContentCaptureEnabled()) {
         ContentCaptureSession session = getContentCaptureSession();
         if (session != null) {
           session.notifyViewTextChanged(getAutofillId(), getText());
         }
    }
  }
  </code>
```

If your view provides its own virtual hierarchy (for example, if it's a browser that draws the HTML using [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#) or native libraries in a different render process), then the view is also responsible to notify the session when the virtual elements appear and disappear - see [View.onProvideContentCaptureStructure(ViewStructure, int)](https://developer.android.com/reference/kotlin/android/view/View.html#onProvideContentCaptureStructure(android.view.ViewStructure,%20kotlin.Int))for more info.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DATA_SHARE_ERROR_CONCURRENT_REQUEST](https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureManager#DATA_SHARE_ERROR_CONCURRENT_REQUEST:kotlin.Int) Request has been rejected, because a concurrent data share sessions is in progress. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DATA_SHARE_ERROR_TIMEOUT_INTERRUPTED](https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureManager#DATA_SHARE_ERROR_TIMEOUT_INTERRUPTED:kotlin.Int) Request has been interrupted because of data share session timeout. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DATA_SHARE_ERROR_UNKNOWN](https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureManager#DATA_SHARE_ERROR_UNKNOWN:kotlin.Int) Error happened during the data sharing session. |
| --- | --- |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [ContentCaptureCondition](https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureCondition)!\>? | [getContentCaptureConditions](https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureManager#getContentCaptureConditions())`()` Gets the list of conditions for when content capture should be allowed. |
| [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)? | [getServiceComponentName](https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureManager#getServiceComponentName())`()` Returns the component name of the system service that is consuming the captured events for the current user. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isContentCaptureEnabled](https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureManager#isContentCaptureEnabled())`()` Checks whether content capture is enabled for this activity. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeData](https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureManager#removeData(android.view.contentcapture.DataRemovalRequest))`(`request:` ` [DataRemovalRequest](https://developer.android.com/reference/kotlin/android/view/contentcapture/DataRemovalRequest)`)` Called by the app to request the content capture service to remove content capture data associated with some context. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContentCaptureEnabled](https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureManager#setContentCaptureEnabled(kotlin.Boolean))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called by apps to explicitly enable or disable content capture. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [shareData](https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureManager#shareData(android.view.contentcapture.DataShareRequest,%20java.util.concurrent.Executor,%20android.view.contentcapture.DataShareWriteAdapter))`(`request:` ` [DataShareRequest](https://developer.android.com/reference/kotlin/android/view/contentcapture/DataShareRequest)`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `dataShareWriteAdapter:` ` [DataShareWriteAdapter](https://developer.android.com/reference/kotlin/android/view/contentcapture/DataShareWriteAdapter)`)` Called by the app to request data sharing via writing to a file. |
| --- | --- |

## Constants

### DATA_SHARE_ERROR_CONCURRENT_REQUEST

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA_SHARE_ERROR_CONCURRENT_REQUEST: Int
```

Request has been rejected, because a concurrent data share sessions is in progress. 

 Value: 2

### DATA_SHARE_ERROR_TIMEOUT_INTERRUPTED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA_SHARE_ERROR_TIMEOUT_INTERRUPTED: Int
```

Request has been interrupted because of data share session timeout. 

 Value: 3

### DATA_SHARE_ERROR_UNKNOWN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA_SHARE_ERROR_UNKNOWN: Int
```

Error happened during the data sharing session. 

 Value: 1

## Public methods

### getContentCaptureConditions

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getContentCaptureConditions(): MutableSet<ContentCaptureCondition!>?
```

Gets the list of conditions for when content capture should be allowed.

This method is typically used by web browsers so they don't generate unnecessary content capture events for websites the content capture service is not interested on.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [ContentCaptureCondition](https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureCondition)!>? | list of conditions, or`null`if the service didn't set any restriction (in which case content capture events should always be generated). If the list is empty, then it should not generate any event at all. |

### getServiceComponentName

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getServiceComponentName(): ComponentName?
```

Returns the component name of the system service that is consuming the captured events for the current user.

| Return ||
|------------------------------------------------------------------------------------------------------|--------------------------|
| [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)? | This value may be`null`. |

| Exceptions ||
|------------------------------|---------------------------------------------|
| `java.lang.RuntimeException` | if getting the component name is timed out. |

### isContentCaptureEnabled

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isContentCaptureEnabled(): Boolean
```

Checks whether content capture is enabled for this activity.

There are many reasons it could be disabled, such as:

- App itself disabled content capture through [setContentCaptureEnabled(boolean)](https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureManager#setContentCaptureEnabled(kotlin.Boolean)).
- Intelligence service did not allowlist content capture for this activity's package.
- Intelligence service did not allowlist content capture for this specific activity.
- Intelligence service disabled content capture globally.
- User disabled content capture globally through the Android Settings app.
- Device manufacturer (OEM) disabled content capture globally.
- Transient errors, such as intelligence service package being updated. 

### removeData

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun removeData(request: DataRemovalRequest): Unit
```

Called by the app to request the content capture service to remove content capture data associated with some context.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [DataRemovalRequest](https://developer.android.com/reference/kotlin/android/view/contentcapture/DataRemovalRequest):object specifying what user data should be removed. This value cannot be`null`. |

### setContentCaptureEnabled

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setContentCaptureEnabled(enabled: Boolean): Unit
```

Called by apps to explicitly enable or disable content capture.

**Note:** this call is not persisted accross reboots, so apps should typically call it on [android.app.Activity#onCreate(android.os.Bundle, android.os.PersistableBundle)](https://developer.android.com/reference/kotlin/android/app/Activity.html#onCreate(android.os.Bundle,%20android.os.PersistableBundle)). 

### shareData

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun shareData(
    request: DataShareRequest, 
    executor: Executor, 
    dataShareWriteAdapter: DataShareWriteAdapter
): Unit
```

Called by the app to request data sharing via writing to a file.

The ContentCaptureService app will receive a read-only file descriptor pointing to the same file and will be able to read data being shared from it.

Note: using this API doesn't guarantee the app staying alive and is "best-effort". Starting a foreground service would minimize the chances of the app getting killed during the file sharing session.

| Parameters ||
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [DataShareRequest](https://developer.android.com/reference/kotlin/android/view/contentcapture/DataShareRequest):object specifying details of the data being shared. This value cannot be`null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `dataShareWriteAdapter` | [DataShareWriteAdapter](https://developer.android.com/reference/kotlin/android/view/contentcapture/DataShareWriteAdapter):This value cannot be`null`. |
| --- | --- |
