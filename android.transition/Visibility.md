# Visibility

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Visibility

Kotlin| [Java](Visibility.md) 
| --- | --- |

```
abstract class Visibility : Transition
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.transition.Transition](Transition.md) ||
| | ↳ | [android.transition.Visibility](Visibility.md) |

| Known Direct Subclasses [Explode](Explode.md), [Fade](Fade.md), [Slide](Slide.md) |--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Explode](Explode.md) | This transition tracks changes to the visibility of target views in the start and end scenes and moves views in or out from the edges of the scene. | | [Fade](Fade.md) | This transition tracks changes to the visibility of target views in the start and end scenes and fades views in or out when they become visible or non-visible. | | [Slide](Slide.md) | This transition tracks changes to the visibility of target views in the start and end scenes and moves views in or out from one of the edges of the scene. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

This transition tracks changes to the visibility of target views in the start and end scenes. Visibility is determined not just by the [View.setVisibility(int)](../android.view/View.md))state of views, but also whether views exist in the current view hierarchy. The class is intended to be a utility for subclasses such as [Fade](Fade.md), which use this visibility information to determine the specific animations to run when visibility changes occur. Subclasses should implement one or both of the methods [onAppear(android.view.ViewGroup,android.transition.TransitionValues,int,android.transition.TransitionValues,int)](Visibility.md)), [onDisappear(android.view.ViewGroup,android.transition.TransitionValues,int,android.transition.TransitionValues,int)](Visibility.md))or [onAppear(android.view.ViewGroup,android.view.View,android.transition.TransitionValues,android.transition.TransitionValues)](Visibility.md)), [onDisappear(android.view.ViewGroup,android.view.View,android.transition.TransitionValues,android.transition.TransitionValues)](Visibility.md)).

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_IN](Visibility.md) Mode used in [setMode(int)](Visibility.md))to make the transition operate on targets that are appearing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_OUT](Visibility.md) Mode used in [setMode(int)](Visibility.md))to make the transition operate on targets that are disappearing. |

| Inherited constants ||
|---|---|
| From class [Transition](Transition.md) |----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MATCH_ID](Transition.md) <br /> With [setMatchOrder(int...)](Transition.md)), chooses to match by [android.view.View#getId()](../android.view/View.md)). Negative IDs will not be matched. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MATCH_INSTANCE](Transition.md) <br /> With [setMatchOrder(int...)](Transition.md)), chooses to match by View instance. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MATCH_ITEM_ID](Transition.md) <br /> With [setMatchOrder(int...)](Transition.md)), chooses to match by the [android.widget.Adapter](../android.widget/Adapter.md) item id. When [android.widget.Adapter#hasStableIds()](../android.widget/Adapter.md))returns false, no match will be made for items. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MATCH_NAME](Transition.md) <br /> With [setMatchOrder(int...)](Transition.md)), chooses to match by [android.view.View#getTransitionName()](../android.view/View.md)). Null names will not be matched. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Visibility](Visibility.md))`()` <br /> |
| [Visibility](Visibility.md))`(`context:` ` [Context](../android.content/Context.md)!`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)!`)` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [captureEndValues](Visibility.md))`(`transitionValues:` ` [TransitionValues](TransitionValues.md)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [captureStartValues](Visibility.md))`(`transitionValues:` ` [TransitionValues](TransitionValues.md)!`)` <br /> |
| open [Animator](../android.animation/Animator.md)? | [createAnimator](Visibility.md))`(`sceneRoot:` ` [ViewGroup](../android.view/ViewGroup.md)`, `startValues:` ` [TransitionValues](TransitionValues.md)?`, `endValues:` ` [TransitionValues](TransitionValues.md)?`)` This method creates an animation that will be run for this transition given the information in the startValues and endValues structures captured earlier for the start and end scenes. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMode](Visibility.md))`()` Returns whether appearing and/or disappearing Views are supported. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getTransitionProperties](Visibility.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTransitionRequired](Visibility.md))`(`startValues:` ` [TransitionValues](TransitionValues.md)?`, `newValues:` ` [TransitionValues](TransitionValues.md)?`)` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isVisible](Visibility.md))`(`values:` ` [TransitionValues](TransitionValues.md)!`)` Returns whether the view is 'visible' according to the given values object. |
| open [Animator](../android.animation/Animator.md)! | [onAppear](Visibility.md))`(`sceneRoot:` ` [ViewGroup](../android.view/ViewGroup.md)!`, `startValues:` ` [TransitionValues](TransitionValues.md)!`, `startVisibility:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `endValues:` ` [TransitionValues](TransitionValues.md)!`, `endVisibility:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` The default implementation of this method calls [onAppear(android.view.ViewGroup,android.view.View,android.transition.TransitionValues,android.transition.TransitionValues)](Visibility.md)). |
| open [Animator](../android.animation/Animator.md)! | [onAppear](Visibility.md))`(`sceneRoot:` ` [ViewGroup](../android.view/ViewGroup.md)!`, `view:` ` [View](../android.view/View.md)!`, `startValues:` ` [TransitionValues](TransitionValues.md)!`, `endValues:` ` [TransitionValues](TransitionValues.md)!`)` The default implementation of this method returns a null Animator. |
| --- | --- |
| open [Animator](../android.animation/Animator.md)! | [onDisappear](Visibility.md))`(`sceneRoot:` ` [ViewGroup](../android.view/ViewGroup.md)!`, `startValues:` ` [TransitionValues](TransitionValues.md)!`, `startVisibility:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `endValues:` ` [TransitionValues](TransitionValues.md)!`, `endVisibility:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Subclasses should override this method or [onDisappear(android.view.ViewGroup,android.view.View,android.transition.TransitionValues,android.transition.TransitionValues)](Visibility.md))if they need to create an Animator when targets disappear. |
| open [Animator](../android.animation/Animator.md)! | [onDisappear](Visibility.md))`(`sceneRoot:` ` [ViewGroup](../android.view/ViewGroup.md)!`, `view:` ` [View](../android.view/View.md)!`, `startValues:` ` [TransitionValues](TransitionValues.md)!`, `endValues:` ` [TransitionValues](TransitionValues.md)!`)` The default implementation of this method returns a null Animator. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMode](Visibility.md))`(`mode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Changes the transition to support appearing and/or disappearing Views, depending on`mode`. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [Transition](Transition.md) |-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Transition](Transition.md)! | [addListener](Transition.md))`(`listener:` ` [Transition.TransitionListener](../android/transition/Transition.TransitionListener.md)!`)` <br /> Adds a listener to the set of listeners that are sent events through the life of an animation, such as start, repeat, and end. <br /> | | [Transition](Transition.md)! | [addTarget](Transition.md))`(`target:` ` [View](../android.view/View.md)!`)` <br /> Sets the target view instances that this Transition is interested in animating. By default, there are no targets, and a Transition will listen for changes on every view in the hierarchy below the sceneRoot of the Scene being transitioned into. Setting targets constrains the Transition to only listen for, and act on, these views. All other views will be ignored. The target list is like the [targetId](Transition.md))list except this list specifies the actual View instances, not the ids of the views. This is an important distinction when scene changes involve view hierarchies which have been inflated separately; different views may share the same id but not actually be the same instance. If the transition should treat those views as the same, then [addTarget(int)](Transition.md))should be used instead of [addTarget(android.view.View)](Transition.md)). If, on the other hand, scene changes involve changes all within the same view hierarchy, among views which do not necessarily have ids set on them, then the target list of views may be more convenient. <br /> | | [Transition](Transition.md)! | [addTarget](Transition.md))`(`targetId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Adds the id of a target view that this Transition is interested in animating. By default, there are no targetIds, and a Transition will listen for changes on every view in the hierarchy below the sceneRoot of the Scene being transitioned into. Setting targetIds constrains the Transition to only listen for, and act on, views with these IDs. Views with different IDs, or no IDs whatsoever, will be ignored. Note that using ids to specify targets implies that ids should be unique within the view hierarchy underneath the scene root. <br /> | | [Transition](Transition.md)! | [addTarget](Transition.md))`(`targetType:` ` [Class](../java.lang/Class.md)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`)` <br /> Adds the Class of a target view that this Transition is interested in animating. By default, there are no targetTypes, and a Transition will listen for changes on every view in the hierarchy below the sceneRoot of the Scene being transitioned into. Setting targetTypes constrains the Transition to only listen for, and act on, views with these classes. Views with different classes will be ignored. Note that any View that can be cast to targetType will be included, so if targetType is`View.class`, all Views will be included. <br /> | | [Transition](Transition.md)! | [addTarget](Transition.md))`(`targetName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Adds the transitionName of a target view that this Transition is interested in animating. By default, there are no targetNames, and a Transition will listen for changes on every view in the hierarchy below the sceneRoot of the Scene being transitioned into. Setting targetNames constrains the Transition to only listen for, and act on, views with these transitionNames. Views with different transitionNames, or no transitionName whatsoever, will be ignored. Note that transitionNames should be unique within the view hierarchy. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canRemoveViews](Transition.md))`()` <br /> | | [Transition](Transition.md) | [clone](Transition.md))`()` <br /> | | [Transition](Transition.md)! | [excludeChildren](Transition.md))`(`target:` ` [View](../android.view/View.md)!`, `exclude:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Whether to add the children of given target to the list of target children to exclude from this transition. The`exclude`parameter specifies whether the target should be added to or removed from the excluded list. Excluding targets is a general mechanism for allowing transitions to run on a view hierarchy while skipping target views that should not be part of the transition. For example, you may want to avoid animating children of a specific ListView or Spinner. Views can be excluded either by their id, or by their instance reference, or by the Class of that view (eg, [Spinner](../android.widget/Spinner.md)). <br /> | | [Transition](Transition.md)! | [excludeChildren](Transition.md))`(`targetId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `exclude:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Whether to add the children of the given id to the list of targets to exclude from this transition. The`exclude`parameter specifies whether the children of the target should be added to or removed from the excluded list. Excluding children in this way provides a simple mechanism for excluding all children of specific targets, rather than individually excluding each child individually. Excluding targets is a general mechanism for allowing transitions to run on a view hierarchy while skipping target views that should not be part of the transition. For example, you may want to avoid animating children of a specific ListView or Spinner. Views can be excluded either by their id, or by their instance reference, or by the Class of that view (eg, [Spinner](../android.widget/Spinner.md)). <br /> | | [Transition](Transition.md)! | [excludeChildren](Transition.md))`(`type:` ` [Class](../java.lang/Class.md)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`, `exclude:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Whether to add the given type to the list of types whose children should be excluded from this transition. The`exclude`parameter specifies whether the target type should be added to or removed from the excluded list. Excluding targets is a general mechanism for allowing transitions to run on a view hierarchy while skipping target views that should not be part of the transition. For example, you may want to avoid animating children of a specific ListView or Spinner. Views can be excluded either by their id, or by their instance reference, or by the Class of that view (eg, [Spinner](../android.widget/Spinner.md)). <br /> | | [Transition](Transition.md)! | [excludeTarget](Transition.md))`(`target:` ` [View](../android.view/View.md)!`, `exclude:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Whether to add the given target to the list of targets to exclude from this transition. The`exclude`parameter specifies whether the target should be added to or removed from the excluded list. Excluding targets is a general mechanism for allowing transitions to run on a view hierarchy while skipping target views that should not be part of the transition. For example, you may want to avoid animating children of a specific ListView or Spinner. Views can be excluded either by their id, or by their instance reference, or by the Class of that view (eg, [Spinner](../android.widget/Spinner.md)). <br /> | | [Transition](Transition.md)! | [excludeTarget](Transition.md))`(`targetId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `exclude:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Whether to add the given id to the list of target ids to exclude from this transition. The`exclude`parameter specifies whether the target should be added to or removed from the excluded list. Excluding targets is a general mechanism for allowing transitions to run on a view hierarchy while skipping target views that should not be part of the transition. For example, you may want to avoid animating children of a specific ListView or Spinner. Views can be excluded either by their id, or by their instance reference, or by the Class of that view (eg, [Spinner](../android.widget/Spinner.md)). <br /> | | [Transition](Transition.md)! | [excludeTarget](Transition.md))`(`type:` ` [Class](../java.lang/Class.md)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`, `exclude:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Whether to add the given type to the list of types to exclude from this transition. The`exclude`parameter specifies whether the target type should be added to or removed from the excluded list. Excluding targets is a general mechanism for allowing transitions to run on a view hierarchy while skipping target views that should not be part of the transition. For example, you may want to avoid animating children of a specific ListView or Spinner. Views can be excluded either by their id, or by their instance reference, or by the Class of that view (eg, [Spinner](../android.widget/Spinner.md)). <br /> | | [Transition](Transition.md)! | [excludeTarget](Transition.md))`(`targetName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `exclude:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Whether to add the given transitionName to the list of target transitionNames to exclude from this transition. The`exclude`parameter specifies whether the target should be added to or removed from the excluded list. Excluding targets is a general mechanism for allowing transitions to run on a view hierarchy while skipping target views that should not be part of the transition. For example, you may want to avoid animating children of a specific ListView or Spinner. Views can be excluded by their id, their instance reference, their transitionName, or by the Class of that view (eg, [Spinner](../android.widget/Spinner.md)). <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getDuration](Transition.md))`()` <br /> Returns the duration set on this transition. If no duration has been set, the returned value will be negative, indicating that resulting animators will retain their own durations. <br /> | | [Rect](../android.graphics/Rect.md)! | [getEpicenter](Transition.md))`()` <br /> Returns the epicenter as specified by the [android.transition.Transition.EpicenterCallback](../android/transition/Transition.EpicenterCallback.md) or null if no callback exists. <br /> | | [Transition.EpicenterCallback](../android/transition/Transition.EpicenterCallback.md)! | [getEpicenterCallback](Transition.md))`()` <br /> Returns the callback used to find the epicenter of the Transition. Transitions like [android.transition.Explode](Explode.md) use a point or Rect to orient the direction of travel. This is called the epicenter of the Transition and is typically centered on a touched View. The [android.transition.Transition.EpicenterCallback](../android/transition/Transition.EpicenterCallback.md) allows a Transition to dynamically retrieve the epicenter during a Transition. <br /> | | [TimeInterpolator](../android.animation/TimeInterpolator.md)! | [getInterpolator](Transition.md))`()` <br /> Returns the interpolator set on this transition. If no interpolator has been set, the returned value will be null, indicating that resulting animators will retain their own interpolators. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](Transition.md))`()` <br /> Returns the name of this Transition. This name is used internally to distinguish between different transitions to determine when interrupting transitions overlap. For example, a ChangeBounds running on the same target view as another ChangeBounds should determine whether the old transition is animating to different end values and should be canceled in favor of the new transition. By default, a Transition's name is simply the value of [Class.getName()](../java.lang/Class.md)), but subclasses are free to override and return something different. <br /> | | [PathMotion](PathMotion.md)! | [getPathMotion](Transition.md))`()` <br /> Returns the algorithm object used to interpolate along two dimensions. This is typically used to determine the View motion between two points. When describing in XML, use a nested XML tag for the path motion. It can be one of the built-in tags`arcMotion`or`patternPathMotion`or it can be a custom PathMotion using`pathMotion`with the`class`attributed with the fully-described class name. For example: ```kotlin <code>&lt;changeBounds&gt; &lt;pathMotion class="my.app.transition.MyPathMotion"/&gt; &lt;/changeBounds&gt;</code> ``` or ```kotlin <code>&lt;changeBounds&gt; &lt;arcMotion android:minimumHorizontalAngle="15" android:minimumVerticalAngle="0" android:maximumAngle="90"/&gt; &lt;/changeBounds&gt;</code> ``` <br /> | | [TransitionPropagation](TransitionPropagation.md)! | [getPropagation](Transition.md))`()` <br /> Returns the [android.transition.TransitionPropagation](TransitionPropagation.md) used to calculate Animator start delays. When a Transition affects several Views like [android.transition.Explode](Explode.md) or [android.transition.Slide](Slide.md), there may be a desire to have a "wave-front" effect such that the Animator start delay depends on position of the View. The TransitionPropagation specifies how the start delays are calculated. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getStartDelay](Transition.md))`()` <br /> Returns the startDelay set on this transition. If no startDelay has been set, the returned value will be negative, indicating that resulting animators will retain their own startDelays. <br /> | | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!>! | [getTargetIds](Transition.md))`()` <br /> Returns the list of target IDs that this transition limits itself to tracking and animating. If the list is null or empty for [getTargetIds()](Transition.md)), [getTargets()](Transition.md)), [getTargetNames()](Transition.md)), and [getTargetTypes()](Transition.md))then this transition is not limited to specific views, and will handle changes to any views in the hierarchy of a scene change. <br /> | | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | [getTargetNames](Transition.md))`()` <br /> Returns the list of target transitionNames that this transition limits itself to tracking and animating. If the list is null or empty for [getTargetIds()](Transition.md)), [getTargets()](Transition.md)), [getTargetNames()](Transition.md)), and [getTargetTypes()](Transition.md))then this transition is not limited to specific views, and will handle changes to any views in the hierarchy of a scene change. <br /> | | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Class](../java.lang/Class.md)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!>! | [getTargetTypes](Transition.md))`()` <br /> Returns the list of target transitionNames that this transition limits itself to tracking and animating. If the list is null or empty for [getTargetIds()](Transition.md)), [getTargets()](Transition.md)), [getTargetNames()](Transition.md)), and [getTargetTypes()](Transition.md))then this transition is not limited to specific views, and will handle changes to any views in the hierarchy of a scene change. <br /> | | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [View](../android.view/View.md)!>! | [getTargets](Transition.md))`()` <br /> Returns the list of target views that this transition limits itself to tracking and animating. If the list is null or empty for [getTargetIds()](Transition.md)), [getTargets()](Transition.md)), [getTargetNames()](Transition.md)), and [getTargetTypes()](Transition.md))then this transition is not limited to specific views, and will handle changes to any views in the hierarchy of a scene change. <br /> | | [TransitionValues](TransitionValues.md)! | [getTransitionValues](Transition.md))`(`view:` ` [View](../android.view/View.md)!`, `start:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> This method can be called by transitions to get the TransitionValues for any particular view during the transition-playing process. This might be necessary, for example, to query the before/after state of related views for a given transition. <br /> | | [Transition](Transition.md)! | [removeListener](Transition.md))`(`listener:` ` [Transition.TransitionListener](../android/transition/Transition.TransitionListener.md)!`)` <br /> Removes a listener from the set listening to this animation. <br /> | | [Transition](Transition.md)! | [removeTarget](Transition.md))`(`target:` ` [View](../android.view/View.md)!`)` <br /> Removes the given target from the list of targets that this Transition is interested in animating. <br /> | | [Transition](Transition.md)! | [removeTarget](Transition.md))`(`targetId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Removes the given targetId from the list of ids that this Transition is interested in animating. <br /> | | [Transition](Transition.md)! | [removeTarget](Transition.md))`(`target:` ` [Class](../java.lang/Class.md)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`)` <br /> Removes the given target from the list of targets that this Transition is interested in animating. <br /> | | [Transition](Transition.md)! | [removeTarget](Transition.md))`(`targetName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Removes the given targetName from the list of transitionNames that this Transition is interested in animating. <br /> | | [Transition](Transition.md)! | [setDuration](Transition.md))`(`duration:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Sets the duration of this transition. By default, there is no duration (indicated by a negative number), which means that the Animator created by the transition will have its own specified duration. If the duration of a Transition is set, that duration will override the Animator duration. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEpicenterCallback](Transition.md))`(`epicenterCallback:` ` [Transition.EpicenterCallback](../android/transition/Transition.EpicenterCallback.md)!`)` <br /> Sets the callback to use to find the epicenter of a Transition. A null value indicates that there is no epicenter in the Transition and onGetEpicenter() will return null. Transitions like [android.transition.Explode](Explode.md) use a point or Rect to orient the direction of travel. This is called the epicenter of the Transition and is typically centered on a touched View. The [android.transition.Transition.EpicenterCallback](../android/transition/Transition.EpicenterCallback.md) allows a Transition to dynamically retrieve the epicenter during a Transition. <br /> | | [Transition](Transition.md)! | [setInterpolator](Transition.md))`(`interpolator:` ` [TimeInterpolator](../android.animation/TimeInterpolator.md)!`)` <br /> Sets the interpolator of this transition. By default, the interpolator is null, which means that the Animator created by the transition will have its own specified interpolator. If the interpolator of a Transition is set, that interpolator will override the Animator interpolator. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMatchOrder](Transition.md))`(`vararg` `matches:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the order in which Transition matches View start and end values. The default behavior is to match first by [android.view.View#getTransitionName()](../android.view/View.md)), then by View instance, then by [android.view.View#getId()](../android.view/View.md))and finally by its item ID if it is in a direct child of ListView. The caller can choose to have only some or all of the values of [MATCH_INSTANCE](Transition.md), [MATCH_NAME](Transition.md), [MATCH_ITEM_ID](Transition.md), and [MATCH_ID](Transition.md). Only the match algorithms supplied will be used to determine whether Views are the the same in both the start and end Scene. Views that do not match will be considered as entering or leaving the Scene. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPathMotion](Transition.md))`(`pathMotion:` ` [PathMotion](PathMotion.md)!`)` <br /> Sets the algorithm used to calculate two-dimensional interpolation. Transitions such as [android.transition.ChangeBounds](ChangeBounds.md) move Views, typically in a straight path between the start and end positions. Applications that desire to have these motions move in a curve can change how Views interpolate in two dimensions by extending PathMotion and implementing [android.transition.PathMotion#getPath(float, float, float, float)](PathMotion.md)). When describing in XML, use a nested XML tag for the path motion. It can be one of the built-in tags`arcMotion`or`patternPathMotion`or it can be a custom PathMotion using`pathMotion`with the`class`attributed with the fully-described class name. For example: ```kotlin <code>&lt;changeBounds&gt; &lt;pathMotion class="my.app.transition.MyPathMotion"/&gt; &lt;/changeBounds&gt; </code> ``` or ```kotlin <code>&lt;changeBounds&gt; &lt;arcMotion android:minimumHorizontalAngle="15" android:minimumVerticalAngle="0" android:maximumAngle="90"/&gt; &lt;/changeBounds&gt; </code> ``` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPropagation](Transition.md))`(`transitionPropagation:` ` [TransitionPropagation](TransitionPropagation.md)!`)` <br /> Sets the method for determining Animator start delays. When a Transition affects several Views like [android.transition.Explode](Explode.md) or [android.transition.Slide](Slide.md), there may be a desire to have a "wave-front" effect such that the Animator start delay depends on position of the View. The TransitionPropagation specifies how the start delays are calculated. <br /> | | [Transition](Transition.md)! | [setStartDelay](Transition.md))`(`startDelay:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Sets the startDelay of this transition. By default, there is no delay (indicated by a negative number), which means that the Animator created by the transition will have its own specified startDelay. If the delay of a Transition is set, that delay will override the Animator delay. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](Transition.md))`()` <br /> | ||

