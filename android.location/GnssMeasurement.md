Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GnssMeasurement

```
class GnssMeasurement : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.location.GnssMeasurement](https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#) |

A class representing a GNSS satellite measurement, containing raw and computed information.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#ADR_STATE_CYCLE_SLIP:kotlin.Int` The state of the `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getAccumulatedDeltaRangeMeters()` has a cycle slip detected. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#ADR_STATE_HALF_CYCLE_REPORTED:kotlin.Int` Reports whether the flag `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#ADR_STATE_HALF_CYCLE_RESOLVED:kotlin.Int` has been reported by the GNSS hardware. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#ADR_STATE_HALF_CYCLE_RESOLVED:kotlin.Int` Reports whether the value `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getAccumulatedDeltaRangeMeters()` has resolved the half cycle ambiguity. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#ADR_STATE_RESET:kotlin.Int` The state of the `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getAccumulatedDeltaRangeMeters()` has detected a reset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#ADR_STATE_UNKNOWN:kotlin.Int` The state of the value `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getAccumulatedDeltaRangeMeters()` is invalid or unknown. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#ADR_STATE_VALID:kotlin.Int` The state of the `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getAccumulatedDeltaRangeMeters()` is valid. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_A:kotlin.String` Code type for: GALILEO E1A, GALILEO E6A, NavIC L5A SPS, NavIC SA SPS, GLONASS G1a L1OCd, GLONASS G2a L2CSI. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_B:kotlin.String` Code type for: GALILEO E1B, GALILEO E6B, NavIC L5B RS (D), NavIC SB RS (D), GLONASS G1a L1OCp, GLONASS G2a L2OCp, QZSS L1Sb. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_C:kotlin.String` Code type for: GPS L1 C/A, GPS L2 C/A, GLONASS G1 C/A, GLONASS G2 C/A, GALILEO E1C, GALILEO E6C, SBAS L1 C/A, QZSS L1 C/A, NavIC L5C RS (P), NavIC SC RS (P). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_D:kotlin.String` Code type for: GPS L2 (L1(C/A) + (P2-P1) (semi-codeless)), QZSS L5S(I), BDS B1C Data, BDS B2a Data, BDS B2b Data, BDS B2 (B2a+B2b) Data, BDS B3a Data, NavIC L1 Data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_E:kotlin.String` Code type for: QZSS L1 C/B, QZSS L6E. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_I:kotlin.String` Code type for: GPS L5 I, GLONASS G3 I, GALILEO E5a I, GALILEO E5b I, GALILEO E5a+b I, SBAS L5 I, QZSS L5 I, BDS B1 I, BDS B2 I, BDS B3 I. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_L:kotlin.String` Code type for: GPS L1C (P), GPS L2C (L), QZSS L1C (P), QZSS L2C (L), QZSS L6P, BDS B1a Pilot. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_M:kotlin.String` Code type for: GPS L1M, GPS L2M. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_N:kotlin.String` Code type for: GPS L1 codeless, GPS L2 codeless. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_P:kotlin.String` Code type for: GPS L1P, GPS L2P, GLONASS G1P, GLONASS G2P, BDS B1C Pilot, BDS B2a Pilot, BDS B2b Pilot, BDS B2 (B2a+B2b) Pilot, BDS B3a Pilot, QZSS L5S(Q), NavIC L1 Pilot. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_Q:kotlin.String` Code type for: GPS L5 Q, GLONASS G3 Q, GALILEO E5a Q, GALILEO E5b Q, GALILEO E5a+b Q, SBAS L5 Q, QZSS L5 Q, BDS B1 Q, BDS B2 Q, BDS B3 Q. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_S:kotlin.String` Code type for: GPS L1C (D), GPS L2C (M), QZSS L1C (D), QZSS L2C (M), QZSS L6D, BDS B1a Data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_UNKNOWN:kotlin.String` Code type when the code type is unknown. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_W:kotlin.String` Code type for: GPS L1 Z-tracking, GPS L2 Z-tracking. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_X:kotlin.String` Code type for: GPS L1C (D+P), GPS L2C (M+L), GPS L5 (I+Q), GLONASS G1a L1OCd+L1OCp, GLONASS G2a L2CSI+L2OCp, GLONASS G3 (I+Q), GALILEO E1 (B+C), GALILEO E5a (I+Q), GALILEO E5b (I+Q), GALILEO E5a+b (I+Q), GALILEO E6 (B+C), SBAS L5 (I+Q), QZSS L1C (D+P), QZSS L2C (M+L), QZSS L5 (I+Q), QZSS L6 (D+P), BDS B1 (I+Q), BDS B1C Data+Pilot, BDS B2a Data+Pilot, BDS B2 (I+Q), BDS B2 (B2a+B2b) Data+Pilot, BDS B3 (I+Q), NavIC L5 (B+C), NavIC S (B+C), NavIC L1 Data+Pilot. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_Y:kotlin.String` Code type for: GPS L1Y, GPS L2Y. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_Z:kotlin.String` Code type for: GALILEO E1 (A+B+C), GALILEO E6 (A+B+C), QZSS L1S/L1-SAIF, QZSS L5S (I+Q), QZSS L6(D+E), BDS B1A Data+Pilot, BDS B2b Data+Pilot, BDS B3a Data+Pilot. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#MULTIPATH_INDICATOR_DETECTED:kotlin.Int` The measurement shows signs of multi-path. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#MULTIPATH_INDICATOR_NOT_DETECTED:kotlin.Int` The measurement shows no signs of multi-path. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#MULTIPATH_INDICATOR_UNKNOWN:kotlin.Int` The indicator is not available or the presence or absence of multipath is unknown. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#STATE_2ND_CODE_LOCK:kotlin.Int` This GNSS measurement's tracking state has secondary code lock. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#STATE_BDS_D2_BIT_SYNC:kotlin.Int` This Beidou measurement's tracking state has D2 bit sync. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#STATE_BDS_D2_SUBFRAME_SYNC:kotlin.Int` This Beidou measurement's tracking state has D2 sub-frame sync. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#STATE_BIT_SYNC:kotlin.Int` This GNSS measurement's tracking state has bit sync. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#STATE_CODE_LOCK:kotlin.Int` This GNSS measurement's tracking state has code lock. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#STATE_GAL_E1BC_CODE_LOCK:kotlin.Int` This Galileo measurement's tracking state has E1B/C code lock. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#STATE_GAL_E1B_PAGE_SYNC:kotlin.Int` This Galileo measurement's tracking state has E1B page sync. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#STATE_GAL_E1C_2ND_CODE_LOCK:kotlin.Int` This Galileo measurement's tracking state has E1C secondary code lock. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#STATE_GLO_STRING_SYNC:kotlin.Int` This Glonass measurement's tracking state has string sync. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#STATE_GLO_TOD_DECODED:kotlin.Int` This Glonass measurement's tracking state has time-of-day decoded. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#STATE_GLO_TOD_KNOWN:kotlin.Int` This Glonass measurement's tracking state has time-of-day known, possibly not decoded over the air but has been determined from other sources. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#STATE_MSEC_AMBIGUOUS:kotlin.Int` This GNSS measurement's tracking state contains millisecond ambiguity. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#STATE_SBAS_SYNC:kotlin.Int` This SBAS measurement's tracking state has whole second level sync. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#STATE_SUBFRAME_SYNC:kotlin.Int` This GNSS measurement's tracking state has sub-frame sync. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#STATE_SYMBOL_SYNC:kotlin.Int` This GNSS measurement's tracking state has symbol sync. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#STATE_TOW_DECODED:kotlin.Int` This GNSS measurement's tracking state has time-of-week decoded. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#STATE_TOW_KNOWN:kotlin.Int` This GNSS measurement's tracking state has time-of-week known, possibly not decoded over the air but has been determined from other sources. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#STATE_UNKNOWN:kotlin.Int` This GNSS measurement's tracking state is invalid or unknown. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getAccumulatedDeltaRangeMeters()()` Gets the accumulated delta range since the last channel reset, in meters. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getAccumulatedDeltaRangeState()()` Gets 'Accumulated Delta Range' state. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getAccumulatedDeltaRangeUncertaintyMeters()()` Gets the accumulated delta range's uncertainty (1-Sigma) in meters. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getAutomaticGainControlLevelDb()()` Gets the Automatic Gain Control level in dB. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getBasebandCn0DbHz()()` Gets the baseband carrier-to-noise density in dB-Hz. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getCarrierCycles()()` The number of full carrier cycles between the satellite and the receiver. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getCarrierFrequencyHz()()` Gets the carrier frequency of the tracked signal. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getCarrierPhase()()` Gets the RF phase detected by the receiver. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getCarrierPhaseUncertainty()()` Gets the carrier-phase's uncertainty (1-Sigma). |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getCn0DbHz()()` Gets the Carrier-to-noise density in dB-Hz. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getCodeType()()` Gets the GNSS measurement's code type. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getConstellationType()()` Gets the constellation type. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getFullInterSignalBiasNanos()()` Gets the GNSS measurement's inter-signal bias in nanoseconds with sub-nanosecond accuracy. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getFullInterSignalBiasUncertaintyNanos()()` Gets the GNSS measurement's inter-signal bias uncertainty (1 sigma) in nanoseconds with sub-nanosecond accuracy. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getMultipathIndicator()()` Gets a value indicating the 'multipath' state of the event. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getPseudorangeRateMetersPerSecond()()` Gets the Pseudorange rate at the timestamp in m/s. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getPseudorangeRateUncertaintyMetersPerSecond()()` Gets the pseudorange's rate uncertainty (1-Sigma) in m/s. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getReceivedSvTimeNanos()()` Gets the received GNSS satellite time, at the measurement time, in nanoseconds. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getReceivedSvTimeUncertaintyNanos()()` Gets the error estimate (1-sigma) for the received GNSS time, in nanoseconds. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getSatelliteInterSignalBiasNanos()()` Gets the GNSS measurement's satellite inter-signal bias in nanoseconds with sub-nanosecond accuracy. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getSatelliteInterSignalBiasUncertaintyNanos()()` Gets the GNSS measurement's satellite inter-signal bias uncertainty (1 sigma) in nanoseconds with sub-nanosecond accuracy. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getSnrInDb()()` Gets the (post-correlation \& integration) Signal-to-Noise ratio (SNR) in dB. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getState()()` Gets per-satellite-signal sync state. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getSvid()()` Gets the satellite ID. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getTimeOffsetNanos()()` Gets the time offset at which the measurement was taken in nanoseconds. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#hasAutomaticGainControlLevelDb()()` Returns `true` if `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getAutomaticGainControlLevelDb()` is available, `false` otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#hasBasebandCn0DbHz()()` Returns `true` if `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getBasebandCn0DbHz()` is available, `false` otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#hasCarrierCycles()()` Returns `true` if `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getCarrierCycles()` is available, `false` otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#hasCarrierFrequencyHz()()` Returns `true` if `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getCarrierFrequencyHz()` is available, `false` otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#hasCarrierPhase()()` Returns `true` if `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getCarrierPhase()` is available, `false` otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#hasCarrierPhaseUncertainty()()` Returns `true` if `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getCarrierPhaseUncertainty()` is available, `false` otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#hasCodeType()()` Returns `true` if `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getCodeType()` is available, `false` otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#hasFullInterSignalBiasNanos()()` Returns `true` if `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getFullInterSignalBiasNanos()` is available, `false` otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#hasFullInterSignalBiasUncertaintyNanos()()` Returns `true` if `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getFullInterSignalBiasUncertaintyNanos()` is available, `false` otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#hasSatelliteInterSignalBiasNanos()()` Returns `true` if `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getSatelliteInterSignalBiasNanos()` is available, `false` otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#hasSatelliteInterSignalBiasUncertaintyNanos()()` Returns `true` if `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getSatelliteInterSignalBiasUncertaintyNanos()` is available, `false` otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#hasSnrInDb()()` Returns `true` if `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getSnrInDb()` is available, `false` otherwise. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#writeToParcel(android.os.Parcel,%20kotlin.Int)(parcel: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [GnssMeasurement](https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#)!\> | `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### ADR_STATE_CYCLE_SLIP

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ADR_STATE_CYCLE_SLIP: Int
```

The state of the `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getAccumulatedDeltaRangeMeters()` has a cycle slip detected.

 Value: 4

### ADR_STATE_HALF_CYCLE_REPORTED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ADR_STATE_HALF_CYCLE_REPORTED: Int
```

