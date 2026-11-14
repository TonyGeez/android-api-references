# AccessibilityNodeProvider

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AccessibilityNodeProvider

Kotlin| [Java](AccessibilityNodeProvider.md) 
| --- | --- |

```
abstract class AccessibilityNodeProvider
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.accessibility.AccessibilityNodeProvider](AccessibilityNodeProvider.md) |

This class is the contract a client should implement to enable support of a virtual view hierarchy rooted at a given view for accessibility purposes. A virtual view hierarchy is a tree of imaginary Views that is reported as a part of the view hierarchy when an [AccessibilityService](../android.accessibilityservice/AccessibilityService.md) explores the window content. Since the virtual View tree does not exist this class is responsible for managing the [AccessibilityNodeInfo](AccessibilityNodeInfo.md) s describing that tree to accessibility services.

<br />

The main use case of these APIs is to enable a custom view that draws complex content, for example a monthly calendar grid, to be presented as a tree of logical nodes, for example month days each containing events, thus conveying its logical structure.

<br />

A typical use case is to override [View.getAccessibilityNodeProvider()](../android.view/View.md))of the View that is a root of a virtual View hierarchy to return an instance of this class. In such a case this instance is responsible for managing [AccessibilityNodeInfo](AccessibilityNodeInfo.md) s describing the virtual sub-tree rooted at the View including the one representing the View itself. Similarly the returned instance is responsible for performing accessibility actions on any virtual view or the root view itself. For example:
**Note:** Consider using a androidx.customview.widget.ExploreByTouchHelper, a utility extension of AccessibilityNodeProvider, to simplify many aspects of providing information to accessibility services and managing accessibility focus.

<br />

<br />

### Kotlin

```kotlin
// "view" is the View instance on which this class performs accessibility functions.
  class MyCalendarViewAccessibilityDelegate(
        private var view: MyCalendarView) : AccessibilityDelegate() {
      override fun getAccessibilityNodeProvider(host: View): AccessibilityNodeProvider {
          return object : AccessibilityNodeProvider() {
              override fun createAccessibilityNodeInfo(virtualViewId: Int):
                      AccessibilityNodeInfo? {
                  when (virtualViewId) {
                      <var>host-view-id</var>-> {
                          val node = AccessibilityNodeInfo.obtain(view)
                          node.addChild(view, <var>child-view-id</var>)
                          // Set other attributes like screenReaderFocusable
                          // and contentDescription.
                          return node
                      }
                      <var>child-view-id</var>-> {
                          val node = AccessibilityNodeInfo
                                  .obtain(view, virtualViewId)
                          node.setParent(view)
                          node.addAction(ACTION_SCROLL_UP)
                          node.addAction(ACTION_SCROLL_DOWN)
                          // Set other attributes like focusable and visibleToUser.
                          node.setBoundsInScreen(
                                  Rect(<var>coords-of-edges-relative-to-screen</var>))
                          return node
                      }
                      else -> return null
                  }
              }
 
              override fun performAction(
                  virtualViewId: Int,
                  action: Int,
                  arguments: Bundle
              ): Boolean {
                  if (virtualViewId == <var>host-view-id</var>) {
                      return view.performAccessibilityAction(action, arguments)
                  }
                  when (action) {
                      ACTION_SCROLL_UP.id -> {
                          // Implement logic in a separate method.
                          navigateToPreviousMonth()
 
                          return true
                      }
                      ACTION_SCROLL_DOWN.id ->
                          // Implement logic in a separate method.
                          navigateToNextMonth()
 
                          return true
                      else -> return false
                  }
              }
          }
      }
  }
  
```

### Java

```kotlin
final class MyCalendarViewAccessibilityDelegate extends AccessibilityDelegate {
      // The View instance on which this class performs accessibility functions.
      private final MyCalendarView view;
 
      MyCalendarViewAccessibilityDelegate(MyCalendarView view) {
          this.view = view;
      }
 
