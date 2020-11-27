[*description*][description]

# Hero class #

A widget that marks its child as being a candidate for [hero animations][].

When a PageRoute is pushed or popped with the Navigator, the entire screen's content is replaced. An old route disappears and a new route appears. If there's a common visual feature on both routes then it can be helpful for orienting the user for the feature to physically move from one page to the other during the routes' transition. Such an animation is called a *hero animation*. The hero widgets "fly" in the Navigator's overlay during the transition and while they're in-flight they're, by default, not shown in their original locations in the old and new routes.

To label a widget as such a feature, wrap it in a Hero widget. When navigation happens, the Hero widgets on each route are identified by the HeroController. For each pair of Hero widgets that have the same tag, a hero animation is triggered.

If a Hero is already in flight when navigation occurs, its flight animation will be redirected to its new destination. The widget shown in-flight during the transition is, by default, the destination route's Hero's child.

For a Hero animation to trigger, the Hero has to exist on the very first frame of the new page's animation.

Routes must not contain more than one Hero for each tag.

## Discussion ##

Heroes and the Navigator's Overlay Stack must be axis-aligned for all this to work. The top left and bottom right coordinates of each animated Hero will be converted to global coordinates and then from there converted to that Stack's coordinate space, and the entire Hero subtree will, for the duration of the animation, be lifted out of its original place, and positioned on that stack. If the Hero isn't axis aligned, this is going to fail in a rather ugly fashion. Don't rotate your heroes!

To make the animations look good, it's critical that the widget tree for the hero in both locations be essentially identical. The widget of the *target* is, by default, used to do the transition: when going from route A to route B, route B's hero's widget is placed over route A's hero's widget. If a flightShuttleBuilder is supplied, its output widget is shown during the flight transition instead.

By default, both route A and route B's heroes are hidden while the transitioning widget is animating in-flight above the 2 routes. placeholderBuilder can be used to show a custom widget in their place instead once the transition has taken flight.

During the transition, the transition widget is animated to route B's hero's position, and then the widget is inserted into route B. When going back from B to A, route A's hero's widget is, by default, placed over where route B's hero's widget was, and then the animation goes the other way.

### Nested Navigators ###

If either or both routes contain nested Navigators, only Heroes contained in the top-most routes (as defined by Route.isCurrent) *of those nested Navigators* are considered for animation. Just like in the non-nested case the top-most routes containing these Heroes in the nested Navigators have to be PageRoutes.

## Parts of a Hero Transition ##

![Diagrams with parts of the Hero transition.][]

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  StatefulWidget
 *  Hero

## Constructors ##

Hero(\{Key key, @required Object tag, CreateRectTween createRectTween, HeroFlightShuttleBuilder flightShuttleBuilder, HeroPlaceholderBuilder placeholderBuilder, bool transitionOnUserGestures: false, @required Widget child\})

Create a hero. \[...\]

const

## Properties ##

child → Widget

The widget subtree that will "fly" from one route to another during a Navigator push or pop transition. \[...\]

final

createRectTween → CreateRectTween

Defines how the destination hero's bounds change as it flies from the starting route to the destination route. \[...\]

final

flightShuttleBuilder → HeroFlightShuttleBuilder

Optional override to supply a widget that's shown during the hero's flight. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

key → Key

Controls how one widget replaces another widget in the tree. \[...\]

final, inherited

placeholderBuilder → HeroPlaceholderBuilder

Placeholder widget left in place as the Hero's child once the flight takes off. \[...\]

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

tag → Object

The identifier for this particular hero. If the tag of this hero matches the tag of a hero on a PageRoute that we're navigating to or from, then a hero animation will be triggered.

final

transitionOnUserGestures → bool

Whether to perform the hero transition if the PageRoute transition was triggered by a user gesture, such as a back swipe on iOS. \[...\]

final

## Methods ##

createElement() → StatefulElement

Creates a StatefulElement to manage this widget's location in the tree. \[...\]

inherited

createState() → \_HeroState

Creates the mutable state for this widget at a given location in the tree. \[...\]

override

debugDescribeChildren() → List<DiagnosticsNode>

Returns a list of DiagnosticsNode objects describing this node's children. \[...\]

@protected, inherited

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

toStringDeep(\{String prefixLineOne: '', String prefixOtherLines, DiagnosticLevel minLevel: DiagnosticLevel.debug\}) → String

Returns a string representation of this node and its descendants. \[...\]

inherited

toStringShallow(\{String joiner: ', ', DiagnosticLevel minLevel: DiagnosticLevel.debug\}) → String

Returns a one-line detailed description of the object. \[...\]

inherited

toStringShort() → String

A short, textual description of this widget.

inherited

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

@nonVirtual, inherited


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/heroes.dart#L154
[hero animations]: https://flutter.dev/docs/development/ui/animations/hero-animations
[Diagrams with parts of the Hero transition.]: https://flutter.github.io/assets-for-api-docs/assets/interaction/heroes.png