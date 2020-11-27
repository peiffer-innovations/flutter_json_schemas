# Locale class Null safety #

An identifier used to select a user's language and formatting preferences.

This represents a [Unicode Language Identifier][] (i.e. without Locale extensions), except variants are not supported.

Locales are canonicalized according to the "preferred value" entries in the [IANA Language Subtag Registry][]. For example, `const Locale('he')` and `const Locale('iw')` are equal and both have the languageCode `he`, because `iw` is a deprecated language subtag that was replaced by the subtag `he`.

See also:

 *  Window.locale, which specifies the system's currently selected Locale.

## Constructors ##

Locale(String \_languageCode, \[String? \_countryCode\])

Creates a new Locale object. The first argument is the primary language subtag, the second is the region (also referred to as 'country') subtag. \[...\]

const

Locale.fromSubtags(\{String languageCode: 'und', String? scriptCode, String? countryCode\})

Creates a new Locale object. \[...\]

const

## Properties ##

countryCode → String?

The region subtag for the locale. \[...\]

read-only

hashCode → int

The hash code for this object. \[...\]

read-only, override

languageCode → String

The primary language subtag for the locale. \[...\]

read-only

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

scriptCode → String?

The script subtag for the locale. \[...\]

final

## Methods ##

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

toLanguageTag() → String

Returns a syntactically valid Unicode BCP47 Locale Identifier. \[...\]

toString() → String

Returns a string representing the locale. \[...\]

@keepToString, override

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

override


[Unicode Language Identifier]: https://www.unicode.org/reports/tr35/#Unicode_language_identifier
[IANA Language Subtag Registry]: https://www.iana.org/assignments/language-subtag-registry/language-subtag-registry