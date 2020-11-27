[*description*][description]

# VisualDensity class #

Defines the visual density of user interface components.

Density, in the context of a UI, is the vertical and horizontal "compactness" of the components in the UI. It is unitless, since it means different things to different UI components.

The default for visual densities is zero for both vertical and horizontal densities, which corresponds to the default visual density of components in the Material Design specification. It does not affect text sizes, icon sizes, or padding values.

For example, for buttons, it affects the spacing around the child of the button. For lists, it affects the distance between baselines of entries in the list. For chips, it only affects the vertical size, not the horizontal size.

See also:

 *  ThemeData.visualDensity, where this property is used to specify the base horizontal density of Material components.
 *  [Material design guidance on density][].

Mixed in types

 *  Diagnosticable

Annotations

 *  @immutable

## Constructors ##

VisualDensity(\{double horizontal: 0.0, double vertical: 0.0\})

A const constructor for VisualDensity. \[...\]

const

## Properties ##

baseSizeAdjustment → Offset

The base adjustment in logical pixels of the visual density of UI components. \[...\]

read-only

hashCode → int

The hash code for this object. \[...\]

read-only, override

horizontal → double

The horizontal visual density of UI components. \[...\]

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

vertical → double

The vertical visual density of UI components. \[...\]

final

## Methods ##

copyWith(\{double horizontal, double vertical\}) → VisualDensity

Copy the current VisualDensity with the given values replacing the current values.

debugFillProperties(DiagnosticPropertiesBuilder properties) → void

Add additional properties associated with the node. \[...\]

override

effectiveConstraints(BoxConstraints constraints) → BoxConstraints

Return a copy of `constraints` whose minimum width and height have been updated with the baseSizeAdjustment.

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

toDiagnosticsNode(\{String name, DiagnosticsTreeStyle style\}) → DiagnosticsNode

Returns a debug representation of the object that is used by debugging tools and by DiagnosticsNode.toStringDeep. \[...\]

inherited

toString(\{DiagnosticLevel minLevel: DiagnosticLevel.info\}) → String

Returns a string representation of this object.

inherited

toStringShort() → String

A brief description of this object, usually just the runtimeType and the hashCode. \[...\]

override

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

override

## Static Properties ##

adaptivePlatformDensity → VisualDensity

Returns a visual density that is adaptive based on the defaultTargetPlatform. \[...\]

read-only

## Static Methods ##

lerp(VisualDensity a, VisualDensity b, double t) → VisualDensity

Linearly interpolate between two densities.

## Constants ##

comfortable → const VisualDensity

The profile for a "comfortable" interpretation of VisualDensity. \[...\]

`VisualDensity(horizontal: -1.0, vertical: -1.0)`

compact → const VisualDensity

The profile for a "compact" interpretation of VisualDensity. \[...\]

`VisualDensity(horizontal: -2.0, vertical: -2.0)`

maximumDensity → const double

The maximum allowed density.

`4.0`

minimumDensity → const double

The minimum allowed density.

`-4.0`

standard → const VisualDensity

The default profile for VisualDensity in ThemeData. \[...\]

`VisualDensity()`


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/theme_data.dart#L1890
[Material design guidance on density]: https://material.io/design/layout/applying-density.html