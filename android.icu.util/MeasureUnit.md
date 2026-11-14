# MeasureUnit

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MeasureUnit

Kotlin| [Java](../android/icu/util/MeasureUnit.md) 
| --- | --- |

```
open class MeasureUnit : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.util.MeasureUnit](../android/icu/util/MeasureUnit.md) |

| Known Direct Subclasses [Currency](../android/icu/util/Currency.md), [TimeUnit](../android/icu/util/TimeUnit.md) |--------------------------------------------------------------------------------------|-----------------------------------------------------------| | [Currency](../android/icu/util/Currency.md) | A class encapsulating a currency, as defined by ISO 4217. | | [TimeUnit](../android/icu/util/TimeUnit.md) | Measurement unit for time units. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A unit such as length, mass, volume, currency, etc. A unit is coupled with a numeric amount to produce a Measure. MeasureUnit objects are immutable. All subclasses must guarantee that. (However, subclassing is discouraged.)

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Complexity](../android/icu/util/MeasureUnit.Complexity.md) Enumeration for unit complexity. |
| | [MeasurePrefix](../android/icu/util/MeasureUnit.MeasurePrefix.md) Enumeration for SI and binary prefixes, e. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/icu/util/MeasureUnit.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| openstatic [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [forIdentifier](../android/icu/util/MeasureUnit.md))`(`identifier:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Construct a MeasureUnit from a CLDR Core Unit Identifier, defined in UTS 35. |
| openstatic [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [MeasureUnit](../android/icu/util/MeasureUnit.md)!\>! | [getAvailable](../android/icu/util/MeasureUnit.md))`()` Get all of the available units. |
| --- | --- |
| openstatic [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [MeasureUnit](../android/icu/util/MeasureUnit.md)!\>! | [getAvailable](../android/icu/util/MeasureUnit.md))`(`type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` For the given type, return the available units. |
| openstatic [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getAvailableTypes](../android/icu/util/MeasureUnit.md))`()` Get all of the available units' types. |
| open [MeasureUnit.Complexity](../android/icu/util/MeasureUnit.Complexity.md)! | [getComplexity](../android/icu/util/MeasureUnit.md))`()` Compute the complexity of the unit. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDimensionality](../android/icu/util/MeasureUnit.md))`()` Returns the dimensionality (power) of this MeasureUnit. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getIdentifier](../android/icu/util/MeasureUnit.md))`()` Get CLDR Unit Identifier for this MeasureUnit, as defined in UTS 35. |
| open [MeasureUnit.MeasurePrefix](../android/icu/util/MeasureUnit.MeasurePrefix.md)! | [getPrefix](../android/icu/util/MeasureUnit.md))`()` Returns the current SI or binary prefix of this SINGLE unit. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSubtype](../android/icu/util/MeasureUnit.md))`()` Get the subType, such as "foot". |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getType](../android/icu/util/MeasureUnit.md))`()` Get the type, such as "length". |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/icu/util/MeasureUnit.md))`()` Returns a hash code value for the object. |
| --- | --- |
| open [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [product](../android/icu/util/MeasureUnit.md))`(`other:` ` [MeasureUnit](../android/icu/util/MeasureUnit.md)!`)` Computes the product of this unit with another unit. |
| open [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [reciprocal](../android/icu/util/MeasureUnit.md))`()` Computes the reciprocal of this MeasureUnit, with the numerator and denominator flipped. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MeasureUnit](../android/icu/util/MeasureUnit.md)!\>! | [splitToSingleUnits](../android/icu/util/MeasureUnit.md))`()` Returns the list of SINGLE units contained within a sequence of COMPOUND units. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/icu/util/MeasureUnit.md))`()` Returns a string representation of the object. |
| open [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [withDimensionality](../android/icu/util/MeasureUnit.md))`(`dimensionality:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a MeasureUnit which is this SINGLE unit augmented with the specified dimensionality (power). |
| open [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [withPrefix](../android/icu/util/MeasureUnit.md))`(`prefix:` ` [MeasureUnit.MeasurePrefix](../android/icu/util/MeasureUnit.MeasurePrefix.md)!`)` Creates a MeasureUnit which is this SINGLE unit augmented with the specified prefix. |
| --- | --- |

