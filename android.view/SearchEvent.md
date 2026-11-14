# SearchEvent

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SearchEvent

Kotlin| [Java](SearchEvent.md) 
| --- | --- |

```
open class SearchEvent
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.SearchEvent](SearchEvent.md) |

Class that contains information about an event that triggers a search.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SearchEvent](SearchEvent.md))`(`inputDevice:` ` [InputDevice](InputDevice.md)!`)` Create a new search event. |

| Public methods ||
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [InputDevice](InputDevice.md)! | [getInputDevice](SearchEvent.md))`()` Returns the [InputDevice](InputDevice.md) that triggered the search. |

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

Returns the [InputDevice](InputDevice.md) that triggered the search.

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------------|
| [InputDevice](InputDevice.md)! | InputDevice the InputDevice that triggered the search. |
