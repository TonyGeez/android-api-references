# Scene

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Scene

Kotlin| [Java](../android/transition/Scene.md) 
| --- | --- |

```
class Scene
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.transition.Scene](../android/transition/Scene.md) |

A scene represents the collection of values that various properties in the View hierarchy will have when the scene is applied. A Scene can be configured to automatically run a Transition when it is applied, which will animate the various property changes that take place during the scene change.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Scene](../android/transition/Scene.md))`(`sceneRoot:` ` [ViewGroup](../android/view/ViewGroup.md)!`)` Constructs a Scene with no information about how values will change when this scene is applied. |
| [Scene](../android/transition/Scene.md))`(`sceneRoot:` ` [ViewGroup](../android/view/ViewGroup.md)!`, `layout:` ` [View](../android/view/View.md)!`)` Constructs a Scene which, when entered, will remove any children from the sceneRoot container and add the layout object as a new child of that container. |
| [Scene](../android/transition/Scene.md))`(`sceneRoot:` ` [ViewGroup](../android/view/ViewGroup.md)!`, `layout:` ` [ViewGroup](../android/view/ViewGroup.md)!`)` <br /> |

| Public methods ||
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [enter](../android/transition/Scene.md))`()` Enters this scene, which entails changing all values that are specified by this scene. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [exit](../android/transition/Scene.md))`()` Exits this scene, if it is the current scene on the scene's [scene root](../android/transition/Scene.md)). |
| static [Scene](../android/transition/Scene.md)? | [getCurrentScene](../android/transition/Scene.md))`(`sceneRoot:` ` [ViewGroup](../android/view/ViewGroup.md)`)` Gets the current [Scene](../android/transition/Scene.md) set on the given ViewGroup. |
| --- | --- |
| static [Scene](../android/transition/Scene.md)! | [getSceneForLayout](../android/transition/Scene.md))`(`sceneRoot:` ` [ViewGroup](../android/view/ViewGroup.md)!`, `layoutId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `context:` ` [Context](../android/content/Context.md)!`)` Returns a Scene described by the resource file associated with the given`layoutId`parameter. |
| [ViewGroup](../android/view/ViewGroup.md)! | [getSceneRoot](../android/transition/Scene.md))`()` Gets the root of the scene, which is the root of the view hierarchy affected by changes due to this scene, and which will be animated when this scene is entered. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEnterAction](../android/transition/Scene.md))`(`action:` ` [Runnable](../java/lang/Runnable.md)!`)` Scenes that are not defined with layout resources or hierarchies, or which need to perform additional steps after those hierarchies are changed to, should set an enter action, and possibly an exit action as well. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setExitAction](../android/transition/Scene.md))`(`action:` ` [Runnable](../java/lang/Runnable.md)!`)` Scenes that are not defined with layout resources or hierarchies, or which need to perform additional steps after those hierarchies are changed to, should set an enter action, and possibly an exit action as well. |

## Public constructors

### Scene

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Scene(sceneRoot: ViewGroup!)
```

Constructs a Scene with no information about how values will change when this scene is applied. This constructor might be used when a Scene is created with the intention of being dynamically configured, through setting [setEnterAction(java.lang.Runnable)](../android/transition/Scene.md))and possibly [setExitAction(java.lang.Runnable)](../android/transition/Scene.md)).

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sceneRoot` | [ViewGroup](../android/view/ViewGroup.md)!:The root of the hierarchy in which scene changes and transitions will take place. |

### Scene

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Scene(
    sceneRoot: ViewGroup!, 
    layout: View!)
```

Constructs a Scene which, when entered, will remove any children from the sceneRoot container and add the layout object as a new child of that container.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sceneRoot` | [ViewGroup](../android/view/ViewGroup.md)!:The root of the hierarchy in which scene changes and transitions will take place. |
| `layout` | [View](../android/view/View.md)!:The view hierarchy of this scene, added as a child of sceneRoot when this scene is entered. |

### Scene

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Scene(
    sceneRoot: ViewGroup!, 
    layout: ViewGroup!)