## Constants

### MODE_IN

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODE_IN: Int
```

Mode used in [setMode(int)](Visibility.md))to make the transition operate on targets that are appearing. Maybe be combined with [MODE_OUT](Visibility.md) to target Visibility changes both in and out. 

 Value: 1

### MODE_OUT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODE_OUT: Int
```

Mode used in [setMode(int)](Visibility.md))to make the transition operate on targets that are disappearing. Maybe be combined with [MODE_IN](Visibility.md) to target Visibility changes both in and out. 

 Value: 2

## Public constructors

### Visibility

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Visibility()
```  

### Visibility

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Visibility(
    context: Context!, 
    attrs: AttributeSet!)
```

## Public methods

### captureEndValues

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun captureEndValues(transitionValues: TransitionValues!): Unit
```

| Parameters ||
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transitionValues` | [TransitionValues](TransitionValues.md)!:The holder for any values that the Transition wishes to store. Values are stored in the`values`field of this TransitionValues object and are keyed from a String value. For example, to store a view's rotation value, a transition might call`transitionValues.values.put("appname:transitionname:rotation", view.getRotation())`. The target view will already be stored in the transitionValues structure when this method is called. |

### captureStartValues

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun captureStartValues(transitionValues: TransitionValues!): Unit
```

| Parameters ||
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transitionValues` | [TransitionValues](TransitionValues.md)!:The holder for any values that the Transition wishes to store. Values are stored in the`values`field of this TransitionValues object and are keyed from a String value. For example, to store a view's rotation value, a transition might call`transitionValues.values.put("appname:transitionname:rotation", view.getRotation())`. The target view will already be stored in the transitionValues structure when this method is called. |

