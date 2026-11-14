# TvContentRating

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TvContentRating

Kotlin| [Java](https://developer.android.com/reference/android/media/tv/TvContentRating "View this page in Java") 

```
class TvContentRating
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.media.tv.TvContentRating](https://developer.android.com/reference/kotlin/android/media/tv/TvContentRating#) |

A class representing a TV content rating. When a TV input service inserts the content rating information on a program into the database, this class can be used to generate the formatted string for [TvContract.Programs.COLUMN_CONTENT_RATING](https://developer.android.com/reference/kotlin/android/media/tv/TvContract.Programs#COLUMN_CONTENT_RATING:kotlin.String). To create a object, use the [TvContentRating.createRating](https://developer.android.com/reference/kotlin/android/media/tv/TvContentRating#createRating(kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String))method with valid rating system string constants.

It is possible for an application to define its own content rating system by supplying a content rating system definition XML resource (see example below) and declaring a broadcast receiver that filters [TvInputManager.ACTION_QUERY_CONTENT_RATING_SYSTEMS](https://developer.android.com/reference/kotlin/android/media/tv/TvInputManager#ACTION_QUERY_CONTENT_RATING_SYSTEMS:kotlin.String) in its manifest.

### Example: Rating system definition for the TV Parental Guidelines

The following XML example shows how the TV Parental Guidelines in the United States can be defined:

<br />

```kotlin
<rating-system-definitions xmlns:android="http://schemas.android.com/apk/res/android"
      android:versionCode="1">
      <rating-system-definition android:name="US_TV"
          android:country="US"
          android:description="@string/description_us_tv">
          <sub-rating-definition android:name="US_TV_D"
              android:title="D"
              android:description="@string/description_us_tv_d" />
          <sub-rating-definition android:name="US_TV_L"
              android:title="L"
              android:description="@string/description_us_tv_l" />
          <sub-rating-definition android:name="US_TV_S"
              android:title="S"
              android:description="@string/description_us_tv_s" />
          <sub-rating-definition android:name="US_TV_V"
              android:title="V"
              android:description="@string/description_us_tv_v" />
          <sub-rating-definition android:name="US_TV_FV"
              android:title="FV"
              android:description="@string/description_us_tv_fv" />
 
          <rating-definition android:name="US_TV_Y"
              android:title="TV-Y"
              android:description="@string/description_us_tv_y"
              android:icon="@drawable/icon_us_tv_y"
              android:contentAgeHint="0" />
          <rating-definition android:name="US_TV_Y7"
              android:title="TV-Y7"
              android:description="@string/description_us_tv_y7"
              android:icon="@drawable/icon_us_tv_y7"
              android:contentAgeHint="7">
              <sub-rating android:name="US_TV_FV" />
          </rating-definition>
          <rating-definition android:name="US_TV_G"
              android:title="TV-G"
              android:description="@string/description_us_tv_g"
              android:icon="@drawable/icon_us_tv_g"
              android:contentAgeHint="0" />
          <rating-definition android:name="US_TV_PG"
              android:title="TV-PG"
              android:description="@string/description_us_tv_pg"
              android:icon="@drawable/icon_us_tv_pg"
              android:contentAgeHint="14">
              <sub-rating android:name="US_TV_D" />
              <sub-rating android:name="US_TV_L" />
              <sub-rating android:name="US_TV_S" />
              <sub-rating android:name="US_TV_V" />
          </rating-definition>
          <rating-definition android:name="US_TV_14"
              android:title="TV-14"
              android:description="@string/description_us_tv_14"
              android:icon="@drawable/icon_us_tv_14"
              android:contentAgeHint="14">
              <sub-rating android:name="US_TV_D" />
              <sub-rating android:name="US_TV_L" />
              <sub-rating android:name="US_TV_S" />
              <sub-rating android:name="US_TV_V" />
          </rating-definition>
          <rating-definition android:name="US_TV_MA"
              android:title="TV-MA"
              android:description="@string/description_us_tv_ma"
              android:icon="@drawable/icon_us_tv_ma"
              android:contentAgeHint="17">
              <sub-rating android:name="US_TV_L" />
              <sub-rating android:name="US_TV_S" />
              <sub-rating android:name="US_TV_V" />
          </rating-definition>
          <rating-order>
              <rating android:name="US_TV_Y" />
              <rating android:name="US_TV_Y7" />
          </rating-order>
          <rating-order>
              <rating android:name="US_TV_G" />
              <rating android:name="US_TV_PG" />
              <rating android:name="US_TV_14" />
              <rating android:name="US_TV_MA" />
          </rating-order>
      </rating-system-definition>
  </rating-system-definitions>
```

### System defined rating strings

The following strings are defined by the system to provide a standard way to create`TvContentRating`objects.

For example, to create an object that represents TV-PG rating with suggestive dialogue and coarse language from the TV Parental Guidelines in the United States, one can use the following code snippet: 

```kotlin
TvContentRating rating = TvContentRating.createRating(
          "com.android.tv",
          "US_TV",
          "US_TV_PG",
          "US_TV_D", "US_TV_L");
  
```

#### System defined string for domains

| Constant Value | Description |
|----------------|--------------------------------------------------|
| com.android.tv | Used for creating system defined content ratings |

#### System defined strings for rating systems

| Constant Value | Description |
|----------------|---------------------------------------------------|
| AR_TV | TV content rating system for Argentina |
| AU_TV | TV content rating system for Australia |
| BR_TV | TV content rating system for Brazil |
| CA_TV_EN | TV content rating system for Canada (English) |
| CA_TV_FR | TV content rating system for Canada (French) |
| DTMB | DTMB content rating system |
| DVB | DVB content rating system |
| ES_DVB | DVB content rating system for Spain |
| FR_DVB | DVB content rating system for France |
| ISDB | ISDB content rating system |
| KR_TV | TV content rating system for South Korea |
| NZ_TV | TV content rating system for New Zealand |
| SG_TV | TV content rating system for Singapore |
| TH_TV | TV content rating system for Thailand |
| US_MV | Movie content rating system for the United States |
| US_TV | TV content rating system for the United States |

#### System defined strings for ratings

| Rating System | Constant Value | Description |
|---------------|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AR_TV | AR_TV_ATP | Suitable for all audiences. Programs may contain mild violence, language and mature situations |
| AR_TV | AR_TV_SAM_13 | Suitable for ages 13 and up. Programs may contain mild to moderate language and mild violence and sexual references |
| AR_TV | AR_TV_SAM_16 | Suitable for ages 16 and up. Programs may contain more intensive violence and coarse language, partial nudity and moderate sexual references |
| AR_TV | AR_TV_SAM_18 | Suitable for mature audiences only. Programs contain strong violence, coarse language and explicit sexual references |
| AU_TV | AU_TV_P | Recommended for younger children aged between 2 and 11 years |
| AU_TV | AU_TV_C | Recommended for older children aged between 5 and 14 years |
| AU_TV | AU_TV_G | Recommended for all ages |
| AU_TV | AU_TV_PG | Parental guidance is recommended for young viewers under 15 |
| AU_TV | AU_TV_M | Recommended for mature audiences aged 15 years and over |
| AU_TV | AU_TV_MA | Not suitable for children and teens under 15, due to sexual descriptions, course language, adult themes or drug use |
| AU_TV | AU_TV_AV | Not suitable for children and teens under 15. This category is used specifically for violent programs |
| AU_TV | AU_TV_R | Not for children under 18. Content may include graphic violence, sexual situations, coarse language and explicit drug use |
| BR_TV | BR_TV_L | Content is suitable for all audiences |
| BR_TV | BR_TV_10 | Content suitable for viewers over the age of 10 |
| BR_TV | BR_TV_12 | Content suitable for viewers over the age of 12 |
| BR_TV | BR_TV_14 | Content suitable for viewers over the age of 14 |
| BR_TV | BR_TV_16 | Content suitable for viewers over the age of 16 |
| BR_TV | BR_TV_18 | Content suitable for viewers over the age of 18 |
| CA_TV_EN | CA_TV_EN_EXEMPT | Exempt from ratings |
| CA_TV_EN | CA_TV_EN_C | Suitable for children ages 2--7 |
| CA_TV_EN | CA_TV_EN_C8 | Suitable for children ages 8 and older |
| CA_TV_EN | CA_TV_EN_G | Suitable for the entire family |
| CA_TV_EN | CA_TV_EN_PG | May contain moderate violence, profanity, nudity, and sexual references |
| CA_TV_EN | CA_TV_EN_14 | Intended for viewers ages 14 and older |
| CA_TV_EN | CA_TV_EN_18 | Intended for viewers ages 18 and older |
| CA_TV_FR | CA_TV_FR_E | Exempt from ratings |
| CA_TV_FR | CA_TV_FR_G | Appropriate for all ages |
| CA_TV_FR | CA_TV_FR_8 | Appropriate for children 8 |
| CA_TV_FR | CA_TV_FR_13 | Suitable for children 13 |
| CA_TV_FR | CA_TV_FR_16 | Recommended for children over the age of 16 |
| CA_TV_FR | CA_TV_FR_18 | Only to be viewed by adults |
| DTMB | DTMB_4 | Recommended for ages 4 and over |
| DTMB | DTMB_5 | Recommended for ages 5 and over |
| DTMB | DTMB_6 | Recommended for ages 6 and over |
| DTMB | DTMB_7 | Recommended for ages 7 and over |
| DTMB | DTMB_8 | Recommended for ages 8 and over |
| DTMB | DTMB_9 | Recommended for ages 9 and over |
| DTMB | DTMB_10 | Recommended for ages 10 and over |
| DTMB | DTMB_11 | Recommended for ages 11 and over |
| DTMB | DTMB_12 | Recommended for ages 12 and over |
| DTMB | DTMB_13 | Recommended for ages 13 and over |
| DTMB | DTMB_14 | Recommended for ages 14 and over |
| DTMB | DTMB_15 | Recommended for ages 15 and over |
| DTMB | DTMB_16 | Recommended for ages 16 and over |
| DTMB | DTMB_17 | Recommended for ages 17 and over |
| DTMB | DTMB_18 | Recommended for ages 18 and over |
| DVB | DVB_4 | Recommended for ages 4 and over |
| DVB | DVB_5 | Recommended for ages 5 and over |
| DVB | DVB_6 | Recommended for ages 6 and over |
| DVB | DVB_7 | Recommended for ages 7 and over |
| DVB | DVB_8 | Recommended for ages 8 and over |
| DVB | DVB_9 | Recommended for ages 9 and over |
| DVB | DVB_10 | Recommended for ages 10 and over |
| DVB | DVB_11 | Recommended for ages 11 and over |
| DVB | DVB_12 | Recommended for ages 12 and over |
| DVB | DVB_13 | Recommended for ages 13 and over |
| DVB | DVB_14 | Recommended for ages 14 and over |
| DVB | DVB_15 | Recommended for ages 15 and over |
| DVB | DVB_16 | Recommended for ages 16 and over |
| DVB | DVB_17 | Recommended for ages 17 and over |
| DVB | DVB_18 | Recommended for ages 18 and over |
| ES_DVB | ES_DVB_ALL | Recommended for all ages |
| ES_DVB | ES_DVB_C | Recommended for children |
| ES_DVB | ES_DVB_X | Recommended for adults |
| ES_DVB | ES_DVB_4 | Recommended for ages 4 and over |
| ES_DVB | ES_DVB_5 | Recommended for ages 5 and over |
| ES_DVB | ES_DVB_6 | Recommended for ages 6 and over |
| ES_DVB | ES_DVB_7 | Recommended for ages 7 and over |
| ES_DVB | ES_DVB_8 | Recommended for ages 8 and over |
| ES_DVB | ES_DVB_9 | Recommended for ages 9 and over |
| ES_DVB | ES_DVB_10 | Recommended for ages 10 and over |
| ES_DVB | ES_DVB_11 | Recommended for ages 11 and over |
| ES_DVB | ES_DVB_12 | Recommended for ages 12 and over |
| ES_DVB | ES_DVB_13 | Recommended for ages 13 and over |
| ES_DVB | ES_DVB_14 | Recommended for ages 14 and over |
| ES_DVB | ES_DVB_15 | Recommended for ages 15 and over |
| ES_DVB | ES_DVB_16 | Recommended for ages 16 and over |
| ES_DVB | ES_DVB_17 | Recommended for ages 17 and over |
| ES_DVB | ES_DVB_18 | Recommended for ages 18 and over |
| FR_DVB | FR_DVB_U | Recommended for all ages |
| FR_DVB | FR_DVB_4 | Recommended for ages 4 and over |
| FR_DVB | FR_DVB_5 | Recommended for ages 5 and over |
| FR_DVB | FR_DVB_6 | Recommended for ages 6 and over |
| FR_DVB | FR_DVB_7 | Recommended for ages 7 and over |
| FR_DVB | FR_DVB_8 | Recommended for ages 8 and over |
| FR_DVB | FR_DVB_9 | Recommended for ages 9 and over |
| FR_DVB | FR_DVB_10 | Recommended for ages 10 and over |
| FR_DVB | FR_DVB_11 | Recommended for ages 11 and over |
| FR_DVB | FR_DVB_12 | Recommended for ages 12 and over |
| FR_DVB | FR_DVB_13 | Recommended for ages 13 and over |
| FR_DVB | FR_DVB_14 | Recommended for ages 14 and over |
| FR_DVB | FR_DVB_15 | Recommended for ages 15 and over |
| FR_DVB | FR_DVB_16 | Recommended for ages 16 and over |
| FR_DVB | FR_DVB_17 | Recommended for ages 17 and over |
| FR_DVB | FR_DVB_18 | Recommended for ages 18 and over |
| ISDB | ISDB_4 | Recommended for ages 4 and over |
| ISDB | ISDB_5 | Recommended for ages 5 and over |
| ISDB | ISDB_6 | Recommended for ages 6 and over |
| ISDB | ISDB_7 | Recommended for ages 7 and over |
| ISDB | ISDB_8 | Recommended for ages 8 and over |
| ISDB | ISDB_9 | Recommended for ages 9 and over |
| ISDB | ISDB_10 | Recommended for ages 10 and over |
| ISDB | ISDB_11 | Recommended for ages 11 and over |
| ISDB | ISDB_12 | Recommended for ages 12 and over |
| ISDB | ISDB_13 | Recommended for ages 13 and over |
| ISDB | ISDB_14 | Recommended for ages 14 and over |
| ISDB | ISDB_15 | Recommended for ages 15 and over |
| ISDB | ISDB_16 | Recommended for ages 16 and over |
| ISDB | ISDB_17 | Recommended for ages 17 and over |
| ISDB | ISDB_18 | Recommended for ages 18 and over |
| ISDB | ISDB_19 | Recommended for ages 19 and over |
| ISDB | ISDB_20 | Recommended for ages 20 and over |
| KR_TV | KR_TV_ALL | Appropriate for all ages |
| KR_TV | KR_TV_7 | May contain material inappropriate for children younger than 7, and parental discretion should be used |
| KR_TV | KR_TV_12 | May deemed inappropriate for those younger than 12, and parental discretion should be used |
| KR_TV | KR_TV_15 | May be inappropriate for children under 15, and that parental discretion should be used |
| KR_TV | KR_TV_19 | For adults only |
| NZ_TV | NZ_TV_G | Programmes which exclude material likely to be unsuitable for children. Programmes may not necessarily be designed for child viewers but should not contain material likely to alarm or distress them |
| NZ_TV | NZ_TV_PGR | Programmes containing material more suited for mature audiences but not necessarily unsuitable for child viewers when subject to the guidance of a parent or an adult |
| NZ_TV | NZ_TV_AO | Programmes containing adult themes and directed primarily at mature audiences |
| SG_TV | SG_TV_G | Suitable for all ages |
| SG_TV | SG_TV_PG | Suitable for all but parents should guide their young |
| SG_TV | SG_TV_PG13 | Suitable for persons aged 13 and above but parental guidance is advised for children below 13 |
| SG_TV | SG_TV_NC16 | Suitable for persons aged 16 and above |
| SG_TV | SG_TV_M18 | Suitable for persons aged 18 and above |
| SG_TV | SG_TV_R21 | Suitable for adults aged 21 and above |
| TH_TV | TH_TV_4 | Suitable for audiences 3 to 5 years of age |
| TH_TV | TH_TV_6 | Suitable for audiences 6 to 12 years of age |
| TH_TV | TH_TV_10 | Suitable for all audiences |
| TH_TV | TH_TV_13 | Parental guidance suggested for viewers age below 13 |
| TH_TV | TH_TV_18 | Parental guidance suggested for viewers age below 18 |
| TH_TV | TH_TV_19 | Not suitable for children and teenagers |
| US_MV | US_MV_G | General audiences |
| US_MV | US_MV_PG | Parental guidance suggested |
| US_MV | US_MV_PG13 | Parents strongly cautioned |
| US_MV | US_MV_R | Restricted, under 17 requires accompanying parent or adult guardian |
| US_MV | US_MV_NC17 | No one 17 and under admitted |
| US_TV | US_TV_Y | This program is designed to be appropriate for all children |
| US_TV | US_TV_Y7 | This program is designed for children age 7 and above |
| US_TV | US_TV_G | Most parents would find this program suitable for all ages |
| US_TV | US_TV_PG | This program contains material that parents may find unsuitable for younger children |
| US_TV | US_TV_14 | This program contains some material that many parents would find unsuitable for children under 14 years of age |
| US_TV | US_TV_MA | This program is specifically designed to be viewed by adults and therefore may be unsuitable for children under 17 |

#### System defined strings for sub-ratings

| Rating System | Constant Value | Description |
|---------------|----------------|------------------------------------------------------------------------------------------|
| BR_TV | BR_TV_D | Drugs Applicable to BR_TV_L, BR_TV_10, BR_TV_12, BR_TV_14, BR_TV_16, and BR_TV_18 |
| BR_TV | BR_TV_S | Sex Applicable to BR_TV_L, BR_TV_10, BR_TV_12, BR_TV_14, BR_TV_16, and BR_TV_18 |
| BR_TV | BR_TV_V | Violence Applicable to BR_TV_L, BR_TV_10, BR_TV_12, BR_TV_14, BR_TV_16, and BR_TV_18 |
| US_TV | US_TV_D | Suggestive dialogue (Usually means talks about sex) Applicable to US_TV_PG, and US_TV_14 |
| US_TV | US_TV_L | Coarse language Applicable to US_TV_PG, US_TV_14, and US_TV_MA |
| US_TV | US_TV_S | Sexual content Applicable to US_TV_PG, US_TV_14, and US_TV_MA |
| US_TV | US_TV_V | Violence Applicable to US_TV_PG, US_TV_14, and US_TV_MA |
| US_TV | US_TV_FV | Fantasy violence (Children's programming only) Applicable to US_TV_Y7 |

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](https://developer.android.com/reference/kotlin/android/media/tv/TvContentRating#contains(android.media.tv.TvContentRating))`(`rating:` ` [TvContentRating](https://developer.android.com/reference/kotlin/android/media/tv/TvContentRating#)`)` Returns`true`if this rating has the same main rating as the specified rating and when this rating's sub-ratings contain the other's. |
| static [TvContentRating](https://developer.android.com/reference/kotlin/android/media/tv/TvContentRating#)! | [createRating](https://developer.android.com/reference/kotlin/android/media/tv/TvContentRating#createRating(kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String))`(`domain:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `ratingSystem:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `rating:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vararg` `subRatings:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a`TvContentRating`object with predefined content rating strings. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/media/tv/TvContentRating#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [flattenToString](https://developer.android.com/reference/kotlin/android/media/tv/TvContentRating#flattenToString())`()` Returns a string that unambiguously describes the rating information contained in a`TvContentRating`object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDomain](https://developer.android.com/reference/kotlin/android/media/tv/TvContentRating#getDomain())`()` Returns the domain of this`TvContentRating`object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getMainRating](https://developer.android.com/reference/kotlin/android/media/tv/TvContentRating#getMainRating())`()` Returns the main rating of this`TvContentRating`object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getRatingSystem](https://developer.android.com/reference/kotlin/android/media/tv/TvContentRating#getRatingSystem())`()` Returns the rating system of this`TvContentRating`object. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getSubRatings](https://developer.android.com/reference/kotlin/android/media/tv/TvContentRating#getSubRatings())`()` Returns the unmodifiable sub-rating string [List](https://developer.android.com/reference/kotlin/java/util/List.html#) of this`TvContentRating`object. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/media/tv/TvContentRating#hashCode())`()` <br /> |
| static [TvContentRating](https://developer.android.com/reference/kotlin/android/media/tv/TvContentRating#)! | [unflattenFromString](https://developer.android.com/reference/kotlin/android/media/tv/TvContentRating#unflattenFromString(kotlin.String))`(`ratingString:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Recovers a`TvContentRating`object from the string that was previously created from [flattenToString](https://developer.android.com/reference/kotlin/android/media/tv/TvContentRating#flattenToString()). |

| Properties ||
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [TvContentRating](https://developer.android.com/reference/kotlin/android/media/tv/TvContentRating#)! | [UNRATED](https://developer.android.com/reference/kotlin/android/media/tv/TvContentRating#UNRATED:android.media.tv.TvContentRating) Rating constant denoting unrated content. |

## Public methods

### contains

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun contains(rating: TvContentRating): Boolean
```

Returns`true`if this rating has the same main rating as the specified rating and when this rating's sub-ratings contain the other's.

For example, a`TvContentRating`object that represents TV-PG with S(Sexual content) and V(Violence) contains TV-PG, TV-PG/S, TV-PG/V and itself.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `rating` | [TvContentRating](https://developer.android.com/reference/kotlin/android/media/tv/TvContentRating#):The [TvContentRating](https://developer.android.com/reference/kotlin/android/media/tv/TvContentRating#) to check. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object contains`rating`,`false`otherwise. |

### createRating

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createRating(
    domain: String!, 
    ratingSystem: String!, 
    rating: String!, 
    vararg subRatings: String!
): TvContentRating!
```

Creates a`TvContentRating`object with predefined content rating strings.

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `domain` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The domain string. For example, "com.android.tv". |
| `ratingSystem` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The rating system string. For example, "US_TV". |
| `rating` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The content rating string. For example, "US_TV_PG". |
| `subRatings` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The sub-rating strings. For example, "US_TV_D" and "US_TV_L". |

| Return ||
|------------------------------------------------------------------------------------------------------|---------------------------|
| [TvContentRating](https://developer.android.com/reference/kotlin/android/media/tv/TvContentRating#)! | A`TvContentRating`object. |

| Exceptions ||
|--------------------------------------|----------------------------------------------|
| `java.lang.IllegalArgumentException` | If`domain`,`ratingSystem`or`rating`is`null`. |

### equals

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### flattenToString

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun flattenToString(): String!
```

Returns a string that unambiguously describes the rating information contained in a`TvContentRating`object. One can later recover the object from this string through [unflattenFromString](https://developer.android.com/reference/kotlin/android/media/tv/TvContentRating#unflattenFromString(kotlin.String)).

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a string containing the rating information, which can later be stored in the database. |

**See Also**

- [#unflattenFromString](https://developer.android.com/reference/kotlin/android/media/tv/TvContentRating#unflattenFromString(kotlin.String)) 

### getDomain

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDomain(): String!
```

Returns the domain of this`TvContentRating`object. 

### getMainRating

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMainRating(): String!
```

Returns the main rating of this`TvContentRating`object. 

### getRatingSystem

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRatingSystem(): String!
```

Returns the rating system of this`TvContentRating`object. 

### getSubRatings

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSubRatings(): MutableList<String!>!
```

Returns the unmodifiable sub-rating string [List](https://developer.android.com/reference/kotlin/java/util/List.html#) of this`TvContentRating`object. 

### hashCode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### unflattenFromString

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun unflattenFromString(ratingString: String!): TvContentRating!
```

Recovers a`TvContentRating`object from the string that was previously created from [flattenToString](https://developer.android.com/reference/kotlin/android/media/tv/TvContentRating#flattenToString()).

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ratingString` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The string returned by [flattenToString](https://developer.android.com/reference/kotlin/android/media/tv/TvContentRating#flattenToString()). |

| Return ||
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [TvContentRating](https://developer.android.com/reference/kotlin/android/media/tv/TvContentRating#)! | the`TvContentRating`object containing the domain, rating system, rating and sub-ratings information encoded in`ratingString`. |

**See Also**

- [#flattenToString](https://developer.android.com/reference/kotlin/android/media/tv/TvContentRating#flattenToString())

## Properties

### UNRATED

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNRATED: TvContentRating!
```

Rating constant denoting unrated content. Used to handle the case where the content rating information is missing.

TV input services can call [TvInputManager.isRatingBlocked](https://developer.android.com/reference/kotlin/android/media/tv/TvInputManager#isRatingBlocked(android.media.tv.TvContentRating))with this constant to determine whether they should block unrated content. The subsequent call to [TvInputService.Session.notifyContentBlocked](https://developer.android.com/reference/kotlin/android/media/tv/TvInputService.Session#notifyContentBlocked(android.media.tv.TvContentRating))with the same constant notifies applications that the current program content is blocked by parental controls.