| Properties ||
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [ACRE](../android/icu/util/MeasureUnit.md) Constant for unit of area: acre |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [ACRE_FOOT](../android/icu/util/MeasureUnit.md) Constant for unit of volume: acre-foot |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [AMPERE](../android/icu/util/MeasureUnit.md) Constant for unit of electric: ampere |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [ARC_MINUTE](../android/icu/util/MeasureUnit.md) Constant for unit of angle: arc-minute |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [ARC_SECOND](../android/icu/util/MeasureUnit.md) Constant for unit of angle: arc-second |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [ASTRONOMICAL_UNIT](../android/icu/util/MeasureUnit.md) Constant for unit of length: astronomical-unit |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [ATMOSPHERE](../android/icu/util/MeasureUnit.md) Constant for unit of pressure: atmosphere |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [BEAUFORT](../android/icu/util/MeasureUnit.md) Constant for unit of speed: beaufort |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [BIT](../android/icu/util/MeasureUnit.md) Constant for unit of digital: bit |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [BUSHEL](../android/icu/util/MeasureUnit.md) Constant for unit of volume: bushel |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [BYTE](../android/icu/util/MeasureUnit.md) Constant for unit of digital: byte |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [CALORIE](../android/icu/util/MeasureUnit.md) Constant for unit of energy: calorie |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [CANDELA](../android/icu/util/MeasureUnit.md) Constant for unit of light: candela |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [CARAT](../android/icu/util/MeasureUnit.md) Constant for unit of mass: carat |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [CELSIUS](../android/icu/util/MeasureUnit.md) Constant for unit of temperature: celsius |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [CENTILITER](../android/icu/util/MeasureUnit.md) Constant for unit of volume: centiliter |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [CENTIMETER](../android/icu/util/MeasureUnit.md) Constant for unit of length: centimeter |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [CENTURY](../android/icu/util/MeasureUnit.md) Constant for unit of duration: century |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [CUBIC_CENTIMETER](../android/icu/util/MeasureUnit.md) Constant for unit of volume: cubic-centimeter |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [CUBIC_FOOT](../android/icu/util/MeasureUnit.md) Constant for unit of volume: cubic-foot |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [CUBIC_INCH](../android/icu/util/MeasureUnit.md) Constant for unit of volume: cubic-inch |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [CUBIC_KILOMETER](../android/icu/util/MeasureUnit.md) Constant for unit of volume: cubic-kilometer |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [CUBIC_METER](../android/icu/util/MeasureUnit.md) Constant for unit of volume: cubic-meter |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [CUBIC_MILE](../android/icu/util/MeasureUnit.md) Constant for unit of volume: cubic-mile |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [CUBIC_YARD](../android/icu/util/MeasureUnit.md) Constant for unit of volume: cubic-yard |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [CUP](../android/icu/util/MeasureUnit.md) Constant for unit of volume: cup |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [CUP_METRIC](../android/icu/util/MeasureUnit.md) Constant for unit of volume: cup-metric |
| --- | --- |
| static [TimeUnit](../android/icu/util/TimeUnit.md)! | [DAY](../android/icu/util/MeasureUnit.md) Constant for unit of duration: day |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [DECADE](../android/icu/util/MeasureUnit.md) Constant for unit of duration: decade |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [DECILITER](../android/icu/util/MeasureUnit.md) Constant for unit of volume: deciliter |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [DECIMETER](../android/icu/util/MeasureUnit.md) Constant for unit of length: decimeter |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [DEGREE](../android/icu/util/MeasureUnit.md) Constant for unit of angle: degree |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [DOT](../android/icu/util/MeasureUnit.md) Constant for unit of graphics: dot |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [DOT_PER_CENTIMETER](../android/icu/util/MeasureUnit.md) Constant for unit of graphics: dot-per-centimeter |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [DOT_PER_INCH](../android/icu/util/MeasureUnit.md) Constant for unit of graphics: dot-per-inch |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [EM](../android/icu/util/MeasureUnit.md) Constant for unit of graphics: em |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [FAHRENHEIT](../android/icu/util/MeasureUnit.md) Constant for unit of temperature: fahrenheit |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [FATHOM](../android/icu/util/MeasureUnit.md) Constant for unit of length: fathom |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [FLUID_OUNCE](../android/icu/util/MeasureUnit.md) Constant for unit of volume: fluid-ounce |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [FOODCALORIE](../android/icu/util/MeasureUnit.md) Constant for unit of energy: foodcalorie |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [FOOT](../android/icu/util/MeasureUnit.md) Constant for unit of length: foot |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [FURLONG](../android/icu/util/MeasureUnit.md) Constant for unit of length: furlong |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [GALLON](../android/icu/util/MeasureUnit.md) Constant for unit of volume: gallon |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [GALLON_IMPERIAL](../android/icu/util/MeasureUnit.md) Constant for unit of volume: gallon-imperial |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [GASOLINE_ENERGY_DENSITY](../android/icu/util/MeasureUnit.md) Constant for unit of pressure: gasoline-energy-density |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [GENERIC_TEMPERATURE](../android/icu/util/MeasureUnit.md) Constant for unit of temperature: generic |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [GIGABIT](../android/icu/util/MeasureUnit.md) Constant for unit of digital: gigabit |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [GIGABYTE](../android/icu/util/MeasureUnit.md) Constant for unit of digital: gigabyte |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [GIGAHERTZ](../android/icu/util/MeasureUnit.md) Constant for unit of frequency: gigahertz |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [GIGAWATT](../android/icu/util/MeasureUnit.md) Constant for unit of power: gigawatt |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [GRAM](../android/icu/util/MeasureUnit.md) Constant for unit of mass: gram |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [G_FORCE](../android/icu/util/MeasureUnit.md) Constant for unit of acceleration: g-force |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [HECTARE](../android/icu/util/MeasureUnit.md) Constant for unit of area: hectare |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [HECTOLITER](../android/icu/util/MeasureUnit.md) Constant for unit of volume: hectoliter |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [HECTOPASCAL](../android/icu/util/MeasureUnit.md) Constant for unit of pressure: hectopascal |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [HERTZ](../android/icu/util/MeasureUnit.md) Constant for unit of frequency: hertz |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [HORSEPOWER](../android/icu/util/MeasureUnit.md) Constant for unit of power: horsepower |
| --- | --- |
| static [TimeUnit](../android/icu/util/TimeUnit.md)! | [HOUR](../android/icu/util/MeasureUnit.md) Constant for unit of duration: hour |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [INCH](../android/icu/util/MeasureUnit.md) Constant for unit of length: inch |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [INCH_HG](../android/icu/util/MeasureUnit.md) Constant for unit of pressure: inch-ofhg |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [ITEM](../android/icu/util/MeasureUnit.md) Constant for unit of concentr: item |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [JOULE](../android/icu/util/MeasureUnit.md) Constant for unit of energy: joule |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [KARAT](../android/icu/util/MeasureUnit.md) Constant for unit of concentr: karat |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [KELVIN](../android/icu/util/MeasureUnit.md) Constant for unit of temperature: kelvin |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [KILOBIT](../android/icu/util/MeasureUnit.md) Constant for unit of digital: kilobit |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [KILOBYTE](../android/icu/util/MeasureUnit.md) Constant for unit of digital: kilobyte |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [KILOCALORIE](../android/icu/util/MeasureUnit.md) Constant for unit of energy: kilocalorie |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [KILOGRAM](../android/icu/util/MeasureUnit.md) Constant for unit of mass: kilogram |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [KILOHERTZ](../android/icu/util/MeasureUnit.md) Constant for unit of frequency: kilohertz |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [KILOJOULE](../android/icu/util/MeasureUnit.md) Constant for unit of energy: kilojoule |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [KILOMETER](../android/icu/util/MeasureUnit.md) Constant for unit of length: kilometer |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [KILOMETER_PER_HOUR](../android/icu/util/MeasureUnit.md) Constant for unit of speed: kilometer-per-hour |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [KILOWATT](../android/icu/util/MeasureUnit.md) Constant for unit of power: kilowatt |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [KILOWATT_HOUR](../android/icu/util/MeasureUnit.md) Constant for unit of energy: kilowatt-hour |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [KILOWATT_HOUR_PER_100_KILOMETER](../android/icu/util/MeasureUnit.md) Constant for unit of force: kilowatt-hour-per-100-kilometer |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [KNOT](../android/icu/util/MeasureUnit.md) Constant for unit of speed: knot |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [LIGHT_YEAR](../android/icu/util/MeasureUnit.md) Constant for unit of length: light-year |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [LITER](../android/icu/util/MeasureUnit.md) Constant for unit of volume: liter |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [LITER_PER_100KILOMETERS](../android/icu/util/MeasureUnit.md) Constant for unit of consumption: liter-per-100-kilometer |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [LITER_PER_KILOMETER](../android/icu/util/MeasureUnit.md) Constant for unit of consumption: liter-per-kilometer |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [LUMEN](../android/icu/util/MeasureUnit.md) Constant for unit of light: lumen |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [LUX](../android/icu/util/MeasureUnit.md) Constant for unit of light: lux |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [MEGABIT](../android/icu/util/MeasureUnit.md) Constant for unit of digital: megabit |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [MEGABYTE](../android/icu/util/MeasureUnit.md) Constant for unit of digital: megabyte |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [MEGAHERTZ](../android/icu/util/MeasureUnit.md) Constant for unit of frequency: megahertz |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [MEGALITER](../android/icu/util/MeasureUnit.md) Constant for unit of volume: megaliter |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [MEGAPIXEL](../android/icu/util/MeasureUnit.md) Constant for unit of graphics: megapixel |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [MEGAWATT](../android/icu/util/MeasureUnit.md) Constant for unit of power: megawatt |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [METER](../android/icu/util/MeasureUnit.md) Constant for unit of length: meter |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [METER_PER_SECOND](../android/icu/util/MeasureUnit.md) Constant for unit of speed: meter-per-second |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [METER_PER_SECOND_SQUARED](../android/icu/util/MeasureUnit.md) Constant for unit of acceleration: meter-per-square-second |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [METRIC_TON](../android/icu/util/MeasureUnit.md) Constant for unit of mass: metric-ton (renamed to tonne in CLDR 42 / ICU 72). |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [MICROGRAM](../android/icu/util/MeasureUnit.md) Constant for unit of mass: microgram |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [MICROMETER](../android/icu/util/MeasureUnit.md) Constant for unit of length: micrometer |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [MICROSECOND](../android/icu/util/MeasureUnit.md) Constant for unit of duration: microsecond |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [MILE](../android/icu/util/MeasureUnit.md) Constant for unit of length: mile |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [MILE_PER_GALLON](../android/icu/util/MeasureUnit.md) Constant for unit of consumption: mile-per-gallon |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [MILE_PER_GALLON_IMPERIAL](../android/icu/util/MeasureUnit.md) Constant for unit of consumption: mile-per-gallon-imperial |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [MILE_PER_HOUR](../android/icu/util/MeasureUnit.md) Constant for unit of speed: mile-per-hour |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [MILE_SCANDINAVIAN](../android/icu/util/MeasureUnit.md) Constant for unit of length: mile-scandinavian |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [MILLIAMPERE](../android/icu/util/MeasureUnit.md) Constant for unit of electric: milliampere |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [MILLIBAR](../android/icu/util/MeasureUnit.md) Constant for unit of pressure: millibar |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [MILLIGRAM](../android/icu/util/MeasureUnit.md) Constant for unit of mass: milligram |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [MILLIGRAM_OFGLUCOSE_PER_DECILITER](../android/icu/util/MeasureUnit.md) Constant for unit of concentr: milligram-ofglucose-per-deciliter |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [MILLIGRAM_PER_DECILITER](../android/icu/util/MeasureUnit.md) Constant for unit of concentr: milligram-per-deciliter |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [MILLILITER](../android/icu/util/MeasureUnit.md) Constant for unit of volume: milliliter |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [MILLIMETER](../android/icu/util/MeasureUnit.md) Constant for unit of length: millimeter |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [MILLIMETER_OF_MERCURY](../android/icu/util/MeasureUnit.md) Constant for unit of pressure: millimeter-ofhg |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [MILLIMOLE_PER_LITER](../android/icu/util/MeasureUnit.md) Constant for unit of concentr: millimole-per-liter |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [MILLISECOND](../android/icu/util/MeasureUnit.md) Constant for unit of duration: millisecond |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [MILLIWATT](../android/icu/util/MeasureUnit.md) Constant for unit of power: milliwatt |
| --- | --- |
| static [TimeUnit](../android/icu/util/TimeUnit.md)! | [MINUTE](../android/icu/util/MeasureUnit.md) Constant for unit of duration: minute |
| static [TimeUnit](../android/icu/util/TimeUnit.md)! | [MONTH](../android/icu/util/MeasureUnit.md) Constant for unit of duration: month |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [NANOMETER](../android/icu/util/MeasureUnit.md) Constant for unit of length: nanometer |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [NANOSECOND](../android/icu/util/MeasureUnit.md) Constant for unit of duration: nanosecond |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [NAUTICAL_MILE](../android/icu/util/MeasureUnit.md) Constant for unit of length: nautical-mile |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [OHM](../android/icu/util/MeasureUnit.md) Constant for unit of electric: ohm |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [OUNCE](../android/icu/util/MeasureUnit.md) Constant for unit of mass: ounce |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [OUNCE_TROY](../android/icu/util/MeasureUnit.md) Constant for unit of mass: ounce-troy |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [PARSEC](../android/icu/util/MeasureUnit.md) Constant for unit of length: parsec |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [PART_PER_MILLION](../android/icu/util/MeasureUnit.md) Constant for unit of concentr: permillion |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [PERCENT](../android/icu/util/MeasureUnit.md) Constant for unit of concentr: percent |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [PERMILLE](../android/icu/util/MeasureUnit.md) Constant for unit of concentr: permille |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [PETABYTE](../android/icu/util/MeasureUnit.md) Constant for unit of digital: petabyte |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [PICOMETER](../android/icu/util/MeasureUnit.md) Constant for unit of length: picometer |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [PINT](../android/icu/util/MeasureUnit.md) Constant for unit of volume: pint |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [PINT_METRIC](../android/icu/util/MeasureUnit.md) Constant for unit of volume: pint-metric |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [PIXEL](../android/icu/util/MeasureUnit.md) Constant for unit of graphics: pixel |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [PIXEL_PER_CENTIMETER](../android/icu/util/MeasureUnit.md) Constant for unit of graphics: pixel-per-centimeter |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [PIXEL_PER_INCH](../android/icu/util/MeasureUnit.md) Constant for unit of graphics: pixel-per-inch |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [POINT](../android/icu/util/MeasureUnit.md) Constant for unit of length: point |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [POUND](../android/icu/util/MeasureUnit.md) Constant for unit of mass: pound |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [POUND_PER_SQUARE_INCH](../android/icu/util/MeasureUnit.md) Constant for unit of pressure: pound-force-per-square-inch |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [QUART](../android/icu/util/MeasureUnit.md) Constant for unit of volume: quart |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [QUARTER](../android/icu/util/MeasureUnit.md) Constant for unit of duration: quarter |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [RADIAN](../android/icu/util/MeasureUnit.md) Constant for unit of angle: radian |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [REVOLUTION_ANGLE](../android/icu/util/MeasureUnit.md) Constant for unit of angle: revolution |
| static [TimeUnit](../android/icu/util/TimeUnit.md)! | [SECOND](../android/icu/util/MeasureUnit.md) Constant for unit of duration: second |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [SQUARE_CENTIMETER](../android/icu/util/MeasureUnit.md) Constant for unit of area: square-centimeter |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [SQUARE_FOOT](../android/icu/util/MeasureUnit.md) Constant for unit of area: square-foot |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [SQUARE_INCH](../android/icu/util/MeasureUnit.md) Constant for unit of area: square-inch |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [SQUARE_KILOMETER](../android/icu/util/MeasureUnit.md) Constant for unit of area: square-kilometer |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [SQUARE_METER](../android/icu/util/MeasureUnit.md) Constant for unit of area: square-meter |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [SQUARE_MILE](../android/icu/util/MeasureUnit.md) Constant for unit of area: square-mile |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [SQUARE_YARD](../android/icu/util/MeasureUnit.md) Constant for unit of area: square-yard |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [STONE](../android/icu/util/MeasureUnit.md) Constant for unit of mass: stone |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [TABLESPOON](../android/icu/util/MeasureUnit.md) Constant for unit of volume: tablespoon |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [TEASPOON](../android/icu/util/MeasureUnit.md) Constant for unit of volume: teaspoon |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [TERABIT](../android/icu/util/MeasureUnit.md) Constant for unit of digital: terabit |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [TERABYTE](../android/icu/util/MeasureUnit.md) Constant for unit of digital: terabyte |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [TON](../android/icu/util/MeasureUnit.md) Constant for unit of mass: ton |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [TONNE](../android/icu/util/MeasureUnit.md) Constant for unit of mass: tonne |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [VOLT](../android/icu/util/MeasureUnit.md) Constant for unit of electric: volt |
| --- | --- |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [WATT](../android/icu/util/MeasureUnit.md) Constant for unit of power: watt |
| static [TimeUnit](../android/icu/util/TimeUnit.md)! | [WEEK](../android/icu/util/MeasureUnit.md) Constant for unit of duration: week |
| static [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [YARD](../android/icu/util/MeasureUnit.md) Constant for unit of length: yard |
| --- | --- |
| static [TimeUnit](../android/icu/util/TimeUnit.md)! | [YEAR](../android/icu/util/MeasureUnit.md) Constant for unit of duration: year |

## Public methods

### equals

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### forIdentifier

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun forIdentifier(identifier: String!): MeasureUnit!
```

Construct a MeasureUnit from a CLDR Core Unit Identifier, defined in UTS 35. (Core unit identifiers and mixed unit identifiers are supported, long unit identifiers are not.) Validates and canonicalizes the identifier. Note: dimensionless`MeasureUnit`is`null` 

```kotlin
MeasureUnit example = MeasureUnit::forIdentifier("furlong-per-nanosecond")
  
```

<br />

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------|
| `identifier` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:CLDR Unit Identifier |

| Exceptions ||
|--------------------------------------|-------------------------------|
| `java.lang.IllegalArgumentException` | if the identifier is invalid. |

### getAvailable

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getAvailable(): MutableSet<MeasureUnit!>!
```

Get all of the available units. Returned set is unmodifiable. 

### getAvailable

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getAvailable(type: String!): MutableSet<MeasureUnit!>!
```

For the given type, return the available units.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------|
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the type |

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [MeasureUnit](../android/icu/util/MeasureUnit.md)!>! | the available units for type. Returned set is unmodifiable. |

### getAvailableTypes

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getAvailableTypes(): MutableSet<String!>!
```

Get all of the available units' types. Returned set is unmodifiable. 

### getComplexity

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getComplexity(): MeasureUnit.Complexity!
```

Compute the complexity of the unit. See Complexity for more information.

| Return ||
|-------------------------------------------------------------------------------------------------------------------|----------------------|
| [MeasureUnit.Complexity](../android/icu/util/MeasureUnit.Complexity.md)! | The unit complexity. |

### getDimensionality

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDimensionality(): Int
```

Returns the dimensionality (power) of this MeasureUnit. For example, if the unit is square, then 2 is returned.

NOTE: Only works on SINGLE units. If this is a COMPOUND or MIXED unit, an exception will be thrown. For more information, [Complexity](../android/icu/util/MeasureUnit.Complexity.md).

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The dimensionality (power) of this simple unit. |

| Exceptions ||
|-------------------------------------------|-----------------------------------|
| `java.lang.UnsupportedOperationException` | if the unit is COMPOUND or MIXED. |

### getIdentifier

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIdentifier(): String!
```

Get CLDR Unit Identifier for this MeasureUnit, as defined in UTS 35.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The string form of this unit. |

### getPrefix

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPrefix(): MeasureUnit.MeasurePrefix!
```

Returns the current SI or binary prefix of this SINGLE unit. For example, if the unit has the prefix "kilo", then MeasurePrefix.KILO is returned.

NOTE: Only works on SINGLE units. If this is a COMPOUND or MIXED unit, an error will occur. For more information, [Complexity](../android/icu/util/MeasureUnit.Complexity.md).

| Return ||
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [MeasureUnit.MeasurePrefix](../android/icu/util/MeasureUnit.MeasurePrefix.md)! | The prefix of this SINGLE unit, from MeasurePrefix. |

| Exceptions ||
|-------------------------------------------|-----------------------------------|
| `java.lang.UnsupportedOperationException` | if the unit is COMPOUND or MIXED. |

### getSubtype

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSubtype(): String!
```

Get the subType, such as "foot". May return null. 

### getType

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getType(): String!
```

Get the type, such as "length". May return null. 

### hashCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by [java.util.HashMap](../java/util/HashMap.md).

The general contract of`hashCode`is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the`hashCode`method must consistently return the same integer, provided no information used in`equals`comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the [equals](../java/lang/Object.md))method, then calling the`hashCode`method on each of the two objects must produce the same integer result.
- It is*not* required that if two objects are unequal according to the [equals](../java/lang/Object.md))method, then calling the`hashCode`method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### product

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun product(other: MeasureUnit!): MeasureUnit!
```

Computes the product of this unit with another unit. This is a way to build units from constituent parts.

The numerator and denominator are preserved through this operation.

For example, if the receiver is "kilowatt" and the argument is "hour-per-day", then the unit "kilowatt-hour-per-day" is returned.

NOTE: Only works on SINGLE and COMPOUND units. If either unit (receivee and argument) is a MIXED unit, an error will occur. For more information, [Complexity](../android/icu/util/MeasureUnit.Complexity.md).

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `other` | [MeasureUnit](../android/icu/util/MeasureUnit.md)!:The MeasureUnit to multiply with the target. |

| Return ||
|----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [MeasureUnit](../android/icu/util/MeasureUnit.md)! | The product of the target unit with the provided unit. |

| Exceptions ||
|-------------------------------------------|-----------------------|
| `java.lang.UnsupportedOperationException` | if the unit is MIXED. |

### reciprocal

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reciprocal(): MeasureUnit!
```

