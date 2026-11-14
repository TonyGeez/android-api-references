Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnNmeaMessageListener

Kotlin | [Java](OnNmeaMessageListener.md)
| --- | --- |

```
interface OnNmeaMessageListener
```

| [android.location.OnNmeaMessageListener](OnNmeaMessageListener.md) |

Used for receiving NMEA sentences from the GNSS. NMEA 0183 is a standard for communicating with marine electronic devices and is a common method for receiving data from a GNSS, typically over a serial port. See [NMEA 0183](http://en.wikipedia.org/wiki/NMEA_0183) for more details. You can implement this interface and call addNmeaListener to receive NMEA data from the GNSS engine.

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onNmeaMessage Called when an NMEA message is received. |

## Public methods

### onNmeaMessage

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onNmeaMessage(
    message: String!, 
    timestamp: Long
): Unit
```

Called when an NMEA message is received.

| Parameters ||
|---|---|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: NMEA message |
| `timestamp` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): Timestamp of the location fix, as reported by the GNSS chipset. The value is specified in Unix time milliseconds since 1st January 1970, 00:00:00 UTC |
