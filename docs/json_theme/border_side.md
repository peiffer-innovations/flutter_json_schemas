[*description*][description]

# BorderSide class Null safety #

A side of a border of a box.

A Border consists of four BorderSide objects: Border.top, Border.left, Border.right, and Border.bottom.

Note that setting BorderSide.width to 0.0 will result in hairline rendering. A more involved explanation is present in BorderSide.width.

 *link* 

Sample

This sample shows how BorderSide objects can be used in a Container, via a BoxDecoration and a Border, to decorate some Text. In this example, the text has a thick bar above it that is light blue, and a thick bar below it that is a darker shade of blue.

*assignment*

    Container(
      padding: EdgeInsets.all(8.0),
      decoration: BoxDecoration(
        border: Border(
          top: BorderSide(width: 16.0, color: Colors.lightBlue.shade50),
          bottom: BorderSide(width: 16.0, color: Colors.lightBlue.shade900),
        ),
      ),
      child: Text('Flutter in the sky', textAlign: TextAlign.center),
    )

See also:

 *  Border, which uses BorderSide objects to represent its sides.
 *  BoxDecoration, which optionally takes a Border object.
 *  TableBorder, which is similar to Border but has two more sides (TableBorder.horizontalInside and TableBorder.verticalInside), both of which are also BorderSide objects.

Annotations

 *  @immutable

## Constructors ##

BorderSide(\{Color color: const Color(0xFF000000), double width: 1.0, BorderStyle style: BorderStyle.solid\})

Creates the side of a border. \[...\]

const

## Properties ##

color → Color

The color of this side of the border.

final

hashCode → int

The hash code for this object. \[...\]

read-only, override

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

style → BorderStyle

The style of this side of the border. \[...\]

final

width → double

The width of this side of the border, in logical pixels. \[...\]

final

## Methods ##

copyWith(\{Color? color, double? width, BorderStyle? style\}) → BorderSide

Creates a copy of this border but with the given fields replaced with the new values.

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

scale(double t) → BorderSide

Creates a copy of this border side description but with the width scaled by the factor `t`. \[...\]

toPaint() → Paint

Create a Paint object that, if used to stroke a line, will draw the line in this border's style. \[...\]

toString() → String

Returns a string representation of this object.

override

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

override

## Static Methods ##

canMerge(BorderSide a, BorderSide b) → bool

Whether the two given BorderSides can be merged using new BorderSide.merge. \[...\]

lerp(BorderSide a, BorderSide b, double t) → BorderSide

Linearly interpolate between two border sides. \[...\]

merge(BorderSide a, BorderSide b) → BorderSide

Creates a BorderSide that represents the addition of the two given BorderSides. \[...\]

## Constants ##

none → const BorderSide

A hairline black border that is not rendered.

`BorderSide(width: 0.0, style: BorderStyle.none)`


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/painting/borders.dart#L62