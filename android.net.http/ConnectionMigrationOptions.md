# ConnectionMigrationOptions

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

# ConnectionMigrationOptions

Kotlin| [Java](https://developer.android.com/reference/android/net/http/ConnectionMigrationOptions "View this page in Java") 

```
open class ConnectionMigrationOptions
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.net.http.ConnectionMigrationOptions](https://developer.android.com/reference/kotlin/android/net/http/ConnectionMigrationOptions#) |

A class configuring the HTTP connection migration functionality.

Connection migration stops open connections to servers from being destroyed when the client device switches its L4 connectivity (typically the IP address as a result of using a different network). This is particularly common with mobile devices losing wifi connectivity and switching to cellular data, or vice versa (a.k.a. the parking lot problem). QUIC uses connection identifiers which are independent of the underlying transport layer to make this possible. If the client connects to a new network and wants to preserve the existing connection, they can do so by using a connection identifier the server knows to be a continuation of the existing connection.

The features are only available for QUIC connections and the server needs to support connection migration.

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/net/http/ConnectionMigrationOptions.Builder) Builder for [ConnectionMigrationOptions](https://developer.android.com/reference/kotlin/android/net/http/ConnectionMigrationOptions#). |

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIGRATION_OPTION_DISABLED](https://developer.android.com/reference/kotlin/android/net/http/ConnectionMigrationOptions#MIGRATION_OPTION_DISABLED:kotlin.Int) Option is disabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIGRATION_OPTION_ENABLED](https://developer.android.com/reference/kotlin/android/net/http/ConnectionMigrationOptions#MIGRATION_OPTION_ENABLED:kotlin.Int) Option is enabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIGRATION_OPTION_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/net/http/ConnectionMigrationOptions#MIGRATION_OPTION_UNSPECIFIED:kotlin.Int) Option is unspecified, platform default value will be used. |

| Public methods ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAllowNonDefaultNetworkUsage](https://developer.android.com/reference/kotlin/android/net/http/ConnectionMigrationOptions#getAllowNonDefaultNetworkUsage())`()` See [Builder.setAllowNonDefaultNetworkUsage(int)](https://developer.android.com/reference/kotlin/android/net/http/ConnectionMigrationOptions.Builder#setAllowNonDefaultNetworkUsage(kotlin.Int)) |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDefaultNetworkMigration](https://developer.android.com/reference/kotlin/android/net/http/ConnectionMigrationOptions#getDefaultNetworkMigration())`()` See [Builder.setDefaultNetworkMigration(int)](https://developer.android.com/reference/kotlin/android/net/http/ConnectionMigrationOptions.Builder#setDefaultNetworkMigration(kotlin.Int)) |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPathDegradationMigration](https://developer.android.com/reference/kotlin/android/net/http/ConnectionMigrationOptions#getPathDegradationMigration())`()` See [Builder.setPathDegradationMigration(int)](https://developer.android.com/reference/kotlin/android/net/http/ConnectionMigrationOptions.Builder#setPathDegradationMigration(kotlin.Int)) |

## Constants

### MIGRATION_OPTION_DISABLED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
static val MIGRATION_OPTION_DISABLED: Int
```

Option is disabled. 

 Value: 2

### MIGRATION_OPTION_ENABLED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
static val MIGRATION_OPTION_ENABLED: Int
```

Option is enabled. 

 Value: 1

### MIGRATION_OPTION_UNSPECIFIED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
static val MIGRATION_OPTION_UNSPECIFIED: Int
```

Option is unspecified, platform default value will be used. 

 Value: 0

## Public methods

### getAllowNonDefaultNetworkUsage

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
open fun getAllowNonDefaultNetworkUsage(): Int
```

See [Builder.setAllowNonDefaultNetworkUsage(int)](https://developer.android.com/reference/kotlin/android/net/http/ConnectionMigrationOptions.Builder#setAllowNonDefaultNetworkUsage(kotlin.Int))

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.net.http.ConnectionMigrationOptions#MIGRATION_OPTION_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/net/http/ConnectionMigrationOptions#MIGRATION_OPTION_UNSPECIFIED:kotlin.Int), [android.net.http.ConnectionMigrationOptions#MIGRATION_OPTION_ENABLED](https://developer.android.com/reference/kotlin/android/net/http/ConnectionMigrationOptions#MIGRATION_OPTION_ENABLED:kotlin.Int), or [android.net.http.ConnectionMigrationOptions#MIGRATION_OPTION_DISABLED](https://developer.android.com/reference/kotlin/android/net/http/ConnectionMigrationOptions#MIGRATION_OPTION_DISABLED:kotlin.Int) |

### getDefaultNetworkMigration

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
open fun getDefaultNetworkMigration(): Int
```

See [Builder.setDefaultNetworkMigration(int)](https://developer.android.com/reference/kotlin/android/net/http/ConnectionMigrationOptions.Builder#setDefaultNetworkMigration(kotlin.Int))

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.net.http.ConnectionMigrationOptions#MIGRATION_OPTION_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/net/http/ConnectionMigrationOptions#MIGRATION_OPTION_UNSPECIFIED:kotlin.Int), [android.net.http.ConnectionMigrationOptions#MIGRATION_OPTION_ENABLED](https://developer.android.com/reference/kotlin/android/net/http/ConnectionMigrationOptions#MIGRATION_OPTION_ENABLED:kotlin.Int), or [android.net.http.ConnectionMigrationOptions#MIGRATION_OPTION_DISABLED](https://developer.android.com/reference/kotlin/android/net/http/ConnectionMigrationOptions#MIGRATION_OPTION_DISABLED:kotlin.Int) |

### getPathDegradationMigration

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
open fun getPathDegradationMigration(): Int
```

See [Builder.setPathDegradationMigration(int)](https://developer.android.com/reference/kotlin/android/net/http/ConnectionMigrationOptions.Builder#setPathDegradationMigration(kotlin.Int))

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.net.http.ConnectionMigrationOptions#MIGRATION_OPTION_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/net/http/ConnectionMigrationOptions#MIGRATION_OPTION_UNSPECIFIED:kotlin.Int), [android.net.http.ConnectionMigrationOptions#MIGRATION_OPTION_ENABLED](https://developer.android.com/reference/kotlin/android/net/http/ConnectionMigrationOptions#MIGRATION_OPTION_ENABLED:kotlin.Int), or [android.net.http.ConnectionMigrationOptions#MIGRATION_OPTION_DISABLED](https://developer.android.com/reference/kotlin/android/net/http/ConnectionMigrationOptions#MIGRATION_OPTION_DISABLED:kotlin.Int) |
