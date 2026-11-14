Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ContentCaptureSession

```
abstract class ContentCaptureSession : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.contentcapture.ContentCaptureSession](../android/view/contentcapture/ContentCaptureSession.md) |

Session used when notifying the Android system about events associated with views.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#VERSION_1:kotlin.Int` Content Capture Version 1. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#VERSION_2:kotlin.Int` Content Capture Version 2. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#close()()` Closes this resource, relinquishing any underlying resources. |
| [ContentCaptureSession](../android/view/contentcapture/ContentCaptureSession.md) | `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#createContentCaptureSession(android.view.contentcapture.ContentCaptureContext)(context: https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureContext)` Creates a new `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#destroy()()` Destroys this session, flushing out all pending notifications to the service. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#flush()()` Flushes an internal buffer of UI events and signals System Intelligence (SI) that a semantically meaningful state has been reached. |
| [ContentCaptureContext](../android/view/contentcapture/ContentCaptureContext.md)? | `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#getContentCaptureContext()()` Gets the `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureContext` associated with the session. |
| [ContentCaptureSessionId](../android/view/contentcapture/ContentCaptureSessionId.md) | `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#getContentCaptureSessionId()()` Gets the id used to identify this session. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#getContentCaptureVersion()()` Gets the Content Capture version enabled for this session. |
| open [AutofillId](../android/view/autofill/AutofillId.md) | `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#newAutofillId(android.view.autofill.AutofillId,%20kotlin.Long)(hostId: https://developer.android.com/reference/kotlin/android/view/autofill/AutofillId.html#, virtualChildId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Creates a new `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillId.html#` for a virtual child, so it can be used to uniquely identify the children in the session. |
| [ViewStructure](../android/view/ViewStructure.md) | `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#newViewStructure(android.view.View)(view: https://developer.android.com/reference/kotlin/android/view/View.html#)` Creates a `https://developer.android.com/reference/kotlin/android/view/ViewStructure.html#` for a "standard" view. |
| --- | --- |
| [ViewStructure](../android/view/ViewStructure.md) | `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#newVirtualViewStructure(android.view.autofill.AutofillId,%20kotlin.Long)(parentId: https://developer.android.com/reference/kotlin/android/view/autofill/AutofillId.html#, virtualId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Creates a `https://developer.android.com/reference/kotlin/android/view/ViewStructure.html#` for a "virtual" view, so it can be passed to `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#notifyViewAppeared(android.view.ViewStructure)` by the view managing the virtual view hierarchy. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#notifyContentInteractionEvent(android.view.autofill.AutofillId)(autofillId: https://developer.android.com/reference/kotlin/android/view/autofill/AutofillId.html#)` Notifies the Intelligence Service that a view has been interacted. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#notifyNodeAppearedOrChanged(android.view.autofill.AutofillId,%20android.view.contentcapture.ContentCaptureNodeProperties)(id: https://developer.android.com/reference/kotlin/android/view/autofill/AutofillId.html#, properties: https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureNodeProperties?)` Creates a new node or updates an existing one according to the changes in properties. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#notifyNodeDisappeared(android.view.autofill.AutofillId)(id: https://developer.android.com/reference/kotlin/android/view/autofill/AutofillId.html#)` Removes a node from the active content capture hierarchy. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#notifySessionPaused()()` Notifies the Content Capture Service that a session has paused. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#notifySessionResumed()()` Notifies the Content Capture Service that a session has resumed. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#notifyViewAppeared(android.view.ViewStructure)(node: https://developer.android.com/reference/kotlin/android/view/ViewStructure.html#)` Notifies the Content Capture Service that a node has been added to the view structure. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#notifyViewDisappeared(android.view.autofill.AutofillId)(id: https://developer.android.com/reference/kotlin/android/view/autofill/AutofillId.html#)` Notifies the Content Capture Service that a node has been removed from the view structure. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#notifyViewInsetsChanged(android.graphics.Insets)(viewInsets: https://developer.android.com/reference/kotlin/android/graphics/Insets.html#)` Notifies the Intelligence Service that the insets of a view have changed. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#notifyViewTextChanged(android.view.autofill.AutofillId,%20kotlin.CharSequence)(id: https://developer.android.com/reference/kotlin/android/view/autofill/AutofillId.html#, text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?)` Notifies the Intelligence Service that the value of a text node has been changed. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#notifyViewsAppeared(kotlin.collections.MutableList)(appearedNodes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/view/ViewStructure.html#!>)` Notifies the Content Capture Service that a list of nodes has appeared in the view structure. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#notifyViewsDisappeared(android.view.autofill.AutofillId,%20kotlin.LongArray)(hostId: https://developer.android.com/reference/kotlin/android/view/autofill/AutofillId.html#, virtualIds: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)` Notifies the Content Capture Service that many nodes has been removed from a virtual view structure. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#setContentCaptureContext(android.view.contentcapture.ContentCaptureContext)(context: https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureContext?)` Sets the `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureContext` associated with the session. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#toString()()` Returns a string representation of the object. |

