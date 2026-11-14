# ExifInterface

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ExifInterface

Kotlin| [Java](ExifInterface.md) 
| --- | --- |

```
open class ExifInterface
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.ExifInterface](ExifInterface.md) |

This is a class for reading and writing Exif tags in various image file formats.

**Note:** This class has known issues on some versions of Android. It is recommended to use the [AndroidX](https://developer.android.com/jetpack/androidx.html) [ExifInterface Library](../androidx/exifinterface/media/ExifInterface.md) since it offers a superset of the functionality of this class and is more easily updateable. In addition to the functionality of this class, it supports parsing extra metadata such as exposure and data compression information as well as setting extra metadata such as GPS and datetime information.

Supported for reading: JPEG, PNG, WebP, HEIF, DNG, CR2, NEF, NRW, ARW, RW2, ORF, PEF, SRW, RAF, AVIF.

Supported for writing: JPEG, PNG, WebP.

Note: JPEG and HEIF files may contain XMP data either inside the Exif data chunk or outside of it. This class will search both locations for XMP data, but if XMP data exist both inside and outside Exif, will favor the XMP data inside Exif over the one outside.

<br />

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORIENTATION_FLIP_HORIZONTAL](ExifInterface.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORIENTATION_FLIP_VERTICAL](ExifInterface.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORIENTATION_NORMAL](ExifInterface.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORIENTATION_ROTATE_180](ExifInterface.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORIENTATION_ROTATE_270](ExifInterface.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORIENTATION_ROTATE_90](ExifInterface.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORIENTATION_TRANSPOSE](ExifInterface.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORIENTATION_TRANSVERSE](ExifInterface.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORIENTATION_UNDEFINED](ExifInterface.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STREAM_TYPE_EXIF_DATA_ONLY](ExifInterface.md) Constant used to indicate that the input stream contains only Exif data. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STREAM_TYPE_FULL_IMAGE_DATA](ExifInterface.md) Constant used to indicate that the input stream contains the full image data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_APERTURE](ExifInterface.md) Type is double. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_APERTURE_VALUE](ExifInterface.md) Type is rational. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_ARTIST](ExifInterface.md) Type is String. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_BITS_PER_SAMPLE](ExifInterface.md) Type is int. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_BRIGHTNESS_VALUE](ExifInterface.md) Type is rational. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_CFA_PATTERN](ExifInterface.md) Type is String. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_COLOR_SPACE](ExifInterface.md) Type is int. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_COMPONENTS_CONFIGURATION](ExifInterface.md) Type is String. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_COMPRESSED_BITS_PER_PIXEL](ExifInterface.md) Type is rational. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_COMPRESSION](ExifInterface.md) Type is int. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_CONTRAST](ExifInterface.md) Type is int. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_COPYRIGHT](ExifInterface.md) Type is String. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_CUSTOM_RENDERED](ExifInterface.md) Type is int. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_DATETIME](ExifInterface.md) Type is String. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_DATETIME_DIGITIZED](ExifInterface.md) Type is String. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_DATETIME_ORIGINAL](ExifInterface.md) Type is String. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_DEFAULT_CROP_SIZE](ExifInterface.md) Type is int. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_DEVICE_SETTING_DESCRIPTION](ExifInterface.md) Type is String. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_DIGITAL_ZOOM_RATIO](ExifInterface.md) Type is double. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_DNG_VERSION](ExifInterface.md) Type is int. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_EXIF_VERSION](ExifInterface.md) Type is String. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_EXPOSURE_BIAS_VALUE](ExifInterface.md) Type is double. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_EXPOSURE_INDEX](ExifInterface.md) Type is rational. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_EXPOSURE_MODE](ExifInterface.md) Type is int. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_EXPOSURE_PROGRAM](ExifInterface.md) Type is int. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_EXPOSURE_TIME](ExifInterface.md) Type is double. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_FILE_SOURCE](ExifInterface.md) Type is String. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_FLASH](ExifInterface.md) Type is int. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_FLASHPIX_VERSION](ExifInterface.md) Type is String. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_FLASH_ENERGY](ExifInterface.md) Type is rational. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_FOCAL_LENGTH](ExifInterface.md) Type is rational. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_FOCAL_LENGTH_IN_35MM_FILM](ExifInterface.md) Type is int. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_FOCAL_PLANE_RESOLUTION_UNIT](ExifInterface.md) Type is int. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_FOCAL_PLANE_X_RESOLUTION](ExifInterface.md) Type is rational. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_FOCAL_PLANE_Y_RESOLUTION](ExifInterface.md) Type is rational. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_F_NUMBER](ExifInterface.md) Type is double. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_GAIN_CONTROL](ExifInterface.md) Type is int. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_GPS_ALTITUDE](ExifInterface.md) The altitude (in meters) based on the reference in TAG_GPS_ALTITUDE_REF. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_GPS_ALTITUDE_REF](ExifInterface.md) 0 if the altitude is above sea level. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_GPS_AREA_INFORMATION](ExifInterface.md) Type is String. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_GPS_DATESTAMP](ExifInterface.md) Type is String. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_GPS_DEST_BEARING](ExifInterface.md) Type is rational. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_GPS_DEST_BEARING_REF](ExifInterface.md) Type is String. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_GPS_DEST_DISTANCE](ExifInterface.md) Type is rational. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_GPS_DEST_DISTANCE_REF](ExifInterface.md) Type is String. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_GPS_DEST_LATITUDE](ExifInterface.md) Type is rational. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_GPS_DEST_LATITUDE_REF](ExifInterface.md) Type is String. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_GPS_DEST_LONGITUDE](ExifInterface.md) Type is rational. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_GPS_DEST_LONGITUDE_REF](ExifInterface.md) Type is String. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_GPS_DIFFERENTIAL](ExifInterface.md) Type is int. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_GPS_DOP](ExifInterface.md) Type is rational. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_GPS_IMG_DIRECTION](ExifInterface.md) Type is rational. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_GPS_IMG_DIRECTION_REF](ExifInterface.md) Type is String. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_GPS_LATITUDE](ExifInterface.md) Type is rational. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_GPS_LATITUDE_REF](ExifInterface.md) Type is String. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_GPS_LONGITUDE](ExifInterface.md) Type is rational. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_GPS_LONGITUDE_REF](ExifInterface.md) Type is String. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_GPS_MAP_DATUM](ExifInterface.md) Type is String. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_GPS_MEASURE_MODE](ExifInterface.md) Type is String. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_GPS_PROCESSING_METHOD](ExifInterface.md) Type is String. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_GPS_SATELLITES](ExifInterface.md) Type is String. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_GPS_SPEED](ExifInterface.md) Type is rational. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_GPS_SPEED_REF](ExifInterface.md) Type is String. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_GPS_STATUS](ExifInterface.md) Type is String. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_GPS_TIMESTAMP](ExifInterface.md) Type is String. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_GPS_TRACK](ExifInterface.md) Type is rational. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_GPS_TRACK_REF](ExifInterface.md) Type is String. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_GPS_VERSION_ID](ExifInterface.md) Type is String. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_IMAGE_DESCRIPTION](ExifInterface.md) Type is String. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_IMAGE_LENGTH](ExifInterface.md) Type is int. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_IMAGE_UNIQUE_ID](ExifInterface.md) Type is String. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_IMAGE_WIDTH](ExifInterface.md) Type is int. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_INTEROPERABILITY_INDEX](ExifInterface.md) Type is String. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_ISO](ExifInterface.md) Type is int. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_ISO_SPEED_RATINGS](ExifInterface.md) Type is int. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_JPEG_INTERCHANGE_FORMAT](ExifInterface.md) Type is int. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_JPEG_INTERCHANGE_FORMAT_LENGTH](ExifInterface.md) Type is int. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_LIGHT_SOURCE](ExifInterface.md) Type is int. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_MAKE](ExifInterface.md) Type is String. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_MAKER_NOTE](ExifInterface.md) Type is String. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_MAX_APERTURE_VALUE](ExifInterface.md) Type is rational. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_METERING_MODE](ExifInterface.md) Type is int. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_MODEL](ExifInterface.md) Type is String. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_NEW_SUBFILE_TYPE](ExifInterface.md) Type is int. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_OECF](ExifInterface.md) Type is String. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_OFFSET_TIME](ExifInterface.md) A tag used to record the offset from UTC (the time difference from Universal Time Coordinated including daylight saving time) of the time of DateTime tag. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_OFFSET_TIME_DIGITIZED](ExifInterface.md) A tag used to record the offset from UTC (the time difference from Universal Time Coordinated including daylight saving time) of the time of DateTimeDigitized tag. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_OFFSET_TIME_ORIGINAL](ExifInterface.md) A tag used to record the offset from UTC (the time difference from Universal Time Coordinated including daylight saving time) of the time of DateTimeOriginal tag. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_ORF_ASPECT_FRAME](ExifInterface.md) Type is int. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_ORF_PREVIEW_IMAGE_LENGTH](ExifInterface.md) Type is int. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_ORF_PREVIEW_IMAGE_START](ExifInterface.md) Type is int. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_ORF_THUMBNAIL_IMAGE](ExifInterface.md) Type is undefined. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_ORIENTATION](ExifInterface.md) Type is int. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_PHOTOMETRIC_INTERPRETATION](ExifInterface.md) Type is int. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_PIXEL_X_DIMENSION](ExifInterface.md) Type is int. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_PIXEL_Y_DIMENSION](ExifInterface.md) Type is int. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_PLANAR_CONFIGURATION](ExifInterface.md) Type is int. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_PRIMARY_CHROMATICITIES](ExifInterface.md) Type is rational. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_REFERENCE_BLACK_WHITE](ExifInterface.md) Type is rational. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_RELATED_SOUND_FILE](ExifInterface.md) Type is String. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_RESOLUTION_UNIT](ExifInterface.md) Type is int. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_ROWS_PER_STRIP](ExifInterface.md) Type is int. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_RW2_ISO](ExifInterface.md) Type is int. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_RW2_JPG_FROM_RAW](ExifInterface.md) Type is undefined. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_RW2_SENSOR_BOTTOM_BORDER](ExifInterface.md) Type is int. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_RW2_SENSOR_LEFT_BORDER](ExifInterface.md) Type is int. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_RW2_SENSOR_RIGHT_BORDER](ExifInterface.md) Type is int. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_RW2_SENSOR_TOP_BORDER](ExifInterface.md) Type is int. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_SAMPLES_PER_PIXEL](ExifInterface.md) Type is int. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_SATURATION](ExifInterface.md) Type is int. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_SCENE_CAPTURE_TYPE](ExifInterface.md) Type is int. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_SCENE_TYPE](ExifInterface.md) Type is String. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_SENSING_METHOD](ExifInterface.md) Type is int. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_SHARPNESS](ExifInterface.md) Type is int. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_SHUTTER_SPEED_VALUE](ExifInterface.md) Type is rational. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_SOFTWARE](ExifInterface.md) Type is String. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_SPATIAL_FREQUENCY_RESPONSE](ExifInterface.md) Type is String. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_SPECTRAL_SENSITIVITY](ExifInterface.md) Type is String. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_STRIP_BYTE_COUNTS](ExifInterface.md) Type is int. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_STRIP_OFFSETS](ExifInterface.md) Type is int. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_SUBFILE_TYPE](ExifInterface.md) Type is int. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_SUBJECT_AREA](ExifInterface.md) Type is int. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_SUBJECT_DISTANCE](ExifInterface.md) Type is double. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_SUBJECT_DISTANCE_RANGE](ExifInterface.md) Type is int. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_SUBJECT_LOCATION](ExifInterface.md) Type is int. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_SUBSEC_TIME](ExifInterface.md) Type is String. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_SUBSEC_TIME_DIG](ExifInterface.md) Type is String. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_SUBSEC_TIME_DIGITIZED](ExifInterface.md) Type is String. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_SUBSEC_TIME_ORIG](ExifInterface.md) Type is String. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_SUBSEC_TIME_ORIGINAL](ExifInterface.md) Type is String. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_THUMBNAIL_IMAGE_LENGTH](ExifInterface.md) Type is int. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_THUMBNAIL_IMAGE_WIDTH](ExifInterface.md) Type is int. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_THUMBNAIL_ORIENTATION](ExifInterface.md) Type is int. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_TRANSFER_FUNCTION](ExifInterface.md) Type is int. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_USER_COMMENT](ExifInterface.md) Type is String. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_WHITE_BALANCE](ExifInterface.md) Type is int. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_WHITE_POINT](ExifInterface.md) Type is rational. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_XMP](ExifInterface.md) Type is byte\[\]. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_X_RESOLUTION](ExifInterface.md) Type is rational. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_Y_CB_CR_COEFFICIENTS](ExifInterface.md) Type is rational. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_Y_CB_CR_POSITIONING](ExifInterface.md) Type is int. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_Y_CB_CR_SUB_SAMPLING](ExifInterface.md) Type is int. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_Y_RESOLUTION](ExifInterface.md) Type is rational. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WHITEBALANCE_AUTO](ExifInterface.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WHITEBALANCE_MANUAL](ExifInterface.md) <br /> |
| --- | --- |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ExifInterface](ExifInterface.md))`(`file:` ` [File](../java.io/File.md)`)` Reads Exif tags from the specified image file. |
| [ExifInterface](ExifInterface.md))`(`fileDescriptor:` ` [FileDescriptor](../java.io/FileDescriptor.md)`)` Reads Exif tags from the specified image file descriptor. |
| [ExifInterface](ExifInterface.md))`(`inputStream:` ` [InputStream](../java.io/InputStream.md)`)` Reads Exif tags from the specified image input stream. |
| [ExifInterface](ExifInterface.md))`(`inputStream:` ` [InputStream](../java.io/InputStream.md)`, `streamType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads Exif tags from the specified image input stream based on the stream type. |
| [ExifInterface](ExifInterface.md))`(`filename:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Reads Exif tags from the specified image file. |

| Public methods ||
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getAltitude](ExifInterface.md))`(`defaultValue:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Return the altitude in meters. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getAttribute](ExifInterface.md))`(`tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns the value of the specified tag or`null`if there is no such tag in the image file. |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | [getAttributeBytes](ExifInterface.md))`(`tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns the raw bytes for the value of the requested tag inside the image file, or`null`if the tag is not contained. |
| --- | --- |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getAttributeDouble](ExifInterface.md))`(`tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `defaultValue:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Returns the double value of the tag that is specified as rational or contains a double-formatted value. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAttributeInt](ExifInterface.md))`(`tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `defaultValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the integer value of the specified tag. |
| open [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)? | [getAttributeRange](ExifInterface.md))`(`tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns the offset and length of the requested tag inside the image file, or`null`if the tag is not contained. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getDateTime](ExifInterface.md))`()` Returns parsed [TAG_DATETIME](ExifInterface.md) value, or -1 if unavailable or invalid. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getDateTimeDigitized](ExifInterface.md))`()` Returns parsed [TAG_DATETIME_DIGITIZED](ExifInterface.md) value, or -1 if unavailable or invalid. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getDateTimeOriginal](ExifInterface.md))`()` Returns parsed [TAG_DATETIME_ORIGINAL](ExifInterface.md) value, or -1 if unavailable or invalid. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getGpsDateTime](ExifInterface.md))`()` Returns number of milliseconds since Jan. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getLatLong](ExifInterface.md))`(`output:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Stores the latitude and longitude value in a float array. |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getThumbnail](ExifInterface.md))`()` Returns the JPEG compressed thumbnail inside the image file, or`null`if there is no JPEG compressed thumbnail. |
| --- | --- |
| open [Bitmap](../android.graphics/Bitmap.md)! | [getThumbnailBitmap](ExifInterface.md))`()` Creates and returns a Bitmap object of the thumbnail image based on the byte array and the thumbnail compression value, or`null`if the compression type is unsupported. |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getThumbnailBytes](ExifInterface.md))`()` Returns the thumbnail bytes inside the image file, regardless of the compression type of the thumbnail image. |
| open [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)? | [getThumbnailRange](ExifInterface.md))`()` Returns the offset and length of thumbnail inside the image file, or`null`if either there is no thumbnail or the thumbnail bytes are stored non-consecutively. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasAttribute](ExifInterface.md))`(`tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns true if the image file has the given attribute defined. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasThumbnail](ExifInterface.md))`()` Returns true if the image file has a thumbnail. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSupportedMimeType](ExifInterface.md))`(`mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns whether ExifInterface currently supports reading data from the specified mime type or not. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isThumbnailCompressed](ExifInterface.md))`()` Returns true if thumbnail image is JPEG Compressed, or false if either thumbnail image does not exist or thumbnail image is uncompressed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [saveAttributes](ExifInterface.md))`()` Save the tag data into the original image file. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAttribute](ExifInterface.md))`(`tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Set the value of the specified tag. |
| --- | --- |

## Constants

### ORIENTATION_FLIP_HORIZONTAL

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ORIENTATION_FLIP_HORIZONTAL: Int
```  

 Value: 2

### ORIENTATION_FLIP_VERTICAL

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ORIENTATION_FLIP_VERTICAL: Int
```  

 Value: 4

### ORIENTATION_NORMAL

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ORIENTATION_NORMAL: Int
```  

 Value: 1

### ORIENTATION_ROTATE_180

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ORIENTATION_ROTATE_180: Int
```  

 Value: 3

### ORIENTATION_ROTATE_270

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ORIENTATION_ROTATE_270: Int
```  

 Value: 8

### ORIENTATION_ROTATE_90

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ORIENTATION_ROTATE_90: Int
```  

 Value: 6

### ORIENTATION_TRANSPOSE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ORIENTATION_TRANSPOSE: Int
```  

 Value: 5

### ORIENTATION_TRANSVERSE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ORIENTATION_TRANSVERSE: Int
```  

 Value: 7

### ORIENTATION_UNDEFINED

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ORIENTATION_UNDEFINED: Int
```  

 Value: 0

### STREAM_TYPE_EXIF_DATA_ONLY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STREAM_TYPE_EXIF_DATA_ONLY: Int
```

Constant used to indicate that the input stream contains only Exif data.

The format of the Exif-only data must follow the below structure: Exif Identifier Code ("Exif\\0\\0") + TIFF header + IFD data See JEITA CP-3451C Section 4.5.2 and 4.5.4 specifications for more details. 

 Value: 1

### STREAM_TYPE_FULL_IMAGE_DATA

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STREAM_TYPE_FULL_IMAGE_DATA: Int
```

Constant used to indicate that the input stream contains the full image data.

The format of the image data should follow one of the image formats supported by this class. 

 Value: 0

### TAG_APERTURE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_APERTURE: String
```

**Deprecated:** *use [TAG_F_NUMBER](ExifInterface.md) instead*

Type is double. 

 Value: "FNumber"

### TAG_APERTURE_VALUE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_APERTURE_VALUE: String
```

Type is rational. 

 Value: "ApertureValue"

### TAG_ARTIST

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_ARTIST: String
```

Type is String. 

 Value: "Artist"

### TAG_BITS_PER_SAMPLE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_BITS_PER_SAMPLE: String
```

Type is int. 

 Value: "BitsPerSample"

### TAG_BRIGHTNESS_VALUE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_BRIGHTNESS_VALUE: String
```

Type is rational. 

 Value: "BrightnessValue"

### TAG_CFA_PATTERN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_CFA_PATTERN: String
```

Type is String. 

 Value: "CFAPattern"

### TAG_COLOR_SPACE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_COLOR_SPACE: String
```

Type is int. 

 Value: "ColorSpace"

### TAG_COMPONENTS_CONFIGURATION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_COMPONENTS_CONFIGURATION: String
```

Type is String. 

 Value: "ComponentsConfiguration"

### TAG_COMPRESSED_BITS_PER_PIXEL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_COMPRESSED_BITS_PER_PIXEL: String
```

Type is rational. 

 Value: "CompressedBitsPerPixel"

### TAG_COMPRESSION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_COMPRESSION: String
```

Type is int. 

 Value: "Compression"

### TAG_CONTRAST

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_CONTRAST: String
```

Type is int. 

 Value: "Contrast"

### TAG_COPYRIGHT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_COPYRIGHT: String
```

Type is String. 

 Value: "Copyright"

### TAG_CUSTOM_RENDERED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_CUSTOM_RENDERED: String
```

Type is int. 

 Value: "CustomRendered"

### TAG_DATETIME

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_DATETIME: String
```

Type is String. 

 Value: "DateTime"

### TAG_DATETIME_DIGITIZED

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_DATETIME_DIGITIZED: String
```

Type is String. 

 Value: "DateTimeDigitized"

### TAG_DATETIME_ORIGINAL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_DATETIME_ORIGINAL: String
```

Type is String. 

 Value: "DateTimeOriginal"

### TAG_DEFAULT_CROP_SIZE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_DEFAULT_CROP_SIZE: String
```

Type is int. DNG Specification 1.4.0.0. Section 4 

 Value: "DefaultCropSize"

### TAG_DEVICE_SETTING_DESCRIPTION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_DEVICE_SETTING_DESCRIPTION: String
```

Type is String. 

 Value: "DeviceSettingDescription"

### TAG_DIGITAL_ZOOM_RATIO

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_DIGITAL_ZOOM_RATIO: String
```

Type is double. 

 Value: "DigitalZoomRatio"

### TAG_DNG_VERSION

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_DNG_VERSION: String
```

Type is int. DNG Specification 1.4.0.0. Section 4 

 Value: "DNGVersion"

### TAG_EXIF_VERSION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_EXIF_VERSION: String
```

Type is String. 

 Value: "ExifVersion"

### TAG_EXPOSURE_BIAS_VALUE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_EXPOSURE_BIAS_VALUE: String
```

Type is double. 

 Value: "ExposureBiasValue"

### TAG_EXPOSURE_INDEX

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_EXPOSURE_INDEX: String
```

Type is rational. 

 Value: "ExposureIndex"

### TAG_EXPOSURE_MODE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_EXPOSURE_MODE: String
```

Type is int. 

 Value: "ExposureMode"

### TAG_EXPOSURE_PROGRAM

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_EXPOSURE_PROGRAM: String
```

Type is int. 

 Value: "ExposureProgram"

### TAG_EXPOSURE_TIME

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_EXPOSURE_TIME: String
```

Type is double. 

 Value: "ExposureTime"

### TAG_FILE_SOURCE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_FILE_SOURCE: String
```

Type is String. 

 Value: "FileSource"

### TAG_FLASH

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_FLASH: String
```

Type is int. 

 Value: "Flash"

### TAG_FLASHPIX_VERSION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_FLASHPIX_VERSION: String
```

Type is String. 

 Value: "FlashpixVersion"

### TAG_FLASH_ENERGY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_FLASH_ENERGY: String
```

Type is rational. 

 Value: "FlashEnergy"

### TAG_FOCAL_LENGTH

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_FOCAL_LENGTH: String
```

Type is rational. 

 Value: "FocalLength"

### TAG_FOCAL_LENGTH_IN_35MM_FILM

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_FOCAL_LENGTH_IN_35MM_FILM: String
```

Type is int. 

 Value: "FocalLengthIn35mmFilm"

### TAG_FOCAL_PLANE_RESOLUTION_UNIT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_FOCAL_PLANE_RESOLUTION_UNIT: String
```

Type is int. 

 Value: "FocalPlaneResolutionUnit"

### TAG_FOCAL_PLANE_X_RESOLUTION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_FOCAL_PLANE_X_RESOLUTION: String
```

Type is rational. 

 Value: "FocalPlaneXResolution"

### TAG_FOCAL_PLANE_Y_RESOLUTION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_FOCAL_PLANE_Y_RESOLUTION: String
```

Type is rational. 

 Value: "FocalPlaneYResolution"

### TAG_F_NUMBER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_F_NUMBER: String
```

Type is double. 

 Value: "FNumber"

### TAG_GAIN_CONTROL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_GAIN_CONTROL: String
```

Type is int. 

 Value: "GainControl"

### TAG_GPS_ALTITUDE

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_GPS_ALTITUDE: String
```

The altitude (in meters) based on the reference in TAG_GPS_ALTITUDE_REF. Type is rational. 

 Value: "GPSAltitude"

### TAG_GPS_ALTITUDE_REF

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_GPS_ALTITUDE_REF: String
```

0 if the altitude is above sea level. 1 if the altitude is below sea level. Type is int. 

 Value: "GPSAltitudeRef"

### TAG_GPS_AREA_INFORMATION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_GPS_AREA_INFORMATION: String
```

Type is String. 

 Value: "GPSAreaInformation"

### TAG_GPS_DATESTAMP

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_GPS_DATESTAMP: String
```

Type is String. 

 Value: "GPSDateStamp"

### TAG_GPS_DEST_BEARING

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_GPS_DEST_BEARING: String
```

Type is rational. 

 Value: "GPSDestBearing"

### TAG_GPS_DEST_BEARING_REF

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_GPS_DEST_BEARING_REF: String
```

Type is String. 

 Value: "GPSDestBearingRef"

### TAG_GPS_DEST_DISTANCE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_GPS_DEST_DISTANCE: String
```

Type is rational. 

 Value: "GPSDestDistance"

### TAG_GPS_DEST_DISTANCE_REF

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_GPS_DEST_DISTANCE_REF: String
```

Type is String. 

 Value: "GPSDestDistanceRef"

### TAG_GPS_DEST_LATITUDE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_GPS_DEST_LATITUDE: String
```

Type is rational. 

 Value: "GPSDestLatitude"

### TAG_GPS_DEST_LATITUDE_REF

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_GPS_DEST_LATITUDE_REF: String
```

Type is String. 

 Value: "GPSDestLatitudeRef"

### TAG_GPS_DEST_LONGITUDE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_GPS_DEST_LONGITUDE: String
```

Type is rational. 

 Value: "GPSDestLongitude"

### TAG_GPS_DEST_LONGITUDE_REF

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_GPS_DEST_LONGITUDE_REF: String
```

Type is String. 

 Value: "GPSDestLongitudeRef"

### TAG_GPS_DIFFERENTIAL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_GPS_DIFFERENTIAL: String
```

Type is int. 

 Value: "GPSDifferential"

### TAG_GPS_DOP

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_GPS_DOP: String
```

Type is rational. 

 Value: "GPSDOP"

### TAG_GPS_IMG_DIRECTION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_GPS_IMG_DIRECTION: String
```

Type is rational. 

 Value: "GPSImgDirection"

### TAG_GPS_IMG_DIRECTION_REF

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_GPS_IMG_DIRECTION_REF: String
```

Type is String. 

 Value: "GPSImgDirectionRef"

### TAG_GPS_LATITUDE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_GPS_LATITUDE: String
```

Type is rational. Format is "num1/denom1,num2/denom2,num3/denom3". 

 Value: "GPSLatitude"

### TAG_GPS_LATITUDE_REF

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_GPS_LATITUDE_REF: String
```

Type is String. 

 Value: "GPSLatitudeRef"

### TAG_GPS_LONGITUDE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_GPS_LONGITUDE: String
```

Type is rational. Format is "num1/denom1,num2/denom2,num3/denom3". 

 Value: "GPSLongitude"

### TAG_GPS_LONGITUDE_REF

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_GPS_LONGITUDE_REF: String
```

Type is String. 

 Value: "GPSLongitudeRef"

### TAG_GPS_MAP_DATUM

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_GPS_MAP_DATUM: String
```

Type is String. 

 Value: "GPSMapDatum"

### TAG_GPS_MEASURE_MODE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_GPS_MEASURE_MODE: String
```

Type is String. 

 Value: "GPSMeasureMode"

### TAG_GPS_PROCESSING_METHOD

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_GPS_PROCESSING_METHOD: String
```

Type is String. Name of GPS processing method used for location finding. 

 Value: "GPSProcessingMethod"

### TAG_GPS_SATELLITES

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_GPS_SATELLITES: String
```

Type is String. 

 Value: "GPSSatellites"

### TAG_GPS_SPEED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_GPS_SPEED: String
```

Type is rational. 

 Value: "GPSSpeed"

### TAG_GPS_SPEED_REF

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_GPS_SPEED_REF: String
```

Type is String. 

 Value: "GPSSpeedRef"

### TAG_GPS_STATUS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_GPS_STATUS: String
```

Type is String. 

 Value: "GPSStatus"

### TAG_GPS_TIMESTAMP

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_GPS_TIMESTAMP: String
```

Type is String. Format is "hh:mm:ss". 

 Value: "GPSTimeStamp"

### TAG_GPS_TRACK

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_GPS_TRACK: String
```

Type is rational. 

 Value: "GPSTrack"

### TAG_GPS_TRACK_REF

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_GPS_TRACK_REF: String
```

Type is String. 

 Value: "GPSTrackRef"

### TAG_GPS_VERSION_ID

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_GPS_VERSION_ID: String
```

Type is String. 

 Value: "GPSVersionID"

### TAG_IMAGE_DESCRIPTION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_IMAGE_DESCRIPTION: String
```

Type is String. 

 Value: "ImageDescription"

### TAG_IMAGE_LENGTH

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_IMAGE_LENGTH: String
```

Type is int. 

 Value: "ImageLength"

### TAG_IMAGE_UNIQUE_ID

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_IMAGE_UNIQUE_ID: String
```

Type is String. 

 Value: "ImageUniqueID"

### TAG_IMAGE_WIDTH

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_IMAGE_WIDTH: String
```

Type is int. 

 Value: "ImageWidth"

### TAG_INTEROPERABILITY_INDEX

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_INTEROPERABILITY_INDEX: String
```

Type is String. 

 Value: "InteroperabilityIndex"

### TAG_ISO

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_ISO: String
```

**Deprecated:** *use [TAG_ISO_SPEED_RATINGS](ExifInterface.md) instead*

Type is int. 

 Value: "ISOSpeedRatings"

### TAG_ISO_SPEED_RATINGS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_ISO_SPEED_RATINGS: String
```

Type is int. 

 Value: "ISOSpeedRatings"

### TAG_JPEG_INTERCHANGE_FORMAT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_JPEG_INTERCHANGE_FORMAT: String
```

Type is int. 

 Value: "JPEGInterchangeFormat"

### TAG_JPEG_INTERCHANGE_FORMAT_LENGTH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_JPEG_INTERCHANGE_FORMAT_LENGTH: String
```

Type is int. 

 Value: "JPEGInterchangeFormatLength"

### TAG_LIGHT_SOURCE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_LIGHT_SOURCE: String
```

Type is int. 

 Value: "LightSource"

### TAG_MAKE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_MAKE: String
```

Type is String. 

 Value: "Make"

### TAG_MAKER_NOTE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_MAKER_NOTE: String
```

Type is String. 

 Value: "MakerNote"

### TAG_MAX_APERTURE_VALUE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_MAX_APERTURE_VALUE: String
```

Type is rational. 

 Value: "MaxApertureValue"

### TAG_METERING_MODE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_METERING_MODE: String
```

Type is int. 

 Value: "MeteringMode"

### TAG_MODEL

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_MODEL: String
```

Type is String. 

 Value: "Model"

### TAG_NEW_SUBFILE_TYPE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_NEW_SUBFILE_TYPE: String
```

Type is int. 

 Value: "NewSubfileType"

### TAG_OECF

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_OECF: String
```

Type is String. 

 Value: "OECF"

### TAG_OFFSET_TIME

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_OFFSET_TIME: String
```

A tag used to record the offset from UTC (the time difference from Universal Time Coordinated including daylight saving time) of the time of DateTime tag. The format when recording the offset is "±HH:MM". The part of "±" shall be recorded as "+" or "-". When the offsets are unknown, all the character spaces except colons (":") should be filled with blank characters, or else the Interoperability field should be filled with blank characters. The character string length is 7 Bytes including NULL for termination. When the field is left blank, it is treated as unknown.

- Tag = 36880
- Type = String
- Length = 7
- Default = None

 Value: "OffsetTime"

### TAG_OFFSET_TIME_DIGITIZED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_OFFSET_TIME_DIGITIZED: String
```

A tag used to record the offset from UTC (the time difference from Universal Time Coordinated including daylight saving time) of the time of DateTimeDigitized tag. The format when recording the offset is "±HH:MM". The part of "±" shall be recorded as "+" or "-". When the offsets are unknown, all the character spaces except colons (":") should be filled with blank characters, or else the Interoperability field should be filled with blank characters. The character string length is 7 Bytes including NULL for termination. When the field is left blank, it is treated as unknown.

- Tag = 36882
- Type = String
- Length = 7
- Default = None

 Value: "OffsetTimeDigitized"

### TAG_OFFSET_TIME_ORIGINAL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_OFFSET_TIME_ORIGINAL: String
```

A tag used to record the offset from UTC (the time difference from Universal Time Coordinated including daylight saving time) of the time of DateTimeOriginal tag. The format when recording the offset is "±HH:MM". The part of "±" shall be recorded as "+" or "-". When the offsets are unknown, all the character spaces except colons (":") should be filled with blank characters, or else the Interoperability field should be filled with blank characters. The character string length is 7 Bytes including NULL for termination. When the field is left blank, it is treated as unknown.

- Tag = 36881
- Type = String
- Length = 7
- Default = None

 Value: "OffsetTimeOriginal"

### TAG_ORF_ASPECT_FRAME

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_ORF_ASPECT_FRAME: String
```

Type is int. See Olympus Image Processing tags in http://www.exiv2.org/tags-olympus.html. 

 Value: "AspectFrame"

### TAG_ORF_PREVIEW_IMAGE_LENGTH

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_ORF_PREVIEW_IMAGE_LENGTH: String
```

Type is int. See Olympus Camera Settings tags in http://www.exiv2.org/tags-olympus.html. 

 Value: "PreviewImageLength"

### TAG_ORF_PREVIEW_IMAGE_START

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_ORF_PREVIEW_IMAGE_START: String
```

Type is int. See Olympus Camera Settings tags in http://www.exiv2.org/tags-olympus.html. 

 Value: "PreviewImageStart"

### TAG_ORF_THUMBNAIL_IMAGE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_ORF_THUMBNAIL_IMAGE: String
```

Type is undefined. See Olympus MakerNote tags in http://www.exiv2.org/tags-olympus.html. 

 Value: "ThumbnailImage"

### TAG_ORIENTATION

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_ORIENTATION: String
```

Type is int. 

 Value: "Orientation"

### TAG_PHOTOMETRIC_INTERPRETATION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_PHOTOMETRIC_INTERPRETATION: String
```

Type is int. 

 Value: "PhotometricInterpretation"

### TAG_PIXEL_X_DIMENSION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_PIXEL_X_DIMENSION: String
```

Type is int. 

 Value: "PixelXDimension"

### TAG_PIXEL_Y_DIMENSION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_PIXEL_Y_DIMENSION: String
```

Type is int. 

 Value: "PixelYDimension"

### TAG_PLANAR_CONFIGURATION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_PLANAR_CONFIGURATION: String
```

Type is int. 

 Value: "PlanarConfiguration"

### TAG_PRIMARY_CHROMATICITIES

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_PRIMARY_CHROMATICITIES: String
```

Type is rational. 

 Value: "PrimaryChromaticities"

### TAG_REFERENCE_BLACK_WHITE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_REFERENCE_BLACK_WHITE: String
```

Type is rational. 

 Value: "ReferenceBlackWhite"

### TAG_RELATED_SOUND_FILE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_RELATED_SOUND_FILE: String
```

Type is String. 

 Value: "RelatedSoundFile"

### TAG_RESOLUTION_UNIT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_RESOLUTION_UNIT: String
```

Type is int. 

 Value: "ResolutionUnit"

### TAG_ROWS_PER_STRIP

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_ROWS_PER_STRIP: String
```

Type is int. 

 Value: "RowsPerStrip"

### TAG_RW2_ISO

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_RW2_ISO: String
```

Type is int. See PanasonicRaw tags in http://www.sno.phy.queensu.ca/\~phil/exiftool/TagNames/PanasonicRaw.html 

 Value: "ISO"

### TAG_RW2_JPG_FROM_RAW

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_RW2_JPG_FROM_RAW: String
```

Type is undefined. See PanasonicRaw tags in http://www.sno.phy.queensu.ca/\~phil/exiftool/TagNames/PanasonicRaw.html 

 Value: "JpgFromRaw"

### TAG_RW2_SENSOR_BOTTOM_BORDER

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_RW2_SENSOR_BOTTOM_BORDER: String
```

Type is int. See PanasonicRaw tags in http://www.sno.phy.queensu.ca/\~phil/exiftool/TagNames/PanasonicRaw.html 

 Value: "SensorBottomBorder"

### TAG_RW2_SENSOR_LEFT_BORDER

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_RW2_SENSOR_LEFT_BORDER: String
```

Type is int. See PanasonicRaw tags in http://www.sno.phy.queensu.ca/\~phil/exiftool/TagNames/PanasonicRaw.html 

 Value: "SensorLeftBorder"

### TAG_RW2_SENSOR_RIGHT_BORDER

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_RW2_SENSOR_RIGHT_BORDER: String
```

Type is int. See PanasonicRaw tags in http://www.sno.phy.queensu.ca/\~phil/exiftool/TagNames/PanasonicRaw.html 

 Value: "SensorRightBorder"

### TAG_RW2_SENSOR_TOP_BORDER

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_RW2_SENSOR_TOP_BORDER: String
```

Type is int. See PanasonicRaw tags in http://www.sno.phy.queensu.ca/\~phil/exiftool/TagNames/PanasonicRaw.html 

 Value: "SensorTopBorder"

### TAG_SAMPLES_PER_PIXEL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_SAMPLES_PER_PIXEL: String
```

Type is int. 

 Value: "SamplesPerPixel"

### TAG_SATURATION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_SATURATION: String
```

Type is int. 

 Value: "Saturation"

### TAG_SCENE_CAPTURE_TYPE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_SCENE_CAPTURE_TYPE: String
```

Type is int. 

 Value: "SceneCaptureType"

### TAG_SCENE_TYPE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_SCENE_TYPE: String
```

Type is String. 

 Value: "SceneType"

### TAG_SENSING_METHOD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_SENSING_METHOD: String
```

Type is int. 

 Value: "SensingMethod"

### TAG_SHARPNESS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_SHARPNESS: String
```

Type is int. 

 Value: "Sharpness"

### TAG_SHUTTER_SPEED_VALUE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_SHUTTER_SPEED_VALUE: String
```

Type is rational. 

 Value: "ShutterSpeedValue"

### TAG_SOFTWARE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_SOFTWARE: String
```

Type is String. 

 Value: "Software"

### TAG_SPATIAL_FREQUENCY_RESPONSE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_SPATIAL_FREQUENCY_RESPONSE: String
```

Type is String. 

 Value: "SpatialFrequencyResponse"

### TAG_SPECTRAL_SENSITIVITY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_SPECTRAL_SENSITIVITY: String
```

Type is String. 

 Value: "SpectralSensitivity"

### TAG_STRIP_BYTE_COUNTS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_STRIP_BYTE_COUNTS: String
```

Type is int. 

 Value: "StripByteCounts"

### TAG_STRIP_OFFSETS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_STRIP_OFFSETS: String
```

Type is int. 

 Value: "StripOffsets"

### TAG_SUBFILE_TYPE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_SUBFILE_TYPE: String
```

Type is int. 

 Value: "SubfileType"

### TAG_SUBJECT_AREA

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_SUBJECT_AREA: String
```

Type is int. 

 Value: "SubjectArea"

### TAG_SUBJECT_DISTANCE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_SUBJECT_DISTANCE: String
```

Type is double. 

 Value: "SubjectDistance"

### TAG_SUBJECT_DISTANCE_RANGE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_SUBJECT_DISTANCE_RANGE: String
```

Type is int. 

 Value: "SubjectDistanceRange"

### TAG_SUBJECT_LOCATION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_SUBJECT_LOCATION: String
```

Type is int. 

 Value: "SubjectLocation"

### TAG_SUBSEC_TIME

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_SUBSEC_TIME: String
```

Type is String. 

 Value: "SubSecTime"

### TAG_SUBSEC_TIME_DIG

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_SUBSEC_TIME_DIG: String
```

**Deprecated:** *use [TAG_SUBSEC_TIME_DIGITIZED](ExifInterface.md) instead*

Type is String. 

 Value: "SubSecTimeDigitized"

### TAG_SUBSEC_TIME_DIGITIZED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_SUBSEC_TIME_DIGITIZED: String
```

Type is String. 

 Value: "SubSecTimeDigitized"

### TAG_SUBSEC_TIME_ORIG

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_SUBSEC_TIME_ORIG: String
```

**Deprecated:** *use [TAG_SUBSEC_TIME_ORIGINAL](ExifInterface.md) instead*

Type is String. 

 Value: "SubSecTimeOriginal"

### TAG_SUBSEC_TIME_ORIGINAL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_SUBSEC_TIME_ORIGINAL: String
```

Type is String. 

 Value: "SubSecTimeOriginal"

### TAG_THUMBNAIL_IMAGE_LENGTH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_THUMBNAIL_IMAGE_LENGTH: String
```

Type is int. 

 Value: "ThumbnailImageLength"

### TAG_THUMBNAIL_IMAGE_WIDTH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_THUMBNAIL_IMAGE_WIDTH: String
```

Type is int. 

 Value: "ThumbnailImageWidth"

### TAG_THUMBNAIL_ORIENTATION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_THUMBNAIL_ORIENTATION: String
```

Type is int. 

 Value: "ThumbnailOrientation"

### TAG_TRANSFER_FUNCTION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_TRANSFER_FUNCTION: String
```

Type is int. 

 Value: "TransferFunction"

### TAG_USER_COMMENT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_USER_COMMENT: String
```

Type is String. 

 Value: "UserComment"

### TAG_WHITE_BALANCE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_WHITE_BALANCE: String
```

Type is int. 

 Value: "WhiteBalance"

### TAG_WHITE_POINT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_WHITE_POINT: String
```

Type is rational. 

 Value: "WhitePoint"

### TAG_XMP

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_XMP: String
```

Type is byte\[\]. See [Extensible Metadata Platform (XMP)](https://en.wikipedia.org/wiki/Extensible_Metadata_Platform) for details on contents. 

 Value: "Xmp"

### TAG_X_RESOLUTION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_X_RESOLUTION: String
```

Type is rational. 

 Value: "XResolution"

### TAG_Y_CB_CR_COEFFICIENTS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_Y_CB_CR_COEFFICIENTS: String
```

Type is rational. 

 Value: "YCbCrCoefficients"

### TAG_Y_CB_CR_POSITIONING

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_Y_CB_CR_POSITIONING: String
```

Type is int. 

 Value: "YCbCrPositioning"

### TAG_Y_CB_CR_SUB_SAMPLING

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_Y_CB_CR_SUB_SAMPLING: String
```

Type is int. 

 Value: "YCbCrSubSampling"

### TAG_Y_RESOLUTION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_Y_RESOLUTION: String
```

Type is rational. 

 Value: "YResolution"

### WHITEBALANCE_AUTO

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WHITEBALANCE_AUTO: Int
```  

 Value: 0

### WHITEBALANCE_MANUAL

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WHITEBALANCE_MANUAL: Int
```  

 Value: 1

## Public constructors

### ExifInterface

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ExifInterface(file: File)
```

Reads Exif tags from the specified image file.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------|
| `file` | [File](../java.io/File.md):the file of the image data This value cannot be`null`. |

| Exceptions ||
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if file is null |
| `java.io.IOException` | if an I/O error occurs while retrieving file descriptor via [FileInputStream.getFD()](../java.io/FileInputStream.md)). |

### ExifInterface

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ExifInterface(fileDescriptor: FileDescriptor)
```

Reads Exif tags from the specified image file descriptor. Attribute mutation is supported for writable and seekable file descriptors only. This constructor will not rewind the offset of the given file descriptor. Developers should close the file descriptor after use.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fileDescriptor` | [FileDescriptor](../java.io/FileDescriptor.md):the file descriptor of the image data This value cannot be`null`. |

| Exceptions ||
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if file descriptor is null |
| `java.io.IOException` | if an error occurs while duplicating the file descriptor via [Os.dup(FileDescriptor)](../android.system/Os.md)). |

### ExifInterface

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ExifInterface(inputStream: InputStream)
```

Reads Exif tags from the specified image input stream. Attribute mutation is not supported for input streams. The given input stream will proceed from its current position. Developers should close the input stream after use. This constructor is not intended to be used with an input stream that performs any networking operations.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `inputStream` | [InputStream](../java.io/InputStream.md):the input stream that contains the image data This value cannot be`null`. |

| Exceptions ||
|----------------------------------|-----------------------------|
| `java.lang.NullPointerException` | if the input stream is null |

### ExifInterface

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ExifInterface(
    inputStream: InputStream, 
    streamType: Int)
```

Reads Exif tags from the specified image input stream based on the stream type. Attribute mutation is not supported for input streams. The given input stream will proceed from its current position. Developers should close the input stream after use. This constructor is not intended to be used with an input stream that performs any networking operations.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `inputStream` | [InputStream](../java.io/InputStream.md):the input stream that contains the image data This value cannot be`null`. |
| `streamType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the type of input stream Value is [android.media.ExifInterface#STREAM_TYPE_FULL_IMAGE_DATA](ExifInterface.md), or [android.media.ExifInterface#STREAM_TYPE_EXIF_DATA_ONLY](ExifInterface.md) |

| Exceptions ||
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the input stream is null |
| `java.io.IOException` | if an I/O error occurs while retrieving file descriptor via [FileInputStream.getFD()](../java.io/FileInputStream.md)). |

### ExifInterface

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ExifInterface(filename: String)
```

Reads Exif tags from the specified image file.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `filename` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the name of the file of the image data This value cannot be`null`. |

| Exceptions ||
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if file name is null |
| `java.io.IOException` | if an I/O error occurs while retrieving file descriptor via [FileInputStream.getFD()](../java.io/FileInputStream.md)). |

## Public methods

### getAltitude

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAltitude(defaultValue: Double): Double
```

Return the altitude in meters. If the exif tag does not exist, return defaultValue.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------|
| `defaultValue` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the value to return if the tag is not available. |

### getAttribute

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAttribute(tag: String): String?
```

Returns the value of the specified tag or`null`if there is no such tag in the image file.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------|
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the name of the tag. This value cannot be`null`. |

### getAttributeBytes

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAttributeBytes(tag: String): ByteArray?
```

Returns the raw bytes for the value of the requested tag inside the image file, or`null`if the tag is not contained.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------|
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | raw bytes for the value of the requested tag, or`null`if no tag was found. |

### getAttributeDouble

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAttributeDouble(
    tag: String, 
    defaultValue: Double
): Double
```

Returns the double value of the tag that is specified as rational or contains a double-formatted value. If there is no such tag in the image file or the value cannot be parsed as double, return defaultValue.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------|
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the name of the tag. This value cannot be`null`. |
| `defaultValue` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the value to return if the tag is not available. |

### getAttributeInt

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAttributeInt(
    tag: String, 
    defaultValue: Int
): Int
```

Returns the integer value of the specified tag. If there is no such tag in the image file or the value cannot be parsed as integer, return defaultValue.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------|
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the name of the tag. This value cannot be`null`. |
| `defaultValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value to return if the tag is not available. |

### getAttributeRange

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAttributeRange(tag: String): LongArray?
```

Returns the offset and length of the requested tag inside the image file, or`null`if the tag is not contained.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------|
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)? | two-element array, the offset in the first value, and length in the second, or`null`if no tag was found. |

| Exceptions ||
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if [saveAttributes()](ExifInterface.md))has been called since the underlying file was initially parsed, since that means offsets may have changed. |

### getDateTime

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDateTime(): Long
```

Returns parsed [TAG_DATETIME](ExifInterface.md) value, or -1 if unavailable or invalid. 
Value is a non-negative timestamp measured as the number of milliseconds since 1970-01-01T00:00:00Z.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Value is a non-negative timestamp measured as the number of milliseconds since 1970-01-01T00:00:00Z. |

### getDateTimeDigitized

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDateTimeDigitized(): Long
```

Returns parsed [TAG_DATETIME_DIGITIZED](ExifInterface.md) value, or -1 if unavailable or invalid. 
Value is a non-negative timestamp measured as the number of milliseconds since 1970-01-01T00:00:00Z.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Value is a non-negative timestamp measured as the number of milliseconds since 1970-01-01T00:00:00Z. |

### getDateTimeOriginal

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDateTimeOriginal(): Long
```

Returns parsed [TAG_DATETIME_ORIGINAL](ExifInterface.md) value, or -1 if unavailable or invalid. 
Value is a non-negative timestamp measured as the number of milliseconds since 1970-01-01T00:00:00Z.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Value is a non-negative timestamp measured as the number of milliseconds since 1970-01-01T00:00:00Z. |

### getGpsDateTime

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGpsDateTime(): Long
```

Returns number of milliseconds since Jan. 1, 1970, midnight UTC. Returns -1 if the date time information if not available. 

### getLatLong

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLatLong(output: FloatArray!): Boolean
```

Stores the latitude and longitude value in a float array. The first element is the latitude, and the second element is the longitude. Returns false if the Exif tags are not available. 

### getThumbnail

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getThumbnail(): ByteArray!
```

Returns the JPEG compressed thumbnail inside the image file, or`null`if there is no JPEG compressed thumbnail. The returned data can be decoded using[android.graphics.BitmapFactory#decodeByteArray(byte[],int,int)](https://developer.android.com/reference/kotlin/android/graphics/BitmapFactory.html#decodeByteArray(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)) 

### getThumbnailBitmap

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getThumbnailBitmap(): Bitmap!
```

Creates and returns a Bitmap object of the thumbnail image based on the byte array and the thumbnail compression value, or`null`if the compression type is unsupported. 

### getThumbnailBytes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getThumbnailBytes(): ByteArray!
```

Returns the thumbnail bytes inside the image file, regardless of the compression type of the thumbnail image. 

### getThumbnailRange

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getThumbnailRange(): LongArray?
```

Returns the offset and length of thumbnail inside the image file, or`null`if either there is no thumbnail or the thumbnail bytes are stored non-consecutively.

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)? | two-element array, the offset in the first value, and length in the second, or`null`if no thumbnail was found or the thumbnail strips are not placed consecutively. |

| Exceptions ||
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if [saveAttributes()](ExifInterface.md))has been called since the underlying file was initially parsed, since that means offsets may have changed. |

### hasAttribute

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasAttribute(tag: String): Boolean
```

Returns true if the image file has the given attribute defined.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------|
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the name of the tag. This value cannot be`null`. |

### hasThumbnail

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasThumbnail(): Boolean
```

Returns true if the image file has a thumbnail. 

### isSupportedMimeType

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isSupportedMimeType(mimeType: String): Boolean
```

Returns whether ExifInterface currently supports reading data from the specified mime type or not.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the string value of mime type This value cannot be`null`. |

### isThumbnailCompressed

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isThumbnailCompressed(): Boolean
```

Returns true if thumbnail image is JPEG Compressed, or false if either thumbnail image does not exist or thumbnail image is uncompressed. 

### saveAttributes

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun saveAttributes(): Unit
```

Save the tag data into the original image file. This is expensive because it involves copying all the data from one file to another and deleting the old file and renaming the other. It's best to use [setAttribute(java.lang.String,java.lang.String)](ExifInterface.md))to set all attributes to write and make a single call rather than multiple calls for each attribute.

This method is supported for JPEG, PNG, and WebP files.

Note: after calling this method, any attempts to obtain range information from [getAttributeRange(java.lang.String)](ExifInterface.md))or [getThumbnailRange()](ExifInterface.md))will throw [IllegalStateException](../java.lang/IllegalStateException.md), since the offsets may have changed in the newly written file.

For WebP format, the Exif data will be stored as an Extended File Format, and it may not be supported for older readers.

For PNG format, the Exif data will be stored as an "eXIf" chunk as per "Extensions to the PNG 1.2 Specification, Version 1.5.0".

**Warning:** Calling this method on a DNG-based instance of`ExifInterface`may result in the original image file being overwritten with invalid data on some versions of Android 13 (API 33). 

### setAttribute

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAttribute(
    tag: String, 
    value: String?
): Unit
```

Set the value of the specified tag.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------|
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the name of the tag. This value cannot be`null`. |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:the value of the tag. This value may be`null`. |
