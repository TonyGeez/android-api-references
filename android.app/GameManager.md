# GameManager

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GameManager

Kotlin| [Java](GameManager.md) 
| --- | --- |

```
class GameManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.GameManager](GameManager.md) |

The GameManager allows system apps to modify and query the game mode of apps.

**Note:** After [android.os.Build.VERSION_CODES#VANILLA_ICE_CREAM](../android/os/Build.VERSION_CODES.md), some devices that do not support the GameManager features*may*not publish a GameManager instance. These device types include:

- Wear devices ([PackageManager.FEATURE_WATCH](../android.content.pm/PackageManager.md))

Therefore, you should always do a`null`check on the return value of [Context.getSystemService(Class)](../android.content/Context.md))and [Context.getSystemService(String)](../android.content/Context.md))when trying to obtain an instance of GameManager on the aforementioned device types.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GAME_MODE_BATTERY](GameManager.md) Battery game mode will save battery and give longer game play time. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GAME_MODE_CUSTOM](GameManager.md) Custom game mode that has user-provided configuration overrides. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GAME_MODE_PERFORMANCE](GameManager.md) Performance game mode maximizes the game's performance. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GAME_MODE_STANDARD](GameManager.md) Standard game mode means the platform will use the game's default performance characteristics. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GAME_MODE_UNSUPPORTED](GameManager.md) Game mode is not supported for this application. |

| Public methods ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGameMode](GameManager.md))`()` Return the user selected game mode for this application. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGameState](GameManager.md))`(`gameState:` ` [GameState](GameState.md)`)` Called by games to communicate the current state to the platform. |

## Constants

### GAME_MODE_BATTERY

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GAME_MODE_BATTERY: Int
```

Battery game mode will save battery and give longer game play time. 

 Value: 3

### GAME_MODE_CUSTOM

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GAME_MODE_CUSTOM: Int
```

Custom game mode that has user-provided configuration overrides.

Custom game mode is expected to be handled only by the platform using users' preferred config. It is currently not allowed to opt in custom mode in game mode XML file nor expected to perform app-based optimizations when activated. 

 Value: 4

### GAME_MODE_PERFORMANCE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GAME_MODE_PERFORMANCE: Int
```

Performance game mode maximizes the game's performance.

This game mode is highly likely to increase battery consumption. 

 Value: 2

### GAME_MODE_STANDARD

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GAME_MODE_STANDARD: Int
```

Standard game mode means the platform will use the game's default performance characteristics. 

 Value: 1

### GAME_MODE_UNSUPPORTED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GAME_MODE_UNSUPPORTED: Int
```

Game mode is not supported for this application. 

 Value: 0

## Public methods

### getGameMode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGameMode(): Int
```

Return the user selected game mode for this application.

An application can use`android:isGame="true"`or`android:appCategory="game"`to indicate that the application is a game. If an application is not a game, always return [GAME_MODE_UNSUPPORTED](GameManager.md).

Developers should call this API every time the application is resumed.

If a game's`targetSdkVersion`is [android.os.Build.VERSION_CODES#TIRAMISU](../android/os/Build.VERSION_CODES.md) or lower, and when the game mode is set to [GAME_MODE_CUSTOM](GameManager.md) which is available in [android.os.Build.VERSION_CODES#UPSIDE_DOWN_CAKE](../android/os/Build.VERSION_CODES.md) or newer, this API will return [GAME_MODE_STANDARD](GameManager.md) instead for backward compatibility.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.app.GameManager#GAME_MODE_UNSUPPORTED](GameManager.md), [android.app.GameManager#GAME_MODE_STANDARD](GameManager.md), [android.app.GameManager#GAME_MODE_PERFORMANCE](GameManager.md), [android.app.GameManager#GAME_MODE_BATTERY](GameManager.md), or [android.app.GameManager#GAME_MODE_CUSTOM](GameManager.md) |

### setGameState

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setGameState(gameState: GameState): Unit
```

Called by games to communicate the current state to the platform.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `gameState` | [GameState](GameState.md):An object set to the current state. This value cannot be`null`. |