Computes the reciprocal of this MeasureUnit, with the numerator and denominator flipped.

For example, if the receiver is "meter-per-second", the unit "second-per-meter" is returned.

NOTE: Only works on SINGLE and COMPOUND units. If this is a MIXED unit, an error will occur. For more information, [Complexity](../android/icu/util/MeasureUnit.Complexity.md).

| Return ||
|----------------------------------------------------------------------------------------------|------------------------------------|
| [MeasureUnit](../android/icu/util/MeasureUnit.md)! | The reciprocal of the target unit. |

| Exceptions ||
|-------------------------------------------|-----------------------|
| `java.lang.UnsupportedOperationException` | if the unit is MIXED. |

### splitToSingleUnits

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun splitToSingleUnits(): MutableList<MeasureUnit!>!
```

Returns the list of SINGLE units contained within a sequence of COMPOUND units.

Examples: - Given "meter-kilogram-per-second", three units will be returned: "meter", "kilogram", and "per-second". - Given "hour+minute+second", three units will be returned: "hour", "minute", and "second".

If this is a SINGLE unit, a list of length 1 will be returned.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [MeasureUnit](../android/icu/util/MeasureUnit.md)!>! | An unmodifiable list of single units |

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### withDimensionality

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun withDimensionality(dimensionality: Int): MeasureUnit!
```

