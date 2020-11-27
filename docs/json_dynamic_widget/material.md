[*description*][description]

# Material class #

A piece of material.

The Material widget is responsible for:

1.  Clipping: If clipBehavior is not Clip.none, Material clips its widget sub-tree to the shape specified by shape, type, and borderRadius. By default, clipBehavior is Clip.none for performance considerations.
2.  Elevation: Material elevates its widget sub-tree on the Z axis by elevation pixels, and draws the appropriate shadow.
3.  Ink effects: Material shows ink effects implemented by InkFeatures like InkSplash and InkHighlight below its children.

## The Material Metaphor ##

Material is the central metaphor in material design. Each piece of material exists at a given elevation, which influences how that piece of material visually relates to other pieces of material and how that material casts shadows.

Most user interface elements are either conceptually printed on a piece of material or themselves made of material. Material reacts to user input using InkSplash and InkHighlight effects. To trigger a reaction on the material, use a MaterialInkController obtained via Material.of.

In general, the features of a Material should not change over time (e.g. a Material should not change its color, shadowColor or type). Changes to elevation and shadowColor are animated for animationDuration. Changes to shape are animated if type is not MaterialType.transparency and ShapeBorder.lerp between the previous and next shape values is supported. Shape changes are also animated for animationDuration.

## Shape ##

The shape for material is determined by shape, type, and borderRadius.

 *  If shape is non null, it determines the shape.
 *  If shape is null and borderRadius is non null, the shape is a rounded rectangle, with corners specified by borderRadius.
 *  If shape and borderRadius are null, type determines the shape as follows:
    
     *  MaterialType.canvas: the default material shape is a rectangle.
     *  MaterialType.card: the default material shape is a rectangle with rounded edges. The edge radii is specified by kMaterialEdges.
     *  MaterialType.circle: the default material shape is a circle.
     *  MaterialType.button: the default material shape is a rectangle with rounded edges. The edge radii is specified by kMaterialEdges.
     *  MaterialType.transparency: the default material shape is a rectangle.

## Border ##

If shape is not null, then its border will also be painted (if any).

## Layout change notifications ##

If the layout changes (e.g. because there's a list on the material, and it's been scrolled), a LayoutChangedNotification must be dispatched at the relevant subtree. This in particular means that transitions (e.g. SlideTransition) should not be placed inside Material widgets so as to move subtrees that contain InkResponses, InkWells, Inks, or other widgets that use the InkFeature mechanism. Otherwise, in-progress ink features (e.g., ink splashes and ink highlights) won't move to account for the new layout.

## Painting over the material ##

Material widgets will often trigger reactions on their nearest material ancestor. For example, ListTile.hoverColor triggers a reaction on the tile's material when a pointer is hovering over it. These reactions will be obscured if any widget in between them and the material paints in such a way as to obscure the material (such as setting a BoxDecoration.color on a DecoratedBox). To avoid this behavior, use InkDecoration to decorate the material itself.

See also:

 *  MergeableMaterial, a piece of material that can split and re-merge.
 *  Card, a wrapper for a Material of type MaterialType.card.
 *  [material.io/design/][material.io_design]

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  StatefulWidget
 *  Material

## Constructors ##

Material(\{Key key, MaterialType type: MaterialType.canvas, double elevation: 0.0, Color color, Color shadowColor, TextStyle textStyle, BorderRadiusGeometry borderRadius, ShapeBorder shape, bool borderOnForeground: true, Clip clipBehavior: Clip.none, Duration animationDuration: kThemeChangeDuration, Widget child\})

Creates a piece of material. \[...\]

const

## Properties ##

animationDuration → Duration

Defines the duration of animated changes for shape, elevation, shadowColor and the elevation overlay if it is applied. \[...\]

final

borderOnForeground → bool

Whether to paint the shape border in front of the child. \[...\]

final

borderRadius → BorderRadiusGeometry

If non-null, the corners of this box are rounded by this BorderRadiusGeometry value. \[...\]

final

child → Widget

The widget below this widget in the tree. \[...\]

final

clipBehavior → Clip

The content will be clipped (or not) according to this option. \[...\]

final

color → Color

The color to paint the material. \[...\]

final

elevation → double

The z-coordinate at which to place this material relative to its parent. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

key → Key

Controls how one widget replaces another widget in the tree. \[...\]

final, inherited

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

shadowColor → Color

The color to paint the shadow below the material. \[...\]

final

shape → ShapeBorder

Defines the material's shape as well its shadow. \[...\]

final

textStyle → TextStyle

The typographical style to use for text within this material.

final

type → MaterialType

The kind of material to show (e.g., card or canvas). This affects the shape of the widget, the roundness of its corners if the shape is rectangular, and the default color.

final

## Methods ##

createElement() → StatefulElement

Creates a StatefulElement to manage this widget's location in the tree. \[...\]

inherited

createState() → \_MaterialState

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

## Static Methods ##

of(BuildContext context) → MaterialInkController

The ink controller from the closest instance of this class that encloses the given context. \[...\]

## Constants ##

defaultSplashRadius → const double

The default radius of an ink splash in logical pixels.

`35.0`


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/material.dart#L167
[material.io_design]: https://material.io/design/