## Constants

### VERSION_1

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VERSION_1: Int
```

Content Capture Version 1.

The first Content Capture version is an information rich, event based system that attempts to transfer the current view hierarchy from the application process to a system intelligence service through periodic event dumps, e.g. `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#flush()`. However, this system can also be resource heavy due to the large number of events it generates.

When this version is returned by `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#getContentCaptureVersion()`, developers should use Version 1 APIs to notify the system of view hierarchy changes. Calling Version 2 APIs when the session is configured for Version 1 will result in no-ops.

A list of functions that belong explicitly to Content Capture Version 1:

- `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#notifyViewAppeared(android.view.ViewStructure)`
- `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#notifyViewDisappeared(android.view.autofill.AutofillId)`
- `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#notifyViewsAppeared(kotlin.collections.MutableList)`
- `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#notifyViewsDisappeared(android.view.autofill.AutofillId,%20kotlin.LongArray)`
- `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#notifyViewTextChanged(android.view.autofill.AutofillId,%20kotlin.CharSequence)`
- `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#flush()`
- `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#newViewStructure(android.view.View)`
- `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#newVirtualViewStructure(android.view.autofill.AutofillId,%20kotlin.Long)`

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#getContentCaptureVersion()`
- `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#VERSION_2:kotlin.Int`

### VERSION_2

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VERSION_2: Int
```

Content Capture Version 2.

The second and newer Content Capture takes a more focused and leaner approach to passing the view hierarchy from the application to a system intelligence service. The required information is mostly limited to text on screen and bounding boxes of these text nodes. This version of Content Capture is also significantly more efficient at resource usage and recommended to be the default one for various system intelligence services to use.

When this version is returned by `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#getContentCaptureVersion()`, developers should use Version 2 APIs to report node lifecycle and property updates. Calling Version 1 APIs when the session is configured for Version 2 will result in no-ops.

A list of functions that belong explicitly to Content Capture Version 2:

- `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#notifyNodeAppearedOrChanged(android.view.autofill.AutofillId,%20android.view.contentcapture.ContentCaptureNodeProperties)`
- `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#notifyNodeDisappeared(android.view.autofill.AutofillId)`

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#getContentCaptureVersion()`
- `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#VERSION_1:kotlin.Int`

## Public methods

### close

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun close(): Unit
```

Closes this resource, relinquishing any underlying resources. This method is invoked automatically on objects managed by the `try`-with-resources statement.

| Exceptions ||
|---|---|
| `java.lang.Exception` | if this resource cannot be closed |

### createContentCaptureSession

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun createContentCaptureSession(context: ContentCaptureContext): ContentCaptureSession
```

Creates a new `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#`.

See `https://developer.android.com/reference/kotlin/android/view/View.html#setContentCaptureSession(android.view.contentcapture.ContentCaptureSession)` for more info.

| Parameters ||
|---|---|
| `context` | [ContentCaptureContext](../android/view/contentcapture/ContentCaptureContext.md): This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#` | This value cannot be `null`. |

### destroy

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun destroy(): Unit
```

Destroys this session, flushing out all pending notifications to the service.

Once destroyed, any new notification will be dropped.

### flush

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun flush(): Unit
```

Flushes an internal buffer of UI events and signals System Intelligence (SI) that a semantically meaningful state has been reached. SI uses this signal to potentially rebuild the view hierarchy and understand the current state of the UI.

UI events are often batched together for performance reasons. A semantic batch represents a series of events that, when applied sequentially, result in a meaningful and complete UI state.

It is crucial to call `flush()` after completing a semantic batch to ensure SI can accurately reconstruct the view hierarchy.

**Premature Flushing:** Calling `flush()` within a semantic batch may lead to SI failing to rebuild the view hierarchy correctly. This could manifest as incorrect ordering of sibling nodes.

**Delayed Flushing:** While not immediately flushing after a semantic batch is generally safe, it's recommended to do so as soon as possible. In the worst-case scenario where a `flush()` is never called, SI will attempt to process the events after a short delay based on view appearance and disappearance events.

Note; This function belongs to Content Capture Version 1.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#getContentCaptureVersion()`