Creates a MeasureUnit which is this SINGLE unit augmented with the specified dimensionality (power). For example, if dimensionality is 2, the unit will be squared.

NOTE: Only works on SINGLE units. If this is a COMPOUND or MIXED unit, an exception is thrown. For more information, [Complexity](../android/icu/util/MeasureUnit.Complexity.md).

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------|
| `dimensionality` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The dimensionality (power). |

| Return ||
|----------------------------------------------------------------------------------------------|--------------------|
| [MeasureUnit](../android/icu/util/MeasureUnit.md)! | A new SINGLE unit. |

| Exceptions ||
|-------------------------------------------|-----------------------------------|
| `java.lang.UnsupportedOperationException` | if the unit is COMPOUND or MIXED. |

### withPrefix

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun withPrefix(prefix: MeasureUnit.MeasurePrefix!): MeasureUnit!
```

Creates a MeasureUnit which is this SINGLE unit augmented with the specified prefix. For example, MeasurePrefix.KILO for "kilo", or MeasurePrefix.KIBI for "kibi". May return`this`if this unit already has that prefix.

There is sufficient locale data to format all standard prefixes.

NOTE: Only works on SINGLE units. If this is a COMPOUND or MIXED unit, an error will occur. For more information, [Complexity](../android/icu/util/MeasureUnit.Complexity.md).

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `prefix` | [MeasureUnit.MeasurePrefix](../android/icu/util/MeasureUnit.MeasurePrefix.md)!:The prefix, from MeasurePrefix. |

| Return ||
|----------------------------------------------------------------------------------------------|--------------------|
| [MeasureUnit](../android/icu/util/MeasureUnit.md)! | A new SINGLE unit. |

| Exceptions ||
|-------------------------------------------|-------------------------------------------|
| `java.lang.UnsupportedOperationException` | if this unit is a COMPOUND or MIXED unit. |

## Properties

### ACRE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACRE: MeasureUnit!
```