### createAnimator

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun createAnimator(
    sceneRoot: ViewGroup, 
    startValues: TransitionValues?, 
    endValues: TransitionValues?
): Animator?
```

This method creates an animation that will be run for this transition given the information in the startValues and endValues structures captured earlier for the start and end scenes. Subclasses of Transition should override this method. The method should only be called by the transition system; it is not intended to be called from external classes.

This method is called by the transition's parent (all the way up to the topmost Transition in the hierarchy) with the sceneRoot and start/end values that the transition may need to set up initial target values and construct an appropriate animation. For example, if an overall Transition is a [TransitionSet](TransitionSet.md) consisting of several child transitions in sequence, then some of the child transitions may want to set initial values on target views prior to the overall Transition commencing, to put them in an appropriate state for the delay between that start and the child Transition start time. For example, a transition that fades an item in may wish to set the starting alpha value to 0, to avoid it blinking in prior to the transition actually starting the animation. This is necessary because the scene change that triggers the Transition will automatically set the end-scene on all target views, so a Transition that wants to animate from a different value should set that value prior to returning from this method.

Additionally, a Transition can perform logic to determine whether the transition needs to run on the given target and start/end values. For example, a transition that resizes objects on the screen may wish to avoid running for views which are not present in either the start or end scenes.

If there is an animator created and returned from this method, the transition mechanism will apply any applicable duration, startDelay, and interpolator to that animation and start it. A return value of`null`indicates that no animation should run. The default implementation returns null.

The method is called for every applicable target object, which is stored in the [TransitionValues.view](TransitionValues.md) field.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------|
| `sceneRoot` | [ViewGroup](../android.view/ViewGroup.md):This value cannot be`null`. |
| `startValues` | [TransitionValues](TransitionValues.md)?:This value may be`null`. |
| `endValues` | [TransitionValues](TransitionValues.md)?:This value may be`null`. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------------|--------------------------|
| [Animator](../android.animation/Animator.md)? | This value may be`null`. |

### getMode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMode(): Int
```

