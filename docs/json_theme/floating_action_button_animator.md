[*description*][description]

# FloatingActionButtonAnimator class #

Provider of animations to move the FloatingActionButton between FloatingActionButtonLocations.

The Scaffold uses Scaffold.floatingActionButtonAnimator to define:

 *  The Offset of the FloatingActionButton between the old and new FloatingActionButtonLocations as part of the transition animation.
 *  An Animation to scale the FloatingActionButton during the transition.
 *  An Animation to rotate the FloatingActionButton during the transition.
 *  Where to start a new animation from if an animation is interrupted.

See also:

 *  FloatingActionButton, which is a circular button typically shown in the bottom right corner of the app.
 *  FloatingActionButtonLocation, which the Scaffold uses to place the Scaffold.floatingActionButton within the Scaffold's layout.

## Constructors ##

FloatingActionButtonAnimator()

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

getAnimationRestart(double previousValue) → double

Gets the progress value to restart a motion animation from when the animation is interrupted. \[...\]

getOffset(\{Offset begin, Offset end, double progress\}) → Offset

Gets the FloatingActionButton's position relative to the origin of the Scaffold based on `progress`. \[...\]

getRotationAnimation(\{Animation<double> parent\}) → Animation<double>

Animates the rotation of Scaffold.floatingActionButton. \[...\]

getScaleAnimation(\{Animation<double> parent\}) → Animation<double>

Animates the scale of the FloatingActionButton. \[...\]

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

scaling → const FloatingActionButtonAnimator

Moves the FloatingActionButton by scaling out and then in at a new FloatingActionButtonLocation. \[...\]

`_ScalingFabMotionAnimator()`


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/floating_action_button_location.dart#L699