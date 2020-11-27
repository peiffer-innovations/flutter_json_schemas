[*description*][description]

# InteractiveInkFeatureFactory class #

An encapsulation of an InteractiveInkFeature constructor used by InkWell, InkResponse, and ThemeData.

Interactive ink feature implementations should provide a static const `splashFactory` value that's an instance of this class. The `splashFactory` can be used to configure an InkWell, InkResponse or ThemeData.

See also:

 *  InkSplash.splashFactory
 *  InkRipple.splashFactory

## Constructors ##

InteractiveInkFeatureFactory()

Subclasses should provide a const constructor.

const

## Properties ##

hashCode → int

The hash code for this object. \[...\]

read-only, inherited

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

## Methods ##

create(\{MaterialInkController controller, RenderBox referenceBox, Offset position, Color color, TextDirection textDirection, bool containedInkWell: false, RectCallback rectCallback, BorderRadius borderRadius, ShapeBorder customBorder, double radius, VoidCallback onRemoved\}) → InteractiveInkFeature

The factory method. \[...\]

@factory

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

toString() → String

Returns a string representation of this object.

inherited

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

inherited


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/ink_well.dart#L157