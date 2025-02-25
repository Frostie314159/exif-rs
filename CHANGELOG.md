## 0.6

   -  Rust 1.60 or later is now required to build this package.

## 0.5.5 (2022-10-22)

   -  `Value::as_uint` and `Error::UnexpectedValue` have been added.

## 0.5.4 (2021-03-26)

   -  WebP format support has been added.

## 0.5.3 (2021-01-05)

   -  An infinite loop in reading PNG files has been fixed.
   -  PNG reader now handles `std::io::ErrorKind::Interrupted` correctly.

## 0.5.2 (2020-08-07)

   -  PNG format support has been added.
   -  DCF (Design rule for Camera File system) 2.0 tags have been added.

## 0.5.1 (2020-02-15)

   -  Exif 2.32 tags have been added.

## 0.5 (2020-01-26)

   -  Support for HEIF has been added.
   -  `Exif` has been separated from `Reader`.
   -  `Error::description` has been removed because it has been
      soft-deprecated.

## 0.4 (2019-12-22)

   -  Support for displaying values with units has been added.
   -  Rust 1.40 or later is required.
   -  The deprecated `tag` module has been removed.
   -  Support for reading up to 8 IFDs has been added.
   -  Enums `Context` and `Error` are now non_exhaustive.
   -  `Value` and `Field` no longer borrows the raw buffer.
   -  Struct `In` has been added to indicate primary/thumbnail images.
   -  `Reader::fields` now returns an iterator.
   -  The associated value of `Value::Undefined` and `Value::Ascii` has been
      changed from a slice to a `Vec`.

## 0.3.1 (2018-06-17)

   -  IFDs other than 0th and 1st are ignored for now.

## 0.3 (2017-10-22)

   -  Enum `Error` now has two new variants: `TooBig` and `NotSupported`.
   -  `Value::Undefined` now has the 2nd member to keep the offset of the
      value.
   -  Struct `DateTime` now has two new fields: `nanosecond` and
      `time_offset`.
   -  The tag constants have been changed to associated constants of
      struct `Tag`.  Use `Tag::TagName` instead of `tag::TagName`.

## 0.2.3 (2017-07-16)

   -  Experimental support for writing Exif data has been added.
   -  The `Hash` trait has been derived for `Tag` and `Context`.
   -  `Reader::get_value` and `Value::iter_uint` have been added.

## 0.2.2 (2017-06-17)

   -  The `std::fmt::Display` trait has been implemented for `Rational`,
      `SRational`, and `DateTime`.
   -  The `Copy` and `Clone` traits have been derived for `Rational`
      and `SRational`.
   -  Converters from `Rational`/`SRational` to `f64`/`f32` have been added.
      -  `Rational::to_f64` and `SRational::to_f64`.
      -  `From<Rational>` and `From<SRational>` traits for `f64` and `f32`.
   -  Human readable printing of a `Value` has been supported.
      The `Value::display_as` method returns an object that implements
      the `Display` trait.
   -  The `Value::get_uint` method has been added.

## 0.2.1 (2017-03-27)

   -  A typo in the documentation has been fixed.

## 0.2 (2017-03-26)

   -  The `Copy` and `Clone` traits have been derived for `Tag`.
   -  The `Tag::default_value` function has been added.
   -  DateTime parser has been added.
   -  A new variant `Error::BlankValue` has been added.
   -  Rust 1.15 is now required to compile.
   -  The `Reader::fields` method now returns a slice instead of a reference
      to a `Vec`.
   -  The `parse_image` function has been removed.
   -  The `Tag::value` method was renamed to `Tag::number`.

## 0.1.3 (2017-03-12)

   -  Constants for the new tags in Exif 2.31 have been added.
   -  An ASCII field with zero count 0 is parsed to an empty Vec.
   -  `Tag` and `Context` are no longer re-exported.

## 0.1.2 (2017-02-25)

   -  Struct `Reader` has been added.
   -  The `parse_image` function has been deperecated.

## 0.1.1 (2017-01-12)

   -  The `parse_image` function has been added.

## 0.1 (2016-12-30)

   -  The first public version.