### getContentCaptureContext

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getContentCaptureContext(): ContentCaptureContext?
```

Gets the `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureContext` associated with the session.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureContext?` | context set on constructor or by `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#setContentCaptureContext(android.view.contentcapture.ContentCaptureContext)`, or `null` if never explicitly set. |

### getContentCaptureSessionId

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getContentCaptureSessionId(): ContentCaptureSessionId
```

Gets the id used to identify this session.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSessionId` | This value cannot be `null`. |

### getContentCaptureVersion

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getContentCaptureVersion(): Int
```

Gets the Content Capture version enabled for this session.

ContentCaptureSession offers two versions: `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#VERSION_1:kotlin.Int` (legacy event-based capture using `https://developer.android.com/reference/kotlin/android/view/ViewStructure.html#`) and `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#VERSION_2:kotlin.Int` (leaner, buffer-backed capture focused on text and bounding boxes).

The returned version is decided by the system intelligence service that coordinates this ContentCaptureSession.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the enabled version, either `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#VERSION_1:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#VERSION_2:kotlin.Int`. Calls to Version 1 methods become no-ops if the returned version is not `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#VERSION_1:kotlin.Int`, and calls to Version 2 methods become no-ops if the returned version is not `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#VERSION_2:kotlin.Int`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#VERSION_1:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#VERSION_2:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#VERSION_1:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#VERSION_2:kotlin.Int`

### newAutofillId

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun newAutofillId(
    hostId: AutofillId, 
    virtualChildId: Long
): AutofillId
```

Creates a new `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillId.html#` for a virtual child, so it can be used to uniquely identify the children in the session.

| Parameters ||
|---|---|
| `hostId` | [AutofillId](../android/view/autofill/AutofillId.md): id of the non-virtual view hosting the virtual view hierarchy (it can be obtained by calling `https://developer.android.com/reference/kotlin/android/view/ViewStructure.html#getAutofillId()`). This value cannot be `null`. |
| `virtualChildId` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): id of the virtual child, relative to the parent. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillId.html#` | if for the virtual child. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the `parentId` is a virtual child id. |

### newViewStructure

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun newViewStructure(view: View): ViewStructure
```

Creates a `https://developer.android.com/reference/kotlin/android/view/ViewStructure.html#` for a "standard" view.

This method should be called after a visible view is laid out; the view then must populate the structure and pass it to `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#notifyViewAppeared(android.view.ViewStructure)`. **Note:** views that manage a virtual structure under this view must populate just the node representing this view and return right away, then asynchronously report (not necessarily in the UI thread) when the children nodes appear, disappear or have their text changed by calling `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#notifyViewAppeared(android.view.ViewStructure)`, `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#notifyViewDisappeared(android.view.autofill.AutofillId)`, and `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#notifyViewTextChanged(android.view.autofill.AutofillId,%20kotlin.CharSequence)` respectively. The structure for the a child must be created using `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#newVirtualViewStructure(android.view.autofill.AutofillId,%20kotlin.Long)`, and the `autofillId` for a child can be obtained either through `childStructure.getAutofillId()` or `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#newAutofillId(android.view.autofill.AutofillId,%20kotlin.Long)`.

When the virtual view hierarchy represents a web page, you should also:

- Call `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureManager#getContentCaptureConditions()` to infer content capture events should be generate for that URL.
- Create a new `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#` child for every HTML element that renders a new URL (like an `IFRAME`) and use that session to notify events from that subtree.

**Note:** the following methods of the `structure` will be ignored:

- `https://developer.android.com/reference/kotlin/android/view/ViewStructure.html#setChildCount(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/view/ViewStructure.html#addChildCount(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/view/ViewStructure.html#getChildCount()`
- `https://developer.android.com/reference/kotlin/android/view/ViewStructure.html#newChild(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/view/ViewStructure.html#asyncNewChild(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/view/ViewStructure.html#asyncCommit()`
- `https://developer.android.com/reference/kotlin/android/view/ViewStructure.html#setWebDomain(kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/view/ViewStructure.html#newHtmlInfoBuilder(kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/view/ViewStructure.html#setHtmlInfo(android.view.ViewStructure.HtmlInfo)`
- `https://developer.android.com/reference/kotlin/android/view/ViewStructure.html#setDataIsSensitive(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/view/ViewStructure.html#setAlpha(kotlin.Float)`
- `https://developer.android.com/reference/kotlin/android/view/ViewStructure.html#setElevation(kotlin.Float)`
- `https://developer.android.com/reference/kotlin/android/view/ViewStructure.html#setTransformation(android.graphics.Matrix)`

Note: This function belongs to Content Capture Version 1.