```

**Deprecated:** *use [Scene(android.view.ViewGroup,android.view.View)](../android/transition/Scene.md)).*

## Public methods

### enter

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun enter(): Unit
```

Enters this scene, which entails changing all values that are specified by this scene. These may be values associated with a layout view group or layout resource file which will now be added to the scene root, or it may be values changed by an [setEnterAction(java.lang.Runnable)](../android/transition/Scene.md))enter action}, or a combination of the these. No transition will be run when the scene is entered. To get transition behavior in scene changes, use one of the methods in [TransitionManager](../android/transition/TransitionManager.md) instead. 

### exit

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun exit(): Unit
```

Exits this scene, if it is the current scene on the scene's [scene root](../android/transition/Scene.md)). The current scene is set when [entering](../android/transition/Scene.md))a scene. Exiting a scene runs the [exit action](../android/transition/Scene.md))if there is one. 

### getCurrentScene

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getCurrentScene(sceneRoot: ViewGroup): Scene?
```

Gets the current [Scene](../android/transition/Scene.md) set on the given ViewGroup. A scene is set on a ViewGroup only if that ViewGroup is the scene root.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sceneRoot` | [ViewGroup](../android/view/ViewGroup.md):The ViewGroup on which the current scene will be returned This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Scene](../android/transition/Scene.md)? | The current Scene set on this ViewGroup. A value of null indicates that no Scene is currently set. |

### getSceneForLayout

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getSceneForLayout(
    sceneRoot: ViewGroup!, 
    layoutId: Int, 
    context: Context!
): Scene!
```

Returns a Scene described by the resource file associated with the given`layoutId`parameter. If such a Scene has already been created for the given`sceneRoot`, that same Scene will be returned. This caching of layoutId-based scenes enables sharing of common scenes between those created in code and those referenced by [TransitionManager](../android/transition/TransitionManager.md) XML resource files.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sceneRoot` | [ViewGroup](../android/view/ViewGroup.md)!:The root of the hierarchy in which scene changes and transitions will take place. |
| `layoutId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The id of a standard layout resource file. |
| `context` | [Context](../android/content/Context.md)!:The context used in the process of inflating the layout resource. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------|
| [Scene](../android/transition/Scene.md)! | The scene for the given root and layout id |

### getSceneRoot

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSceneRoot(): ViewGroup!
```

Gets the root of the scene, which is the root of the view hierarchy affected by changes due to this scene, and which will be animated when this scene is entered.

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [ViewGroup](../android/view/ViewGroup.md)! | The root of the view hierarchy affected by this scene. |

### setEnterAction

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setEnterAction(action: Runnable!): Unit
```

Scenes that are not defined with layout resources or hierarchies, or which need to perform additional steps after those hierarchies are changed to, should set an enter action, and possibly an exit action as well. An enter action will cause Scene to call back into application code to do anything else the application needs after transitions have captured pre-change values and after any other scene changes have been applied, such as the layout (if any) being added to the view hierarchy. After this method is called, Transitions will be played.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [Runnable](../java/lang/Runnable.md)!:The runnable whose [run()](../java/lang/Runnable.md))method will be called when this scene is entered |

**See Also**

- [#setExitAction(Runnable)](../android/transition/Scene.md))
- [android.transition.Scene#Scene(ViewGroup, View)](../android/transition/Scene.md)) 

### setExitAction

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setExitAction(action: Runnable!): Unit
```

Scenes that are not defined with layout resources or hierarchies, or which need to perform additional steps after those hierarchies are changed to, should set an enter action, and possibly an exit action as well. An exit action will cause Scene to call back into application code to do anything the application needs to do after applicable transitions have captured pre-change values, but before any other scene changes have been applied, such as the new layout (if any) being added to the view hierarchy. After this method is called, the next scene will be entered, including a call to [setEnterAction(java.lang.Runnable)](../android/transition/Scene.md))if an enter action is set. 
**See Also**

- [#setEnterAction(Runnable)](../android/transition/Scene.md))
- [android.transition.Scene#Scene(ViewGroup, View)](../android/transition/Scene.md))
