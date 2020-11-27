[*description*][description]

# AssetImage class Null safety #

Fetches an image from an AssetBundle, having determined the exact image to use based on the context.

Given a main asset and a set of variants, AssetImage chooses the most appropriate asset for the current context, based on the device pixel ratio and size given in the configuration passed to resolve.

To show a specific image from a bundle without any asset resolution, use an AssetBundleImageProvider.

## Naming assets for matching with different pixel densities ##

Main assets are presumed to match a nominal pixel ratio of 1.0. To specify assets targeting different pixel ratios, place the variant assets in the application bundle under subdirectories named in the form "Nx", where N is the nominal device pixel ratio for that asset.

For example, suppose an application wants to use an icon named "heart.png". This icon has representations at 1.0 (the main icon), as well as 1.5 and 2.0 pixel ratios (variants). The asset bundle should then contain the following assets:

    heart.png
    1.5x/heart.png
    2.0x/heart.png

On a device with a 1.0 device pixel ratio, the image chosen would be heart.png; on a device with a 1.3 device pixel ratio, the image chosen would be 1.5x/heart.png.

The directory level of the asset does not matter as long as the variants are at the equivalent level; that is, the following is also a valid bundle structure:

    icons/heart.png
    icons/1.5x/heart.png
    icons/2.0x/heart.png

assets/icons/3.0x/heart.png would be a valid variant of assets/icons/heart.png.

## Fetching assets ##

When fetching an image provided by the app itself, use the assetName argument to name the asset to choose. For instance, consider the structure above. First, the `pubspec.yaml` of the project should specify its assets in the `flutter` section:

    flutter:
      assets:
        - icons/heart.png

Then, to fetch the image, use:

    AssetImage('icons/heart.png')

## Assets in packages ##

To fetch an asset from a package, the package argument must be provided. For instance, suppose the structure above is inside a package called `my_icons`. Then to fetch the image, use:

    AssetImage('icons/heart.png', package: 'my_icons')

Assets used by the package itself should also be fetched using the package argument as above.

If the desired asset is specified in the `pubspec.yaml` of the package, it is bundled automatically with the app. In particular, assets used by the package itself must be specified in its `pubspec.yaml`.

A package can also choose to have assets in its 'lib/' folder that are not specified in its `pubspec.yaml`. In this case for those images to be bundled, the app has to specify which ones to include. For instance a package named `fancy_backgrounds` could have:

    lib/backgrounds/background1.png
    lib/backgrounds/background2.png
    lib/backgrounds/background3.png

To include, say the first image, the `pubspec.yaml` of the app should specify it in the `assets` section:

    assets:
        - packages/fancy_backgrounds/backgrounds/background1.png

The `lib/` is implied, so it should not be included in the asset path.

See also:

 *  Image.asset for a shorthand of an Image widget backed by AssetImage when used without a scale.

Inheritance

 *  Object
 *  ImageProvider<AssetBundleImageKey>
 *  AssetBundleImageProvider
 *  AssetImage

Annotations

 *  @immutable

## Constructors ##

AssetImage(String assetName, \{AssetBundle? bundle, String? package\})

Creates an object that fetches an image from an asset bundle. \[...\]

const

## Properties ##

assetName → String

The name of the main asset from the set of images to choose from. See the documentation for the AssetImage class itself for details.

final

bundle → AssetBundle?

The bundle from which the image will be obtained. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

read-only, override

keyName → String

The name used to generate the key to obtain the asset. For local assets this is assetName, and for assets from packages the assetName is prefixed 'packages/

read-only

package → String?

The name of the package from which the image is included. See the documentation for the AssetImage class itself for details.

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

## Methods ##

createStream(ImageConfiguration configuration) → ImageStream

Called by resolve to create the ImageStream it returns. \[...\]

@protected, inherited

evict(\{ImageCache? cache, ImageConfiguration configuration: ImageConfiguration.empty\}) → Future<bool>

Evicts an entry from the image cache. \[...\]

inherited

load(AssetBundleImageKey key, DecoderCallback decode) → ImageStreamCompleter

Converts a key into an ImageStreamCompleter, and begins fetching the image.

inherited

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

obtainCacheStatus(\{required ImageConfiguration configuration, ImageErrorListener? handleError\}) → Future<ImageCacheStatus>

Returns the cache location for the key that this ImageProvider creates. \[...\]

inherited

obtainKey(ImageConfiguration configuration) → Future<AssetBundleImageKey>

Converts an ImageProvider's settings plus an ImageConfiguration to a key that describes the precise image to load. \[...\]

override

resolve(ImageConfiguration configuration) → ImageStream

Resolves this image provider using the given `configuration`, returning an ImageStream. \[...\]

@nonVirtual, inherited

resolveStreamForKey(ImageConfiguration configuration, ImageStream stream, AssetBundleImageKey key, ImageErrorListener handleError) → void

Called by resolve with the key returned by obtainKey. \[...\]

@protected, inherited

toString() → String

Returns a string representation of this object.

override

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

override


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/painting/image_resolution.dart#L125