| Parameters ||
|---|---|
| `view` | [View](../android/view/View.md): This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/ViewStructure.html#` | This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#getContentCaptureVersion()`

### newVirtualViewStructure

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun newVirtualViewStructure(
    parentId: AutofillId, 
    virtualId: Long
): ViewStructure
```

Creates a `https://developer.android.com/reference/kotlin/android/view/ViewStructure.html#` for a "virtual" view, so it can be passed to `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#notifyViewAppeared(android.view.ViewStructure)` by the view managing the virtual view hierarchy.

Note: This function belongs to Content Capture Version 1.

| Parameters ||
|---|---|
| `parentId` | [AutofillId](../android/view/autofill/AutofillId.md): id of the virtual view parent (it can be obtained by calling `https://developer.android.com/reference/kotlin/android/view/ViewStructure.html#getAutofillId()` on the parent). This value cannot be `null`. |
| `virtualId` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): id of the virtual child, relative to the parent. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/ViewStructure.html#` | a new `https://developer.android.com/reference/kotlin/android/view/ViewStructure.html#` that can be used for Content Capture purposes. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#getContentCaptureVersion()`
- `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#getContentCaptureVersion()`

### notifyContentInteractionEvent

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun notifyContentInteractionEvent(autofillId: AutofillId): Unit
```

Notifies the Intelligence Service that a view has been interacted.

The view must have appeared before sending the interaction event.

| Parameters ||
|---|---|
| `autofillId` | [AutofillId](../android/view/autofill/AutofillId.md): id of the node. This value cannot be `null`. |

### notifyNodeAppearedOrChanged

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun notifyNodeAppearedOrChanged(
    id: AutofillId, 
    properties: ContentCaptureNodeProperties?
): Unit
```

Creates a new node or updates an existing one according to the changes in properties.

This is the primary method to construct and report the UI hierarchy in Content Capture Version 2. It unifies the reporting of both standard `https://developer.android.com/reference/kotlin/android/view/View.html#` and virtual views (e.g., inside a Webview) into a single, cohesive API. Call this method when a node is attached, laid out, and ready to be drawn in the active UI hierarchy, or when its properties (like text or bounds) change.

For standard views, the `id` can be obtained via `https://developer.android.com/reference/kotlin/android/view/View.html#getAutofillId()`. For virtual views, the `id` must be created using `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#newAutofillId(android.view.autofill.AutofillId,%20kotlin.Long)`.

To minimize memory allocations, applications should reuse a single `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureNodeProperties` instance, calling `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureNodeProperties#clear()` before populating it for a new node.

If the node already exists, only the properties explicitly set in the `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureNodeProperties` payload will be updated. The parent-child relationship is modified based on the parent ID configuration:

- **Setting parent ID to `null`:** Guarantees that this node is treated as a root node with no parent.
- **Not setting parent ID at all:** Leaves the existing parent unchanged. If the node is appearing for the first time, it defaults to a root node.

<br />

Note: This function belongs to Content Capture Version 2.
. 
This method must be called on the thread that originally created this UI element. This is typically the [main thread](../android/os/Looper.md)) of your app.

| Parameters ||
|---|---|
| `id` | [AutofillId](../android/view/autofill/AutofillId.md): The `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillId.html#` of the node. This value cannot be `null`. |
| `properties` | [ContentCaptureNodeProperties](../android/view/contentcapture/ContentCaptureNodeProperties.md)?: The `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureNodeProperties` holding the attributes for this node. This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#getContentCaptureVersion()`
- `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureNodeProperties`
- `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#notifyNodeDisappeared(android.view.autofill.AutofillId)`

### notifyNodeDisappeared

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun notifyNodeDisappeared(id: AutofillId): Unit
```

Removes a node from the active content capture hierarchy.

This is the primary method to report the removal of UI components in Content Capture Version 2. It applies to both standard `https://developer.android.com/reference/kotlin/android/view/View.html#` and virtual views, signaling that the node is no longer part of the visible hierarchy.

When a node is deleted:

- Its internal resources (such as text and content description allocations) are freed.
- Its children are **orphaned** and promoted to root nodes (their parent pointer is cleared). If you want to remove an entire subtree, you must recursively call this method for all descendant nodes in the subtree. Re-adding this node will not automatically relink previous children.

<br />

Note; This function belongs to Content Capture Version 2.
. 
This method must be called on the thread that originally created this UI element. This is typically the [main thread](../android/os/Looper.md)) of your app.

