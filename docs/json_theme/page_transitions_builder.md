[*description*][description]

# PageTransitionsBuilder class #

Used by PageTransitionsTheme to define a MaterialPageRoute page transition animation.

Apps can configure the map of builders for ThemeData.pageTransitionsTheme to customize the default MaterialPageRoute page transition animation for different platforms.

See also:

 *  FadeUpwardsPageTransitionsBuilder, which defines a default page transition.
 *  OpenUpwardsPageTransitionsBuilder, which defines a page transition that's similar to the one provided by Android P.
 *  ZoomPageTransitionsBuilder, which defines a page transition similar to the one provided in Android 10.
 *  CupertinoPageTransitionsBuilder, which defines a horizontal page transition that matches native iOS page transitions.

Implementers

 *  CupertinoPageTransitionsBuilder
 *  FadeUpwardsPageTransitionsBuilder
 *  OpenUpwardsPageTransitionsBuilder
 *  ZoomPageTransitionsBuilder

## Constructors ##

PageTransitionsBuilder()

Abstract const constructor. This constructor enables subclasses to provide const constructors so that they can be used in const expressions.

const

## Properties ##

hashCode → int

The hash code for this object. \[...\]

read-only, inherited

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

## Methods ##

buildTransitions<T>(PageRoute<T> route, BuildContext context, Animation<double> animation, Animation<double> secondaryAnimation, Widget child) → Widget

Wraps the child with one or more transition widgets which define how `route` arrives on and leaves the screen. \[...\]

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/page_transitions_theme.dart#L404