# AccessibilityNodeProvider

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AccessibilityNodeProvider

Kotlin| [Java](https://developer.android.com/reference/android/view/accessibility/AccessibilityNodeProvider "View this page in Java") 

```
abstract class AccessibilityNodeProvider
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.view.accessibility.AccessibilityNodeProvider](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeProvider#) |

This class is the contract a client should implement to enable support of a virtual view hierarchy rooted at a given view for accessibility purposes. A virtual view hierarchy is a tree of imaginary Views that is reported as a part of the view hierarchy when an [AccessibilityService](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#) explores the window content. Since the virtual View tree does not exist this class is responsible for managing the [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo) s describing that tree to accessibility services.

<br />

The main use case of these APIs is to enable a custom view that draws complex content, for example a monthly calendar grid, to be presented as a tree of logical nodes, for example month days each containing events, thus conveying its logical structure.

<br />

A typical use case is to override [View.getAccessibilityNodeProvider()](https://developer.android.com/reference/kotlin/android/view/View.html#getAccessibilityNodeProvider())of the View that is a root of a virtual View hierarchy to return an instance of this class. In such a case this instance is responsible for managing [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo) s describing the virtual sub-tree rooted at the View including the one representing the View itself. Similarly the returned instance is responsible for performing accessibility actions on any virtual view or the root view itself. For example:
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
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HOST_VIEW_ID](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeProvider#HOST_VIEW_ID:kotlin.Int) The virtual id for the hosting View. |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AccessibilityNodeProvider](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeProvider#AccessibilityNodeProvider())`()` <br /> |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addExtraDataToAccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeProvider#addExtraDataToAccessibilityNodeInfo(kotlin.Int,%20android.view.accessibility.AccessibilityNodeInfo,%20kotlin.String,%20android.os.Bundle))`(`virtualViewId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `info:` ` [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo)!`, `extraDataKey:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `arguments:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` Adds extra data to an [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo) based on an explicit request for the additional data. |
| open [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo)? | [createAccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeProvider#createAccessibilityNodeInfo(kotlin.Int))`(`virtualViewId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns an [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo) representing a virtual view, such as a descendant of the host View, with the given`virtualViewId`or the host View itself if`virtualViewId`equals to [HOST_VIEW_ID](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeProvider#HOST_VIEW_ID:kotlin.Int). |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo)!\>? | [findAccessibilityNodeInfosByText](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeProvider#findAccessibilityNodeInfosByText(kotlin.String,%20kotlin.Int))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `virtualViewId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Finds [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo) s by text. |
| open [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo)? | [findFocus](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeProvider#findFocus(kotlin.Int))`(`focus:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Find the virtual view, such as a descendant of the host View, that has the specified focus type. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [performAction](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeProvider#performAction(kotlin.Int,%20kotlin.Int,%20android.os.Bundle))`(`virtualViewId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `action:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `arguments:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`)` Performs an accessibility action on a virtual view, such as a descendant of the host View, with the given`virtualViewId`or the host View itself if`virtualViewId`equals to [HOST_VIEW_ID](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeProvider#HOST_VIEW_ID:kotlin.Int). |

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

Adds extra data to an [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo) based on an explicit request for the additional data.

This method only needs to be implemented if a virtual view offers to provide additional data.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `virtualViewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The virtual view id used to create the node |
| `info` | [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo)!:The info to which to add the extra data |
| `extraDataKey` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A key specifying the type of extra data to add to the info. The extra data should be added to the [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) returned by the info's [AccessibilityNodeInfo.getExtras](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getExtras())method. |
| `arguments` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!:A [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) holding any arguments relevant for this request. |

**See Also**

- [android.view.accessibility.AccessibilityNodeInfo#setAvailableExtraData(List)](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setAvailableExtraData(kotlin.collections.MutableList)) 

### createAccessibilityNodeInfo

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun createAccessibilityNodeInfo(virtualViewId: Int): AccessibilityNodeInfo?
```

Returns an [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo) representing a virtual view, such as a descendant of the host View, with the given`virtualViewId`or the host View itself if`virtualViewId`equals to [HOST_VIEW_ID](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeProvider#HOST_VIEW_ID:kotlin.Int).

A virtual descendant is an imaginary View that is reported as a part of the view hierarchy for accessibility purposes. This enables custom views that draw complex content to report them selves as a tree of virtual views, thus conveying their logical structure.

The implementer is responsible for obtaining an accessibility node info from the pool of reusable instances and setting the desired properties of the node info before returning it.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------|
| `virtualViewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A client defined virtual view id. |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo)? | A populated [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo) for a virtual descendant or the host View. This value may be`null`. |

**See Also**

- [android.view.View#createAccessibilityNodeInfo()](https://developer.android.com/reference/kotlin/android/view/View.html#createAccessibilityNodeInfo())
- [android.view.accessibility.AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo) 

### findAccessibilityNodeInfosByText

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun findAccessibilityNodeInfosByText(
    text: String!, 
    virtualViewId: Int
): MutableList<AccessibilityNodeInfo!>?
```

Finds [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo) s by text. The match is case insensitive containment. The search is relative to the virtual view, i.e. a descendant of the host View, with the given`virtualViewId`or the host View itself`virtualViewId`equals to [HOST_VIEW_ID](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeProvider#HOST_VIEW_ID:kotlin.Int).

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `virtualViewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A client defined virtual view id which defined the root of the tree in which to perform the search. |
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The searched text. |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo)!>? | A list of node info. This value may be`null`. |

**See Also**

- [#createAccessibilityNodeInfo(int)](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeProvider#createAccessibilityNodeInfo(kotlin.Int))
- [android.view.accessibility.AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo) 

### findFocus

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun findFocus(focus: Int): AccessibilityNodeInfo?
```

Find the virtual view, such as a descendant of the host View, that has the specified focus type.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `focus` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The focus to find. One of [AccessibilityNodeInfo.FOCUS_INPUT](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FOCUS_INPUT:kotlin.Int) or [AccessibilityNodeInfo.FOCUS_ACCESSIBILITY](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FOCUS_ACCESSIBILITY:kotlin.Int). |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo)? | The node info of the focused view or null. |

**See Also**

- [android.view.accessibility.AccessibilityNodeInfo#FOCUS_INPUT](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FOCUS_INPUT:kotlin.Int)
- [android.view.accessibility.AccessibilityNodeInfo#FOCUS_ACCESSIBILITY](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FOCUS_ACCESSIBILITY:kotlin.Int) 

### performAction

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun performAction(
    virtualViewId: Int, 
    action: Int, 
    arguments: Bundle?
): Boolean
```

Performs an accessibility action on a virtual view, such as a descendant of the host View, with the given`virtualViewId`or the host View itself if`virtualViewId`equals to [HOST_VIEW_ID](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeProvider#HOST_VIEW_ID:kotlin.Int).

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `virtualViewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A client defined virtual view id. |
| `action` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The action to perform. |
| `arguments` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:Optional action arguments. This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the action was performed. |

**See Also**

- [android.view.View#performAccessibilityAction(int, Bundle)](https://developer.android.com/reference/kotlin/android/view/View.html#performAccessibilityAction(kotlin.Int,%20android.os.Bundle))
- [#createAccessibilityNodeInfo(int)](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeProvider#createAccessibilityNodeInfo(kotlin.Int))
- [android.view.accessibility.AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo)
