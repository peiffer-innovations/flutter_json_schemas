# Matrix4 class Null safety #

4D Matrix. Values are stored in column major order.

## Constructors ##

Matrix4(double arg0, double arg1, double arg2, double arg3, double arg4, double arg5, double arg6, double arg7, double arg8, double arg9, double arg10, double arg11, double arg12, double arg13, double arg14, double arg15)

Constructs a new mat4.

factory

Matrix4.columns(Vector4 arg0, Vector4 arg1, Vector4 arg2, Vector4 arg3)

Constructs a new mat4 from columns.

factory

Matrix4.compose(Vector3 translation, Quaternion rotation, Vector3 scale)

Constructs Matrix4 from `translation`, `rotation` and `scale`.

factory

Matrix4.copy(Matrix4 other)

Copies values from `other`.

factory

Matrix4.diagonal3(Vector3 scale)

Scale matrix.

factory

Matrix4.diagonal3Values(double x, double y, double z)

Scale matrix.

factory

Matrix4.fromBuffer(ByteBuffer buffer, int offset)

Constructs Matrix4 with a storage that views given `buffer` starting at `offset`. `offset` has to be multiple of Float64List.bytesPerElement.

Matrix4.fromFloat64List(Float64List \_m4storage)

Constructs Matrix4 with given Float64List as storage.

Matrix4.fromList(List<double> values)

New matrix from `values`.

factory

Matrix4.identity()

Identity matrix.

factory

Matrix4.inverted(Matrix4 other)

Constructs a matrix that is the inverse of `other`.

factory

Matrix4.outer(Vector4 u, Vector4 v)

Outer product of `u` and `v`.

factory

Matrix4.rotationX(double radians)

Rotation of `radians` around X.

factory

Matrix4.rotationY(double radians)

Rotation of `radians` around Y.

factory

Matrix4.rotationZ(double radians)

Rotation of `radians` around Z.

factory

Matrix4.skew(double alpha, double beta)

Skew matrix around X axis (alpha) and Y axis (beta).

factory

Matrix4.skewX(double alpha)

Skew matrix around X axis

factory

Matrix4.skewY(double beta)

Skew matrix around Y axis.

factory

Matrix4.translation(Vector3 translation)

Translation matrix.

factory

Matrix4.translationValues(double x, double y, double z)

Translation matrix.

factory

Matrix4.zero()

Zero matrix.

## Properties ##

dimension → int

Dimension of the matrix.

read-only

forward → Vector3

read-only

hashCode → int

The hash code for this object. \[...\]

read-only, override

right → Vector3

read-only

row0 ↔ Vector4

Returns row 0

read / write

row1 ↔ Vector4

Returns row 1

read / write

row2 ↔ Vector4

Returns row 2

read / write

row3 ↔ Vector4

Returns row 3

read / write

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

storage → Float64List

The components of the matrix.

read-only

up → Vector3

read-only

## Methods ##

absolute() → Matrix4

Returns the component wise absolute value of this.

absoluteError(Matrix4 correct) → double

Returns absolute error between this and `correct`

absoluteRotate(Vector3 arg) → Vector3

Rotates `arg` by the absolute rotation of this Returns `arg`. Primarily used by AABB transformation code.

add(Matrix4 o) → void

Adds `o` to this.

applyToVector3Array(List<double> array, \[int offset = 0\]) → List<double>

Multiply this to each set of xyz values in `array` starting at `offset`.

clone() → Matrix4

Clone matrix.

copyFromArray(List<double> array, \[int offset = 0\]) → void

Copies elements from `array` into this starting at `offset`.

copyInto(Matrix4 arg) → Matrix4

Copy into `arg`.

copyIntoArray(List<num> array, \[int offset = 0\]) → void

Copies this into `array` starting at `offset`.

copyInverse(Matrix4 arg) → double

Set this matrix to be the inverse of `arg`

copyRotation(Matrix3 rotation) → void

Copies the rotation matrix from this homogeneous transformation matrix into `rotation`.

decompose(Vector3 translation, Quaternion rotation, Vector3 scale) → void

Decomposes this into `translation`, `rotation` and `scale` components.

determinant() → double

Returns the determinant of this matrix.

dotColumn(int j, Vector4 v) → double

Returns the dot product of column `j` and `v`.

dotRow(int i, Vector4 v) → double

Returns the dot product of row `i` and `v`.

entry(int row, int col) → double

Value at `row`, `col`.

getColumn(int column) → Vector4

Gets the `column` of the matrix

getMaxScaleOnAxis() → double

Returns the max scale value of the 3 axes.

getNormalMatrix() → Matrix3

Returns the normal matrix from this homogeneous transformation matrix. The normal matrix is the transpose of the inverse of the top-left 3x3 part of this 4x4 matrix.

getRotation() → Matrix3

Returns the rotation matrix from this homogeneous transformation matrix.

getRow(int row) → Vector4

Gets the `row` of the matrix

getTranslation() → Vector3

Returns the translation vector from this homogeneous transformation matrix.

index(int row, int col) → int

Return index in storage for `row`, `col` value.

infinityNorm() → double

Returns infinity norm of the matrix. Used for numerical analysis.

invert() → double

Invert this.

invertRotation() → double

isIdentity() → bool

Is this the identity matrix?

isZero() → bool

Is this the zero matrix?

leftTranslate(dynamic x, \[double y = 0.0, double z = 0.0\]) → void

Multiply this by a translation from the left. The translation can be specified with a Vector3, Vector4, or x, y, z.

multiplied(Matrix4 arg) → Matrix4

Multiply a copy of this with `arg`.

multiply(Matrix4 arg) → void

Multiply this by `arg`.

multiplyTranspose(Matrix4 arg) → void

