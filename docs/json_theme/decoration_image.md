[*description*][description]

# DecorationImage class Null safety #

An image for a box decoration.

The image is painted using paintImage, which describes the meanings of the various fields on this class in more detail.

Annotations

 *  @immutable

## Constructors ##

DecorationImage(\{required ImageProvider<Object> image, ImageErrorListener? onError, ColorFilter? colorFilter, BoxFit? fit, AlignmentGeometry alignment: Alignment.center, Rect? centerSlice, ImageRepeat repeat: ImageRepeat.noRepeat, bool matchTextDirection: false, double scale: 1.0\})

Creates an image to show in a BoxDecoration. \[...\]

const

## Properties ##

alignment → AlignmentGeometry

How to align the image within its bounds. \[...\]

final

centerSlice → Rect?

The center slice for a nine-patch image. \[...\]

final

colorFilter → ColorFilter?

A color filter to apply to the image before painting it.

final

fit → BoxFit?

How the image should be inscribed into the box. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

read-only, override

image → ImageProvider<Object>

The image to be painted into the decoration. \[...\]

final

matchTextDirection → bool

Whether to paint the image in the direction of the TextDirection. \[...\]

final

onError → ImageErrorListener?

An optional error callback for errors emitted when loading image.

final

repeat → ImageRepeat

How to paint any portions of the box that would not otherwise be covered by the image.

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

scale → double

Defines image pixels to be shown per logical pixels. \[...\]

final

## Methods ##

createPainter(VoidCallback onChanged) → DecorationImagePainter

Creates a DecorationImagePainter for this DecorationImage. \[...\]

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

toString() → String

Returns a string representation of this object.

override

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

override


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/painting/decoration_image.dart#L40