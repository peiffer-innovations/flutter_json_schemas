[*description*][description]

# ScrollPhysics class #

Determines the physics of a Scrollable widget.

For example, determines how the Scrollable will behave when the user reaches the maximum scroll extent or when the user stops scrolling.

When starting a physics Simulation, the current scroll position and velocity are used as the initial conditions for the particle in the simulation. The movement of the particle in the simulation is then used to determine the scroll position for the widget.

Instead of creating your own subclasses, parent can be used to combine ScrollPhysics objects of different types to get the desired scroll physics. For example:

    const BouncingScrollPhysics(parent: AlwaysScrollableScrollPhysics())

You can also use `applyTo`, which is useful when you already have an instance of `ScrollPhysics`:

    ScrollPhysics physics = const BouncingScrollPhysics();
    // ...
    physics.applyTo(const AlwaysScrollableScrollPhysics())

Implementers

 *  AlwaysScrollableScrollPhysics
 *  BouncingScrollPhysics
 *  ClampingScrollPhysics
 *  FixedExtentScrollPhysics
 *  NeverScrollableScrollPhysics
 *  PageScrollPhysics
 *  RangeMaintainingScrollPhysics

Annotations

 *  @immutable

## Constructors ##

ScrollPhysics(\{ScrollPhysics parent\})

Creates an object with the default scroll physics.

const

## Properties ##

allowImplicitScrolling → bool

Whether a viewport is allowed to change its scroll position implicitly in response to a call to RenderObject.showOnScreen. \[...\]

read-only

dragStartDistanceMotionThreshold → double

The minimum amount of pixel distance drags must move by to start motion the first time or after each time the drag motion stopped. \[...\]

read-only

hashCode → int

The hash code for this object. \[...\]

read-only, inherited

maxFlingVelocity → double

Scroll fling velocity magnitudes will be clamped to this value.

read-only

minFlingDistance → double

The minimum distance an input pointer drag must have moved to to be considered a scroll fling gesture. \[...\]

read-only

minFlingVelocity → double

The minimum velocity for an input pointer drag to be considered a scroll fling. \[...\]

read-only

parent → ScrollPhysics

If non-null, determines the default behavior for each method. \[...\]

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

spring → SpringDescription

The spring to use for ballistic simulations.

read-only

tolerance → Tolerance

The tolerance to use for ballistic simulations.

read-only

## Methods ##

adjustPositionForNewDimensions(\{ScrollMetrics oldPosition, ScrollMetrics newPosition, bool isScrolling, double velocity\}) → double

Describes what the scroll position should be given new viewport dimensions. \[...\]

applyBoundaryConditions(ScrollMetrics position, double value) → double

Determines the overscroll by applying the boundary conditions. \[...\]

applyPhysicsToUserOffset(ScrollMetrics position, double offset) → double

Used by DragScrollActivity and other user-driven activities to convert an offset in logical pixels as provided by the DragUpdateDetails into a delta to apply (subtract from the current position) using ScrollActivityDelegate.setPixels. \[...\]

applyTo(ScrollPhysics ancestor) → ScrollPhysics

If parent is null then return a ScrollPhysics with the same runtimeType where the parent has been replaced with the `ancestor`. \[...\]

buildParent(ScrollPhysics ancestor) → ScrollPhysics

If parent is null then return ancestor, otherwise recursively build a ScrollPhysics that has `ancestor` as its parent. \[...\]

@protected

carriedMomentum(double existingVelocity) → double

Returns the velocity carried on repeated flings. \[...\]

createBallisticSimulation(ScrollMetrics position, double velocity) → Simulation

Returns a simulation for ballistic scrolling starting from the given position with the given velocity. \[...\]

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

recommendDeferredLoading(double velocity, ScrollMetrics metrics, BuildContext context) → bool

Provides a heuristic to determine if expensive frame-bound tasks should be deferred. \[...\]

shouldAcceptUserOffset(ScrollMetrics position) → bool

Whether the scrollable should let the user adjust the scroll offset, for example by dragging. \[...\]

toString() → String

Returns a string representation of this object.

override

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

inherited


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/scroll_physics.dart#L56