Constant for unit of area: acre 

### ACRE_FOOT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACRE_FOOT: MeasureUnit!
```

Constant for unit of volume: acre-foot 

### AMPERE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AMPERE: MeasureUnit!
```

Constant for unit of electric: ampere 

### ARC_MINUTE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ARC_MINUTE: MeasureUnit!
```

Constant for unit of angle: arc-minute 

### ARC_SECOND

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ARC_SECOND: MeasureUnit!
```

Constant for unit of angle: arc-second 

### ASTRONOMICAL_UNIT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ASTRONOMICAL_UNIT: MeasureUnit!
```

Constant for unit of length: astronomical-unit 

### ATMOSPHERE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ATMOSPHERE: MeasureUnit!
```

Constant for unit of pressure: atmosphere 

### BEAUFORT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BEAUFORT: MeasureUnit!
```

Constant for unit of speed: beaufort 

### BIT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BIT: MeasureUnit!
```

Constant for unit of digital: bit 

### BUSHEL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BUSHEL: MeasureUnit!
```

Constant for unit of volume: bushel 

### BYTE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BYTE: MeasureUnit!
```

Constant for unit of digital: byte 

### CALORIE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CALORIE: MeasureUnit!
```

Constant for unit of energy: calorie 

### CANDELA

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CANDELA: MeasureUnit!
```