Returns whether appearing and/or disappearing Views are supported. Returns whether appearing and/or disappearing Views are supported. A combination of [MODE_IN](Visibility.md) and [MODE_OUT](Visibility.md).

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is either`0`or a combination of [android.transition.Visibility#MODE_IN](Visibility.md), [android.transition.Visibility#MODE_OUT](Visibility.md), [android.transition.Fade#IN](Fade.md), and [android.transition.Fade#OUT](Fade.md) |

### getTransitionProperties

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTransitionProperties(): Array<String!>!
```

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | An array of property names as described in the class documentation for [TransitionValues](TransitionValues.md). The default implementation returns`null`. |

### isTransitionRequired

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isTransitionRequired(
    startValues: TransitionValues?, 
    newValues: TransitionValues?
): Boolean
```

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `startValues` | [TransitionValues](TransitionValues.md)?:the values from captureStartValues, This may be`null`if the View did not exist in the start state. |
| `endValues` | the values from captureEndValues. This may be`null`if the View did not exist in the end state. |

### isVisible

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isVisible(values: TransitionValues!): Boolean
```

Returns whether the view is 'visible' according to the given values object. This is determined by testing the same properties in the values object that are used to determine whether the object is appearing or disappearing in the [android.transition.Transition#createAnimator(android.view.ViewGroup,android.transition.TransitionValues,android.transition.TransitionValues)](Transition.md))method. This method can be called by, for example, subclasses that want to know whether the object is visible in the same way that Visibility determines it for the actual animation.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `values` | [TransitionValues](TransitionValues.md)!:The TransitionValues object that holds the information by which visibility is determined. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the view reference by`values`is visible, false otherwise. |

### onAppear

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAppear(
    sceneRoot: ViewGroup!, 
    startValues: TransitionValues!, 
    startVisibility: Int, 
    endValues: TransitionValues!, 
    endVisibility: Int
): Animator!
```

The default implementation of this method calls [onAppear(android.view.ViewGroup,android.view.View,android.transition.TransitionValues,android.transition.TransitionValues)](Visibility.md)). Subclasses should override this method or [onAppear(android.view.ViewGroup,android.view.View,android.transition.TransitionValues,android.transition.TransitionValues)](Visibility.md)). if they need to create an Animator when targets appear. The method should only be called by the Visibility class; it is not intended to be called from external classes.