Reports whether the flag `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#ADR_STATE_HALF_CYCLE_RESOLVED:kotlin.Int` has been reported by the GNSS hardware.

When this bit is set, the value of `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getAccumulatedDeltaRangeUncertaintyMeters()` can be low (centimeter level) whether or not the half cycle ambiguity is resolved.

When this bit is unset, the value of `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getAccumulatedDeltaRangeUncertaintyMeters()` is larger, to cover the potential error due to half cycle ambiguity being unresolved.

 Value: 16

### ADR_STATE_HALF_CYCLE_RESOLVED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ADR_STATE_HALF_CYCLE_RESOLVED: Int
```

Reports whether the value `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getAccumulatedDeltaRangeMeters()` has resolved the half cycle ambiguity.

When this bit is set, the `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getAccumulatedDeltaRangeMeters()` corresponds to the carrier phase measurement plus an accumulated integer number of carrier full cycles.

When this bit is unset, the `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getAccumulatedDeltaRangeMeters()` corresponds to the carrier phase measurement plus an accumulated integer number of carrier half cycles.

For signals that have databits, the carrier phase tracking loops typically use a costas loop discriminator. This type of tracking loop introduces a half-cycle ambiguity that is resolved by searching through the received data for known patterns of databits (e.g. GPS uses the TLM word) which then determines the polarity of the incoming data and resolves the half-cycle ambiguity.

Before the half-cycle ambiguity has been resolved it is possible that the ADR_STATE_VALID flag is set:

- In cases where ADR_STATE_HALF_CYCLE_REPORTED is not set, the ADR_STATE_HALF_CYCLE_RESOLVED flag will not be available. Here, a half wave length will be added to the returned accumulated delta range uncertainty to indicate the half cycle ambiguity.
- In cases where ADR_STATE_HALF_CYCLE_REPORTED is set, half cycle ambiguity will be indicated via both the ADR_STATE_HALF_CYCLE_RESOLVED flag and as well a half wave length added to the returned accumulated delta range uncertainty.

 Value: 8

### ADR_STATE_RESET

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ADR_STATE_RESET: Int
```