Constant for unit of light: candela 

### CARAT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CARAT: MeasureUnit!
```

Constant for unit of mass: carat 

### CELSIUS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CELSIUS: MeasureUnit!
```

Constant for unit of temperature: celsius 

### CENTILITER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CENTILITER: MeasureUnit!
```

Constant for unit of volume: centiliter 

### CENTIMETER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CENTIMETER: MeasureUnit!
```

Constant for unit of length: centimeter 

### CENTURY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CENTURY: MeasureUnit!
```

Constant for unit of duration: century 

### CUBIC_CENTIMETER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CUBIC_CENTIMETER: MeasureUnit!
```

Constant for unit of volume: cubic-centimeter 

### CUBIC_FOOT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CUBIC_FOOT: MeasureUnit!
```

Constant for unit of volume: cubic-foot 

### CUBIC_INCH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CUBIC_INCH: MeasureUnit!
```

Constant for unit of volume: cubic-inch 

### CUBIC_KILOMETER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CUBIC_KILOMETER: MeasureUnit!
```

Constant for unit of volume: cubic-kilometer 

### CUBIC_METER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CUBIC_METER: MeasureUnit!
```

Constant for unit of volume: cubic-meter 

### CUBIC_MILE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CUBIC_MILE: MeasureUnit!
```

Constant for unit of volume: cubic-mile 

### CUBIC_YARD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CUBIC_YARD: MeasureUnit!
```

Constant for unit of volume: cubic-yard 

### CUP

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CUP: MeasureUnit!
```

Constant for unit of volume: cup 

### CUP_METRIC

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CUP_METRIC: MeasureUnit!
```

Constant for unit of volume: cup-metric 

### DAY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DAY: TimeUnit!
```

Constant for unit of duration: day 

### DECADE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DECADE: MeasureUnit!
```

Constant for unit of duration: decade 

### DECILITER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DECILITER: MeasureUnit!
```

Constant for unit of volume: deciliter 

### DECIMETER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DECIMETER: MeasureUnit!
```

Constant for unit of length: decimeter 

### DEGREE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEGREE: MeasureUnit!
```

Constant for unit of angle: degree 

### DOT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DOT: MeasureUnit!
```

Constant for unit of graphics: dot 

### DOT_PER_CENTIMETER

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DOT_PER_CENTIMETER: MeasureUnit!
```

Constant for unit of graphics: dot-per-centimeter 

### DOT_PER_INCH

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DOT_PER_INCH: MeasureUnit!
```

Constant for unit of graphics: dot-per-inch 

### EM

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EM: MeasureUnit!
```

Constant for unit of graphics: em 

### FAHRENHEIT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FAHRENHEIT: MeasureUnit!
```

Constant for unit of temperature: fahrenheit 

### FATHOM

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FATHOM: MeasureUnit!
```

Constant for unit of length: fathom 

### FLUID_OUNCE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLUID_OUNCE: MeasureUnit!
```

Constant for unit of volume: fluid-ounce 

### FOODCALORIE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FOODCALORIE: MeasureUnit!
```

Constant for unit of energy: foodcalorie 

### FOOT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FOOT: MeasureUnit!
```

Constant for unit of length: foot 

### FURLONG

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FURLONG: MeasureUnit!
```

Constant for unit of length: furlong 

### GALLON

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GALLON: MeasureUnit!
```

Constant for unit of volume: gallon 

### GALLON_IMPERIAL

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GALLON_IMPERIAL: MeasureUnit!
```

Constant for unit of volume: gallon-imperial 

### GASOLINE_ENERGY_DENSITY

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GASOLINE_ENERGY_DENSITY: MeasureUnit!
```

Constant for unit of pressure: gasoline-energy-density 

### GENERIC_TEMPERATURE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GENERIC_TEMPERATURE: MeasureUnit!
```

Constant for unit of temperature: generic 

### GIGABIT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GIGABIT: MeasureUnit!
```

Constant for unit of digital: gigabit 

### GIGABYTE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GIGABYTE: MeasureUnit!
```

Constant for unit of digital: gigabyte 

### GIGAHERTZ

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GIGAHERTZ: MeasureUnit!
```

Constant for unit of frequency: gigahertz 

### GIGAWATT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GIGAWATT: MeasureUnit!
```

Constant for unit of power: gigawatt 

### GRAM

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GRAM: MeasureUnit!
```

Constant for unit of mass: gram 

### G_FORCE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val G_FORCE: MeasureUnit!
```

Constant for unit of acceleration: g-force 

### HECTARE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HECTARE: MeasureUnit!
```

Constant for unit of area: hectare 

### HECTOLITER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HECTOLITER: MeasureUnit!
```

Constant for unit of volume: hectoliter 

### HECTOPASCAL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HECTOPASCAL: MeasureUnit!
```

