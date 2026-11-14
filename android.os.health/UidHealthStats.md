# UidHealthStats

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UidHealthStats

Kotlin| [Java](https://developer.android.com/reference/android/os/health/UidHealthStats "View this page in Java") 
| --- | --- |

```
class UidHealthStats
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.health.UidHealthStats](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#) |

Keys for [HealthStats](https://developer.android.com/reference/kotlin/android/os/health/HealthStats) returned from [SystemHealthManager.takeUidSnapshot(int)](https://developer.android.com/reference/kotlin/android/os/health/SystemHealthManager#takeUidSnapshot(kotlin.Int)), [SystemHealthManager.takeMyUidSnapshot()](https://developer.android.com/reference/kotlin/android/os/health/SystemHealthManager#takeMyUidSnapshot()), and[SystemHealthManager.takeUidSnapshots(int[])](https://developer.android.com/reference/kotlin/android/os/health/SystemHealthManager#takeUidSnapshots(kotlin.IntArray)).

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_BLUETOOTH_IDLE_MS](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#MEASUREMENT_BLUETOOTH_IDLE_MS:kotlin.Int) Key for a measurement of number of millseconds the bluetooth controller was idle but turned on on behalf of this uid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_BLUETOOTH_POWER_MAMS](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#MEASUREMENT_BLUETOOTH_POWER_MAMS:kotlin.Int) Key for a measurement of the estimated number of mA\*ms used by this uid for bluetooth, that is to say the number of milliseconds of activity times the mA current during that period. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_BLUETOOTH_RX_BYTES](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#MEASUREMENT_BLUETOOTH_RX_BYTES:kotlin.Int) Key for a measurement of number of bytes received for this uid by the bluetooth radio. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_BLUETOOTH_RX_MS](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#MEASUREMENT_BLUETOOTH_RX_MS:kotlin.Int) Key for a measurement of number of millseconds the bluetooth transmitter was receiving data for this uid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_BLUETOOTH_RX_PACKETS](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#MEASUREMENT_BLUETOOTH_RX_PACKETS:kotlin.Int) Key for a measurement of number of packets received for this uid by the bluetooth radio. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_BLUETOOTH_TX_BYTES](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#MEASUREMENT_BLUETOOTH_TX_BYTES:kotlin.Int) Key for a measurement of number of bytes transmitted for this uid by the bluetooth radio. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_BLUETOOTH_TX_MS](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#MEASUREMENT_BLUETOOTH_TX_MS:kotlin.Int) Key for a measurement of number of millseconds the bluetooth transmitter was transmitting data for this uid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_BLUETOOTH_TX_PACKETS](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#MEASUREMENT_BLUETOOTH_TX_PACKETS:kotlin.Int) Key for a measurement of number of packets transmitted for this uid by the bluetooth radio. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_BUTTON_USER_ACTIVITY_COUNT](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#MEASUREMENT_BUTTON_USER_ACTIVITY_COUNT:kotlin.Int) Key for a measurement of number of user activity events due to physical button presses caused by the UID. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_CPU_POWER_MAMS](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#MEASUREMENT_CPU_POWER_MAMS:kotlin.Int) An estimate of the number of milliamp-microsends used by this uid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_MOBILE_IDLE_MS](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#MEASUREMENT_MOBILE_IDLE_MS:kotlin.Int) Key for a measurement of number of millseconds the mobile radio controller was idle but turned on on behalf of this uid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_MOBILE_POWER_MAMS](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#MEASUREMENT_MOBILE_POWER_MAMS:kotlin.Int) Key for a measurement of the estimated number of mA\*ms used by this uid for mobile data, that is to say the number of milliseconds of activity times the mA current during that period. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_MOBILE_RX_BYTES](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#MEASUREMENT_MOBILE_RX_BYTES:kotlin.Int) Key for a measurement of number of bytes received for this uid by the mobile radio. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_MOBILE_RX_MS](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#MEASUREMENT_MOBILE_RX_MS:kotlin.Int) Key for a measurement of number of millseconds the mobile radio transmitter was receiving data for this uid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_MOBILE_RX_PACKETS](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#MEASUREMENT_MOBILE_RX_PACKETS:kotlin.Int) Key for a measurement of number of packets received for this uid by the mobile radio. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_MOBILE_TX_BYTES](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#MEASUREMENT_MOBILE_TX_BYTES:kotlin.Int) Key for a measurement of number of bytes transmitted for this uid by the mobile radio. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_MOBILE_TX_MS](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#MEASUREMENT_MOBILE_TX_MS:kotlin.Int) Key for a measurement of number of millseconds the mobile radio transmitter was transmitting data for this uid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_MOBILE_TX_PACKETS](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#MEASUREMENT_MOBILE_TX_PACKETS:kotlin.Int) Key for a measurement of number of packets transmitted for this uid by the mobile radio. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_OTHER_USER_ACTIVITY_COUNT](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#MEASUREMENT_OTHER_USER_ACTIVITY_COUNT:kotlin.Int) Key for a measurement of number of software-generated user activity events caused by the UID. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_REALTIME_BATTERY_MS](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#MEASUREMENT_REALTIME_BATTERY_MS:kotlin.Int) How many milliseconds this statistics report covers in wall-clock time while the device was on battery including both screen-on and screen-off time. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_REALTIME_SCREEN_OFF_BATTERY_MS](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#MEASUREMENT_REALTIME_SCREEN_OFF_BATTERY_MS:kotlin.Int) How many milliseconds this statistics report covers in wall-clock time while the device was on battery including only screen-off time. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_SYSTEM_CPU_TIME_MS](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#MEASUREMENT_SYSTEM_CPU_TIME_MS:kotlin.Int) Key for a measurement of the number of milliseconds spent by the CPU running kernel code for this uid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_TOUCH_USER_ACTIVITY_COUNT](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#MEASUREMENT_TOUCH_USER_ACTIVITY_COUNT:kotlin.Int) Key for a measurement of number of user activity events due to touch events caused by the UID. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_UPTIME_BATTERY_MS](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#MEASUREMENT_UPTIME_BATTERY_MS:kotlin.Int) How many milliseconds this statistics report covers that the CPU was running while the device was on battery including both screen-on and screen-off time. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_UPTIME_SCREEN_OFF_BATTERY_MS](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#MEASUREMENT_UPTIME_SCREEN_OFF_BATTERY_MS:kotlin.Int) How many milliseconds this statistics report covers that the CPU was running while the device was on battery including only screen-off time. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_USER_CPU_TIME_MS](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#MEASUREMENT_USER_CPU_TIME_MS:kotlin.Int) Key for a measurement of the number of milliseconds spent by the CPU running user space code for this uid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_WIFI_FULL_LOCK_MS](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#MEASUREMENT_WIFI_FULL_LOCK_MS:kotlin.Int) Key for a measurement of number of millseconds that this uid held a full wifi lock. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_WIFI_IDLE_MS](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#MEASUREMENT_WIFI_IDLE_MS:kotlin.Int) Key for a measurement of number of millseconds the wifi controller was idle but turned on on behalf of this uid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_WIFI_MULTICAST_MS](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#MEASUREMENT_WIFI_MULTICAST_MS:kotlin.Int) Key for a measurement of number of millseconds that this uid was performing multicast wifi traffic. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_WIFI_POWER_MAMS](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#MEASUREMENT_WIFI_POWER_MAMS:kotlin.Int) Key for a measurement of the estimated number of mA\*ms used by this uid for wifi, that is to say the number of milliseconds of wifi activity times the mA current during that period. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_WIFI_RUNNING_MS](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#MEASUREMENT_WIFI_RUNNING_MS:kotlin.Int) Key for a measurement of number of millseconds the wifi controller was active on behalf of this uid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_WIFI_RX_BYTES](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#MEASUREMENT_WIFI_RX_BYTES:kotlin.Int) Key for a measurement of number of bytes received for this uid by the wifi radio. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_WIFI_RX_MS](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#MEASUREMENT_WIFI_RX_MS:kotlin.Int) Key for a measurement of number of millseconds the wifi transmitter was receiving data for this uid. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_WIFI_RX_PACKETS](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#MEASUREMENT_WIFI_RX_PACKETS:kotlin.Int) Key for a measurement of number of packets received for this uid by the wifi radio. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_WIFI_TX_BYTES](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#MEASUREMENT_WIFI_TX_BYTES:kotlin.Int) Key for a measurement of number of bytes transmitted for this uid by the wifi radio. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_WIFI_TX_MS](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#MEASUREMENT_WIFI_TX_MS:kotlin.Int) Key for a measurement of number of millseconds the wifi transmitter was transmitting data for this uid. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_WIFI_TX_PACKETS](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#MEASUREMENT_WIFI_TX_PACKETS:kotlin.Int) Key for a measurement of number of packets transmitted for this uid by the wifi radio. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATS_PACKAGES](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#STATS_PACKAGES:kotlin.Int) Key for a HealthStats with [PackageHealthStats](https://developer.android.com/reference/kotlin/android/os/health/PackageHealthStats) keys for each of the APKs that share this uid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATS_PIDS](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#STATS_PIDS:kotlin.Int) Key for a HealthStats with [PidHealthStats](https://developer.android.com/reference/kotlin/android/os/health/PidHealthStats) keys for each of the currently running processes for this uid. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATS_PROCESSES](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#STATS_PROCESSES:kotlin.Int) Key for a HealthStats with [ProcessHealthStats](https://developer.android.com/reference/kotlin/android/os/health/ProcessHealthStats) keys for each of the named processes for this uid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIMERS_JOBS](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#TIMERS_JOBS:kotlin.Int) Key for a map of Timers for the [android.app.job.JobScheduler](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler.html#) jobs for this uid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIMERS_SENSORS](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#TIMERS_SENSORS:kotlin.Int) Key for a map of the sensor usage for this uid. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIMERS_SYNCS](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#TIMERS_SYNCS:kotlin.Int) Key for a map of Timers for the sync adapter syncs that were done for this uid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIMERS_WAKELOCKS_DRAW](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#TIMERS_WAKELOCKS_DRAW:kotlin.Int) Key for a TimerStat for the times a system-defined wakelock was acquired to allow the application to draw when it otherwise would not be able to (e.g. on the lock screen or doze screen). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIMERS_WAKELOCKS_FULL](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#TIMERS_WAKELOCKS_FULL:kotlin.Int) Key for a TimerStat for the times a [full wake lock](https://developer.android.com/reference/kotlin/android/os/PowerManager.html#FULL_WAKE_LOCK:kotlin.Int) was acquired for this uid. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIMERS_WAKELOCKS_PARTIAL](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#TIMERS_WAKELOCKS_PARTIAL:kotlin.Int) Key for a TimerStat for the times a [partial wake lock](https://developer.android.com/reference/kotlin/android/os/PowerManager.html#PARTIAL_WAKE_LOCK:kotlin.Int) was acquired for this uid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIMERS_WAKELOCKS_WINDOW](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#TIMERS_WAKELOCKS_WINDOW:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIMER_AUDIO](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#TIMER_AUDIO:kotlin.Int) Key for a timer for the count and duration of audio playback done by this uid. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIMER_BLUETOOTH_SCAN](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#TIMER_BLUETOOTH_SCAN:kotlin.Int) Key for a timer for the count and duration of when this uid was doing bluetooth scans. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIMER_CAMERA](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#TIMER_CAMERA:kotlin.Int) Key for a timer for the count and duration this uid had the camera turned on. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIMER_FLASHLIGHT](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#TIMER_FLASHLIGHT:kotlin.Int) Key for a timer for the count and duration this uid had the flashlight turned on. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIMER_FOREGROUND_ACTIVITY](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#TIMER_FOREGROUND_ACTIVITY:kotlin.Int) Key for a timer for the count and duration of when an activity from this uid was the foreground activitiy. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIMER_GPS_SENSOR](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#TIMER_GPS_SENSOR:kotlin.Int) Key for a timer for the applications use of the GPS sensor. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIMER_MOBILE_RADIO_ACTIVE](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#TIMER_MOBILE_RADIO_ACTIVE:kotlin.Int) Key for a timer for the count and duration the mobile radio was turned on for this uid. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIMER_PROCESS_STATE_BACKGROUND_MS](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#TIMER_PROCESS_STATE_BACKGROUND_MS:kotlin.Int) Key for a timer for the count and duration of when this uid was in the "background" process state. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIMER_PROCESS_STATE_CACHED_MS](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#TIMER_PROCESS_STATE_CACHED_MS:kotlin.Int) Key for a timer for the count and duration of when this uid was in the "cached" process state. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIMER_PROCESS_STATE_FOREGROUND_MS](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#TIMER_PROCESS_STATE_FOREGROUND_MS:kotlin.Int) Key for a timer for the count and duration of when this uid was in the "foreground" process state. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIMER_PROCESS_STATE_FOREGROUND_SERVICE_MS](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#TIMER_PROCESS_STATE_FOREGROUND_SERVICE_MS:kotlin.Int) Key for a timer for the count and duration of when this uid was in the "foreground service" process state. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIMER_PROCESS_STATE_TOP_MS](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#TIMER_PROCESS_STATE_TOP_MS:kotlin.Int) Key for a timer for the count and duration of when this uid was in the "top" process state. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIMER_PROCESS_STATE_TOP_SLEEPING_MS](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#TIMER_PROCESS_STATE_TOP_SLEEPING_MS:kotlin.Int) Key for a timer for the count and duration of when this uid was in the "top sleeping" process state. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIMER_VIBRATOR](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#TIMER_VIBRATOR:kotlin.Int) Key for a timer for the count and duration this uid had the vibrator turned on. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIMER_VIDEO](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#TIMER_VIDEO:kotlin.Int) Key for a timer for the count and duration of video playback done by this uid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIMER_WIFI_SCAN](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#TIMER_WIFI_SCAN:kotlin.Int) Key for a timer for the count and duration of wifi scans done by this uid. |
| --- | --- |

## Constants

### MEASUREMENT_BLUETOOTH_IDLE_MS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_BLUETOOTH_IDLE_MS: Int
```

Key for a measurement of number of millseconds the bluetooth controller was idle but turned on on behalf of this uid. 

 Value: 10020

### MEASUREMENT_BLUETOOTH_POWER_MAMS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_BLUETOOTH_POWER_MAMS: Int
```

Key for a measurement of the estimated number of mA\*ms used by this uid for bluetooth, that is to say the number of milliseconds of activity times the mA current during that period. 

 Value: 10023

### MEASUREMENT_BLUETOOTH_RX_BYTES

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_BLUETOOTH_RX_BYTES: Int
```

Key for a measurement of number of bytes received for this uid by the bluetooth radio. 

 Value: 10052

### MEASUREMENT_BLUETOOTH_RX_MS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_BLUETOOTH_RX_MS: Int
```

Key for a measurement of number of millseconds the bluetooth transmitter was receiving data for this uid. 

 Value: 10021

### MEASUREMENT_BLUETOOTH_RX_PACKETS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_BLUETOOTH_RX_PACKETS: Int
```

Key for a measurement of number of packets received for this uid by the bluetooth radio. 

 Value: 10058

### MEASUREMENT_BLUETOOTH_TX_BYTES

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_BLUETOOTH_TX_BYTES: Int
```

Key for a measurement of number of bytes transmitted for this uid by the bluetooth radio. 

 Value: 10053

### MEASUREMENT_BLUETOOTH_TX_MS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_BLUETOOTH_TX_MS: Int
```

Key for a measurement of number of millseconds the bluetooth transmitter was transmitting data for this uid. 

 Value: 10022

### MEASUREMENT_BLUETOOTH_TX_PACKETS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_BLUETOOTH_TX_PACKETS: Int
```

Key for a measurement of number of packets transmitted for this uid by the bluetooth radio. 

 Value: 10059

### MEASUREMENT_BUTTON_USER_ACTIVITY_COUNT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_BUTTON_USER_ACTIVITY_COUNT: Int
```

Key for a measurement of number of user activity events due to physical button presses caused by the UID. Calls to userActivity() reset the user activity countdown timer and keep the screen on for the user's preferred screen-on setting. 

 Value: 10046

### MEASUREMENT_CPU_POWER_MAMS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_CPU_POWER_MAMS: Int
```

**Deprecated:** *this measurement is vendor-dependent and not reliable.*

An estimate of the number of milliamp-microsends used by this uid. 

 Value: 10064

### MEASUREMENT_MOBILE_IDLE_MS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_MOBILE_IDLE_MS: Int
```

Key for a measurement of number of millseconds the mobile radio controller was idle but turned on on behalf of this uid. 

 Value: 10024

### MEASUREMENT_MOBILE_POWER_MAMS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_MOBILE_POWER_MAMS: Int
```

Key for a measurement of the estimated number of mA\*ms used by this uid for mobile data, that is to say the number of milliseconds of activity times the mA current during that period. 

 Value: 10027

### MEASUREMENT_MOBILE_RX_BYTES

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_MOBILE_RX_BYTES: Int
```

Key for a measurement of number of bytes received for this uid by the mobile radio. 

 Value: 10048

### MEASUREMENT_MOBILE_RX_MS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_MOBILE_RX_MS: Int
```

Key for a measurement of number of millseconds the mobile radio transmitter was receiving data for this uid. 

 Value: 10025

### MEASUREMENT_MOBILE_RX_PACKETS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_MOBILE_RX_PACKETS: Int
```

Key for a measurement of number of packets received for this uid by the mobile radio. 

 Value: 10054

### MEASUREMENT_MOBILE_TX_BYTES

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_MOBILE_TX_BYTES: Int
```

Key for a measurement of number of bytes transmitted for this uid by the mobile radio. 

 Value: 10049

### MEASUREMENT_MOBILE_TX_MS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_MOBILE_TX_MS: Int
```

Key for a measurement of number of millseconds the mobile radio transmitter was transmitting data for this uid. 

 Value: 10026

### MEASUREMENT_MOBILE_TX_PACKETS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_MOBILE_TX_PACKETS: Int
```

Key for a measurement of number of packets transmitted for this uid by the mobile radio. 

 Value: 10055

### MEASUREMENT_OTHER_USER_ACTIVITY_COUNT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_OTHER_USER_ACTIVITY_COUNT: Int
```

Key for a measurement of number of software-generated user activity events caused by the UID. Calls to userActivity() reset the user activity countdown timer and keep the screen on for the user's preferred screen-on setting. 

 Value: 10045

### MEASUREMENT_REALTIME_BATTERY_MS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_REALTIME_BATTERY_MS: Int
```

How many milliseconds this statistics report covers in wall-clock time while the device was on battery including both screen-on and screen-off time. 

 Value: 10001

### MEASUREMENT_REALTIME_SCREEN_OFF_BATTERY_MS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_REALTIME_SCREEN_OFF_BATTERY_MS: Int
```

How many milliseconds this statistics report covers in wall-clock time while the device was on battery including only screen-off time. 

 Value: 10003

### MEASUREMENT_SYSTEM_CPU_TIME_MS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_SYSTEM_CPU_TIME_MS: Int
```

Key for a measurement of the number of milliseconds spent by the CPU running kernel code for this uid. 

 Value: 10063

### MEASUREMENT_TOUCH_USER_ACTIVITY_COUNT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_TOUCH_USER_ACTIVITY_COUNT: Int
```

Key for a measurement of number of user activity events due to touch events caused by the UID. Calls to userActivity() reset the user activity countdown timer and keep the screen on for the user's preferred screen-on setting. 

 Value: 10047

### MEASUREMENT_UPTIME_BATTERY_MS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_UPTIME_BATTERY_MS: Int
```

How many milliseconds this statistics report covers that the CPU was running while the device was on battery including both screen-on and screen-off time. 

 Value: 10002

### MEASUREMENT_UPTIME_SCREEN_OFF_BATTERY_MS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_UPTIME_SCREEN_OFF_BATTERY_MS: Int
```

How many milliseconds this statistics report covers that the CPU was running while the device was on battery including only screen-off time. 

 Value: 10004

### MEASUREMENT_USER_CPU_TIME_MS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_USER_CPU_TIME_MS: Int
```

Key for a measurement of the number of milliseconds spent by the CPU running user space code for this uid. 

 Value: 10062

### MEASUREMENT_WIFI_FULL_LOCK_MS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_WIFI_FULL_LOCK_MS: Int
```

Key for a measurement of number of millseconds that this uid held a full wifi lock. 

 Value: 10029

### MEASUREMENT_WIFI_IDLE_MS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_WIFI_IDLE_MS: Int
```

Key for a measurement of number of millseconds the wifi controller was idle but turned on on behalf of this uid. 

 Value: 10016

### MEASUREMENT_WIFI_MULTICAST_MS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_WIFI_MULTICAST_MS: Int
```

Key for a measurement of number of millseconds that this uid was performing multicast wifi traffic. 

 Value: 10031

### MEASUREMENT_WIFI_POWER_MAMS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_WIFI_POWER_MAMS: Int
```

Key for a measurement of the estimated number of mA\*ms used by this uid for wifi, that is to say the number of milliseconds of wifi activity times the mA current during that period. 

 Value: 10019

### MEASUREMENT_WIFI_RUNNING_MS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_WIFI_RUNNING_MS: Int
```

Key for a measurement of number of millseconds the wifi controller was active on behalf of this uid. 

 Value: 10028

### MEASUREMENT_WIFI_RX_BYTES

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_WIFI_RX_BYTES: Int
```

Key for a measurement of number of bytes received for this uid by the wifi radio. 

 Value: 10050

### MEASUREMENT_WIFI_RX_MS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_WIFI_RX_MS: Int
```

Key for a measurement of number of millseconds the wifi transmitter was receiving data for this uid. 

 Value: 10017

### MEASUREMENT_WIFI_RX_PACKETS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_WIFI_RX_PACKETS: Int
```

Key for a measurement of number of packets received for this uid by the wifi radio. 

 Value: 10056

### MEASUREMENT_WIFI_TX_BYTES

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_WIFI_TX_BYTES: Int
```

Key for a measurement of number of bytes transmitted for this uid by the wifi radio. 

 Value: 10051

### MEASUREMENT_WIFI_TX_MS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_WIFI_TX_MS: Int
```

Key for a measurement of number of millseconds the wifi transmitter was transmitting data for this uid. 

 Value: 10018

### MEASUREMENT_WIFI_TX_PACKETS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_WIFI_TX_PACKETS: Int
```

Key for a measurement of number of packets transmitted for this uid by the wifi radio. 

 Value: 10057

### STATS_PACKAGES

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATS_PACKAGES: Int
```

Key for a HealthStats with [PackageHealthStats](https://developer.android.com/reference/kotlin/android/os/health/PackageHealthStats) keys for each of the APKs that share this uid. 

 Value: 10015

### STATS_PIDS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATS_PIDS: Int
```

Key for a HealthStats with [PidHealthStats](https://developer.android.com/reference/kotlin/android/os/health/PidHealthStats) keys for each of the currently running processes for this uid. 

 Value: 10013

### STATS_PROCESSES

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATS_PROCESSES: Int
```

Key for a HealthStats with [ProcessHealthStats](https://developer.android.com/reference/kotlin/android/os/health/ProcessHealthStats) keys for each of the named processes for this uid. 

 Value: 10014

### TIMERS_JOBS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIMERS_JOBS: Int
```

Key for a map of Timers for the [android.app.job.JobScheduler](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler.html#) jobs for this uid. 

 Value: 10010

### TIMERS_SENSORS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIMERS_SENSORS: Int
```

Key for a map of the sensor usage for this uid. The keys are a string representation of the handle for the sensor. 

 Value: 10012

### TIMERS_SYNCS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIMERS_SYNCS: Int
```

Key for a map of Timers for the sync adapter syncs that were done for this uid. 

 Value: 10009

### TIMERS_WAKELOCKS_DRAW

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIMERS_WAKELOCKS_DRAW: Int
```

Key for a TimerStat for the times a system-defined wakelock was acquired to allow the application to draw when it otherwise would not be able to (e.g. on the lock screen or doze screen). 

 Value: 10008

### TIMERS_WAKELOCKS_FULL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIMERS_WAKELOCKS_FULL: Int
```

Key for a TimerStat for the times a [full wake lock](https://developer.android.com/reference/kotlin/android/os/PowerManager.html#FULL_WAKE_LOCK:kotlin.Int) was acquired for this uid. 

 Value: 10005

### TIMERS_WAKELOCKS_PARTIAL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIMERS_WAKELOCKS_PARTIAL: Int
```

Key for a TimerStat for the times a [partial wake lock](https://developer.android.com/reference/kotlin/android/os/PowerManager.html#PARTIAL_WAKE_LOCK:kotlin.Int) was acquired for this uid. 

 Value: 10006

### TIMERS_WAKELOCKS_WINDOW

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIMERS_WAKELOCKS_WINDOW: Int
```  

 Value: 10007

### TIMER_AUDIO

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIMER_AUDIO: Int
```

Key for a timer for the count and duration of audio playback done by this uid. 

 Value: 10032

### TIMER_BLUETOOTH_SCAN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIMER_BLUETOOTH_SCAN: Int
```

Key for a timer for the count and duration of when this uid was doing bluetooth scans. 

 Value: 10037

### TIMER_CAMERA

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIMER_CAMERA: Int
```

Key for a timer for the count and duration this uid had the camera turned on. 

 Value: 10035

### TIMER_FLASHLIGHT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIMER_FLASHLIGHT: Int
```

Key for a timer for the count and duration this uid had the flashlight turned on. 

 Value: 10034

### TIMER_FOREGROUND_ACTIVITY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIMER_FOREGROUND_ACTIVITY: Int
```

Key for a timer for the count and duration of when an activity from this uid was the foreground activitiy. 

 Value: 10036

### TIMER_GPS_SENSOR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIMER_GPS_SENSOR: Int
```

Key for a timer for the applications use of the GPS sensor. 

 Value: 10011

### TIMER_MOBILE_RADIO_ACTIVE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIMER_MOBILE_RADIO_ACTIVE: Int
```

Key for a timer for the count and duration the mobile radio was turned on for this uid. 

 Value: 10061

### TIMER_PROCESS_STATE_BACKGROUND_MS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIMER_PROCESS_STATE_BACKGROUND_MS: Int
```

Key for a timer for the count and duration of when this uid was in the "background" process state. 

 Value: 10042

### TIMER_PROCESS_STATE_CACHED_MS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIMER_PROCESS_STATE_CACHED_MS: Int
```

Key for a timer for the count and duration of when this uid was in the "cached" process state. 

 Value: 10043

### TIMER_PROCESS_STATE_FOREGROUND_MS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIMER_PROCESS_STATE_FOREGROUND_MS: Int
```

Key for a timer for the count and duration of when this uid was in the "foreground" process state. 

 Value: 10041

### TIMER_PROCESS_STATE_FOREGROUND_SERVICE_MS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIMER_PROCESS_STATE_FOREGROUND_SERVICE_MS: Int
```

Key for a timer for the count and duration of when this uid was in the "foreground service" process state. 

 Value: 10039

### TIMER_PROCESS_STATE_TOP_MS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIMER_PROCESS_STATE_TOP_MS: Int
```

Key for a timer for the count and duration of when this uid was in the "top" process state. 

 Value: 10038

### TIMER_PROCESS_STATE_TOP_SLEEPING_MS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIMER_PROCESS_STATE_TOP_SLEEPING_MS: Int
```

Key for a timer for the count and duration of when this uid was in the "top sleeping" process state. 

 Value: 10040

### TIMER_VIBRATOR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIMER_VIBRATOR: Int
```

Key for a timer for the count and duration this uid had the vibrator turned on. 

 Value: 10044

### TIMER_VIDEO

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIMER_VIDEO: Int
```

Key for a timer for the count and duration of video playback done by this uid. 

 Value: 10033

### TIMER_WIFI_SCAN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIMER_WIFI_SCAN: Int
```

Key for a timer for the count and duration of wifi scans done by this uid. 

 Value: 10030
