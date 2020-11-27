[*description*][description]

# CupertinoThemeData class #

Styling specifications for a CupertinoTheme.

All constructor parameters can be null, in which case a CupertinoColors.activeBlue based default iOS theme styling is used.

Parameters can also be partially specified, in which case some parameters will cascade down to other dependent parameters to create a cohesive visual effect. For instance, if a primaryColor is specified, it would cascade down to affect some fonts in textTheme if textTheme is not specified.

See also:

 *  CupertinoTheme, in which this CupertinoThemeData is inserted.
 *  ThemeData, a Material equivalent that also configures Cupertino styling via a CupertinoThemeData subclass MaterialBasedCupertinoThemeData.

Mixed in types

 *  Diagnosticable

Implementers

 *  MaterialBasedCupertinoThemeData

Annotations

 *  @immutable

## Constructors ##

CupertinoThemeData(\{Brightness brightness, Color primaryColor, Color primaryContrastingColor, CupertinoTextThemeData textTheme, Color barBackgroundColor, Color scaffoldBackgroundColor\})

Creates a CupertinoTheme styling specification. \[...\]

const

CupertinoThemeData.raw(Brightness brightness, Color primaryColor, Color primaryContrastingColor, CupertinoTextThemeData textTheme, Color barBackgroundColor, Color scaffoldBackgroundColor)

Same as the default constructor but with positional arguments to avoid forgetting any and to specify all arguments. \[...\]

const

## Properties ##

barBackgroundColor → Color

Background color of the top nav bar and bottom tab bar. \[...\]

read-only

brightness → Brightness

The brightness override for Cupertino descendants. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

read-only, inherited

primaryColor → Color

A color used on interactive elements of the theme. \[...\]

read-only

primaryContrastingColor → Color

A color that must be easy to see when rendered on a primaryColor background. \[...\]

read-only

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

scaffoldBackgroundColor → Color

Background color of the scaffold. \[...\]

read-only

textTheme → CupertinoTextThemeData

Text styles used by Cupertino widgets. \[...\]

read-only

## Methods ##

copyWith(\{Brightness brightness, Color primaryColor, Color primaryContrastingColor, CupertinoTextThemeData textTheme, Color barBackgroundColor, Color scaffoldBackgroundColor\}) → CupertinoThemeData

Creates a copy of CupertinoThemeData with specified attributes overridden. \[...\]

debugFillProperties(DiagnosticPropertiesBuilder properties) → void

Add additional properties associated with the node. \[...\]

override

noDefault() → CupertinoThemeData

Returns an instance of the CupertinoThemeData whose property getters only return the construction time specifications with no derived values. \[...\]

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

resolveFrom(BuildContext context, \{bool nullOk: false\}) → CupertinoThemeData

Returns a new `CupertinoThemeData` with all its colors resolved against the given BuildContext. \[...\]

@protected

toDiagnosticsNode(\{String name, DiagnosticsTreeStyle style\}) → DiagnosticsNode

Returns a debug representation of the object that is used by debugging tools and by DiagnosticsNode.toStringDeep. \[...\]

inherited

toString(\{DiagnosticLevel minLevel: DiagnosticLevel.info\}) → String

Returns a string representation of this object.

inherited

toStringShort() → String

A brief description of this object, usually just the runtimeType and the hashCode. \[...\]

inherited

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

inherited


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/cupertino/theme.dart#L148