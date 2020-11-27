[*description*][description]

# FloatingActionButtonLocation class #

An object that defines a position for the FloatingActionButton based on the Scaffold's ScaffoldPrelayoutGeometry.

Flutter provides FloatingActionButtonLocations for the common FloatingActionButton placements in Material Design applications. These locations are available as static members of this class.

See also:

 *  FloatingActionButton, which is a circular button typically shown in the bottom right corner of the app.
 *  FloatingActionButtonAnimator, which is used to animate the Scaffold.floatingActionButton from one FloatingActionButtonLocation to another.
 *  ScaffoldPrelayoutGeometry, the geometry that FloatingActionButtonLocations use to position the FloatingActionButton.

Implementers

 *  StandardFabLocation

## Constructors ##

FloatingActionButtonLocation()

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

getOffset(ScaffoldPrelayoutGeometry scaffoldGeometry) → Offset

Places the FloatingActionButton based on the Scaffold's layout. \[...\]

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

toString() → String

Returns a string representation of this object.

override

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

inherited

## Constants ##

centerDocked → const FloatingActionButtonLocation

Centered FloatingActionButton, floating over the Scaffold.bottomNavigationBar so that the center of the floating action button lines up with the top of the bottom navigation bar. \[...\]

`_CenterDockedFabLocation()`

centerFloat → const FloatingActionButtonLocation

Centered FloatingActionButton, floating at the bottom of the screen. \[...\]

`_CenterFloatFabLocation()`

centerTop → const FloatingActionButtonLocation

Centered FloatingActionButton, floating over the transition between the Scaffold.appBar and the Scaffold.body. \[...\]

`_CenterTopFabLocation()`

endDocked → const FloatingActionButtonLocation

End-aligned FloatingActionButton, floating over the Scaffold.bottomNavigationBar so that the center of the floating action button lines up with the top of the bottom navigation bar. \[...\]

`_EndDockedFabLocation()`

endFloat → const FloatingActionButtonLocation

End-aligned FloatingActionButton, floating at the bottom of the screen. \[...\]

`_EndFloatFabLocation()`

endTop → const FloatingActionButtonLocation

End-aligned FloatingActionButton, floating over the transition between the Scaffold.appBar and the Scaffold.body. \[...\]

`_EndTopFabLocation()`

miniCenterDocked → const FloatingActionButtonLocation

Centered FloatingActionButton, floating over the Scaffold.bottomNavigationBar so that the center of the floating action button lines up with the top of the bottom navigation bar; intended to be used with FloatingActionButton.mini set to true. \[...\]

`_MiniCenterDockedFabLocation()`

miniCenterFloat → const FloatingActionButtonLocation

Centered FloatingActionButton, floating at the bottom of the screen, optimized for mini floating action buttons. \[...\]

`_MiniCenterFloatFabLocation()`

miniCenterTop → const FloatingActionButtonLocation

Centered FloatingActionButton, floating over the transition between the Scaffold.appBar and the Scaffold.body, intended to be used with FloatingActionButton.mini set to true. \[...\]

`_MiniCenterTopFabLocation()`

miniEndDocked → const FloatingActionButtonLocation

End-aligned FloatingActionButton, floating over the Scaffold.bottomNavigationBar so that the center of the floating action button lines up with the top of the bottom navigation bar, optimized for mini floating action buttons. \[...\]

`_MiniEndDockedFabLocation()`

miniEndFloat → const FloatingActionButtonLocation

End-aligned FloatingActionButton, floating at the bottom of the screen, optimized for mini floating action buttons. \[...\]

`_MiniEndFloatFabLocation()`

miniEndTop → const FloatingActionButtonLocation

End-aligned FloatingActionButton, floating over the transition between the Scaffold.appBar and the Scaffold.body, optimized for mini floating action buttons. \[...\]

`_MiniEndTopFabLocation()`

miniStartDocked → const FloatingActionButtonLocation

Start-aligned FloatingActionButton, floating over the Scaffold.bottomNavigationBar so that the center of the floating action button lines up with the top of the bottom navigation bar, optimized for mini floating action buttons. \[...\]

`_MiniStartDockedFabLocation()`

miniStartFloat → const FloatingActionButtonLocation

Start-aligned FloatingActionButton, floating at the bottom of the screen, optimized for mini floating action buttons. \[...\]

`_MiniStartFloatFabLocation()`

miniStartTop → const FloatingActionButtonLocation

Start-aligned FloatingActionButton, floating over the transition between the Scaffold.appBar and the Scaffold.body, optimized for mini floating action buttons. \[...\]

`_MiniStartTopFabLocation()`

startDocked → const FloatingActionButtonLocation

Start-aligned FloatingActionButton, floating over the Scaffold.bottomNavigationBar so that the center of the floating action button lines up with the top of the bottom navigation bar. \[...\]

`_StartDockedFabLocation()`

startFloat → const FloatingActionButtonLocation

Start-aligned FloatingActionButton, floating at the bottom of the screen. \[...\]

`_StartFloatFabLocation()`

startTop → const FloatingActionButtonLocation

Start-aligned FloatingActionButton, floating over the transition between the Scaffold.appBar and the Scaffold.body. \[...\]

`_StartTopFabLocation()`


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/floating_action_button_location.dart#L72