Constant for unit of pressure: hectopascal 

### HERTZ

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HERTZ: MeasureUnit!
```

Constant for unit of frequency: hertz 

### HORSEPOWER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HORSEPOWER: MeasureUnit!
```

Constant for unit of power: horsepower 

### HOUR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HOUR: TimeUnit!
```

Constant for unit of duration: hour 

### INCH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INCH: MeasureUnit!
```

Constant for unit of length: inch 

### INCH_HG

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INCH_HG: MeasureUnit!
```

Constant for unit of pressure: inch-ofhg 

### ITEM

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ITEM: MeasureUnit!
```

Constant for unit of concentr: item 

### JOULE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val JOULE: MeasureUnit!
```

Constant for unit of energy: joule 

### KARAT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KARAT: MeasureUnit!
```

Constant for unit of concentr: karat 

### KELVIN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KELVIN: MeasureUnit!
```

Constant for unit of temperature: kelvin 

### KILOBIT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KILOBIT: MeasureUnit!
```

Constant for unit of digital: kilobit 

### KILOBYTE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KILOBYTE: MeasureUnit!
```

Constant for unit of digital: kilobyte 

### KILOCALORIE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KILOCALORIE: MeasureUnit!
```

Constant for unit of energy: kilocalorie 

### KILOGRAM

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KILOGRAM: MeasureUnit!
```

Constant for unit of mass: kilogram 

### KILOHERTZ

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KILOHERTZ: MeasureUnit!
```

Constant for unit of frequency: kilohertz 

### KILOJOULE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KILOJOULE: MeasureUnit!
```

Constant for unit of energy: kilojoule 

### KILOMETER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KILOMETER: MeasureUnit!
```

Constant for unit of length: kilometer 

### KILOMETER_PER_HOUR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KILOMETER_PER_HOUR: MeasureUnit!
```

Constant for unit of speed: kilometer-per-hour 

### KILOWATT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KILOWATT: MeasureUnit!
```

Constant for unit of power: kilowatt 

### KILOWATT_HOUR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KILOWATT_HOUR: MeasureUnit!
```

Constant for unit of energy: kilowatt-hour 

### KILOWATT_HOUR_PER_100_KILOMETER

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KILOWATT_HOUR_PER_100_KILOMETER: MeasureUnit!
```

Constant for unit of force: kilowatt-hour-per-100-kilometer 

### KNOT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KNOT: MeasureUnit!
```

Constant for unit of speed: knot 

### LIGHT_YEAR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LIGHT_YEAR: MeasureUnit!
```

Constant for unit of length: light-year 

### LITER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LITER: MeasureUnit!
```

Constant for unit of volume: liter 

### LITER_PER_100KILOMETERS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LITER_PER_100KILOMETERS: MeasureUnit!
```

Constant for unit of consumption: liter-per-100-kilometer 

### LITER_PER_KILOMETER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LITER_PER_KILOMETER: MeasureUnit!
```

Constant for unit of consumption: liter-per-kilometer 

### LUMEN

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LUMEN: MeasureUnit!
```

Constant for unit of light: lumen 

### LUX

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LUX: MeasureUnit!
```

Constant for unit of light: lux 

### MEGABIT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEGABIT: MeasureUnit!
```

Constant for unit of digital: megabit 

### MEGABYTE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEGABYTE: MeasureUnit!
```

Constant for unit of digital: megabyte 

### MEGAHERTZ

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEGAHERTZ: MeasureUnit!
```

Constant for unit of frequency: megahertz 

### MEGALITER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEGALITER: MeasureUnit!
```

Constant for unit of volume: megaliter 

### MEGAPIXEL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEGAPIXEL: MeasureUnit!
```

Constant for unit of graphics: megapixel 

### MEGAWATT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEGAWATT: MeasureUnit!
```

Constant for unit of power: megawatt 

### METER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METER: MeasureUnit!
```

Constant for unit of length: meter 

### METER_PER_SECOND

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METER_PER_SECOND: MeasureUnit!
```

Constant for unit of speed: meter-per-second 

### METER_PER_SECOND_SQUARED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METER_PER_SECOND_SQUARED: MeasureUnit!
```

Constant for unit of acceleration: meter-per-square-second 

### METRIC_TON

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METRIC_TON: MeasureUnit!
```

Constant for unit of mass: metric-ton (renamed to tonne in CLDR 42 / ICU 72). Note: In ICU 74 this will be deprecated in favor of TONNE, which is currently draft but will become stable in ICU 74, and which uses the preferred naming. 

### MICROGRAM

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MICROGRAM: MeasureUnit!
```

Constant for unit of mass: microgram 

### MICROMETER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MICROMETER: MeasureUnit!
```

Constant for unit of length: micrometer 

### MICROSECOND

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MICROSECOND: MeasureUnit!
```

Constant for unit of duration: microsecond 

### MILE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MILE: MeasureUnit!
```

Constant for unit of length: mile 

### MILE_PER_GALLON

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MILE_PER_GALLON: MeasureUnit!
```

Constant for unit of consumption: mile-per-gallon 

### MILE_PER_GALLON_IMPERIAL

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MILE_PER_GALLON_IMPERIAL: MeasureUnit!
```

Constant for unit of consumption: mile-per-gallon-imperial 

### MILE_PER_HOUR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MILE_PER_HOUR: MeasureUnit!
```

Constant for unit of speed: mile-per-hour 

### MILE_SCANDINAVIAN

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MILE_SCANDINAVIAN: MeasureUnit!
```

Constant for unit of length: mile-scandinavian 

### MILLIAMPERE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MILLIAMPERE: MeasureUnit!
```

Constant for unit of electric: milliampere 

### MILLIBAR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MILLIBAR: MeasureUnit!
```

Constant for unit of pressure: millibar 

### MILLIGRAM

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MILLIGRAM: MeasureUnit!
```

Constant for unit of mass: milligram 