The state of the `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getAccumulatedDeltaRangeMeters()` has detected a reset.

 Value: 2

### ADR_STATE_UNKNOWN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ADR_STATE_UNKNOWN: Int
```

The state of the value `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getAccumulatedDeltaRangeMeters()` is invalid or unknown.

 Value: 0

### ADR_STATE_VALID

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ADR_STATE_VALID: Int
```

The state of the `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getAccumulatedDeltaRangeMeters()` is valid.

 Value: 1

### CODE_TYPE_A

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_TYPE_A: String
```

Code type for: GALILEO E1A, GALILEO E6A, NavIC L5A SPS, NavIC SA SPS, GLONASS G1a L1OCd, GLONASS G2a L2CSI.

 Value: "A"

### CODE_TYPE_B

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_TYPE_B: String
```

Code type for: GALILEO E1B, GALILEO E6B, NavIC L5B RS (D), NavIC SB RS (D), GLONASS G1a L1OCp, GLONASS G2a L2OCp, QZSS L1Sb.

 Value: "B"

### CODE_TYPE_C

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_TYPE_C: String
```

Code type for: GPS L1 C/A, GPS L2 C/A, GLONASS G1 C/A, GLONASS G2 C/A, GALILEO E1C, GALILEO E6C, SBAS L1 C/A, QZSS L1 C/A, NavIC L5C RS (P), NavIC SC RS (P).

 Value: "C"

### CODE_TYPE_D

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_TYPE_D: String
```

Code type for: GPS L2 (L1(C/A) + (P2-P1) (semi-codeless)), QZSS L5S(I), BDS B1C Data, BDS B2a Data, BDS B2b Data, BDS B2 (B2a+B2b) Data, BDS B3a Data, NavIC L1 Data.

 Value: "D"

### CODE_TYPE_E

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_TYPE_E: String
```

Code type for: QZSS L1 C/B, QZSS L6E.

 Value: "E"

### CODE_TYPE_I

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_TYPE_I: String
```

Code type for: GPS L5 I, GLONASS G3 I, GALILEO E5a I, GALILEO E5b I, GALILEO E5a+b I, SBAS L5 I, QZSS L5 I, BDS B1 I, BDS B2 I, BDS B3 I.

 Value: "I"

### CODE_TYPE_L

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_TYPE_L: String
```

Code type for: GPS L1C (P), GPS L2C (L), QZSS L1C (P), QZSS L2C (L), QZSS L6P, BDS B1a Pilot.

 Value: "L"

### CODE_TYPE_M

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_TYPE_M: String
```

Code type for: GPS L1M, GPS L2M.

 Value: "M"

### CODE_TYPE_N

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_TYPE_N: String
```

Code type for: GPS L1 codeless, GPS L2 codeless.

 Value: "N"

### CODE_TYPE_P

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_TYPE_P: String
```

Code type for: GPS L1P, GPS L2P, GLONASS G1P, GLONASS G2P, BDS B1C Pilot, BDS B2a Pilot, BDS B2b Pilot, BDS B2 (B2a+B2b) Pilot, BDS B3a Pilot, QZSS L5S(Q), NavIC L1 Pilot.

 Value: "P"