| Parameters ||
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `sceneRoot` | [ViewGroup](../android.view/ViewGroup.md)!:The root of the transition hierarchy |
| `startValues` | [TransitionValues](TransitionValues.md)!:The target values in the start scene |
| `startVisibility` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The target visibility in the start scene |
| --- | --- |
| `endValues` | [TransitionValues](TransitionValues.md)!:The target values in the end scene |
| `endVisibility` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The target visibility in the end scene |

| Return ||
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [Animator](../android.animation/Animator.md)! | An Animator to be started at the appropriate time in the overall transition for this scene change. A null value means no animation should be run. |

### onAppear

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAppear(
    sceneRoot: ViewGroup!, 
    view: View!, 
    startValues: TransitionValues!, 
    endValues: TransitionValues!
): Animator!
```

The default implementation of this method returns a null Animator. Subclasses should override this method to make targets appear with the desired transition. The method should only be called from [onAppear(android.view.ViewGroup,android.transition.TransitionValues,int,android.transition.TransitionValues,int)](Visibility.md)).

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sceneRoot` | [ViewGroup](../android.view/ViewGroup.md)!:The root of the transition hierarchy |
| `view` | [View](../android.view/View.md)!:The View to make appear. This will be in the target scene's View hierarchy and will be VISIBLE. |
| `startValues` | [TransitionValues](TransitionValues.md)!:The target values in the start scene |
| --- | --- |
| `endValues` | [TransitionValues](TransitionValues.md)!:The target values in the end scene |