Multiply this with a transposed `arg`.

negate() → void

Negate this.

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

perspectiveTransform(Vector3 arg) → Vector3

Transform `arg` of type Vector3 using the perspective transformation defined by this.

relativeError(Matrix4 correct) → double

Returns relative error between this and `correct`

rotate(Vector3 axis, double angle) → void

Rotate this `angle` radians around `axis`

rotate3(Vector3 arg) → Vector3

Rotate `arg` of type Vector3 using the rotation defined by this.

rotated3(Vector3 arg, \[Vector3? out\]) → Vector3

Rotate a copy of `arg` of type Vector3 using the rotation defined by this. If a `out` parameter is supplied, the copy is stored in `out`.

rotateX(double angle) → void

Rotate this `angle` radians around X

rotateY(double angle) → void

Rotate this matrix `angle` radians around Y

rotateZ(double angle) → void

Rotate this matrix `angle` radians around Z

scale(dynamic x, \[double? y, double? z\]) → void

Scale this matrix by a Vector3, Vector4, or x,y,z

scaleAdjoint(double scale) → void

Converts into Adjugate matrix and scales by `scale`

scaled(dynamic x, \[double? y, double? z\]) → Matrix4

Create a copy of this scaled by a Vector3, Vector4 or `x`,`y`, and `z`.

setColumn(int column, Vector4 arg) → void

Assigns the `column` of the matrix `arg`

setColumns(Vector4 arg0, Vector4 arg1, Vector4 arg2, Vector4 arg3) → void

Sets the entire matrix to the column values.

setDiagonal(Vector4 arg) → void

Sets the diagonal of the matrix to be `arg`.

setEntry(int row, int col, double v) → void

Set value at `row`, `col` to be `v`.

setFrom(Matrix4 arg) → void

Sets the entire matrix to the matrix in `arg`.

setFromTranslationRotation(Vector3 arg0, Quaternion arg1) → void

Sets the matrix from translation `arg0` and rotation `arg1`.

setFromTranslationRotationScale(Vector3 translation, Quaternion rotation, Vector3 scale) → void

Sets the matrix from `translation`, `rotation` and `scale`.

setIdentity() → void

Makes this into the identity matrix.

setOuter(Vector4 u, Vector4 v) → void

setRotation(Matrix3 r) → void

Sets the rotation matrix in this homogeneous transformation matrix.

setRotationX(double radians) → void

Sets the upper 3x3 to a rotation of `radians` around X

setRotationY(double radians) → void

Sets the upper 3x3 to a rotation of `radians` around Y

setRotationZ(double radians) → void

Sets the upper 3x3 to a rotation of `radians` around Z

setRow(int row, Vector4 arg) → void

Assigns the `row` of the matrix `arg`

setTranslation(Vector3 t) → void

Sets the translation vector in this homogeneous transformation matrix.

setTranslationRaw(double x, double y, double z) → void

Sets the translation vector in this homogeneous transformation matrix.

setUpper2x2(Matrix2 arg) → void

Sets the upper 2x2 of the matrix to be `arg`.

setValues(double arg0, double arg1, double arg2, double arg3, double arg4, double arg5, double arg6, double arg7, double arg8, double arg9, double arg10, double arg11, double arg12, double arg13, double arg14, double arg15) → void

Sets the matrix with specified values.

setZero() → void

Zeros this.

splatDiagonal(double arg) → void

Sets the diagonal to `arg`.

sub(Matrix4 o) → void

Subtracts `o` from this.

toString() → String

Returns a printable string

override

trace() → double

Returns the trace of the matrix. The trace of a matrix is the sum of the diagonal entries.

transform(Vector4 arg) → Vector4

Transform `arg` of type Vector4 using the transformation defined by this.

transform3(Vector3 arg) → Vector3

Transform `arg` of type Vector3 using the transformation defined by this.

transformed(Vector4 arg, \[Vector4? out\]) → Vector4

Transform a copy of `arg` of type Vector4 using the transformation defined by this. If a `out` parameter is supplied, the copy is stored in `out`.

transformed3(Vector3 arg, \[Vector3? out\]) → Vector3

Transform a copy of `arg` of type Vector3 using the transformation defined by this. If a `out` parameter is supplied, the copy is stored in `out`.

translate(dynamic x, \[double y = 0.0, double z = 0.0\]) → void

Translate this matrix by a Vector3, Vector4, or x,y,z

transpose() → void

transposed() → Matrix4

Returns the tranpose of this.

transposeMultiply(Matrix4 arg) → void

Multiply a transposed this with `arg`.

transposeRotation() → void

Transposes just the upper 3x3 rotation matrix.

## Operators ##

operator \*(dynamic arg) → dynamic

Returns a new vector or matrix by multiplying this with `arg`.

operator +(Matrix4 arg) → Matrix4

Returns new matrix after component wise this + `arg`

operator -(Matrix4 arg) → Matrix4

Returns new matrix after component wise this - `arg`

operator ==(Object? other) → bool

Check if two matrices are the same.

override

operator \[\](int i) → double

Access the element of the matrix at the index `i`.

operator \[\]=(int i, double v) → void

Set the element of the matrix at the index `i`.

operator unary-() → Matrix4

Returns new matrix -this

## Static Methods ##

solve(Matrix4 A, Vector4 x, Vector4 b) → void

Solve `A` \* `x` = `b`.

solve2(Matrix4 A, Vector2 x, Vector2 b) → void

Solve `A` \* `x` = `b`.

solve3(Matrix4 A, Vector3 x, Vector3 b) → void

Solve `A` \* `x` = `b`.

tryInvert(Matrix4 other) → Matrix4?

Returns a matrix that is the inverse of `other` if `other` is invertible, otherwise `null`.