### CODE_TYPE_Q

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_TYPE_Q: String
```

Code type for: GPS L5 Q, GLONASS G3 Q, GALILEO E5a Q, GALILEO E5b Q, GALILEO E5a+b Q, SBAS L5 Q, QZSS L5 Q, BDS B1 Q, BDS B2 Q, BDS B3 Q.

 Value: "Q"

### CODE_TYPE_S

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_TYPE_S: String
```

Code type for: GPS L1C (D), GPS L2C (M), QZSS L1C (D), QZSS L2C (M), QZSS L6D, BDS B1a Data.

 Value: "S"

### CODE_TYPE_UNKNOWN

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_TYPE_UNKNOWN: String
```

Code type when the code type is unknown.

 Value: "UNKNOWN"

### CODE_TYPE_W

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_TYPE_W: String
```

Code type for: GPS L1 Z-tracking, GPS L2 Z-tracking.

 Value: "W"

### CODE_TYPE_X

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_TYPE_X: String
```

Code type for: GPS L1C (D+P), GPS L2C (M+L), GPS L5 (I+Q), GLONASS G1a L1OCd+L1OCp, GLONASS G2a L2CSI+L2OCp, GLONASS G3 (I+Q), GALILEO E1 (B+C), GALILEO E5a (I+Q), GALILEO E5b (I+Q), GALILEO E5a+b (I+Q), GALILEO E6 (B+C), SBAS L5 (I+Q), QZSS L1C (D+P), QZSS L2C (M+L), QZSS L5 (I+Q), QZSS L6 (D+P), BDS B1 (I+Q), BDS B1C Data+Pilot, BDS B2a Data+Pilot, BDS B2 (I+Q), BDS B2 (B2a+B2b) Data+Pilot, BDS B3 (I+Q), NavIC L5 (B+C), NavIC S (B+C), NavIC L1 Data+Pilot.

 Value: "X"

### CODE_TYPE_Y

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_TYPE_Y: String
```

Code type for: GPS L1Y, GPS L2Y.

 Value: "Y"

### CODE_TYPE_Z

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODE_TYPE_Z: String
```

Code type for: GALILEO E1 (A+B+C), GALILEO E6 (A+B+C), QZSS L1S/L1-SAIF, QZSS L5S (I+Q), QZSS L6(D+E), BDS B1A Data+Pilot, BDS B2b Data+Pilot, BDS B3a Data+Pilot.

 Value: "Z"

### MULTIPATH_INDICATOR_DETECTED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MULTIPATH_INDICATOR_DETECTED: Int
```

The measurement shows signs of multi-path.

 Value: 1

### MULTIPATH_INDICATOR_NOT_DETECTED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MULTIPATH_INDICATOR_NOT_DETECTED: Int
```

The measurement shows no signs of multi-path.

 Value: 2

### MULTIPATH_INDICATOR_UNKNOWN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MULTIPATH_INDICATOR_UNKNOWN: Int
```

The indicator is not available or the presence or absence of multipath is unknown.

 Value: 0

### STATE_2ND_CODE_LOCK

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_2ND_CODE_LOCK: Int
```

This GNSS measurement's tracking state has secondary code lock.

 Value: 65536

### STATE_BDS_D2_BIT_SYNC

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_BDS_D2_BIT_SYNC: Int
```

This Beidou measurement's tracking state has D2 bit sync.

 Value: 256

### STATE_BDS_D2_SUBFRAME_SYNC

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_BDS_D2_SUBFRAME_SYNC: Int
```

This Beidou measurement's tracking state has D2 sub-frame sync.

 Value: 512

### STATE_BIT_SYNC

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_BIT_SYNC: Int
```

This GNSS measurement's tracking state has bit sync.

 Value: 2

### STATE_CODE_LOCK

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_CODE_LOCK: Int
```

This GNSS measurement's tracking state has code lock.

 Value: 1

### STATE_GAL_E1BC_CODE_LOCK

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_GAL_E1BC_CODE_LOCK: Int
```

This Galileo measurement's tracking state has E1B/C code lock.

 Value: 1024

### STATE_GAL_E1B_PAGE_SYNC

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_GAL_E1B_PAGE_SYNC: Int
```

This Galileo measurement's tracking state has E1B page sync.

 Value: 4096

### STATE_GAL_E1C_2ND_CODE_LOCK

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_GAL_E1C_2ND_CODE_LOCK: Int
```

This Galileo measurement's tracking state has E1C secondary code lock.

 Value: 2048

### STATE_GLO_STRING_SYNC

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_GLO_STRING_SYNC: Int
```

This Glonass measurement's tracking state has string sync.

 Value: 64

### STATE_GLO_TOD_DECODED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_GLO_TOD_DECODED: Int
```

This Glonass measurement's tracking state has time-of-day decoded.

 Value: 128

### STATE_GLO_TOD_KNOWN

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_GLO_TOD_KNOWN: Int
```

This Glonass measurement's tracking state has time-of-day known, possibly not decoded over the air but has been determined from other sources. If TOD decoded is set then TOD Known will also be set.

 Value: 32768

### STATE_MSEC_AMBIGUOUS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_MSEC_AMBIGUOUS: Int
```

This GNSS measurement's tracking state contains millisecond ambiguity.

 Value: 16

### STATE_SBAS_SYNC

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_SBAS_SYNC: Int
```

This SBAS measurement's tracking state has whole second level sync.

 Value: 8192

### STATE_SUBFRAME_SYNC

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_SUBFRAME_SYNC: Int
```

This GNSS measurement's tracking state has sub-frame sync.

 Value: 4

### STATE_SYMBOL_SYNC

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_SYMBOL_SYNC: Int
```

This GNSS measurement's tracking state has symbol sync.

 Value: 32

### STATE_TOW_DECODED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_TOW_DECODED: Int
```

This GNSS measurement's tracking state has time-of-week decoded.

 Value: 8

### STATE_TOW_KNOWN

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_TOW_KNOWN: Int
```

This GNSS measurement's tracking state has time-of-week known, possibly not decoded over the air but has been determined from other sources. If TOW decoded is set then TOW Known will also be set.

 Value: 16384

### STATE_UNKNOWN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_UNKNOWN: Int
```