      @Override
      public AccessibilityNodeProvider getAccessibilityNodeProvider(View host) {
          return new AccessibilityNodeProvider() {
              @Override
              @Nullable
              public AccessibilityNodeInfo createAccessibilityNodeInfo(int virtualViewId) {
                  if (virtualViewId == <var>host-view-id</var>) {
                      AccessibilityNodeInfo node = AccessibilityNodeInfo.obtain(view);
                      node.addChild(view, <var>child-view-id</var>);
                      // Set other attributes like screenReaderFocusable and contentDescription.
                      return node;
                  } else if (virtualViewId == <var>child-view-id</var>) {
                      AccessibilityNodeInfo node =
                          AccessibilityNodeInfo.obtain(view, virtualViewId);
                      node.setParent(view);
                      node.addAction(ACTION_SCROLL_UP);
                      node.addAction(ACTION_SCROLL_DOWN);
                      // Set other attributes like focusable and visibleToUser.
                      node.setBoundsInScreen(
                          new Rect(<var>coordinates-of-edges-relative-to-screen</var>));
                      return node;
                  } else {
                      return null;
                  }
              }
 
              @Override
              public boolean performAction(int virtualViewId, int action, Bundle arguments) {
                  if (virtualViewId == <var>host-view-id</var>) {
                      return view.performAccessibilityAction(action, arguments);
                  }
 
                  if (action == ACTION_SCROLL_UP.getId()) {
                      // Implement logic in a separate method.
                      navigateToPreviousMonth();
 
                      return true;
                  } else if (action == ACTION_SCROLL_DOWN.getId()) {
                      // Implement logic in a separate method.
                      navigateToNextMonth();
 
                      return true;
                  } else {
                      return false;
                  }
              }
          };
      }
  }
  
```

<br />

<br />

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HOST_VIEW_ID](AccessibilityNodeProvider.md) The virtual id for the hosting View. |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AccessibilityNodeProvider](AccessibilityNodeProvider.md))`()` <br /> |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addExtraDataToAccessibilityNodeInfo](AccessibilityNodeProvider.md))`(`virtualViewId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `info:` ` [AccessibilityNodeInfo](AccessibilityNodeInfo.md)!`, `extraDataKey:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `arguments:` ` [Bundle](../android.os/Bundle.md)!`)` Adds extra data to an [AccessibilityNodeInfo](AccessibilityNodeInfo.md) based on an explicit request for the additional data. |
| open [AccessibilityNodeInfo](AccessibilityNodeInfo.md)? | [createAccessibilityNodeInfo](AccessibilityNodeProvider.md))`(`virtualViewId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns an [AccessibilityNodeInfo](AccessibilityNodeInfo.md) representing a virtual view, such as a descendant of the host View, with the given`virtualViewId`or the host View itself if`virtualViewId`equals to [HOST_VIEW_ID](AccessibilityNodeProvider.md). |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AccessibilityNodeInfo](AccessibilityNodeInfo.md)!\>? | [findAccessibilityNodeInfosByText](AccessibilityNodeProvider.md))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `virtualViewId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Finds [AccessibilityNodeInfo](AccessibilityNodeInfo.md) s by text. |
| --- | --- |
| open [AccessibilityNodeInfo](AccessibilityNodeInfo.md)? | [findFocus](AccessibilityNodeProvider.md))`(`focus:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Find the virtual view, such as a descendant of the host View, that has the specified focus type. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [performAction](AccessibilityNodeProvider.md))`(`virtualViewId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `action:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `arguments:` ` [Bundle](../android.os/Bundle.md)?`)` Performs an accessibility action on a virtual view, such as a descendant of the host View, with the given`virtualViewId`or the host View itself if`virtualViewId`equals to [HOST_VIEW_ID](AccessibilityNodeProvider.md). |

## Constants

### HOST_VIEW_ID

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HOST_VIEW_ID: Int
```

The virtual id for the hosting View. 

 Value: -1

## Public constructors

### AccessibilityNodeProvider

```
AccessibilityNodeProvider()
```

## Public methods

### addExtraDataToAccessibilityNodeInfo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addExtraDataToAccessibilityNodeInfo(
    virtualViewId: Int, 
    info: AccessibilityNodeInfo!, 
    extraDataKey: String!, 
    arguments: Bundle!
): Unit
```

Adds extra data to an [AccessibilityNodeInfo](AccessibilityNodeInfo.md) based on an explicit request for the additional data.

