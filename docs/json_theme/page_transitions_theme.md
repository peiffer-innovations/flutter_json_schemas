[*description*][description]

# PageTransitionsTheme class #

Defines the page transition animations used by MaterialPageRoute for different TargetPlatforms.

The MaterialPageRoute.buildTransitions method looks up the current current PageTransitionsTheme with `Theme.of(context).pageTransitionsTheme` and delegates to buildTransitions.

If a builder with a matching platform is not found, then the FadeUpwardsPageTransitionsBuilder is used.

See also:

 *  ThemeData.pageTransitionsTheme, which defines the default page transitions for the overall theme.
 *  FadeUpwardsPageTransitionsBuilder, which defines a default page transition.
 *  OpenUpwardsPageTransitionsBuilder, which defines a page transition that's similar to the one provided by Android P.
 *  CupertinoPageTransitionsBuilder, which defines a horizontal page transition that matches native iOS page transitions.

Mixed in types

 *  Diagnosticable

Annotations

 *  @immutable

## Constructors ##

PageTransitionsTheme(\{Map<TargetPlatform, PageTransitionsBuilder> builders\})

Construct a PageTransitionsTheme. \[...\]

const

## Properties ##

builders → Map<TargetPlatform, PageTransitionsBuilder>

The PageTransitionsBuilders supported by this theme.

read-only

hashCode → int

The hash code for this object. \[...\]

read-only, override

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

## Methods ##

buildTransitions<T>(PageRoute<T> route, BuildContext context, Animation<double> animation, Animation<double> secondaryAnimation, Widget child) → Widget

Delegates to the builder for the current ThemeData.platform or FadeUpwardsPageTransitionsBuilder. \[...\]

debugFillProperties(DiagnosticPropertiesBuilder properties) → void

Add additional properties associated with the node. \[...\]

override

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

inherited

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

override


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/page_transitions_theme.dart#L563