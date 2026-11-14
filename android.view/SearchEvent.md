# SearchEvent

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SearchEvent

Kotlin| [Java](../android/view/SearchEvent.md) 
| --- | --- |

```
open class SearchEvent
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.SearchEvent](../android/view/SearchEvent.md) |

Class that contains information about an event that triggers a search.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SearchEvent](../android/view/SearchEvent.md))`(`inputDevice:` ` [InputDevice](../android/view/InputDevice.md)!`)` Create a new search event. |

| Public methods ||
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [InputDevice](../android/view/InputDevice.md)! | [getInputDevice](../android/view/SearchEvent.md))`()` Returns the [InputDevice](../android/view/InputDevice.md) that triggered the search. |

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

Returns the [InputDevice](../android/view/InputDevice.md) that triggered the search.

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------------|
| [InputDevice](../android/view/InputDevice.md)! | InputDevice the InputDevice that triggered the search. |