| Return ||
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [Animator](../android.animation/Animator.md)! | An Animator to be started at the appropriate time in the overall transition for this scene change. A null value means no animation should be run. |

### onDisappear

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onDisappear(
    sceneRoot: ViewGroup!, 
    startValues: TransitionValues!, 
    startVisibility: Int, 
    endValues: TransitionValues!, 
    endVisibility: Int
): Animator!
```

Subclasses should override this method or [onDisappear(android.view.ViewGroup,android.view.View,android.transition.TransitionValues,android.transition.TransitionValues)](Visibility.md))if they need to create an Animator when targets disappear. The method should only be called by the Visibility class; it is not intended to be called from external classes.

The default implementation of this method attempts to find a View to use to call [onDisappear(android.view.ViewGroup,android.view.View,android.transition.TransitionValues,android.transition.TransitionValues)](Visibility.md)), based on the situation of the View in the View hierarchy. For example, if a View was simply removed from its parent, then the View will be added into a [android.view.ViewGroupOverlay](../android.view/ViewGroupOverlay.md) and passed as the`view`parameter in [onDisappear(android.view.ViewGroup,android.view.View,android.transition.TransitionValues,android.transition.TransitionValues)](Visibility.md)). If a visible View is changed to be [View.GONE](../android.view/View.md) or [View.INVISIBLE](../android.view/View.md), then it can be used as the`view`and the visibility will be changed to [View.VISIBLE](../android.view/View.md) for the duration of the animation. However, if a View is in a hierarchy which is also altering its visibility, the situation can be more complicated. In general, if a view that is no longer in the hierarchy in the end scene still has a parent (so its parent hierarchy was removed, but it was not removed from its parent), then it will be left alone to avoid side-effects from improperly removing it from its parent. The only exception to this is if the previous [Scene](Scene.md) was [created from a layout resource file](Scene.md)), then it is considered safe to un-parent the starting scene view in order to make it disappear.

| Parameters ||
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `sceneRoot` | [ViewGroup](../android.view/ViewGroup.md)!:The root of the transition hierarchy |
| `startValues` | [TransitionValues](TransitionValues.md)!:The target values in the start scene |
| `startVisibility` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The target visibility in the start scene |
| --- | --- |
| `endValues` | [TransitionValues](TransitionValues.md)!:The target values in the end scene |
| `endVisibility` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The target visibility in the end scene |

| Return ||
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [Animator](../android.animation/Animator.md)! | An Animator to be started at the appropriate time in the overall transition for this scene change. A null value means no animation should be run. |

### onDisappear

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onDisappear(
    sceneRoot: ViewGroup!, 
    view: View!, 
    startValues: TransitionValues!, 
    endValues: TransitionValues!
): Animator!
```