This GNSS measurement's tracking state is invalid or unknown.

 Value: 0

## Public methods

### describeContents

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getAccumulatedDeltaRangeMeters

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAccumulatedDeltaRangeMeters(): Double
```

Gets the accumulated delta range since the last channel reset, in meters.

The error estimate for this value is `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getAccumulatedDeltaRangeUncertaintyMeters()`.

The availability of the value is represented by `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getAccumulatedDeltaRangeState()`.

A positive value indicates that the SV is moving away from the receiver. The sign of `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getAccumulatedDeltaRangeMeters()` and its relation to the sign of `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getCarrierPhase()` is given by the equation:

```kotlin
accumulated delta range = -k * carrier phase    (where k is a constant)
```

Similar to the concept of an RTCM "Phaserange", when the accumulated delta range is initially chosen, and whenever it is reset, it will retain the integer nature of the relative carrier phase offset between satellites observed by this receiver, such that the double difference of this value between receivers and satellites may be used, together with integer ambiguity resolution, to determine highly precise relative location between receivers.

The alignment of the phase measurement will not be adjusted by the receiver so the in-phase and quadrature phase components will have a quarter cycle offset as they do when transmitted from the satellites. If the measurement is from a combination of the in-phase and quadrature phase components, then the alignment of the phase measurement will be aligned to the in-phase component.

### getAccumulatedDeltaRangeState

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAccumulatedDeltaRangeState(): Int
```

Gets 'Accumulated Delta Range' state.

This indicates the state of the `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getAccumulatedDeltaRangeMeters()` measurement. See the table below for a detailed interpretation of each state.

| ADR_STATE | Time of relevance | Interpretation |
|---|---|---|
| UNKNOWN | ADR(t) | No valid carrier phase information is available at time t. |
| VALID | ADR(t) | Valid carrier phase information is available at time t. This indicates that this measurement can be used as a reference for future measurements. However, to compare it to previous measurements to compute delta range, other bits should be checked. Specifically, it can be used for delta range computation if it is valid and has no reset or cycle slip at this epoch i.e. if VALID_BIT == 1 \&\& CYCLE_SLIP_BIT == 0 \&\& RESET_BIT == 0. |
| RESET | ADR(t) - ADR(t-1) | Carrier phase accumulation has been restarted between current time t and previous time t-1. This indicates that this measurement can be used as a reference for future measurements, but it should not be compared to previous measurements to compute delta range. |
| CYCLE_SLIP | ADR(t) - ADR(t-1) | Cycle slip(s) have been detected between the current time t and previous time t-1. This indicates that this measurement can be used as a reference for future measurements. Clients can use a measurement with a cycle slip to compute delta range against previous measurements at their own risk. |
| HALF_CYCLE_RESOLVED | ADR(t) | Half cycle ambiguity is resolved at time t. |
| HALF_CYCLE_REPORTED | ADR(t) | Half cycle ambiguity is reported at time t. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#ADR_STATE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#ADR_STATE_VALID:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#ADR_STATE_RESET:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#ADR_STATE_CYCLE_SLIP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#ADR_STATE_HALF_CYCLE_RESOLVED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#ADR_STATE_HALF_CYCLE_REPORTED:kotlin.Int` |

### getAccumulatedDeltaRangeUncertaintyMeters

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAccumulatedDeltaRangeUncertaintyMeters(): Double
```

Gets the accumulated delta range's uncertainty (1-Sigma) in meters.

The uncertainty is represented as an absolute (single sided) value.

The status of the value is represented by `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getAccumulatedDeltaRangeState()`.

### getAutomaticGainControlLevelDb

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAutomaticGainControlLevelDb(): Double
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/location/GnssMeasurementsEvent#getGnssAutomaticGainControls()` instead.*

Gets the Automatic Gain Control level in dB.

AGC acts as a variable gain amplifier adjusting the power of the incoming signal. The AGC level may be used to indicate potential interference. Higher gain (and/or lower input power) shall be output as a positive number. Hence in cases of strong jamming, in the band of this signal, this value will go more negative. This value must be consistent given the same level of the incoming signal power.

Note: Different hardware designs (e.g. antenna, pre-amplification, or other RF HW components) may also affect the typical output of of this value on any given hardware design in an open sky test - the important aspect of this output is that changes in this value are indicative of changes on input signal power in the frequency band for this measurement.

This field is part of the GnssMeasurement object so it is only reported when the GNSS measurement is reported. E.g., when a GNSS signal is too weak to be acquired, the AGC value is not reported.

The value is only available if `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#hasAutomaticGainControlLevelDb()` is `true`

### getBasebandCn0DbHz

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getBasebandCn0DbHz(): Double
```

Gets the baseband carrier-to-noise density in dB-Hz.

Typical range: 10-50 dB-Hz. The range of possible baseband C/N0 values is 0-63 dB-Hz to handle some edge cases.

The value contains the measured C/N0 for the signal at the baseband. This is typically a few dB weaker than the value estimated for C/N0 at the antenna port, which is reported in `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getCn0DbHz()`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | Value is between 0.0f and 63.0f inclusive |

### getCarrierCycles

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCarrierCycles(): Long
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getAccumulatedDeltaRangeMeters()` instead.*

The number of full carrier cycles between the satellite and the receiver.

The reference frequency is given by the value of `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getCarrierFrequencyHz()`.

The value is only available if `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#hasCarrierCycles()` is `true`.

### getCarrierFrequencyHz

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCarrierFrequencyHz(): Float
```

Gets the carrier frequency of the tracked signal.

For example it can be the GPS central frequency for L1 = 1575.45 MHz, or L2 = 1227.60 MHz, L5 = 1176.45 MHz, varying GLO channels, etc.

The value is only available if `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#hasCarrierFrequencyHz()` is `true`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the carrier frequency of the signal tracked in Hz. |

