# SearchEvent

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SearchEvent

Kotlin| [Java](https://developer.android.com/reference/android/view/SearchEvent "View this page in Java") 
| --- | --- |

```
open class SearchEvent
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.SearchEvent](https://developer.android.com/reference/kotlin/android/view/SearchEvent#) |

Class that contains information about an event that triggers a search.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SearchEvent](https://developer.android.com/reference/kotlin/android/view/SearchEvent#SearchEvent(android.view.InputDevice))`(`inputDevice:` ` [InputDevice](https://developer.android.com/reference/kotlin/android/view/InputDevice)!`)` Create a new search event. |

| Public methods ||
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [InputDevice](https://developer.android.com/reference/kotlin/android/view/InputDevice)! | [getInputDevice](https://developer.android.com/reference/kotlin/android/view/SearchEvent#getInputDevice())`()` Returns the [InputDevice](https://developer.android.com/reference/kotlin/android/view/InputDevice) that triggered the search. |

## Public constructors

### SearchEvent

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SearchEvent(inputDevice: InputDevice!)
```

Create a new search event.

## Public methods

### getInputDevice

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInputDevice(): InputDevice!
```

Returns the [InputDevice](https://developer.android.com/reference/kotlin/android/view/InputDevice) that triggered the search.

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------------|
| [InputDevice](https://developer.android.com/reference/kotlin/android/view/InputDevice)! | InputDevice the InputDevice that triggered the search. |