### MILLIGRAM_OFGLUCOSE_PER_DECILITER

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MILLIGRAM_OFGLUCOSE_PER_DECILITER: MeasureUnit!
```

Constant for unit of concentr: milligram-ofglucose-per-deciliter 

### MILLIGRAM_PER_DECILITER

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MILLIGRAM_PER_DECILITER: MeasureUnit!
```

Constant for unit of concentr: milligram-per-deciliter 

### MILLILITER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MILLILITER: MeasureUnit!
```

Constant for unit of volume: milliliter 

### MILLIMETER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MILLIMETER: MeasureUnit!
```

Constant for unit of length: millimeter 

### MILLIMETER_OF_MERCURY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MILLIMETER_OF_MERCURY: MeasureUnit!
```

Constant for unit of pressure: millimeter-ofhg 

### MILLIMOLE_PER_LITER

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MILLIMOLE_PER_LITER: MeasureUnit!
```

Constant for unit of concentr: millimole-per-liter 

### MILLISECOND

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MILLISECOND: MeasureUnit!
```

Constant for unit of duration: millisecond 

### MILLIWATT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MILLIWATT: MeasureUnit!
```

Constant for unit of power: milliwatt 

### MINUTE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MINUTE: TimeUnit!
```

Constant for unit of duration: minute 

### MONTH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MONTH: TimeUnit!
```

Constant for unit of duration: month 

### NANOMETER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NANOMETER: MeasureUnit!
```

Constant for unit of length: nanometer 

### NANOSECOND

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NANOSECOND: MeasureUnit!
```

Constant for unit of duration: nanosecond 

### NAUTICAL_MILE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NAUTICAL_MILE: MeasureUnit!
```

Constant for unit of length: nautical-mile 

### OHM

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OHM: MeasureUnit!
```

Constant for unit of electric: ohm 

### OUNCE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OUNCE: MeasureUnit!
```

Constant for unit of mass: ounce 

### OUNCE_TROY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OUNCE_TROY: MeasureUnit!
```

Constant for unit of mass: ounce-troy 

### PARSEC

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PARSEC: MeasureUnit!
```

Constant for unit of length: parsec 

### PART_PER_MILLION

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PART_PER_MILLION: MeasureUnit!
```

Constant for unit of concentr: permillion 

### PERCENT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PERCENT: MeasureUnit!
```

Constant for unit of concentr: percent 

### PERMILLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PERMILLE: MeasureUnit!
```

Constant for unit of concentr: permille 

### PETABYTE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PETABYTE: MeasureUnit!
```

Constant for unit of digital: petabyte 

### PICOMETER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PICOMETER: MeasureUnit!
```

Constant for unit of length: picometer 

### PINT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PINT: MeasureUnit!
```

Constant for unit of volume: pint 

### PINT_METRIC

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PINT_METRIC: MeasureUnit!
```

Constant for unit of volume: pint-metric 

### PIXEL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PIXEL: MeasureUnit!
```

Constant for unit of graphics: pixel 

### PIXEL_PER_CENTIMETER

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PIXEL_PER_CENTIMETER: MeasureUnit!
```

Constant for unit of graphics: pixel-per-centimeter 

### PIXEL_PER_INCH

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PIXEL_PER_INCH: MeasureUnit!
```

Constant for unit of graphics: pixel-per-inch 

### POINT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val POINT: MeasureUnit!
```

Constant for unit of length: point 

### POUND

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val POUND: MeasureUnit!
```

Constant for unit of mass: pound 

### POUND_PER_SQUARE_INCH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val POUND_PER_SQUARE_INCH: MeasureUnit!
```

Constant for unit of pressure: pound-force-per-square-inch 

### QUART

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUART: MeasureUnit!
```

Constant for unit of volume: quart 

### QUARTER

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUARTER: MeasureUnit!
```

Constant for unit of duration: quarter 

### RADIAN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RADIAN: MeasureUnit!
```

Constant for unit of angle: radian 

### REVOLUTION_ANGLE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REVOLUTION_ANGLE: MeasureUnit!
```

Constant for unit of angle: revolution 

### SECOND

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECOND: TimeUnit!
```

Constant for unit of duration: second 

### SQUARE_CENTIMETER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SQUARE_CENTIMETER: MeasureUnit!
```

Constant for unit of area: square-centimeter 

### SQUARE_FOOT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SQUARE_FOOT: MeasureUnit!
```

Constant for unit of area: square-foot 

### SQUARE_INCH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SQUARE_INCH: MeasureUnit!
```

Constant for unit of area: square-inch 

### SQUARE_KILOMETER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SQUARE_KILOMETER: MeasureUnit!
```

Constant for unit of area: square-kilometer 

### SQUARE_METER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SQUARE_METER: MeasureUnit!
```

Constant for unit of area: square-meter 

### SQUARE_MILE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SQUARE_MILE: MeasureUnit!
```

Constant for unit of area: square-mile 

### SQUARE_YARD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SQUARE_YARD: MeasureUnit!
```

Constant for unit of area: square-yard 

### STONE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STONE: MeasureUnit!
```

Constant for unit of mass: stone 

### TABLESPOON

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TABLESPOON: MeasureUnit!
```

Constant for unit of volume: tablespoon 

### TEASPOON

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TEASPOON: MeasureUnit!
```

Constant for unit of volume: teaspoon 

### TERABIT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TERABIT: MeasureUnit!
```

Constant for unit of digital: terabit 

### TERABYTE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TERABYTE: MeasureUnit!
```

Constant for unit of digital: terabyte 

### TON

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TON: MeasureUnit!
```

Constant for unit of mass: ton 

### TONNE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONNE: MeasureUnit!
```

Constant for unit of mass: tonne 

### VOLT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VOLT: MeasureUnit!
```

Constant for unit of electric: volt 

### WATT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WATT: MeasureUnit!
```

Constant for unit of power: watt 

### WEEK

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WEEK: TimeUnit!
```

Constant for unit of duration: week 

### YARD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val YARD: MeasureUnit!
```

Constant for unit of length: yard 

### YEAR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val YEAR: TimeUnit!
```

Constant for unit of duration: year