### getCarrierPhase

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCarrierPhase(): Double
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getAccumulatedDeltaRangeMeters()` instead.*

Gets the RF phase detected by the receiver.

Range: \[0.0, 1.0\].

This is the fractional part of the complete carrier phase measurement.

The reference frequency is given by the value of `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getCarrierFrequencyHz()`.

The error estimate for this value is `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getCarrierPhaseUncertainty()`.

The value is only available if `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#hasCarrierPhase()` is `true`.

### getCarrierPhaseUncertainty

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCarrierPhaseUncertainty(): Double
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getAccumulatedDeltaRangeUncertaintyMeters()` instead.*

Gets the carrier-phase's uncertainty (1-Sigma).

The uncertainty is represented as an absolute (single sided) value.

The value is only available if `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#hasCarrierPhaseUncertainty()` is `true`.

### getCn0DbHz

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCn0DbHz(): Double
```

Gets the Carrier-to-noise density in dB-Hz.

Typical range: 10-50 dB-Hz. The range of possible C/N0 values is 0-63 dB-Hz to handle some edge cases.

The value contains the measured C/N0 for the signal at the antenna input.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | Value is between 0.0f and 63.0f inclusive |

### getCodeType

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCodeType(): String
```

Gets the GNSS measurement's code type.

Similar to the Attribute field described in RINEX 4.00, e.g., in Tables 9-16 (see https://igs.org/wg/rinex/#documents-formats).

See the `CODE_TYPE_*` constants for details on what each string represents (e.g., `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_A:kotlin.String`, `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_C:kotlin.String`, `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_X:kotlin.String`).

Returns `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_UNKNOWN:kotlin.String` if the GNSS Measurement's code type is unknown.

The code type is used to specify the observation descriptor defined in GNSS Observation Data File Header Section Description in the RINEX standard (Version 4.00). In cases where the code type does not align with the above listed values, the code type from the most recent version of RINEX should be used. For example, if a code type "G" is added, this string shall be set to "G".

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_A:kotlin.String` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_B:kotlin.String` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_C:kotlin.String` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_D:kotlin.String` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_E:kotlin.String` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_I:kotlin.String` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_L:kotlin.String` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_M:kotlin.String` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_N:kotlin.String` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_P:kotlin.String` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_Q:kotlin.String` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_S:kotlin.String` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_W:kotlin.String` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_X:kotlin.String` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_Y:kotlin.String` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_Z:kotlin.String` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_UNKNOWN:kotlin.String` |

### getConstellationType

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getConstellationType(): Int
```

Gets the constellation type.

The return value is one of those constants with `CONSTELLATION_` prefix in `https://developer.android.com/reference/kotlin/android/location/GnssStatus`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/location/GnssStatus#CONSTELLATION_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssStatus#CONSTELLATION_GPS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssStatus#CONSTELLATION_SBAS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssStatus#CONSTELLATION_GLONASS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssStatus#CONSTELLATION_QZSS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssStatus#CONSTELLATION_BEIDOU:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssStatus#CONSTELLATION_GALILEO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssStatus#CONSTELLATION_IRNSS:kotlin.Int` |

### getFullInterSignalBiasNanos

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getFullInterSignalBiasNanos(): Double
```

Gets the GNSS measurement's inter-signal bias in nanoseconds with sub-nanosecond accuracy.

This value is the sum of the estimated receiver-side and the space-segment-side inter-system bias, inter-frequency bias and inter-code bias, including:

- Receiver inter-constellation bias (with respect to the constellation in `https://developer.android.com/reference/kotlin/android/location/GnssClock#getReferenceConstellationTypeForIsb()`
- Receiver inter-frequency bias (with respect to the carrier frequency in `https://developer.android.com/reference/kotlin/android/location/GnssClock#getReferenceConstellationTypeForIsb()`
- Receiver inter-code bias (with respect to the code type in `https://developer.android.com/reference/kotlin/android/location/GnssClock#getReferenceConstellationTypeForIsb()`
- Master clock bias (e.g., GPS-GAL Time Offset (GGTO), GPS-UTC Time Offset (TauGps), BDS-GLO Time Offset (BGTO))(with respect to the constellation in `https://developer.android.com/reference/kotlin/android/location/GnssClock#getReferenceConstellationTypeForIsb()`
- Group delay (e.g., Total Group Delay (TGD))
- Satellite inter-frequency bias (GLO only) (with respect to the carrier frequency in `https://developer.android.com/reference/kotlin/android/location/GnssClock#getReferenceConstellationTypeForIsb()`
- Satellite inter-code bias (e.g., Differential Code Bias (DCB)) (with respect to the code type in `https://developer.android.com/reference/kotlin/android/location/GnssClock#getReferenceConstellationTypeForIsb()`

If a component of the above is already compensated in the provided `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getReceivedSvTimeNanos()`, then it must not be included in the reported full ISB.

The value does not include the inter-frequency Ionospheric bias.

The sign of the value is defined by the following equation:

```kotlin
corrected pseudorange = raw pseudorange - FullInterSignalBiasNanos
```

The value is only available if `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#hasFullInterSignalBiasNanos()` is `true`.

### getFullInterSignalBiasUncertaintyNanos

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getFullInterSignalBiasUncertaintyNanos(): Double
```

Gets the GNSS measurement's inter-signal bias uncertainty (1 sigma) in nanoseconds with sub-nanosecond accuracy.

The value is only available if `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#hasFullInterSignalBiasUncertaintyNanos()` is `true`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | Value is 0.0f or greater |

### getMultipathIndicator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMultipathIndicator(): Int
```

Gets a value indicating the 'multipath' state of the event.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#MULTIPATH_INDICATOR_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#MULTIPATH_INDICATOR_DETECTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#MULTIPATH_INDICATOR_NOT_DETECTED:kotlin.Int` |

### getPseudorangeRateMetersPerSecond

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPseudorangeRateMetersPerSecond(): Double
```

Gets the Pseudorange rate at the timestamp in m/s.

The error estimate for this value is `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getPseudorangeRateUncertaintyMetersPerSecond()`.

The value is uncorrected, i.e. corrections for receiver and satellite clock frequency errors are not included.

A positive 'uncorrected' value indicates that the SV is moving away from the receiver. The sign of the 'uncorrected' 'pseudorange rate' and its relation to the sign of 'doppler shift' is given by the equation:

```kotlin
pseudorange rate = -k * doppler shift   (where k is a constant)
```

### getPseudorangeRateUncertaintyMetersPerSecond

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPseudorangeRateUncertaintyMetersPerSecond(): Double
```

Gets the pseudorange's rate uncertainty (1-Sigma) in m/s.

The uncertainty is represented as an absolute (single sided) value.

### getReceivedSvTimeNanos

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getReceivedSvTimeNanos(): Long
```

Gets the received GNSS satellite time, at the measurement time, in nanoseconds.

The received satellite time is relative to the beginning of the system week for all constellations except for Glonass where it is relative to the beginning of the Glonass system day.

The table below indicates the valid range of the received GNSS satellite time. These ranges depend on the constellation and code being tracked and the state of the tracking algorithms given by the `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getState()` method. The minimum value of this field is zero. The maximum value of this field is determined by looking across all of the state flags that are set, for the given constellation and code type, and finding the the maximum value in this table.

For example, for GPS L1 C/A, if STATE_TOW_KNOWN is set, this field can be any value from 0 to 1 week (in nanoseconds), and for GAL E1B code, if only STATE_GAL_E1BC_CODE_LOCK is set, then this field can be any value from 0 to 4 milliseconds (in nanoseconds.)

| | **GPS/QZSS** |||| **GLNS** | **BDS** |||| **GAL** ||| **SBAS** | **NavIC** |
| **State Flag** | **L1 C/A** | **L1 C(P)** | **L5I** | **L5Q** | **L1OF** | **B1I (D1)** | **B1I (D2)** | **B1C (P)** | **B2AQ** | **E1B** | **E1C** | **E5AQ** | **L1 C/A** | **L5C** |
| **STATE_UNKNOWN** | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| **STATE_CODE_LOCK** | 1 ms | 10 ms | 1 ms | 1 ms | 1 ms | 1 ms | 1 ms | 10 ms | 1 ms | - | - | 1 ms | 1 ms | 1 ms |
| **STATE_SYMBOL_SYNC** | - | - | 10 ms | - | 10 ms | - | 2 ms | - | - | - | - | - | 2 ms | - |
| **STATE_BIT_SYNC** | 20 ms | - | 20 ms | - | 20 ms | 20 ms | - | - | - | 8 ms | - | - | 4 ms | 20 ms |
| **STATE_SUBFRAME_SYNC** | 6 s | - | 6 s | - | - | 6 s | - | - | 100 ms | - | - | 100 ms | - | 6 s |
| **STATE_TOW_DECODED** | 1 week | - | 1 week | - | - | 1 week | 1 week | - | - | 1 week | 1 week | - | 1 week | 1 week |
| **STATE_TOW_KNOWN** | 1 week | 1 week | 1 week | 1 week | - | 1 week | 1 week | 1 week | 1 week | 1 week | 1 week | 1 week | 1 week | 1 week |
| **STATE_GLO_STRING_SYNC** | - | - | - | - | 2 s | - | - | - | - | - | - | - | - | - |
| **STATE_GLO_TOD_DECODED** | - | - | - | - | 1 day | - | - | - | - | - | - | - | - | - |
| **STATE_GLO_TOD_KNOWN** | - | - | - | - | 1 day | - | - | - | - | - | - | - | - | - |
| **STATE_BDS_D2_BIT_SYNC** | - | - | - | - | - | - | 2 ms | - | - | - | - | - | - | - |
| **STATE_BDS_D2_SUBFRAME_SYNC** | - | - | - | - | - | - | 600 ms | - | - | - | - | - | - | - |
| **STATE_GAL_E1BC_CODE_LOCK** | - | - | - | - | - | - | - | - | - | 4 ms | 4 ms | - | - | - |
| **STATE_GAL_E1C_2ND_CODE_LOCK** | - | - | - | - | - | - | - | - | - | - | 100 ms | - | - | - |
| **STATE_2ND_CODE_LOCK** | - | 18000 ms | 10 ms | 20 ms | - | - | - | 18000 ms | 100 ms | - | - | 100 ms | - | - |
| **STATE_GAL_E1B_PAGE_SYNC** | - | - | - | - | - | - | - | - | - | 2 s | - | - | - | - |
| **STATE_SBAS_SYNC** | - | - | - | - | - | - | - | - | - | - | - | - | 1 s | - |

Note: TOW Known refers to the case where TOW is possibly not decoded over the air but has been determined from other sources. If TOW decoded is set then TOW Known must also be set.

Note well: if there is any ambiguity in integer millisecond, STATE_MSEC_AMBIGUOUS must be set accordingly, in the 'state' field. This value must be populated, unless the 'state' == STATE_UNKNOWN.

Note on optional flags:

- For L1 C/A and B1I, STATE_SYMBOL_SYNC is optional since the symbol length is the same as the bit length.
- For L5Q and E5aQ, STATE_BIT_SYNC and STATE_SYMBOL_SYNC are optional since they are implied by STATE_CODE_LOCK.
- STATE_2ND_CODE_LOCK for L5I is optional since it is implied by STATE_SYMBOL_SYNC.
- STATE_2ND_CODE_LOCK for E1C is optional since it is implied by STATE_GAL_E1C_2ND_CODE_LOCK.
- For E1B and E1C, STATE_SYMBOL_SYNC is optional, because it is implied by STATE_GAL_E1BC_CODE_LOCK.

### getReceivedSvTimeUncertaintyNanos

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getReceivedSvTimeUncertaintyNanos(): Long
```

Gets the error estimate (1-sigma) for the received GNSS time, in nanoseconds.

### getSatelliteInterSignalBiasNanos

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSatelliteInterSignalBiasNanos(): Double
```

Gets the GNSS measurement's satellite inter-signal bias in nanoseconds with sub-nanosecond accuracy.

This value is the space-segment-side inter-system bias, inter-frequency bias and inter-code bias, including:

- Master clock bias (e.g., GPS-GAL Time Offset (GGTO), GPS-UTC Time Offset (TauGps), BDS-GLO Time Offset (BGTO))(with respect to the constellation in `https://developer.android.com/reference/kotlin/android/location/GnssClock#getReferenceConstellationTypeForIsb()`
- Group delay (e.g., Total Group Delay (TGD))
- Satellite inter-frequency bias (GLO only) (with respect to the carrier frequency in `https://developer.android.com/reference/kotlin/android/location/GnssClock#getReferenceConstellationTypeForIsb()`
- Satellite inter-code bias (e.g., Differential Code Bias (DCB)) (with respect to the code type in `https://developer.android.com/reference/kotlin/android/location/GnssClock#getReferenceConstellationTypeForIsb()`

The sign of the value is defined by the following equation:

```kotlin
corrected pseudorange = raw pseudorange - SatelliteInterSignalBiasNanos
```

The value is only available if `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#hasSatelliteInterSignalBiasNanos()` is `true`.

### getSatelliteInterSignalBiasUncertaintyNanos

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSatelliteInterSignalBiasUncertaintyNanos(): Double
```

Gets the GNSS measurement's satellite inter-signal bias uncertainty (1 sigma) in nanoseconds with sub-nanosecond accuracy.

The value is only available if `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#hasSatelliteInterSignalBiasUncertaintyNanos()` is `true`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | Value is 0.0f or greater |

### getSnrInDb

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSnrInDb(): Double
```

Gets the (post-correlation \& integration) Signal-to-Noise ratio (SNR) in dB.

The value is only available if `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#hasSnrInDb()` is `true`.

### getState

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getState(): Int
```

Gets per-satellite-signal sync state.

It represents the current sync state for the associated satellite signal.

This value helps interpret `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getReceivedSvTimeNanos()`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#STATE_CODE_LOCK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#STATE_BIT_SYNC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#STATE_SUBFRAME_SYNC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#STATE_TOW_DECODED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#STATE_MSEC_AMBIGUOUS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#STATE_SYMBOL_SYNC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#STATE_GLO_STRING_SYNC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#STATE_GLO_TOD_DECODED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#STATE_BDS_D2_BIT_SYNC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#STATE_BDS_D2_SUBFRAME_SYNC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#STATE_GAL_E1BC_CODE_LOCK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#STATE_GAL_E1C_2ND_CODE_LOCK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#STATE_GAL_E1B_PAGE_SYNC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#STATE_SBAS_SYNC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#STATE_TOW_KNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#STATE_GLO_TOD_KNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#STATE_2ND_CODE_LOCK:kotlin.Int` |

### getSvid

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSvid(): Int
```

Gets the satellite ID.

Interpretation depends on `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getConstellationType()`. See `https://developer.android.com/reference/kotlin/android/location/GnssStatus#getSvid(kotlin.Int)`.

### getTimeOffsetNanos

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTimeOffsetNanos(): Double
```

Gets the time offset at which the measurement was taken in nanoseconds.

The reference receiver's time from which this is offset is specified by `https://developer.android.com/reference/kotlin/android/location/GnssClock#getTimeNanos()`.

The sign of this value is given by the following equation:

```kotlin
measurement time = TimeNanos + TimeOffsetNanos
```

The value provides an individual time-stamp for the measurement, and allows sub-nanosecond accuracy.

### hasAutomaticGainControlLevelDb

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasAutomaticGainControlLevelDb(): Boolean
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/location/GnssMeasurementsEvent#getGnssAutomaticGainControls()` instead.*

Returns `true` if `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getAutomaticGainControlLevelDb()` is available, `false` otherwise.

### hasBasebandCn0DbHz

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasBasebandCn0DbHz(): Boolean
```

Returns `true` if `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getBasebandCn0DbHz()` is available, `false` otherwise.

### hasCarrierCycles

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasCarrierCycles(): Boolean
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getAccumulatedDeltaRangeState()` instead.*

Returns `true` if `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getCarrierCycles()` is available, `false` otherwise.

### hasCarrierFrequencyHz

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasCarrierFrequencyHz(): Boolean
```

Returns `true` if `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getCarrierFrequencyHz()` is available, `false` otherwise.

### hasCarrierPhase

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasCarrierPhase(): Boolean
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getAccumulatedDeltaRangeState()` instead.*

Returns `true` if `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getCarrierPhase()` is available, `false` otherwise.

### hasCarrierPhaseUncertainty

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasCarrierPhaseUncertainty(): Boolean
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getAccumulatedDeltaRangeState()` instead.*

Returns `true` if `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getCarrierPhaseUncertainty()` is available, `false` otherwise.

### hasCodeType

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasCodeType(): Boolean
```

Returns `true` if `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getCodeType()` is available, `false` otherwise.

### hasFullInterSignalBiasNanos

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasFullInterSignalBiasNanos(): Boolean
```

Returns `true` if `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getFullInterSignalBiasNanos()` is available, `false` otherwise.

### hasFullInterSignalBiasUncertaintyNanos

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasFullInterSignalBiasUncertaintyNanos(): Boolean
```

Returns `true` if `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getFullInterSignalBiasUncertaintyNanos()` is available, `false` otherwise.

### hasSatelliteInterSignalBiasNanos

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasSatelliteInterSignalBiasNanos(): Boolean
```

Returns `true` if `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getSatelliteInterSignalBiasNanos()` is available, `false` otherwise.

### hasSatelliteInterSignalBiasUncertaintyNanos

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasSatelliteInterSignalBiasUncertaintyNanos(): Boolean
```

Returns `true` if `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getSatelliteInterSignalBiasUncertaintyNanos()` is available, `false` otherwise.

### hasSnrInDb

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasSnrInDb(): Boolean
```

Returns `true` if `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getSnrInDb()` is available, `false` otherwise.

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    parcel: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<GnssMeasurement!>
```