This method only needs to be implemented if a virtual view offers to provide additional data.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `virtualViewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The virtual view id used to create the node |
| `info` | [AccessibilityNodeInfo](AccessibilityNodeInfo.md)!:The info to which to add the extra data |
| `extraDataKey` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A key specifying the type of extra data to add to the info. The extra data should be added to the [Bundle](../android.os/Bundle.md) returned by the info's [AccessibilityNodeInfo.getExtras](AccessibilityNodeInfo.md))method. |
| --- | --- |
| `arguments` | [Bundle](../android.os/Bundle.md)!:A [Bundle](../android.os/Bundle.md) holding any arguments relevant for this request. |

**See Also**

- [android.view.accessibility.AccessibilityNodeInfo#setAvailableExtraData(List)](AccessibilityNodeInfo.md)) 

### createAccessibilityNodeInfo

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun createAccessibilityNodeInfo(virtualViewId: Int): AccessibilityNodeInfo?
```

Returns an [AccessibilityNodeInfo](AccessibilityNodeInfo.md) representing a virtual view, such as a descendant of the host View, with the given`virtualViewId`or the host View itself if`virtualViewId`equals to [HOST_VIEW_ID](AccessibilityNodeProvider.md).

A virtual descendant is an imaginary View that is reported as a part of the view hierarchy for accessibility purposes. This enables custom views that draw complex content to report them selves as a tree of virtual views, thus conveying their logical structure.

The implementer is responsible for obtaining an accessibility node info from the pool of reusable instances and setting the desired properties of the node info before returning it.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------|
| `virtualViewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A client defined virtual view id. |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AccessibilityNodeInfo](AccessibilityNodeInfo.md)? | A populated [AccessibilityNodeInfo](AccessibilityNodeInfo.md) for a virtual descendant or the host View. This value may be`null`. |

**See Also**

- [android.view.View#createAccessibilityNodeInfo()](../android.view/View.md))
- [android.view.accessibility.AccessibilityNodeInfo](AccessibilityNodeInfo.md) 

### findAccessibilityNodeInfosByText

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun findAccessibilityNodeInfosByText(
    text: String!, 
    virtualViewId: Int
): MutableList<AccessibilityNodeInfo!>?
```

Finds [AccessibilityNodeInfo](AccessibilityNodeInfo.md) s by text. The match is case insensitive containment. The search is relative to the virtual view, i.e. a descendant of the host View, with the given`virtualViewId`or the host View itself`virtualViewId`equals to [HOST_VIEW_ID](AccessibilityNodeProvider.md).

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `virtualViewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A client defined virtual view id which defined the root of the tree in which to perform the search. |
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The searched text. |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [AccessibilityNodeInfo](AccessibilityNodeInfo.md)!>? | A list of node info. This value may be`null`. |

**See Also**

- [#createAccessibilityNodeInfo(int)](AccessibilityNodeProvider.md))
- [android.view.accessibility.AccessibilityNodeInfo](AccessibilityNodeInfo.md) 

### findFocus

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun findFocus(focus: Int): AccessibilityNodeInfo?
```

Find the virtual view, such as a descendant of the host View, that has the specified focus type.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `focus` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The focus to find. One of [AccessibilityNodeInfo.FOCUS_INPUT](AccessibilityNodeInfo.md) or [AccessibilityNodeInfo.FOCUS_ACCESSIBILITY](AccessibilityNodeInfo.md). |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| [AccessibilityNodeInfo](AccessibilityNodeInfo.md)? | The node info of the focused view or null. |

**See Also**

- [android.view.accessibility.AccessibilityNodeInfo#FOCUS_INPUT](AccessibilityNodeInfo.md)
- [android.view.accessibility.AccessibilityNodeInfo#FOCUS_ACCESSIBILITY](AccessibilityNodeInfo.md) 

### performAction

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun performAction(
    virtualViewId: Int, 
    action: Int, 
    arguments: Bundle?
): Boolean
```

Performs an accessibility action on a virtual view, such as a descendant of the host View, with the given`virtualViewId`or the host View itself if`virtualViewId`equals to [HOST_VIEW_ID](AccessibilityNodeProvider.md).

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `virtualViewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A client defined virtual view id. |
| `action` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The action to perform. |
| `arguments` | [Bundle](../android.os/Bundle.md)?:Optional action arguments. This value may be`null`. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the action was performed. |

**See Also**

- [android.view.View#performAccessibilityAction(int, Bundle)](../android.view/View.md))
- [#createAccessibilityNodeInfo(int)](AccessibilityNodeProvider.md))
- [android.view.accessibility.AccessibilityNodeInfo](AccessibilityNodeInfo.md)