The default implementation of this method returns a null Animator. Subclasses should override this method to make targets disappear with the desired transition. The method should only be called from [onDisappear(android.view.ViewGroup,android.transition.TransitionValues,int,android.transition.TransitionValues,int)](Visibility.md)).

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sceneRoot` | [ViewGroup](../android.view/ViewGroup.md)!:The root of the transition hierarchy |
| `view` | [View](../android.view/View.md)!:The View to make disappear. This will be in the target scene's View hierarchy or in an [android.view.ViewGroupOverlay](../android.view/ViewGroupOverlay.md) and will be VISIBLE. |
| `startValues` | [TransitionValues](TransitionValues.md)!:The target values in the start scene |
| --- | --- |
| `endValues` | [TransitionValues](TransitionValues.md)!:The target values in the end scene |

| Return ||
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [Animator](../android.animation/Animator.md)! | An Animator to be started at the appropriate time in the overall transition for this scene change. A null value means no animation should be run. |

### setMode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMode(mode: Int): Unit
```

Changes the transition to support appearing and/or disappearing Views, depending on`mode`.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The behavior supported by this transition, a combination of [MODE_IN](Visibility.md) and [MODE_OUT](Visibility.md). Value is either`0`or a combination of [android.transition.Visibility#MODE_IN](Visibility.md), [android.transition.Visibility#MODE_OUT](Visibility.md), [android.transition.Fade#IN](Fade.md), and [android.transition.Fade#OUT](Fade.md) |