| Parameters ||
|---|---|
| `id` | [AutofillId](../android/view/autofill/AutofillId.md): The `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillId.html#` of the node to delete. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#getContentCaptureVersion()`
- `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#notifyNodeAppearedOrChanged(android.view.autofill.AutofillId,%20android.view.contentcapture.ContentCaptureNodeProperties)`

### notifySessionPaused

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun notifySessionPaused(): Unit
```

Notifies the Content Capture Service that a session has paused.

### notifySessionResumed

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun notifySessionResumed(): Unit
```

Notifies the Content Capture Service that a session has resumed.

### notifyViewAppeared

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun notifyViewAppeared(node: ViewStructure): Unit
```

Notifies the Content Capture Service that a node has been added to the view structure.

Typically called "manually" by views that handle their own virtual view hierarchy, or automatically by the Android System for views that return `true` on `https://developer.android.com/reference/kotlin/android/view/View.html#onProvideContentCaptureStructure(android.view.ViewStructure,%20kotlin.Int)`.

Consider use `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#notifyViewsAppeared(kotlin.collections.MutableList)` which has a better performance when notifying a list of nodes has appeared.

Note; This function belongs to Content Capture Version 1.

| Parameters ||
|---|---|
| `node` | [ViewStructure](../android/view/ViewStructure.md): node that has been added. This value cannot be `null`. |

### notifyViewDisappeared

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun notifyViewDisappeared(id: AutofillId): Unit
```

Notifies the Content Capture Service that a node has been removed from the view structure.

Typically called "manually" by views that handle their own virtual view hierarchy, or automatically by the Android System for standard views.

Consider use `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#notifyViewsDisappeared(android.view.autofill.AutofillId,%20kotlin.LongArray)` which has a better performance when notifying a list of nodes has disappeared.

Note; This function belongs to Content Capture Version 1.

| Parameters ||
|---|---|
| `id` | [AutofillId](../android/view/autofill/AutofillId.md): id of the node that has been removed. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#getContentCaptureVersion()`

### notifyViewInsetsChanged

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun notifyViewInsetsChanged(viewInsets: Insets): Unit
```

Notifies the Intelligence Service that the insets of a view have changed.

| Parameters ||
|---|---|
| `viewInsets` | [Insets](../android/graphics/Insets.md): This value cannot be `null`. |

### notifyViewTextChanged

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun notifyViewTextChanged(
    id: AutofillId, 
    text: CharSequence?
): Unit
```

Notifies the Intelligence Service that the value of a text node has been changed.

Note; This function belongs to Content Capture Version 1.

| Parameters ||
|---|---|
| `id` | [AutofillId](../android/view/autofill/AutofillId.md): of the node. This value cannot be `null`. |
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?: new text. This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#getContentCaptureVersion()`
- `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#getContentCaptureVersion()`

### notifyViewsAppeared

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun notifyViewsAppeared(appearedNodes: MutableList<ViewStructure!>): Unit
```

Notifies the Content Capture Service that a list of nodes has appeared in the view structure.

Typically called manually by views that handle their own virtual view hierarchy.

Note; This function belongs to Content Capture Version 1.

| Parameters ||
|---|---|
| `appearedNodes` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ViewStructure](../android/view/ViewStructure.md)!\>: nodes that have appeared. Each element represents a view node that has been added to the view structure. The order of the elements is important, which should be preserved as the attached order of when the node is attached to the virtual view hierarchy. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#getContentCaptureVersion()`

### notifyViewsDisappeared

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun notifyViewsDisappeared(
    hostId: AutofillId, 
    virtualIds: LongArray
): Unit
```

Notifies the Content Capture Service that many nodes has been removed from a virtual view structure.

Should only be called by views that handle their own virtual view hierarchy.

After UPSIDE_DOWN_CAKE, this method wraps the virtual children with a pair of view tree appearing and view tree appeared events.

Note; This function belongs to Content Capture Version 1.

| Parameters ||
|---|---|
| `hostId` | [AutofillId](../android/view/autofill/AutofillId.md): id of the non-virtual view hosting the virtual view hierarchy (it can be obtained by calling `https://developer.android.com/reference/kotlin/android/view/ViewStructure.html#getAutofillId()`). This value cannot be `null`. |
| `virtualIds` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html): ids of the virtual children. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `virtualIds` is empty |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#getContentCaptureVersion()`

### setContentCaptureContext

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setContentCaptureContext(context: ContentCaptureContext?): Unit
```

Sets the `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureContext` associated with the session.

Typically used to change the context associated with the default session from an activity.

| Parameters ||
|---|---|
| `context` | [ContentCaptureContext](../android/view/contentcapture/ContentCaptureContext.md)?: This value may be `null`. |

### toString

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |
