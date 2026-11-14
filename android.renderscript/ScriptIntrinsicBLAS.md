Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScriptIntrinsicBLAS

Kotlin | [Java](ScriptIntrinsicBLAS.md)
| --- | --- |

```
class ScriptIntrinsicBLAS : ScriptIntrinsic
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [android.renderscript.BaseObj](BaseObj.md) ||||
| | ↳ | [android.renderscript.Script](Script.md) |||
| | | ↳ | [android.renderscript.ScriptIntrinsic](ScriptIntrinsic.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.renderscript.ScriptIntrinsicBLAS](ScriptIntrinsicBLAS.md) |

| **This class was deprecated in API level 31.**
|
| Renderscript has been deprecated in API level 31. Please refer to the [migration guide](https://developer.android.com/guide/topics/renderscript/migration-guide) for the proposed alternatives.

ScriptIntrinsicBLAS class provides high performance RenderScript APIs to BLAS. The BLAS (Basic Linear Algebra Subprograms) are routines that provide standard building blocks for performing basic vector and matrix operations. For detailed description of BLAS, please refer to http://www.netlib.org/blas/

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LEFT:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NON_UNIT:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#RIGHT:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UNIT:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` <br /> |
| --- | --- |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | BNNM 8-bit GEMM-like operation for neural networks: C = A \* Transpose(B) Calculations are done in 1. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | CGBMV CGBMV performs one of the matrix-vector operations y := alpha\*A\*x + beta\*y or y := alpha\*A\*\*T\*x + beta\*y or y := alpha\*A\*\*H\*x + beta\*y Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | CGEMM CGEMM performs one of the matrix-matrix operations C := alpha\*op(A)\*op(B) + beta\*C where op(X) is one of op(X) = X or op(X) = X\*\*T or op(X) = X\*\*H Details: http://www. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | CGEMV CGEMV performs one of the matrix-vector operations y := alpha\*A\*x + beta\*y or y := alpha\*A\*\*T\*x + beta\*y or y := alpha\*A\*\*H\*x + beta\*y Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | CGERC CGERC performs the rank 1 operation A := alpha\*x\*y\*\*H + A Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | CGERU CGERU performs the rank 1 operation A := alpha\*x\*y\*\*T + A Details: http://www. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | CHBMV CHBMV performs the matrix-vector operation y := alpha\*A\*x + beta\*y Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | CHEMM CHEMM performs one of the matrix-matrix operations C := alpha\*A\*B + beta\*C or C := alpha\*B\*A + beta\*C Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | CHEMV CHEMV performs the matrix-vector operation y := alpha\*A\*x + beta\*y Details: http://www. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | CHER CHER performs the rank 1 operation A := alpha\*x\*x\*\*H + A Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | CHER2 CHER2 performs the symmetric rank 2 operation A := alpha\*x\*y\*\*H + alpha\*y\*x\*\*H + A Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | CHER2K CHER2K performs one of the hermitian rank 2k operations C := alpha\*A\*B\*\*H + conjg( alpha )\*B\*A\*\*H + beta\*C or C := alpha\*A\*\*H\*B + conjg( alpha )\*B\*\*H\*A + beta\*C Details: http://www. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | CHERK CHERK performs one of the hermitian rank k operations C := alpha\*A\*A\*\*H + beta\*C or C := alpha\*A\*\*H\*A + beta\*C Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | CHPMV CHPMV performs the matrix-vector operation y := alpha\*A\*x + beta\*y Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | CHPR CHPR performs the rank 1 operation A := alpha\*x\*x\*\*H + A Details: http://www. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | CHPR2 CHPR2 performs the symmetric rank 2 operation A := alpha\*x\*y\*\*H + alpha\*y\*x\*\*H + A Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | CSYMM CSYMM performs one of the matrix-matrix operations C := alpha\*A\*B + beta\*C or C := alpha\*B\*A + beta\*C Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | CSYR2K CSYR2K performs one of the symmetric rank 2k operations C := alpha\*A\*B\*\*T + alpha\*B\*A\*\*T + beta\*C or C := alpha\*A\*\*T\*B + alpha\*B\*\*T\*A + beta\*C Details: http://www. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | CSYRK CSYRK performs one of the symmetric rank k operations C := alpha\*A\*A\*\*T + beta\*C or C := alpha\*A\*\*T\*A + beta\*C Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | CTBMV CTBMV performs one of the matrix-vector operations x := A\*x or x := A\*\*T\*x or x := A\*\*H\*x Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | CTBSV CTBSV solves one of the systems of equations A\*x = b or A\*\*T\*x = b or A\*\*H\*x = b Details: http://www. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | CTPMV CTPMV performs one of the matrix-vector operations x := A\*x or x := A\*\*T\*x or x := A\*\*H\*x Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | CTPSV CTPSV solves one of the systems of equations A\*x = b or A\*\*T\*x = b or A\*\*H\*x = b Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | CTRMM CTRMM performs one of the matrix-matrix operations B := alpha\*op(A)\*B or B := alpha\*B\*op(A) op(A) is one of op(A) = A or op(A) = A\*\*T or op(A) = A\*\*H Details: http://www. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | CTRMV CTRMV performs one of the matrix-vector operations x := A\*x or x := A\*\*T\*x or x := A\*\*H\*x Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | CTRSM CTRSM solves one of the matrix equations op(A)\*X := alpha\*B or X\*op(A) := alpha\*B op(A) is one of op(A) = A or op(A) = A\*\*T or op(A) = A\*\*H Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | CTRSV CTRSV solves one of the systems of equations A\*x = b or A\*\*T\*x = b or A\*\*H\*x = b Details: http://www. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | DGBMV DGBMV performs one of the matrix-vector operations y := alpha\*A\*x + beta\*y or y := alpha\*A\*\*T\*x + beta\*y Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | DGEMM DGEMM performs one of the matrix-matrix operations C := alpha\*op(A)\*op(B) + beta\*C where op(X) is one of op(X) = X or op(X) = X\*\*T Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | DGEMV DGEMV performs one of the matrix-vector operations y := alpha\*A\*x + beta\*y or y := alpha\*A\*\*T\*x + beta\*y Details: http://www. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | DGER DGER performs the rank 1 operation A := alpha\*x\*y\*\*T + A Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | DSBMV DSBMV performs the matrix-vector operation y := alpha\*A\*x + beta\*y Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | DSPMV DSPMV performs the matrix-vector operation y := alpha\*A\*x + beta\*y Details: http://www. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | DSPR DSPR performs the rank 1 operation A := alpha\*x\*x\*\*T + A Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | DSPR2 DSPR2 performs the symmetric rank 2 operation A := alpha\*x\*y\*\*T + alpha\*y\*x\*\*T + A Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | DSYMM DSYMM performs one of the matrix-matrix operations C := alpha\*A\*B + beta\*C or C := alpha\*B\*A + beta\*C Details: http://www. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | DSYMV DSYMV performs the matrix-vector operation y := alpha\*A\*x + beta\*y Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | DSYR DSYR performs the rank 1 operation A := alpha\*x\*x\*\*T + A Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | DSYR2 DSYR2 performs the symmetric rank 2 operation A := alpha\*x\*y\*\*T + alpha\*y\*x\*\*T + A Details: http://www. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | DSYR2K DSYR2K performs one of the symmetric rank 2k operations C := alpha\*A\*B\*\*T + alpha\*B\*A\*\*T + beta\*C or C := alpha\*A\*\*T\*B + alpha\*B\*\*T\*A + beta\*C Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | DSYRK DSYRK performs one of the symmetric rank k operations C := alpha\*A\*A\*\*T + beta\*C or C := alpha\*A\*\*T\*A + beta\*C Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | DTBMV DTBMV performs one of the matrix-vector operations x := A\*x or x := A\*\*T\*x Details: http://www. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | DTBSV DTBSV solves one of the systems of equations A\*x = b or A\*\*T\*x = b Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | DTPMV DTPMV performs one of the matrix-vector operations x := A\*x or x := A\*\*T\*x Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | DTPSV DTPSV solves one of the systems of equations A\*x = b or A\*\*T\*x = b Details: http://www. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | DTRMM DTRMM performs one of the matrix-matrix operations B := alpha\*op(A)\*B or B := alpha\*B\*op(A) op(A) is one of op(A) = A or op(A) = A\*\*T Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | DTRMV DTRMV performs one of the matrix-vector operations x := A\*x or x := A\*\*T\*x Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | DTRSM DTRSM solves one of the matrix equations op(A)\*X := alpha\*B or X\*op(A) := alpha\*B op(A) is one of op(A) = A or op(A) = A\*\*T Details: http://www. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | DTRSV DTRSV solves one of the systems of equations A\*x = b or A\*\*T\*x = b Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | SGBMV SGBMV performs one of the matrix-vector operations y := alpha\*A\*x + beta\*y or y := alpha\*A\*\*T\*x + beta\*y Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | SGEMM SGEMM performs one of the matrix-matrix operations C := alpha\*op(A)\*op(B) + beta\*C where op(X) is one of op(X) = X or op(X) = X\*\*T Details: http://www. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | SGEMV SGEMV performs one of the matrix-vector operations y := alpha\*A\*x + beta\*y or y := alpha\*A\*\*T\*x + beta\*y Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | SGER SGER performs the rank 1 operation A := alpha\*x\*y\*\*T + A Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | SSBMV SSBMV performs the matrix-vector operation y := alpha\*A\*x + beta\*y Details: http://www. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | SSPMV SSPMV performs the matrix-vector operation y := alpha\*A\*x + beta\*y Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | SSPR SSPR performs the rank 1 operation A := alpha\*x\*x\*\*T + A Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | SSPR2 SSPR2 performs the symmetric rank 2 operation A := alpha\*x\*y\*\*T + alpha\*y\*x\*\*T + A Details: http://www. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | SSYMM SSYMM performs one of the matrix-matrix operations C := alpha\*A\*B + beta\*C or C := alpha\*B\*A + beta\*C Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | SSYMV SSYMV performs the matrix-vector operation y := alpha\*A\*x + beta\*y Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | SSYR SSYR performs the rank 1 operation A := alpha\*x\*x\*\*T + A Details: http://www. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | SSYR2 SSYR2 performs the symmetric rank 2 operation A := alpha\*x\*y\*\*T + alpha\*y\*x\*\*T + A Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | SSYR2K SSYR2K performs one of the symmetric rank 2k operations C := alpha\*A\*B\*\*T + alpha\*B\*A\*\*T + beta\*C or C := alpha\*A\*\*T\*B + alpha\*B\*\*T\*A + beta\*C Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | SSYRK SSYRK performs one of the symmetric rank k operations C := alpha\*A\*A\*\*T + beta\*C or C := alpha\*A\*\*T\*A + beta\*C Details: http://www. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | STBMV STBMV performs one of the matrix-vector operations x := A\*x or x := A\*\*T\*x Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | STBSV STBSV solves one of the systems of equations A\*x = b or A\*\*T\*x = b Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | STPMV STPMV performs one of the matrix-vector operations x := A\*x or x := A\*\*T\*x Details: http://www. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | STPSV STPSV solves one of the systems of equations A\*x = b or A\*\*T\*x = b Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | STRMM STRMM performs one of the matrix-matrix operations B := alpha\*op(A)\*B or B := alpha\*B\*op(A) op(A) is one of op(A) = A or op(A) = A\*\*T Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | STRMV STRMV performs one of the matrix-vector operations x := A\*x or x := A\*\*T\*x Details: http://www. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | STRSM STRSM solves one of the matrix equations op(A)\*X := alpha\*B or X\*op(A) := alpha\*B op(A) is one of op(A) = A or op(A) = A\*\*T Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | STRSV STRSV solves one of the systems of equations A\*x = b or A\*\*T\*x = b Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | ZGBMV ZGBMV performs one of the matrix-vector operations y := alpha\*A\*x + beta\*y or y := alpha\*A\*\*T\*x + beta\*y or y := alpha\*A\*\*H\*x + beta\*y Details: http://www. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | ZGEMM ZGEMM performs one of the matrix-matrix operations C := alpha\*op(A)\*op(B) + beta\*C where op(X) is one of op(X) = X or op(X) = X\*\*T or op(X) = X\*\*H Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | ZGEMV ZGEMV performs one of the matrix-vector operations y := alpha\*A\*x + beta\*y or y := alpha\*A\*\*T\*x + beta\*y or y := alpha\*A\*\*H\*x + beta\*y Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | ZGERC ZGERC performs the rank 1 operation A := alpha\*x\*y\*\*H + A Details: http://www. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | ZGERU ZGERU performs the rank 1 operation A := alpha\*x\*y\*\*T + A Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | ZHBMV ZHBMV performs the matrix-vector operation y := alpha\*A\*x + beta\*y Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | ZHEMM ZHEMM performs one of the matrix-matrix operations C := alpha\*A\*B + beta\*C or C := alpha\*B\*A + beta\*C Details: http://www. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | ZHEMV ZHEMV performs the matrix-vector operation y := alpha\*A\*x + beta\*y Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | ZHER ZHER performs the rank 1 operation A := alpha\*x\*x\*\*H + A Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | ZHER2 ZHER2 performs the symmetric rank 2 operation A := alpha\*x\*y\*\*H + alpha\*y\*x\*\*H + A Details: http://www. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | ZHER2K ZHER2K performs one of the hermitian rank 2k operations C := alpha\*A\*B\*\*H + conjg( alpha )\*B\*A\*\*H + beta\*C or C := alpha\*A\*\*H\*B + conjg( alpha )\*B\*\*H\*A + beta\*C Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | ZHERK ZHERK performs one of the hermitian rank k operations C := alpha\*A\*A\*\*H + beta\*C or C := alpha\*A\*\*H\*A + beta\*C Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | ZHPMV ZHPMV performs the matrix-vector operation y := alpha\*A\*x + beta\*y Details: http://www. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | ZHPR ZHPR performs the rank 1 operation A := alpha\*x\*x\*\*H + A Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | ZHPR2 ZHPR2 performs the symmetric rank 2 operation A := alpha\*x\*y\*\*H + alpha\*y\*x\*\*H + A Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | ZSYMM ZSYMM performs one of the matrix-matrix operations C := alpha\*A\*B + beta\*C or C := alpha\*B\*A + beta\*C Details: http://www. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | ZSYR2K ZSYR2K performs one of the symmetric rank 2k operations C := alpha\*A\*B\*\*T + alpha\*B\*A\*\*T + beta\*C or C := alpha\*A\*\*T\*B + alpha\*B\*\*T\*A + beta\*C Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | ZSYRK ZSYRK performs one of the symmetric rank k operations C := alpha\*A\*A\*\*T + beta\*C or C := alpha\*A\*\*T\*A + beta\*C Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | ZTBMV ZTBMV performs one of the matrix-vector operations x := A\*x or x := A\*\*T\*x or x := A\*\*H\*x Details: http://www. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | ZTBSV ZTBSV solves one of the systems of equations A\*x = b or A\*\*T\*x = b or A\*\*H\*x = b Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | ZTPMV ZTPMV performs one of the matrix-vector operations x := A\*x or x := A\*\*T\*x or x := A\*\*H\*x Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | ZTPSV ZTPSV solves one of the systems of equations A\*x = b or A\*\*T\*x = b or A\*\*H\*x = b Details: http://www. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | ZTRMM ZTRMM performs one of the matrix-matrix operations B := alpha\*op(A)\*B or B := alpha\*B\*op(A) op(A) is one of op(A) = A or op(A) = A\*\*T or op(A) = A\*\*H Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | ZTRMV ZTRMV performs one of the matrix-vector operations x := A\*x or x := A\*\*T\*x or x := A\*\*H\*x Details: http://www. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | ZTRSM ZTRSM solves one of the matrix equations op(A)\*X := alpha\*B or X\*op(A) := alpha\*B op(A) is one of op(A) = A or op(A) = A\*\*T or op(A) = A\*\*H Details: http://www. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | ZTRSV ZTRSV solves one of the systems of equations A\*x = b or A\*\*T\*x = b or A\*\*H\*x = b Details: http://www. |
| static [ScriptIntrinsicBLAS](ScriptIntrinsicBLAS.md)! | create Create an intrinsic to access BLAS subroutines. |

## Constants

### CONJ_TRANSPOSE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONJ_TRANSPOSE: Int
```

**Deprecated:** *Deprecated in Java.*

 Value: 113

### LEFT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LEFT: Int
```

**Deprecated:** *Deprecated in Java.*

 Value: 141

### LOWER

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LOWER: Int
```

**Deprecated:** *Deprecated in Java.*

 Value: 122

### NON_UNIT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NON_UNIT: Int
```

**Deprecated:** *Deprecated in Java.*

 Value: 131

### NO_TRANSPOSE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NO_TRANSPOSE: Int
```

**Deprecated:** *Deprecated in Java.*

 Value: 111

### RIGHT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RIGHT: Int
```

**Deprecated:** *Deprecated in Java.*

 Value: 142

### TRANSPOSE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRANSPOSE: Int
```

**Deprecated:** *Deprecated in Java.*

 Value: 112

### UNIT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNIT: Int
```

**Deprecated:** *Deprecated in Java.*

 Value: 132

### UPPER

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UPPER: Int
```

**Deprecated:** *Deprecated in Java.*

 Value: 121

## Public methods

### BNNM

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun BNNM(
    A: Allocation!, 
    a_offset: Int, 
    B: Allocation!, 
    b_offset: Int, 
    C: Allocation!, 
    c_offset: Int, 
    c_mult: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

8-bit GEMM-like operation for neural networks: C = A \* Transpose(B) Calculations are done in 1.10.21 fixed-point format for the final output, just before there's a shift down to drop the fractional parts. The output values are gated to 0 to 255 to fit in a byte, but the 10-bit format gives some headroom to avoid wrapping around on small overflows.

| Parameters ||
|---|---|
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type U8. |
| `a_offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The offset for all values in matrix A, e.g A\[i,j\] = A\[i,j\] - a_offset. Value should be from 0 to 255. |
| `B` | [Allocation](Allocation.md)!: The input allocation contains matrix B, supported elements type U8. |
| --- | --- |
| `b_offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The offset for all values in matrix B, e.g B\[i,j\] = B\[i,j\] - b_offset. Value should be from 0 to 255. |
| `C` | [Allocation](Allocation.md)!: The input allocation contains matrix C, supported elements type U8. |
| `c_offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The offset for all values in matrix C. |
| --- | --- |
| `c_mult` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The multiplier for all values in matrix C, e.g C\[i,j\] = (C\[i,j\] + c_offset) \* c_mult. |

### CGBMV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun CGBMV(
    TransA: Int, 
    KL: Int, 
    KU: Int, 
    alpha: Float2!, 
    A: Allocation!, 
    X: Allocation!, 
    incX: Int, 
    beta: Float2!, 
    Y: Allocation!, 
    incY: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

CGBMV performs one of the matrix-vector operations y := alpha\*A\*x + beta\*y or y := alpha\*A\*\*T\*x + beta\*y or y := alpha\*A\*\*H\*x + beta\*y Details: http://www.netlib.org/lapack/explore-html/d0/d75/cgbmv_8f.html Note: For a M\*N matrix, the input Allocation should also be of size M\*N (dimY = M, dimX = N), but only the region M\*(KL+KU+1) will be referenced. The following subroutine can is an example showing how to convert the original matrix 'a' to row-based band matrix 'b'. for i in range(0, m): for j in range(max(0, i-kl), min(i+ku+1, n)): b\[i, j-i+kl\] = a\[i, j\]

| Parameters ||
|---|---|
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `KL` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of sub-diagonals of the matrix A. |
| `KU` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of super-diagonals of the matrix A. |
| --- | --- |
| `alpha` | [Float2](Float2.md)!: The scalar alpha. |
| `A` | [Allocation](Allocation.md)!: The input allocation contains the band matrix A, supported elements type F32_2. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F32_2. |
| --- | --- |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| `beta` | [Float2](Float2.md)!: The scalar beta. |
| `Y` | [Allocation](Allocation.md)!: The input allocation contains vector y, supported elements type F32_2. |
| --- | --- |
| `incY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector y, must be larger than zero. |

### CGEMM

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun CGEMM(
    TransA: Int, 
    TransB: Int, 
    alpha: Float2!, 
    A: Allocation!, 
    B: Allocation!, 
    beta: Float2!, 
    C: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

CGEMM performs one of the matrix-matrix operations C := alpha\*op(A)\*op(B) + beta\*C where op(X) is one of op(X) = X or op(X) = X\*\*T or op(X) = X\*\*H Details: http://www.netlib.org/lapack/explore-html/d6/d5b/cgemm_8f.html

| Parameters ||
|---|---|
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `TransB` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix B. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `alpha` | [Float2](Float2.md)!: The scalar alpha. |
| --- | --- |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F32_2. |
| `B` | [Allocation](Allocation.md)!: The input allocation contains matrix B, supported elements type F32_2. |
| `beta` | [Float2](Float2.md)!: The scalar beta. |
| --- | --- |
| `C` | [Allocation](Allocation.md)!: The input allocation contains matrix C, supported elements type F32_2. |

### CGEMV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun CGEMV(
    TransA: Int, 
    alpha: Float2!, 
    A: Allocation!, 
    X: Allocation!, 
    incX: Int, 
    beta: Float2!, 
    Y: Allocation!, 
    incY: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

CGEMV performs one of the matrix-vector operations y := alpha\*A\*x + beta\*y or y := alpha\*A\*\*T\*x + beta\*y or y := alpha\*A\*\*H\*x + beta\*y Details: http://www.netlib.org/lapack/explore-html/d4/d8a/cgemv_8f.html

| Parameters ||
|---|---|
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `alpha` | [Float2](Float2.md)!: The scalar alpha. |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F32_2. |
| --- | --- |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F32_2. |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| `beta` | [Float2](Float2.md)!: The scalar beta. |
| --- | --- |
| `Y` | [Allocation](Allocation.md)!: The input allocation contains vector y, supported elements type F32_2. |
| `incY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector y, must be larger than zero. |

### CGERC

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun CGERC(
    alpha: Float2!, 
    X: Allocation!, 
    incX: Int, 
    Y: Allocation!, 
    incY: Int, 
    A: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

CGERC performs the rank 1 operation A := alpha\*x\*y\*\*H + A Details: http://www.netlib.org/lapack/explore-html/dd/d84/cgerc_8f.html

| Parameters ||
|---|---|
| `alpha` | [Float2](Float2.md)!: The scalar alpha. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F32_2. |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| --- | --- |
| `Y` | [Allocation](Allocation.md)!: The input allocation contains vector y, supported elements type F32_2. |
| `incY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector y, must be larger than zero. |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F32_2. |
| --- | --- |

### CGERU

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun CGERU(
    alpha: Float2!, 
    X: Allocation!, 
    incX: Int, 
    Y: Allocation!, 
    incY: Int, 
    A: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

CGERU performs the rank 1 operation A := alpha\*x\*y\*\*T + A Details: http://www.netlib.org/lapack/explore-html/db/d5f/cgeru_8f.html

| Parameters ||
|---|---|
| `alpha` | [Float2](Float2.md)!: The scalar alpha. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F32_2. |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| --- | --- |
| `Y` | [Allocation](Allocation.md)!: The input allocation contains vector y, supported elements type F32_2. |
| `incY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector y, must be larger than zero. |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F32_2. |
| --- | --- |

### CHBMV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun CHBMV(
    Uplo: Int, 
    K: Int, 
    alpha: Float2!, 
    A: Allocation!, 
    X: Allocation!, 
    incX: Int, 
    beta: Float2!, 
    Y: Allocation!, 
    incY: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

CHBMV performs the matrix-vector operation y := alpha\*A\*x + beta\*y Details: http://www.netlib.org/lapack/explore-html/db/dc2/chbmv_8f.html Note: For a N\*N matrix, the input Allocation should also be of size N\*N (dimY = N, dimX = N), but only the region N\*(K+1) will be referenced. The following subroutine can is an example showing how to convert a UPPER trianglar matrix 'a' to row-based band matrix 'b'. for i in range(0, n): for j in range(i, min(i+k+1, n)): b\[i, j-i\] = a\[i, j\]

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part of the band matrix A is being supplied. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `K` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of off-diagonals of the matrix A |
| `alpha` | [Float2](Float2.md)!: The scalar alpha. |
| --- | --- |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F32_2. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F32_2. |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| --- | --- |
| `beta` | [Float2](Float2.md)!: The scalar beta. |
| `Y` | [Allocation](Allocation.md)!: The input allocation contains vector y, supported elements type F32_2. |
| `incY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector y, must be larger than zero. |
| --- | --- |

### CHEMM

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun CHEMM(
    Side: Int, 
    Uplo: Int, 
    alpha: Float2!, 
    A: Allocation!, 
    B: Allocation!, 
    beta: Float2!, 
    C: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

CHEMM performs one of the matrix-matrix operations C := alpha\*A\*B + beta\*C or C := alpha\*B\*A + beta\*C Details: http://www.netlib.org/lapack/explore-html/d3/d66/chemm_8f.html

| Parameters ||
|---|---|
| `Side` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the symmetric matrix A appears on the left or right. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#RIGHT:kotlin.Int` |
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part is to be referenced. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `alpha` | [Float2](Float2.md)!: The scalar alpha. |
| --- | --- |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F32_2. |
| `B` | [Allocation](Allocation.md)!: The input allocation contains matrix B, supported elements type F32_2. |
| `beta` | [Float2](Float2.md)!: The scalar beta. |
| --- | --- |
| `C` | [Allocation](Allocation.md)!: The input allocation contains matrix C, supported elements type F32_2. |

### CHEMV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun CHEMV(
    Uplo: Int, 
    alpha: Float2!, 
    A: Allocation!, 
    X: Allocation!, 
    incX: Int, 
    beta: Float2!, 
    Y: Allocation!, 
    incY: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

CHEMV performs the matrix-vector operation y := alpha\*A\*x + beta\*y Details: http://www.netlib.org/lapack/explore-html/d7/d51/chemv_8f.html

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part is to be referenced. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `alpha` | [Float2](Float2.md)!: The scalar alpha. |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F32_2. |
| --- | --- |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F32_2. |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| `beta` | [Float2](Float2.md)!: The scalar beta. |
| --- | --- |
| `Y` | [Allocation](Allocation.md)!: The input allocation contains vector y, supported elements type F32_2. |
| `incY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector y, must be larger than zero. |

### CHER

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun CHER(
    Uplo: Int, 
    alpha: Float, 
    X: Allocation!, 
    incX: Int, 
    A: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

CHER performs the rank 1 operation A := alpha\*x\*x\*\*H + A Details: http://www.netlib.org/lapack/explore-html/d3/d6d/cher_8f.html

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part is to be referenced. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `alpha` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The scalar alpha. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F32_2. |
| --- | --- |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F32_2. |

### CHER2

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun CHER2(
    Uplo: Int, 
    alpha: Float2!, 
    X: Allocation!, 
    incX: Int, 
    Y: Allocation!, 
    incY: Int, 
    A: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

CHER2 performs the symmetric rank 2 operation A := alpha\*x\*y\*\*H + alpha\*y\*x\*\*H + A Details: http://www.netlib.org/lapack/explore-html/db/d87/cher2_8f.html

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part is to be referenced. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `alpha` | [Float2](Float2.md)!: The scalar alpha. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F32_2. |
| --- | --- |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| `Y` | [Allocation](Allocation.md)!: The input allocation contains vector y, supported elements type F32_2. |
| `incY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector y, must be larger than zero. |
| --- | --- |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F32_2. |

### CHER2K

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun CHER2K(
    Uplo: Int, 
    Trans: Int, 
    alpha: Float2!, 
    A: Allocation!, 
    B: Allocation!, 
    beta: Float, 
    C: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

CHER2K performs one of the hermitian rank 2k operations C := alpha\*A\*B\*\*H + conjg( alpha )\*B\*A\*\*H + beta\*C or C := alpha\*A\*\*H\*B + conjg( alpha )\*B\*\*H\*A + beta\*C Details: http://www.netlib.org/lapack/explore-html/d1/d82/cher2k_8f.html

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part of C is to be referenced. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `Trans` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to the operation. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `alpha` | [Float2](Float2.md)!: The scalar alpha. |
| --- | --- |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F32_2. |
| `B` | [Allocation](Allocation.md)!: The input allocation contains matrix B, supported elements type F32_2. |
| `beta` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The scalar beta. |
| --- | --- |
| `C` | [Allocation](Allocation.md)!: The input allocation contains matrix C, supported elements type F32_2. |

### CHERK

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun CHERK(
    Uplo: Int, 
    Trans: Int, 
    alpha: Float, 
    A: Allocation!, 
    beta: Float, 
    C: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

CHERK performs one of the hermitian rank k operations C := alpha\*A\*A\*\*H + beta\*C or C := alpha\*A\*\*H\*A + beta\*C Details: http://www.netlib.org/lapack/explore-html/d8/d52/cherk_8f.html

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part of C is to be referenced. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `Trans` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to the operation. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `alpha` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The scalar alpha. |
| --- | --- |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F32_2. |
| `beta` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The scalar beta. |
| `C` | [Allocation](Allocation.md)!: The input allocation contains matrix C, supported elements type F32_2. |
| --- | --- |

### CHPMV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun CHPMV(
    Uplo: Int, 
    alpha: Float2!, 
    Ap: Allocation!, 
    X: Allocation!, 
    incX: Int, 
    beta: Float2!, 
    Y: Allocation!, 
    incY: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

CHPMV performs the matrix-vector operation y := alpha\*A\*x + beta\*y Details: http://www.netlib.org/lapack/explore-html/d2/d06/chpmv_8f.html Note: For a N\*N matrix, the input Allocation should be a 1D allocation of size dimX = N\*(N+1)/2, The following subroutine can is an example showing how to convert a UPPER trianglar matrix 'a' to packed matrix 'b'. k = 0 for i in range(0, n): for j in range(i, n): b\[k++\] = a\[i, j\]

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part of the matrix A is supplied in packed form. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `alpha` | [Float2](Float2.md)!: The scalar alpha. |
| `Ap` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F32_2. |
| --- | --- |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F32_2. |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| `beta` | [Float2](Float2.md)!: The scalar beta. |
| --- | --- |
| `Y` | [Allocation](Allocation.md)!: The input allocation contains vector y, supported elements type F32_2. |
| `incY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector y, must be larger than zero. |

### CHPR

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun CHPR(
    Uplo: Int, 
    alpha: Float, 
    X: Allocation!, 
    incX: Int, 
    Ap: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

CHPR performs the rank 1 operation A := alpha\*x\*x\*\*H + A Details: http://www.netlib.org/lapack/explore-html/db/dcd/chpr_8f.html Note: For a N\*N matrix, the input Allocation should be a 1D allocation of size dimX = N\*(N+1)/2, The following subroutine can is an example showing how to convert a UPPER trianglar matrix 'a' to packed matrix 'b'. k = 0 for i in range(0, n): for j in range(i, n): b\[k++\] = a\[i, j\]

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part is to be supplied in the packed form. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `alpha` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The scalar alpha. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F32_2. |
| --- | --- |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| `Ap` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F32_2. |

### CHPR2

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun CHPR2(
    Uplo: Int, 
    alpha: Float2!, 
    X: Allocation!, 
    incX: Int, 
    Y: Allocation!, 
    incY: Int, 
    Ap: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

CHPR2 performs the symmetric rank 2 operation A := alpha\*x\*y\*\*H + alpha\*y\*x\*\*H + A Details: http://www.netlib.org/lapack/explore-html/d6/d44/chpr2_8f.html Note: For a N\*N matrix, the input Allocation should be a 1D allocation of size dimX = N\*(N+1)/2, The following subroutine can is an example showing how to convert a UPPER trianglar matrix 'a' to packed matrix 'b'. k = 0 for i in range(0, n): for j in range(i, n): b\[k++\] = a\[i, j\]

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part is to be supplied in the packed form. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `alpha` | [Float2](Float2.md)!: The scalar alpha. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F32_2. |
| --- | --- |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| `Y` | [Allocation](Allocation.md)!: The input allocation contains vector y, supported elements type F32_2. |
| `incY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector y, must be larger than zero. |
| --- | --- |
| `Ap` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F32_2. |

### CSYMM

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun CSYMM(
    Side: Int, 
    Uplo: Int, 
    alpha: Float2!, 
    A: Allocation!, 
    B: Allocation!, 
    beta: Float2!, 
    C: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

CSYMM performs one of the matrix-matrix operations C := alpha\*A\*B + beta\*C or C := alpha\*B\*A + beta\*C Details: http://www.netlib.org/lapack/explore-html/db/d59/csymm_8f.html

| Parameters ||
|---|---|
| `Side` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the symmetric matrix A appears on the left or right. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#RIGHT:kotlin.Int` |
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part is to be referenced. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `alpha` | [Float2](Float2.md)!: The scalar alpha. |
| --- | --- |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F32_2. |
| `B` | [Allocation](Allocation.md)!: The input allocation contains matrix B, supported elements type F32_2. |
| `beta` | [Float2](Float2.md)!: The scalar beta. |
| --- | --- |
| `C` | [Allocation](Allocation.md)!: The input allocation contains matrix C, supported elements type F32_2. |

### CSYR2K

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun CSYR2K(
    Uplo: Int, 
    Trans: Int, 
    alpha: Float2!, 
    A: Allocation!, 
    B: Allocation!, 
    beta: Float2!, 
    C: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

CSYR2K performs one of the symmetric rank 2k operations C := alpha\*A\*B\*\*T + alpha\*B\*A\*\*T + beta\*C or C := alpha\*A\*\*T\*B + alpha\*B\*\*T\*A + beta\*C Details: http://www.netlib.org/lapack/explore-html/de/d7e/csyr2k_8f.html

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part of C is to be referenced. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `Trans` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to the operation. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `alpha` | [Float2](Float2.md)!: The scalar alpha. |
| --- | --- |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F32_2. |
| `B` | [Allocation](Allocation.md)!: The input allocation contains matrix B, supported elements type F32_2. |
| `beta` | [Float2](Float2.md)!: The scalar beta. |
| --- | --- |
| `C` | [Allocation](Allocation.md)!: The input allocation contains matrix C, supported elements type F32_2. |

### CSYRK

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun CSYRK(
    Uplo: Int, 
    Trans: Int, 
    alpha: Float2!, 
    A: Allocation!, 
    beta: Float2!, 
    C: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

CSYRK performs one of the symmetric rank k operations C := alpha\*A\*A\*\*T + beta\*C or C := alpha\*A\*\*T\*A + beta\*C Details: http://www.netlib.org/lapack/explore-html/d3/d6a/csyrk_8f.html

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part of C is to be referenced. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `Trans` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to the operation. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `alpha` | [Float2](Float2.md)!: The scalar alpha. |
| --- | --- |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F32_2. |
| `beta` | [Float2](Float2.md)!: The scalar beta. |
| `C` | [Allocation](Allocation.md)!: The input allocation contains matrix C, supported elements type F32_2. |
| --- | --- |

### CTBMV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun CTBMV(
    Uplo: Int, 
    TransA: Int, 
    Diag: Int, 
    K: Int, 
    A: Allocation!, 
    X: Allocation!, 
    incX: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

CTBMV performs one of the matrix-vector operations x := A\*x or x := A\*\*T\*x or x := A\*\*H\*x Details: http://www.netlib.org/lapack/explore-html/d3/dcd/ctbmv_8f.html Note: For a N\*N matrix, the input Allocation should also be of size N\*N (dimY = N, dimX = N), but only the region N\*(K+1) will be referenced. The following subroutine can is an example showing how to convert a UPPER trianglar matrix 'a' to row-based band matrix 'b'. for i in range(0, n): for j in range(i, min(i+k+1, n)): b\[i, j-i\] = a\[i, j\]

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the matrix is an upper or lower triangular matrix. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `Diag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether or not A is unit triangular. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NON_UNIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UNIT:kotlin.Int` |
| --- | --- |
| `K` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of off-diagonals of the matrix A |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F32_2. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F32_2. |
| --- | --- |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |

### CTBSV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun CTBSV(
    Uplo: Int, 
    TransA: Int, 
    Diag: Int, 
    K: Int, 
    A: Allocation!, 
    X: Allocation!, 
    incX: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

CTBSV solves one of the systems of equations A\*x = b or A\*\*T\*x = b or A\*\*H\*x = b Details: http://www.netlib.org/lapack/explore-html/d9/d5f/ctbsv_8f.html Note: For a N\*N matrix, the input Allocation should also be of size N\*N (dimY = N, dimX = N), but only the region N\*(K+1) will be referenced. The following subroutine can is an example showing how to convert a UPPER trianglar matrix 'a' to row-based band matrix 'b'. for i in range(0, n): for j in range(i, min(i+k+1, n)): b\[i, j-i\] = a\[i, j\]

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the matrix is an upper or lower triangular matrix. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `Diag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether or not A is unit triangular. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NON_UNIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UNIT:kotlin.Int` |
| --- | --- |
| `K` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of off-diagonals of the matrix A |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F32_2. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F32_2. |
| --- | --- |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |

### CTPMV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun CTPMV(
    Uplo: Int, 
    TransA: Int, 
    Diag: Int, 
    Ap: Allocation!, 
    X: Allocation!, 
    incX: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

CTPMV performs one of the matrix-vector operations x := A\*x or x := A\*\*T\*x or x := A\*\*H\*x Details: http://www.netlib.org/lapack/explore-html/d4/dbb/ctpmv_8f.html Note: For a N\*N matrix, the input Allocation should be a 1D allocation of size dimX = N\*(N+1)/2, The following subroutine can is an example showing how to convert a UPPER trianglar matrix 'a' to packed matrix 'b'. k = 0 for i in range(0, n): for j in range(i, n): b\[k++\] = a\[i, j\]

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the matrix is an upper or lower triangular matrix. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `Diag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether or not A is unit triangular. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NON_UNIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UNIT:kotlin.Int` |
| --- | --- |
| `Ap` | [Allocation](Allocation.md)!: The input allocation contains packed matrix A, supported elements type F32_2. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F32_2. |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| --- | --- |

### CTPSV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun CTPSV(
    Uplo: Int, 
    TransA: Int, 
    Diag: Int, 
    Ap: Allocation!, 
    X: Allocation!, 
    incX: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

CTPSV solves one of the systems of equations A\*x = b or A\*\*T\*x = b or A\*\*H\*x = b Details: http://www.netlib.org/lapack/explore-html/d8/d56/ctpsv_8f.html Note: For a N\*N matrix, the input Allocation should be a 1D allocation of size dimX = N\*(N+1)/2, The following subroutine can is an example showing how to convert a UPPER trianglar matrix 'a' to packed matrix 'b'. k = 0 for i in range(0, n): for j in range(i, n): b\[k++\] = a\[i, j\]

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the matrix is an upper or lower triangular matrix. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `Diag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether or not A is unit triangular. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NON_UNIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UNIT:kotlin.Int` |
| --- | --- |
| `Ap` | [Allocation](Allocation.md)!: The input allocation contains packed matrix A, supported elements type F32_2. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F32_2. |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| --- | --- |

### CTRMM

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun CTRMM(
    Side: Int, 
    Uplo: Int, 
    TransA: Int, 
    Diag: Int, 
    alpha: Float2!, 
    A: Allocation!, 
    B: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

CTRMM performs one of the matrix-matrix operations B := alpha\*op(A)\*B or B := alpha\*B\*op(A) op(A) is one of op(A) = A or op(A) = A\*\*T or op(A) = A\*\*H Details: http://www.netlib.org/lapack/explore-html/d4/d9b/ctrmm_8f.html

| Parameters ||
|---|---|
| `Side` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the symmetric matrix A appears on the left or right. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#RIGHT:kotlin.Int` |
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether matrix A is upper or lower triangular. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| --- | --- |
| `Diag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether or not A is unit triangular. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NON_UNIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UNIT:kotlin.Int` |
| `alpha` | [Float2](Float2.md)!: The scalar alpha. |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F32_2. |
| --- | --- |
| `B` | [Allocation](Allocation.md)!: The input allocation contains matrix B, supported elements type F32_2. |

### CTRMV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun CTRMV(
    Uplo: Int, 
    TransA: Int, 
    Diag: Int, 
    A: Allocation!, 
    X: Allocation!, 
    incX: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

CTRMV performs one of the matrix-vector operations x := A\*x or x := A\*\*T\*x or x := A\*\*H\*x Details: http://www.netlib.org/lapack/explore-html/df/d78/ctrmv_8f.html

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the matrix is an upper or lower triangular matrix. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `Diag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether or not A is unit triangular. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NON_UNIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UNIT:kotlin.Int` |
| --- | --- |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F32_2. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F32_2. |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| --- | --- |

### CTRSM

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun CTRSM(
    Side: Int, 
    Uplo: Int, 
    TransA: Int, 
    Diag: Int, 
    alpha: Float2!, 
    A: Allocation!, 
    B: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

CTRSM solves one of the matrix equations op(A)\*X := alpha\*B or X\*op(A) := alpha\*B op(A) is one of op(A) = A or op(A) = A\*\*T or op(A) = A\*\*H Details: http://www.netlib.org/lapack/explore-html/de/d30/ctrsm_8f.html

| Parameters ||
|---|---|
| `Side` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the symmetric matrix A appears on the left or right. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#RIGHT:kotlin.Int` |
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether matrix A is upper or lower triangular. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| --- | --- |
| `Diag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether or not A is unit triangular. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NON_UNIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UNIT:kotlin.Int` |
| `alpha` | [Float2](Float2.md)!: The scalar alpha. |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F32_2. |
| --- | --- |
| `B` | [Allocation](Allocation.md)!: The input allocation contains matrix B, supported elements type F32_2. |

### CTRSV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun CTRSV(
    Uplo: Int, 
    TransA: Int, 
    Diag: Int, 
    A: Allocation!, 
    X: Allocation!, 
    incX: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

CTRSV solves one of the systems of equations A\*x = b or A\*\*T\*x = b or A\*\*H\*x = b Details: http://www.netlib.org/lapack/explore-html/d4/dc8/ctrsv_8f.html

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the matrix is an upper or lower triangular matrix. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `Diag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether or not A is unit triangular. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NON_UNIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UNIT:kotlin.Int` |
| --- | --- |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F32_2. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F32_2. |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| --- | --- |

### DGBMV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun DGBMV(
    TransA: Int, 
    KL: Int, 
    KU: Int, 
    alpha: Double, 
    A: Allocation!, 
    X: Allocation!, 
    incX: Int, 
    beta: Double, 
    Y: Allocation!, 
    incY: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

DGBMV performs one of the matrix-vector operations y := alpha\*A\*x + beta\*y or y := alpha\*A\*\*T\*x + beta\*y Details: http://www.netlib.org/lapack/explore-html/d2/d3f/dgbmv_8f.html Note: For a M\*N matrix, the input Allocation should also be of size M\*N (dimY = M, dimX = N), but only the region M\*(KL+KU+1) will be referenced. The following subroutine can is an example showing how to convert the original matrix 'a' to row-based band matrix 'b'. for i in range(0, m): for j in range(max(0, i-kl), min(i+ku+1, n)): b\[i, j-i+kl\] = a\[i, j\]

| Parameters ||
|---|---|
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `KL` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of sub-diagonals of the matrix A. |
| `KU` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of super-diagonals of the matrix A. |
| --- | --- |
| `alpha` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): The scalar alpha. |
| `A` | [Allocation](Allocation.md)!: The input allocation contains the band matrix A, supported elements type F64. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F64. |
| --- | --- |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| `beta` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): The scalar beta. |
| `Y` | [Allocation](Allocation.md)!: The input allocation contains vector y, supported elements type F64. |
| --- | --- |
| `incY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector y, must be larger than zero. |

### DGEMM

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun DGEMM(
    TransA: Int, 
    TransB: Int, 
    alpha: Double, 
    A: Allocation!, 
    B: Allocation!, 
    beta: Double, 
    C: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

DGEMM performs one of the matrix-matrix operations C := alpha\*op(A)\*op(B) + beta\*C where op(X) is one of op(X) = X or op(X) = X\*\*T Details: http://www.netlib.org/lapack/explore-html/d7/d2b/dgemm_8f.html

| Parameters ||
|---|---|
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `TransB` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix B. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `alpha` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): The scalar alpha. |
| --- | --- |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F64. |
| `B` | [Allocation](Allocation.md)!: The input allocation contains matrix B, supported elements type F64. |
| `beta` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): The scalar beta. |
| --- | --- |
| `C` | [Allocation](Allocation.md)!: The input allocation contains matrix C, supported elements type F64. |

### DGEMV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun DGEMV(
    TransA: Int, 
    alpha: Double, 
    A: Allocation!, 
    X: Allocation!, 
    incX: Int, 
    beta: Double, 
    Y: Allocation!, 
    incY: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

DGEMV performs one of the matrix-vector operations y := alpha\*A\*x + beta\*y or y := alpha\*A\*\*T\*x + beta\*y Details: http://www.netlib.org/lapack/explore-html/dc/da8/dgemv_8f.html

| Parameters ||
|---|---|
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `alpha` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): The scalar alpha. |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F64. |
| --- | --- |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F64. |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| `beta` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): The scalar beta. |
| --- | --- |
| `Y` | [Allocation](Allocation.md)!: The input allocation contains vector y, supported elements type F64. |
| `incY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector y, must be larger than zero. |

### DGER

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun DGER(
    alpha: Double, 
    X: Allocation!, 
    incX: Int, 
    Y: Allocation!, 
    incY: Int, 
    A: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

DGER performs the rank 1 operation A := alpha\*x\*y\*\*T + A Details: http://www.netlib.org/lapack/explore-html/dc/da8/dger_8f.html

| Parameters ||
|---|---|
| `alpha` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): The scalar alpha. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F64. |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| --- | --- |
| `Y` | [Allocation](Allocation.md)!: The input allocation contains vector y, supported elements type F64. |
| `incY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector y, must be larger than zero. |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F64. |
| --- | --- |

### DSBMV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun DSBMV(
    Uplo: Int, 
    K: Int, 
    alpha: Double, 
    A: Allocation!, 
    X: Allocation!, 
    incX: Int, 
    beta: Double, 
    Y: Allocation!, 
    incY: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

DSBMV performs the matrix-vector operation y := alpha\*A\*x + beta\*y Details: http://www.netlib.org/lapack/explore-html/d8/d1e/dsbmv_8f.html Note: For a N\*N matrix, the input Allocation should also be of size N\*N (dimY = N, dimX = N), but only the region N\*(K+1) will be referenced. The following subroutine can is an example showing how to convert a UPPER trianglar matrix 'a' to row-based band matrix 'b'. for i in range(0, n): for j in range(i, min(i+k+1, n)): b\[i, j-i\] = a\[i, j\]

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part of the band matrix A is being supplied. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `K` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of off-diagonals of the matrix A |
| `alpha` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): The scalar alpha. |
| --- | --- |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F64. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F64. |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| --- | --- |
| `beta` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): The scalar beta. |
| `Y` | [Allocation](Allocation.md)!: The input allocation contains vector y, supported elements type F64. |
| `incY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector y, must be larger than zero. |
| --- | --- |

### DSPMV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun DSPMV(
    Uplo: Int, 
    alpha: Double, 
    Ap: Allocation!, 
    X: Allocation!, 
    incX: Int, 
    beta: Double, 
    Y: Allocation!, 
    incY: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

DSPMV performs the matrix-vector operation y := alpha\*A\*x + beta\*y Details: http://www.netlib.org/lapack/explore-html/d4/d85/dspmv_8f.html Note: For a N\*N matrix, the input Allocation should be a 1D allocation of size dimX = N\*(N+1)/2, The following subroutine can is an example showing how to convert a UPPER trianglar matrix 'a' to packed matrix 'b'. k = 0 for i in range(0, n): for j in range(i, n): b\[k++\] = a\[i, j\]

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part of the matrix A is supplied in packed form. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `alpha` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): The scalar alpha. |
| `Ap` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F64. |
| --- | --- |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F64. |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| `beta` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): The scalar beta. |
| --- | --- |
| `Y` | [Allocation](Allocation.md)!: The input allocation contains vector y, supported elements type F64. |
| `incY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector y, must be larger than zero. |

### DSPR

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun DSPR(
    Uplo: Int, 
    alpha: Double, 
    X: Allocation!, 
    incX: Int, 
    Ap: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

DSPR performs the rank 1 operation A := alpha\*x\*x\*\*T + A Details: http://www.netlib.org/lapack/explore-html/dd/dba/dspr_8f.html Note: For a N\*N matrix, the input Allocation should be a 1D allocation of size dimX = N\*(N+1)/2, The following subroutine can is an example showing how to convert a UPPER trianglar matrix 'a' to packed matrix 'b'. k = 0 for i in range(0, n): for j in range(i, n): b\[k++\] = a\[i, j\]

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part is to be supplied in the packed form. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `alpha` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): The scalar alpha. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F64. |
| --- | --- |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| `Ap` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F64. |

### DSPR2

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun DSPR2(
    Uplo: Int, 
    alpha: Double, 
    X: Allocation!, 
    incX: Int, 
    Y: Allocation!, 
    incY: Int, 
    Ap: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

DSPR2 performs the symmetric rank 2 operation A := alpha\*x\*y\*\*T + alpha\*y\*x\*\*T + A Details: http://www.netlib.org/lapack/explore-html/dd/d9e/dspr2_8f.html Note: For a N\*N matrix, the input Allocation should be a 1D allocation of size dimX = N\*(N+1)/2, The following subroutine can is an example showing how to convert a UPPER trianglar matrix 'a' to packed matrix 'b'. k = 0 for i in range(0, n): for j in range(i, n): b\[k++\] = a\[i, j\]

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part is to be supplied in the packed form. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `alpha` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): The scalar alpha. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F64. |
| --- | --- |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| `Y` | [Allocation](Allocation.md)!: The input allocation contains vector y, supported elements type F64. |
| `incY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector y, must be larger than zero. |
| --- | --- |
| `Ap` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F64. |

### DSYMM

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun DSYMM(
    Side: Int, 
    Uplo: Int, 
    alpha: Double, 
    A: Allocation!, 
    B: Allocation!, 
    beta: Double, 
    C: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

DSYMM performs one of the matrix-matrix operations C := alpha\*A\*B + beta\*C or C := alpha\*B\*A + beta\*C Details: http://www.netlib.org/lapack/explore-html/d8/db0/dsymm_8f.html

| Parameters ||
|---|---|
| `Side` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the symmetric matrix A appears on the left or right. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#RIGHT:kotlin.Int` |
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part is to be referenced. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `alpha` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): The scalar alpha. |
| --- | --- |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F64. |
| `B` | [Allocation](Allocation.md)!: The input allocation contains matrix B, supported elements type F64. |
| `beta` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): The scalar beta. |
| --- | --- |
| `C` | [Allocation](Allocation.md)!: The input allocation contains matrix C, supported elements type F64. |

### DSYMV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun DSYMV(
    Uplo: Int, 
    alpha: Double, 
    A: Allocation!, 
    X: Allocation!, 
    incX: Int, 
    beta: Double, 
    Y: Allocation!, 
    incY: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

DSYMV performs the matrix-vector operation y := alpha\*A\*x + beta\*y Details: http://www.netlib.org/lapack/explore-html/d8/dbe/dsymv_8f.html

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part is to be referenced. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `alpha` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): The scalar alpha. |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F64. |
| --- | --- |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F64. |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| `beta` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): The scalar beta. |
| --- | --- |
| `Y` | [Allocation](Allocation.md)!: The input allocation contains vector y, supported elements type F64. |
| `incY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector y, must be larger than zero. |

### DSYR

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun DSYR(
    Uplo: Int, 
    alpha: Double, 
    X: Allocation!, 
    incX: Int, 
    A: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

DSYR performs the rank 1 operation A := alpha\*x\*x\*\*T + A Details: http://www.netlib.org/lapack/explore-html/d3/d60/dsyr_8f.html

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part is to be referenced. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `alpha` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): The scalar alpha. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F64. |
| --- | --- |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F64. |

### DSYR2

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun DSYR2(
    Uplo: Int, 
    alpha: Double, 
    X: Allocation!, 
    incX: Int, 
    Y: Allocation!, 
    incY: Int, 
    A: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

DSYR2 performs the symmetric rank 2 operation A := alpha\*x\*y\*\*T + alpha\*y\*x\*\*T + A Details: http://www.netlib.org/lapack/explore-html/de/d41/dsyr2_8f.html

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part is to be referenced. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `alpha` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): The scalar alpha. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F64. |
| --- | --- |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| `Y` | [Allocation](Allocation.md)!: The input allocation contains vector y, supported elements type F64. |
| `incY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector y, must be larger than zero. |
| --- | --- |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F64. |

### DSYR2K

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun DSYR2K(
    Uplo: Int, 
    Trans: Int, 
    alpha: Double, 
    A: Allocation!, 
    B: Allocation!, 
    beta: Double, 
    C: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

DSYR2K performs one of the symmetric rank 2k operations C := alpha\*A\*B\*\*T + alpha\*B\*A\*\*T + beta\*C or C := alpha\*A\*\*T\*B + alpha\*B\*\*T\*A + beta\*C Details: http://www.netlib.org/lapack/explore-html/d1/dec/dsyr2k_8f.html

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part of C is to be referenced. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `Trans` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to the operation. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `alpha` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): The scalar alpha. |
| --- | --- |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F64. |
| `B` | [Allocation](Allocation.md)!: The input allocation contains matrix B, supported elements type F64. |
| `beta` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): The scalar beta. |
| --- | --- |
| `C` | [Allocation](Allocation.md)!: The input allocation contains matrix C, supported elements type F64. |

### DSYRK

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun DSYRK(
    Uplo: Int, 
    Trans: Int, 
    alpha: Double, 
    A: Allocation!, 
    beta: Double, 
    C: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

DSYRK performs one of the symmetric rank k operations C := alpha\*A\*A\*\*T + beta\*C or C := alpha\*A\*\*T\*A + beta\*C Details: http://www.netlib.org/lapack/explore-html/dc/d05/dsyrk_8f.html

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part of C is to be referenced. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `Trans` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to the operation. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `alpha` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): The scalar alpha. |
| --- | --- |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F64. |
| `beta` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): The scalar beta. |
| `C` | [Allocation](Allocation.md)!: The input allocation contains matrix C, supported elements type F64. |
| --- | --- |

### DTBMV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun DTBMV(
    Uplo: Int, 
    TransA: Int, 
    Diag: Int, 
    K: Int, 
    A: Allocation!, 
    X: Allocation!, 
    incX: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

DTBMV performs one of the matrix-vector operations x := A\*x or x := A\*\*T\*x Details: http://www.netlib.org/lapack/explore-html/df/d29/dtbmv_8f.html Note: For a N\*N matrix, the input Allocation should also be of size N\*N (dimY = N, dimX = N), but only the region N\*(K+1) will be referenced. The following subroutine can is an example showing how to convert a UPPER trianglar matrix 'a' to row-based band matrix 'b'. for i in range(0, n): for j in range(i, min(i+k+1, n)): b\[i, j-i\] = a\[i, j\]

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the matrix is an upper or lower triangular matrix. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `Diag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether or not A is unit triangular. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NON_UNIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UNIT:kotlin.Int` |
| --- | --- |
| `K` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of off-diagonals of the matrix A |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F64. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F64. |
| --- | --- |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |

### DTBSV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun DTBSV(
    Uplo: Int, 
    TransA: Int, 
    Diag: Int, 
    K: Int, 
    A: Allocation!, 
    X: Allocation!, 
    incX: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

DTBSV solves one of the systems of equations A\*x = b or A\*\*T\*x = b Details: http://www.netlib.org/lapack/explore-html/d4/dcf/dtbsv_8f.html Note: For a N\*N matrix, the input Allocation should also be of size N\*N (dimY = N, dimX = N), but only the region N\*(K+1) will be referenced. The following subroutine can is an example showing how to convert a UPPER trianglar matrix 'a' to row-based band matrix 'b'. for i in range(0, n): for j in range(i, min(i+k+1, n)): b\[i, j-i\] = a\[i, j\]

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the matrix is an upper or lower triangular matrix. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `Diag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether or not A is unit triangular. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NON_UNIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UNIT:kotlin.Int` |
| --- | --- |
| `K` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of off-diagonals of the matrix A |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F64. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F64. |
| --- | --- |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |

### DTPMV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun DTPMV(
    Uplo: Int, 
    TransA: Int, 
    Diag: Int, 
    Ap: Allocation!, 
    X: Allocation!, 
    incX: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

DTPMV performs one of the matrix-vector operations x := A\*x or x := A\*\*T\*x Details: http://www.netlib.org/lapack/explore-html/dc/dcd/dtpmv_8f.html Note: For a N\*N matrix, the input Allocation should be a 1D allocation of size dimX = N\*(N+1)/2, The following subroutine can is an example showing how to convert a UPPER trianglar matrix 'a' to packed matrix 'b'. k = 0 for i in range(0, n): for j in range(i, n): b\[k++\] = a\[i, j\]

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the matrix is an upper or lower triangular matrix. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `Diag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether or not A is unit triangular. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NON_UNIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UNIT:kotlin.Int` |
| --- | --- |
| `Ap` | [Allocation](Allocation.md)!: The input allocation contains packed matrix A, supported elements type F64. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F64. |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| --- | --- |

### DTPSV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun DTPSV(
    Uplo: Int, 
    TransA: Int, 
    Diag: Int, 
    Ap: Allocation!, 
    X: Allocation!, 
    incX: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

DTPSV solves one of the systems of equations A\*x = b or A\*\*T\*x = b Details: http://www.netlib.org/lapack/explore-html/d9/d84/dtpsv_8f.html Note: For a N\*N matrix, the input Allocation should be a 1D allocation of size dimX = N\*(N+1)/2, The following subroutine can is an example showing how to convert a UPPER trianglar matrix 'a' to packed matrix 'b'. k = 0 for i in range(0, n): for j in range(i, n): b\[k++\] = a\[i, j\]

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the matrix is an upper or lower triangular matrix. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `Diag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether or not A is unit triangular. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NON_UNIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UNIT:kotlin.Int` |
| --- | --- |
| `Ap` | [Allocation](Allocation.md)!: The input allocation contains packed matrix A, supported elements type F64. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F64. |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| --- | --- |

### DTRMM

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun DTRMM(
    Side: Int, 
    Uplo: Int, 
    TransA: Int, 
    Diag: Int, 
    alpha: Double, 
    A: Allocation!, 
    B: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

DTRMM performs one of the matrix-matrix operations B := alpha\*op(A)\*B or B := alpha\*B\*op(A) op(A) is one of op(A) = A or op(A) = A\*\*T Details: http://www.netlib.org/lapack/explore-html/dd/d19/dtrmm_8f.html

| Parameters ||
|---|---|
| `Side` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the symmetric matrix A appears on the left or right. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#RIGHT:kotlin.Int` |
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether matrix A is upper or lower triangular. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| --- | --- |
| `Diag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether or not A is unit triangular. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NON_UNIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UNIT:kotlin.Int` |
| `alpha` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): The scalar alpha. |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F64. |
| --- | --- |
| `B` | [Allocation](Allocation.md)!: The input allocation contains matrix B, supported elements type F64. |

### DTRMV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun DTRMV(
    Uplo: Int, 
    TransA: Int, 
    Diag: Int, 
    A: Allocation!, 
    X: Allocation!, 
    incX: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

DTRMV performs one of the matrix-vector operations x := A\*x or x := A\*\*T\*x Details: http://www.netlib.org/lapack/explore-html/dc/d7e/dtrmv_8f.html

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the matrix is an upper or lower triangular matrix. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `Diag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether or not A is unit triangular. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NON_UNIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UNIT:kotlin.Int` |
| --- | --- |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F64. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F64. |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| --- | --- |

### DTRSM

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun DTRSM(
    Side: Int, 
    Uplo: Int, 
    TransA: Int, 
    Diag: Int, 
    alpha: Double, 
    A: Allocation!, 
    B: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

DTRSM solves one of the matrix equations op(A)\*X := alpha\*B or X\*op(A) := alpha\*B op(A) is one of op(A) = A or op(A) = A\*\*T Details: http://www.netlib.org/lapack/explore-html/de/da7/dtrsm_8f.html

| Parameters ||
|---|---|
| `Side` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the symmetric matrix A appears on the left or right. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#RIGHT:kotlin.Int` |
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether matrix A is upper or lower triangular. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| --- | --- |
| `Diag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether or not A is unit triangular. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NON_UNIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UNIT:kotlin.Int` |
| `alpha` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): The scalar alpha. |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F64. |
| --- | --- |
| `B` | [Allocation](Allocation.md)!: The input allocation contains matrix B, supported elements type F64. |

### DTRSV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun DTRSV(
    Uplo: Int, 
    TransA: Int, 
    Diag: Int, 
    A: Allocation!, 
    X: Allocation!, 
    incX: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

DTRSV solves one of the systems of equations A\*x = b or A\*\*T\*x = b Details: http://www.netlib.org/lapack/explore-html/d6/d96/dtrsv_8f.html

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the matrix is an upper or lower triangular matrix. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `Diag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether or not A is unit triangular. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NON_UNIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UNIT:kotlin.Int` |
| --- | --- |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F64. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F64. |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| --- | --- |

### SGBMV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun SGBMV(
    TransA: Int, 
    KL: Int, 
    KU: Int, 
    alpha: Float, 
    A: Allocation!, 
    X: Allocation!, 
    incX: Int, 
    beta: Float, 
    Y: Allocation!, 
    incY: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

SGBMV performs one of the matrix-vector operations y := alpha\*A\*x + beta\*y or y := alpha\*A\*\*T\*x + beta\*y Details: http://www.netlib.org/lapack/explore-html/d6/d46/sgbmv_8f.html Note: For a M\*N matrix, the input Allocation should also be of size M\*N (dimY = M, dimX = N), but only the region M\*(KL+KU+1) will be referenced. The following subroutine can is an example showing how to convert the original matrix 'a' to row-based band matrix 'b'. for i in range(0, m): for j in range(max(0, i-kl), min(i+ku+1, n)): b\[i, j-i+kl\] = a\[i, j\]

| Parameters ||
|---|---|
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `KL` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of sub-diagonals of the matrix A. |
| `KU` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of super-diagonals of the matrix A. |
| --- | --- |
| `alpha` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The scalar alpha. |
| `A` | [Allocation](Allocation.md)!: The input allocation contains the band matrix A, supported elements type F32. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F32. |
| --- | --- |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| `beta` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The scalar beta. |
| `Y` | [Allocation](Allocation.md)!: The input allocation contains vector y, supported elements type F32. |
| --- | --- |
| `incY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector y, must be larger than zero. |

### SGEMM

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun SGEMM(
    TransA: Int, 
    TransB: Int, 
    alpha: Float, 
    A: Allocation!, 
    B: Allocation!, 
    beta: Float, 
    C: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

SGEMM performs one of the matrix-matrix operations C := alpha\*op(A)\*op(B) + beta\*C where op(X) is one of op(X) = X or op(X) = X\*\*T Details: http://www.netlib.org/lapack/explore-html/d4/de2/sgemm_8f.html

| Parameters ||
|---|---|
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `TransB` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix B. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `alpha` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The scalar alpha. |
| --- | --- |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F32. |
| `B` | [Allocation](Allocation.md)!: The input allocation contains matrix B, supported elements type F32. |
| `beta` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The scalar beta. |
| --- | --- |
| `C` | [Allocation](Allocation.md)!: The input allocation contains matrix C, supported elements type F32. |

### SGEMV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun SGEMV(
    TransA: Int, 
    alpha: Float, 
    A: Allocation!, 
    X: Allocation!, 
    incX: Int, 
    beta: Float, 
    Y: Allocation!, 
    incY: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

SGEMV performs one of the matrix-vector operations y := alpha\*A\*x + beta\*y or y := alpha\*A\*\*T\*x + beta\*y Details: http://www.netlib.org/lapack/explore-html/db/d58/sgemv_8f.html

| Parameters ||
|---|---|
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `alpha` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The scalar alpha. |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F32. |
| --- | --- |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F32. |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| `beta` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The scalar beta. |
| --- | --- |
| `Y` | [Allocation](Allocation.md)!: The input allocation contains vector y, supported elements type F32. |
| `incY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector y, must be larger than zero. |

### SGER

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun SGER(
    alpha: Float, 
    X: Allocation!, 
    incX: Int, 
    Y: Allocation!, 
    incY: Int, 
    A: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

SGER performs the rank 1 operation A := alpha\*x\*y\*\*T + A Details: http://www.netlib.org/lapack/explore-html/db/d5c/sger_8f.html

| Parameters ||
|---|---|
| `alpha` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The scalar alpha. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F32. |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| --- | --- |
| `Y` | [Allocation](Allocation.md)!: The input allocation contains vector y, supported elements type F32. |
| `incY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector y, must be larger than zero. |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F32. |
| --- | --- |

### SSBMV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun SSBMV(
    Uplo: Int, 
    K: Int, 
    alpha: Float, 
    A: Allocation!, 
    X: Allocation!, 
    incX: Int, 
    beta: Float, 
    Y: Allocation!, 
    incY: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

SSBMV performs the matrix-vector operation y := alpha\*A\*x + beta\*y Details: http://www.netlib.org/lapack/explore-html/d3/da1/ssbmv_8f.html Note: For a N\*N matrix, the input Allocation should also be of size N\*N (dimY = N, dimX = N), but only the region N\*(K+1) will be referenced. The following subroutine can is an example showing how to convert a UPPER trianglar matrix 'a' to row-based band matrix 'b'. for i in range(0, n): for j in range(i, min(i+k+1, n)): b\[i, j-i\] = a\[i, j\]

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part of the band matrix A is being supplied. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `K` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of off-diagonals of the matrix A |
| `alpha` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The scalar alpha. |
| --- | --- |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F32. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F32. |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| --- | --- |
| `beta` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The scalar beta. |
| `Y` | [Allocation](Allocation.md)!: The input allocation contains vector y, supported elements type F32. |
| `incY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector y, must be larger than zero. |
| --- | --- |

### SSPMV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun SSPMV(
    Uplo: Int, 
    alpha: Float, 
    Ap: Allocation!, 
    X: Allocation!, 
    incX: Int, 
    beta: Float, 
    Y: Allocation!, 
    incY: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

SSPMV performs the matrix-vector operation y := alpha\*A\*x + beta\*y Details: http://www.netlib.org/lapack/explore-html/d8/d68/sspmv_8f.html Note: For a N\*N matrix, the input Allocation should be a 1D allocation of size dimX = N\*(N+1)/2, The following subroutine can is an example showing how to convert a UPPER trianglar matrix 'a' to packed matrix 'b'. k = 0 for i in range(0, n): for j in range(i, n): b\[k++\] = a\[i, j\]

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part of the matrix A is supplied in packed form. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `alpha` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The scalar alpha. |
| `Ap` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F32. |
| --- | --- |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F32. |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| `beta` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The scalar beta. |
| --- | --- |
| `Y` | [Allocation](Allocation.md)!: The input allocation contains vector y, supported elements type F32. |
| `incY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector y, must be larger than zero. |

### SSPR

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun SSPR(
    Uplo: Int, 
    alpha: Float, 
    X: Allocation!, 
    incX: Int, 
    Ap: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

SSPR performs the rank 1 operation A := alpha\*x\*x\*\*T + A Details: http://www.netlib.org/lapack/explore-html/d2/d9b/sspr_8f.html Note: For a N\*N matrix, the input Allocation should be a 1D allocation of size dimX = N\*(N+1)/2, The following subroutine can is an example showing how to convert a UPPER trianglar matrix 'a' to packed matrix 'b'. k = 0 for i in range(0, n): for j in range(i, n): b\[k++\] = a\[i, j\]

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part is to be supplied in the packed form. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `alpha` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The scalar alpha. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F32. |
| --- | --- |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| `Ap` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F32. |

### SSPR2

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun SSPR2(
    Uplo: Int, 
    alpha: Float, 
    X: Allocation!, 
    incX: Int, 
    Y: Allocation!, 
    incY: Int, 
    Ap: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

SSPR2 performs the symmetric rank 2 operation A := alpha\*x\*y\*\*T + alpha\*y\*x\*\*T + A Details: http://www.netlib.org/lapack/explore-html/db/d3e/sspr2_8f.html Note: For a N\*N matrix, the input Allocation should be a 1D allocation of size dimX = N\*(N+1)/2, The following subroutine can is an example showing how to convert a UPPER trianglar matrix 'a' to packed matrix 'b'. k = 0 for i in range(0, n): for j in range(i, n): b\[k++\] = a\[i, j\]

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part is to be supplied in the packed form. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `alpha` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The scalar alpha. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F32. |
| --- | --- |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| `Y` | [Allocation](Allocation.md)!: The input allocation contains vector y, supported elements type F32. |
| `incY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector y, must be larger than zero. |
| --- | --- |
| `Ap` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F32. |

### SSYMM

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun SSYMM(
    Side: Int, 
    Uplo: Int, 
    alpha: Float, 
    A: Allocation!, 
    B: Allocation!, 
    beta: Float, 
    C: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

SSYMM performs one of the matrix-matrix operations C := alpha\*A\*B + beta\*C or C := alpha\*B\*A + beta\*C Details: http://www.netlib.org/lapack/explore-html/d7/d42/ssymm_8f.html

| Parameters ||
|---|---|
| `Side` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the symmetric matrix A appears on the left or right. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#RIGHT:kotlin.Int` |
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part is to be referenced. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `alpha` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The scalar alpha. |
| --- | --- |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F32. |
| `B` | [Allocation](Allocation.md)!: The input allocation contains matrix B, supported elements type F32. |
| `beta` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The scalar beta. |
| --- | --- |
| `C` | [Allocation](Allocation.md)!: The input allocation contains matrix C, supported elements type F32. |

### SSYMV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun SSYMV(
    Uplo: Int, 
    alpha: Float, 
    A: Allocation!, 
    X: Allocation!, 
    incX: Int, 
    beta: Float, 
    Y: Allocation!, 
    incY: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

SSYMV performs the matrix-vector operation y := alpha\*A\*x + beta\*y Details: http://www.netlib.org/lapack/explore-html/d2/d94/ssymv_8f.html

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part is to be referenced. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `alpha` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The scalar alpha. |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F32. |
| --- | --- |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F32. |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| `beta` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The scalar beta. |
| --- | --- |
| `Y` | [Allocation](Allocation.md)!: The input allocation contains vector y, supported elements type F32. |
| `incY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector y, must be larger than zero. |

### SSYR

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun SSYR(
    Uplo: Int, 
    alpha: Float, 
    X: Allocation!, 
    incX: Int, 
    A: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

SSYR performs the rank 1 operation A := alpha\*x\*x\*\*T + A Details: http://www.netlib.org/lapack/explore-html/d6/dac/ssyr_8f.html

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part is to be referenced. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `alpha` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The scalar alpha. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F32. |
| --- | --- |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F32. |

### SSYR2

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun SSYR2(
    Uplo: Int, 
    alpha: Float, 
    X: Allocation!, 
    incX: Int, 
    Y: Allocation!, 
    incY: Int, 
    A: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

SSYR2 performs the symmetric rank 2 operation A := alpha\*x\*y\*\*T + alpha\*y\*x\*\*T + A Details: http://www.netlib.org/lapack/explore-html/db/d99/ssyr2_8f.html

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part is to be referenced. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `alpha` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The scalar alpha. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F32. |
| --- | --- |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| `Y` | [Allocation](Allocation.md)!: The input allocation contains vector y, supported elements type F32. |
| `incY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector y, must be larger than zero. |
| --- | --- |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F32. |

### SSYR2K

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun SSYR2K(
    Uplo: Int, 
    Trans: Int, 
    alpha: Float, 
    A: Allocation!, 
    B: Allocation!, 
    beta: Float, 
    C: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

SSYR2K performs one of the symmetric rank 2k operations C := alpha\*A\*B\*\*T + alpha\*B\*A\*\*T + beta\*C or C := alpha\*A\*\*T\*B + alpha\*B\*\*T\*A + beta\*C Details: http://www.netlib.org/lapack/explore-html/df/d3d/ssyr2k_8f.html

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part of C is to be referenced. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `Trans` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to the operation. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `alpha` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The scalar alpha. |
| --- | --- |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F32. |
| `B` | [Allocation](Allocation.md)!: The input allocation contains matrix B, supported elements type F32. |
| `beta` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The scalar beta. |
| --- | --- |
| `C` | [Allocation](Allocation.md)!: The input allocation contains matrix C, supported elements type F32. |

### SSYRK

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun SSYRK(
    Uplo: Int, 
    Trans: Int, 
    alpha: Float, 
    A: Allocation!, 
    beta: Float, 
    C: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

SSYRK performs one of the symmetric rank k operations C := alpha\*A\*A\*\*T + beta\*C or C := alpha\*A\*\*T\*A + beta\*C Details: http://www.netlib.org/lapack/explore-html/d0/d40/ssyrk_8f.html

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part of C is to be referenced. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `Trans` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to the operation. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `alpha` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The scalar alpha. |
| --- | --- |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F32. |
| `beta` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The scalar beta. |
| `C` | [Allocation](Allocation.md)!: The input allocation contains matrix C, supported elements type F32. |
| --- | --- |

### STBMV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun STBMV(
    Uplo: Int, 
    TransA: Int, 
    Diag: Int, 
    K: Int, 
    A: Allocation!, 
    X: Allocation!, 
    incX: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

STBMV performs one of the matrix-vector operations x := A\*x or x := A\*\*T\*x Details: http://www.netlib.org/lapack/explore-html/d6/d7d/stbmv_8f.html Note: For a N\*N matrix, the input Allocation should also be of size N\*N (dimY = N, dimX = N), but only the region N\*(K+1) will be referenced. The following subroutine can is an example showing how to convert a UPPER trianglar matrix 'a' to row-based band matrix 'b'. for i in range(0, n): for j in range(i, min(i+k+1, n)): b\[i, j-i\] = a\[i, j\]

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the matrix is an upper or lower triangular matrix. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `Diag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether or not A is unit triangular. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NON_UNIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UNIT:kotlin.Int` |
| --- | --- |
| `K` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of off-diagonals of the matrix A |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F32. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F32. |
| --- | --- |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |

### STBSV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun STBSV(
    Uplo: Int, 
    TransA: Int, 
    Diag: Int, 
    K: Int, 
    A: Allocation!, 
    X: Allocation!, 
    incX: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

STBSV solves one of the systems of equations A\*x = b or A\*\*T\*x = b Details: http://www.netlib.org/lapack/explore-html/d0/d1f/stbsv_8f.html Note: For a N\*N matrix, the input Allocation should also be of size N\*N (dimY = N, dimX = N), but only the region N\*(K+1) will be referenced. The following subroutine can is an example showing how to convert a UPPER trianglar matrix 'a' to row-based band matrix 'b'. for i in range(0, n): for j in range(i, min(i+k+1, n)): b\[i, j-i\] = a\[i, j\]

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the matrix is an upper or lower triangular matrix. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `Diag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether or not A is unit triangular. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NON_UNIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UNIT:kotlin.Int` |
| --- | --- |
| `K` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of off-diagonals of the matrix A |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F32. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F32. |
| --- | --- |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |

### STPMV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun STPMV(
    Uplo: Int, 
    TransA: Int, 
    Diag: Int, 
    Ap: Allocation!, 
    X: Allocation!, 
    incX: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

STPMV performs one of the matrix-vector operations x := A\*x or x := A\*\*T\*x Details: http://www.netlib.org/lapack/explore-html/db/db1/stpmv_8f.html Note: For a N\*N matrix, the input Allocation should be a 1D allocation of size dimX = N\*(N+1)/2, The following subroutine can is an example showing how to convert a UPPER trianglar matrix 'a' to packed matrix 'b'. k = 0 for i in range(0, n): for j in range(i, n): b\[k++\] = a\[i, j\]

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the matrix is an upper or lower triangular matrix. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `Diag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether or not A is unit triangular. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NON_UNIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UNIT:kotlin.Int` |
| --- | --- |
| `Ap` | [Allocation](Allocation.md)!: The input allocation contains packed matrix A, supported elements type F32. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F32. |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| --- | --- |

### STPSV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun STPSV(
    Uplo: Int, 
    TransA: Int, 
    Diag: Int, 
    Ap: Allocation!, 
    X: Allocation!, 
    incX: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

STPSV solves one of the systems of equations A\*x = b or A\*\*T\*x = b Details: http://www.netlib.org/lapack/explore-html/d0/d7c/stpsv_8f.html Note: For a N\*N matrix, the input Allocation should be a 1D allocation of size dimX = N\*(N+1)/2, The following subroutine can is an example showing how to convert a UPPER trianglar matrix 'a' to packed matrix 'b'. k = 0 for i in range(0, n): for j in range(i, n): b\[k++\] = a\[i, j\]

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the matrix is an upper or lower triangular matrix. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `Diag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether or not A is unit triangular. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NON_UNIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UNIT:kotlin.Int` |
| --- | --- |
| `Ap` | [Allocation](Allocation.md)!: The input allocation contains packed matrix A, supported elements type F32. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F32. |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| --- | --- |

### STRMM

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun STRMM(
    Side: Int, 
    Uplo: Int, 
    TransA: Int, 
    Diag: Int, 
    alpha: Float, 
    A: Allocation!, 
    B: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

STRMM performs one of the matrix-matrix operations B := alpha\*op(A)\*B or B := alpha\*B\*op(A) op(A) is one of op(A) = A or op(A) = A\*\*T Details: http://www.netlib.org/lapack/explore-html/df/d01/strmm_8f.html

| Parameters ||
|---|---|
| `Side` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the symmetric matrix A appears on the left or right. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#RIGHT:kotlin.Int` |
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether matrix A is upper or lower triangular. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| --- | --- |
| `Diag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether or not A is unit triangular. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NON_UNIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UNIT:kotlin.Int` |
| `alpha` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The scalar alpha. |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F32. |
| --- | --- |
| `B` | [Allocation](Allocation.md)!: The input allocation contains matrix B, supported elements type F32. |

### STRMV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun STRMV(
    Uplo: Int, 
    TransA: Int, 
    Diag: Int, 
    A: Allocation!, 
    X: Allocation!, 
    incX: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

STRMV performs one of the matrix-vector operations x := A\*x or x := A\*\*T\*x Details: http://www.netlib.org/lapack/explore-html/de/d45/strmv_8f.html

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the matrix is an upper or lower triangular matrix. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `Diag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether or not A is unit triangular. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NON_UNIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UNIT:kotlin.Int` |
| --- | --- |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F32. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F32. |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| --- | --- |

### STRSM

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun STRSM(
    Side: Int, 
    Uplo: Int, 
    TransA: Int, 
    Diag: Int, 
    alpha: Float, 
    A: Allocation!, 
    B: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

STRSM solves one of the matrix equations op(A)\*X := alpha\*B or X\*op(A) := alpha\*B op(A) is one of op(A) = A or op(A) = A\*\*T Details: http://www.netlib.org/lapack/explore-html/d2/d8b/strsm_8f.html

| Parameters ||
|---|---|
| `Side` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the symmetric matrix A appears on the left or right. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#RIGHT:kotlin.Int` |
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether matrix A is upper or lower triangular. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| --- | --- |
| `Diag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether or not A is unit triangular. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NON_UNIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UNIT:kotlin.Int` |
| `alpha` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The scalar alpha. |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F32. |
| --- | --- |
| `B` | [Allocation](Allocation.md)!: The input allocation contains matrix B, supported elements type F32. |

### STRSV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun STRSV(
    Uplo: Int, 
    TransA: Int, 
    Diag: Int, 
    A: Allocation!, 
    X: Allocation!, 
    incX: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

STRSV solves one of the systems of equations A\*x = b or A\*\*T\*x = b Details: http://www.netlib.org/lapack/explore-html/d0/d2a/strsv_8f.html

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the matrix is an upper or lower triangular matrix. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `Diag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether or not A is unit triangular. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NON_UNIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UNIT:kotlin.Int` |
| --- | --- |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F32. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F32. |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| --- | --- |

### ZGBMV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun ZGBMV(
    TransA: Int, 
    KL: Int, 
    KU: Int, 
    alpha: Double2!, 
    A: Allocation!, 
    X: Allocation!, 
    incX: Int, 
    beta: Double2!, 
    Y: Allocation!, 
    incY: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

ZGBMV performs one of the matrix-vector operations y := alpha\*A\*x + beta\*y or y := alpha\*A\*\*T\*x + beta\*y or y := alpha\*A\*\*H\*x + beta\*y Details: http://www.netlib.org/lapack/explore-html/d9/d46/zgbmv_8f.html Note: For a M\*N matrix, the input Allocation should also be of size M\*N (dimY = M, dimX = N), but only the region M\*(KL+KU+1) will be referenced. The following subroutine can is an example showing how to convert the original matrix 'a' to row-based band matrix 'b'. for i in range(0, m): for j in range(max(0, i-kl), min(i+ku+1, n)): b\[i, j-i+kl\] = a\[i, j\]

| Parameters ||
|---|---|
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `KL` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of sub-diagonals of the matrix A. |
| `KU` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of super-diagonals of the matrix A. |
| --- | --- |
| `alpha` | [Double2](Double2.md)!: The scalar alpha. |
| `A` | [Allocation](Allocation.md)!: The input allocation contains the band matrix A, supported elements type F64_2. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F64_2. |
| --- | --- |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| `beta` | [Double2](Double2.md)!: The scalar beta. |
| `Y` | [Allocation](Allocation.md)!: The input allocation contains vector y, supported elements type F64_2. |
| --- | --- |
| `incY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector y, must be larger than zero. |

### ZGEMM

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun ZGEMM(
    TransA: Int, 
    TransB: Int, 
    alpha: Double2!, 
    A: Allocation!, 
    B: Allocation!, 
    beta: Double2!, 
    C: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

ZGEMM performs one of the matrix-matrix operations C := alpha\*op(A)\*op(B) + beta\*C where op(X) is one of op(X) = X or op(X) = X\*\*T or op(X) = X\*\*H Details: http://www.netlib.org/lapack/explore-html/d7/d76/zgemm_8f.html

| Parameters ||
|---|---|
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `TransB` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix B. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `alpha` | [Double2](Double2.md)!: The scalar alpha. |
| --- | --- |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F64_2. |
| `B` | [Allocation](Allocation.md)!: The input allocation contains matrix B, supported elements type F64_2. |
| `beta` | [Double2](Double2.md)!: The scalar beta. |
| --- | --- |
| `C` | [Allocation](Allocation.md)!: The input allocation contains matrix C, supported elements type F64_2. |

### ZGEMV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun ZGEMV(
    TransA: Int, 
    alpha: Double2!, 
    A: Allocation!, 
    X: Allocation!, 
    incX: Int, 
    beta: Double2!, 
    Y: Allocation!, 
    incY: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

ZGEMV performs one of the matrix-vector operations y := alpha\*A\*x + beta\*y or y := alpha\*A\*\*T\*x + beta\*y or y := alpha\*A\*\*H\*x + beta\*y Details: http://www.netlib.org/lapack/explore-html/db/d40/zgemv_8f.html

| Parameters ||
|---|---|
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `alpha` | [Double2](Double2.md)!: The scalar alpha. |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F64_2. |
| --- | --- |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F64_2. |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| `beta` | [Double2](Double2.md)!: The scalar beta. |
| --- | --- |
| `Y` | [Allocation](Allocation.md)!: The input allocation contains vector y, supported elements type F64_2. |
| `incY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector y, must be larger than zero. |

### ZGERC

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun ZGERC(
    alpha: Double2!, 
    X: Allocation!, 
    incX: Int, 
    Y: Allocation!, 
    incY: Int, 
    A: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

ZGERC performs the rank 1 operation A := alpha\*x\*y\*\*H + A Details: http://www.netlib.org/lapack/explore-html/d3/dad/zgerc_8f.html

| Parameters ||
|---|---|
| `alpha` | [Double2](Double2.md)!: The scalar alpha. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F64_2. |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| --- | --- |
| `Y` | [Allocation](Allocation.md)!: The input allocation contains vector y, supported elements type F64_2. |
| `incY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector y, must be larger than zero. |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F64_2. |
| --- | --- |

### ZGERU

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun ZGERU(
    alpha: Double2!, 
    X: Allocation!, 
    incX: Int, 
    Y: Allocation!, 
    incY: Int, 
    A: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

ZGERU performs the rank 1 operation A := alpha\*x\*y\*\*T + A Details: http://www.netlib.org/lapack/explore-html/d7/d12/zgeru_8f.html

| Parameters ||
|---|---|
| `alpha` | [Double2](Double2.md)!: The scalar alpha. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F64_2. |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| --- | --- |
| `Y` | [Allocation](Allocation.md)!: The input allocation contains vector y, supported elements type F64_2. |
| `incY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector y, must be larger than zero. |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F64_2. |
| --- | --- |

### ZHBMV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun ZHBMV(
    Uplo: Int, 
    K: Int, 
    alpha: Double2!, 
    A: Allocation!, 
    X: Allocation!, 
    incX: Int, 
    beta: Double2!, 
    Y: Allocation!, 
    incY: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

ZHBMV performs the matrix-vector operation y := alpha\*A\*x + beta\*y Details: http://www.netlib.org/lapack/explore-html/d3/d1a/zhbmv_8f.html Note: For a N\*N matrix, the input Allocation should also be of size N\*N (dimY = N, dimX = N), but only the region N\*(K+1) will be referenced. The following subroutine can is an example showing how to convert a UPPER trianglar matrix 'a' to row-based band matrix 'b'. for i in range(0, n): for j in range(i, min(i+k+1, n)): b\[i, j-i\] = a\[i, j\]

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part of the band matrix A is being supplied. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `K` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of off-diagonals of the matrix A |
| `alpha` | [Double2](Double2.md)!: The scalar alpha. |
| --- | --- |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F64_2. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F64_2. |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| --- | --- |
| `beta` | [Double2](Double2.md)!: The scalar beta. |
| `Y` | [Allocation](Allocation.md)!: The input allocation contains vector y, supported elements type F64_2. |
| `incY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector y, must be larger than zero. |
| --- | --- |

### ZHEMM

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun ZHEMM(
    Side: Int, 
    Uplo: Int, 
    alpha: Double2!, 
    A: Allocation!, 
    B: Allocation!, 
    beta: Double2!, 
    C: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

ZHEMM performs one of the matrix-matrix operations C := alpha\*A\*B + beta\*C or C := alpha\*B\*A + beta\*C Details: http://www.netlib.org/lapack/explore-html/d6/d3e/zhemm_8f.html

| Parameters ||
|---|---|
| `Side` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the symmetric matrix A appears on the left or right. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#RIGHT:kotlin.Int` |
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part is to be referenced. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `alpha` | [Double2](Double2.md)!: The scalar alpha. |
| --- | --- |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F64_2. |
| `B` | [Allocation](Allocation.md)!: The input allocation contains matrix B, supported elements type F64_2. |
| `beta` | [Double2](Double2.md)!: The scalar beta. |
| --- | --- |
| `C` | [Allocation](Allocation.md)!: The input allocation contains matrix C, supported elements type F64_2. |

### ZHEMV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun ZHEMV(
    Uplo: Int, 
    alpha: Double2!, 
    A: Allocation!, 
    X: Allocation!, 
    incX: Int, 
    beta: Double2!, 
    Y: Allocation!, 
    incY: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

ZHEMV performs the matrix-vector operation y := alpha\*A\*x + beta\*y Details: http://www.netlib.org/lapack/explore-html/d0/ddd/zhemv_8f.html

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part is to be referenced. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `alpha` | [Double2](Double2.md)!: The scalar alpha. |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F64_2. |
| --- | --- |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F64_2. |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| `beta` | [Double2](Double2.md)!: The scalar beta. |
| --- | --- |
| `Y` | [Allocation](Allocation.md)!: The input allocation contains vector y, supported elements type F64_2. |
| `incY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector y, must be larger than zero. |

### ZHER

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun ZHER(
    Uplo: Int, 
    alpha: Double, 
    X: Allocation!, 
    incX: Int, 
    A: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

ZHER performs the rank 1 operation A := alpha\*x\*x\*\*H + A Details: http://www.netlib.org/lapack/explore-html/de/d0e/zher_8f.html

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part is to be referenced. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `alpha` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): The scalar alpha. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F64_2. |
| --- | --- |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F64_2. |

### ZHER2

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun ZHER2(
    Uplo: Int, 
    alpha: Double2!, 
    X: Allocation!, 
    incX: Int, 
    Y: Allocation!, 
    incY: Int, 
    A: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

ZHER2 performs the symmetric rank 2 operation A := alpha\*x\*y\*\*H + alpha\*y\*x\*\*H + A Details: http://www.netlib.org/lapack/explore-html/da/d8a/zher2_8f.html

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part is to be referenced. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `alpha` | [Double2](Double2.md)!: The scalar alpha. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F64_2. |
| --- | --- |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| `Y` | [Allocation](Allocation.md)!: The input allocation contains vector y, supported elements type F64_2. |
| `incY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector y, must be larger than zero. |
| --- | --- |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F64_2. |

### ZHER2K

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun ZHER2K(
    Uplo: Int, 
    Trans: Int, 
    alpha: Double2!, 
    A: Allocation!, 
    B: Allocation!, 
    beta: Double, 
    C: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

ZHER2K performs one of the hermitian rank 2k operations C := alpha\*A\*B\*\*H + conjg( alpha )\*B\*A\*\*H + beta\*C or C := alpha\*A\*\*H\*B + conjg( alpha )\*B\*\*H\*A + beta\*C Details: http://www.netlib.org/lapack/explore-html/d7/dfa/zher2k_8f.html

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part of C is to be referenced. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `Trans` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to the operation. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `alpha` | [Double2](Double2.md)!: The scalar alpha. |
| --- | --- |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F64_2. |
| `B` | [Allocation](Allocation.md)!: The input allocation contains matrix B, supported elements type F64_2. |
| `beta` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): The scalar beta. |
| --- | --- |
| `C` | [Allocation](Allocation.md)!: The input allocation contains matrix C, supported elements type F64_2. |

### ZHERK

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun ZHERK(
    Uplo: Int, 
    Trans: Int, 
    alpha: Double, 
    A: Allocation!, 
    beta: Double, 
    C: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

ZHERK performs one of the hermitian rank k operations C := alpha\*A\*A\*\*H + beta\*C or C := alpha\*A\*\*H\*A + beta\*C Details: http://www.netlib.org/lapack/explore-html/d1/db1/zherk_8f.html

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part of C is to be referenced. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `Trans` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to the operation. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `alpha` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): The scalar alpha. |
| --- | --- |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F64_2. |
| `beta` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): The scalar beta. |
| `C` | [Allocation](Allocation.md)!: The input allocation contains matrix C, supported elements type F64_2. |
| --- | --- |

### ZHPMV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun ZHPMV(
    Uplo: Int, 
    alpha: Double2!, 
    Ap: Allocation!, 
    X: Allocation!, 
    incX: Int, 
    beta: Double2!, 
    Y: Allocation!, 
    incY: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

ZHPMV performs the matrix-vector operation y := alpha\*A\*x + beta\*y Details: http://www.netlib.org/lapack/explore-html/d0/d60/zhpmv_8f.html Note: For a N\*N matrix, the input Allocation should be a 1D allocation of size dimX = N\*(N+1)/2, The following subroutine can is an example showing how to convert a UPPER trianglar matrix 'a' to packed matrix 'b'. k = 0 for i in range(0, n): for j in range(i, n): b\[k++\] = a\[i, j\]

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part of the matrix A is supplied in packed form. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `alpha` | [Double2](Double2.md)!: The scalar alpha. |
| `Ap` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F64_2. |
| --- | --- |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F64_2. |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| `beta` | [Double2](Double2.md)!: The scalar beta. |
| --- | --- |
| `Y` | [Allocation](Allocation.md)!: The input allocation contains vector y, supported elements type F64_2. |
| `incY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector y, must be larger than zero. |

### ZHPR

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun ZHPR(
    Uplo: Int, 
    alpha: Double, 
    X: Allocation!, 
    incX: Int, 
    Ap: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

ZHPR performs the rank 1 operation A := alpha\*x\*x\*\*H + A Details: http://www.netlib.org/lapack/explore-html/de/de1/zhpr_8f.html Note: For a N\*N matrix, the input Allocation should be a 1D allocation of size dimX = N\*(N+1)/2, The following subroutine can is an example showing how to convert a UPPER trianglar matrix 'a' to packed matrix 'b'. k = 0 for i in range(0, n): for j in range(i, n): b\[k++\] = a\[i, j\]

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part is to be supplied in the packed form. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `alpha` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): The scalar alpha. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F64_2. |
| --- | --- |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| `Ap` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F64_2. |

### ZHPR2

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun ZHPR2(
    Uplo: Int, 
    alpha: Double2!, 
    X: Allocation!, 
    incX: Int, 
    Y: Allocation!, 
    incY: Int, 
    Ap: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

ZHPR2 performs the symmetric rank 2 operation A := alpha\*x\*y\*\*H + alpha\*y\*x\*\*H + A Details: http://www.netlib.org/lapack/explore-html/d5/d52/zhpr2_8f.html Note: For a N\*N matrix, the input Allocation should be a 1D allocation of size dimX = N\*(N+1)/2, The following subroutine can is an example showing how to convert a UPPER trianglar matrix 'a' to packed matrix 'b'. k = 0 for i in range(0, n): for j in range(i, n): b\[k++\] = a\[i, j\]

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part is to be supplied in the packed form. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `alpha` | [Double2](Double2.md)!: The scalar alpha. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F64_2. |
| --- | --- |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| `Y` | [Allocation](Allocation.md)!: The input allocation contains vector y, supported elements type F64_2. |
| `incY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector y, must be larger than zero. |
| --- | --- |
| `Ap` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F64_2. |

### ZSYMM

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun ZSYMM(
    Side: Int, 
    Uplo: Int, 
    alpha: Double2!, 
    A: Allocation!, 
    B: Allocation!, 
    beta: Double2!, 
    C: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

ZSYMM performs one of the matrix-matrix operations C := alpha\*A\*B + beta\*C or C := alpha\*B\*A + beta\*C Details: http://www.netlib.org/lapack/explore-html/df/d51/zsymm_8f.html

| Parameters ||
|---|---|
| `Side` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the symmetric matrix A appears on the left or right. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#RIGHT:kotlin.Int` |
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part is to be referenced. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `alpha` | [Double2](Double2.md)!: The scalar alpha. |
| --- | --- |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F64_2. |
| `B` | [Allocation](Allocation.md)!: The input allocation contains matrix B, supported elements type F64_2. |
| `beta` | [Double2](Double2.md)!: The scalar beta. |
| --- | --- |
| `C` | [Allocation](Allocation.md)!: The input allocation contains matrix C, supported elements type F64_2. |

### ZSYR2K

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun ZSYR2K(
    Uplo: Int, 
    Trans: Int, 
    alpha: Double2!, 
    A: Allocation!, 
    B: Allocation!, 
    beta: Double2!, 
    C: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

ZSYR2K performs one of the symmetric rank 2k operations C := alpha\*A\*B\*\*T + alpha\*B\*A\*\*T + beta\*C or C := alpha\*A\*\*T\*B + alpha\*B\*\*T\*A + beta\*C Details: http://www.netlib.org/lapack/explore-html/df/d20/zsyr2k_8f.html

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part of C is to be referenced. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `Trans` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to the operation. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `alpha` | [Double2](Double2.md)!: The scalar alpha. |
| --- | --- |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F64_2. |
| `B` | [Allocation](Allocation.md)!: The input allocation contains matrix B, supported elements type F64_2. |
| `beta` | [Double2](Double2.md)!: The scalar beta. |
| --- | --- |
| `C` | [Allocation](Allocation.md)!: The input allocation contains matrix C, supported elements type F64_2. |

### ZSYRK

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun ZSYRK(
    Uplo: Int, 
    Trans: Int, 
    alpha: Double2!, 
    A: Allocation!, 
    beta: Double2!, 
    C: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

ZSYRK performs one of the symmetric rank k operations C := alpha\*A\*A\*\*T + beta\*C or C := alpha\*A\*\*T\*A + beta\*C Details: http://www.netlib.org/lapack/explore-html/de/d54/zsyrk_8f.html

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the upper or lower triangular part of C is to be referenced. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `Trans` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to the operation. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `alpha` | [Double2](Double2.md)!: The scalar alpha. |
| --- | --- |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F64_2. |
| `beta` | [Double2](Double2.md)!: The scalar beta. |
| `C` | [Allocation](Allocation.md)!: The input allocation contains matrix C, supported elements type F64_2. |
| --- | --- |

### ZTBMV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun ZTBMV(
    Uplo: Int, 
    TransA: Int, 
    Diag: Int, 
    K: Int, 
    A: Allocation!, 
    X: Allocation!, 
    incX: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

ZTBMV performs one of the matrix-vector operations x := A\*x or x := A\*\*T\*x or x := A\*\*H\*x Details: http://www.netlib.org/lapack/explore-html/d3/d39/ztbmv_8f.html Note: For a N\*N matrix, the input Allocation should also be of size N\*N (dimY = N, dimX = N), but only the region N\*(K+1) will be referenced. The following subroutine can is an example showing how to convert a UPPER trianglar matrix 'a' to row-based band matrix 'b'. for i in range(0, n): for j in range(i, min(i+k+1, n)): b\[i, j-i\] = a\[i, j\]

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the matrix is an upper or lower triangular matrix. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `Diag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether or not A is unit triangular. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NON_UNIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UNIT:kotlin.Int` |
| --- | --- |
| `K` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of off-diagonals of the matrix A |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F64_2. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F64_2. |
| --- | --- |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |

### ZTBSV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun ZTBSV(
    Uplo: Int, 
    TransA: Int, 
    Diag: Int, 
    K: Int, 
    A: Allocation!, 
    X: Allocation!, 
    incX: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

ZTBSV solves one of the systems of equations A\*x = b or A\*\*T\*x = b or A\*\*H\*x = b Details: http://www.netlib.org/lapack/explore-html/d4/d5a/ztbsv_8f.html Note: For a N\*N matrix, the input Allocation should also be of size N\*N (dimY = N, dimX = N), but only the region N\*(K+1) will be referenced. The following subroutine can is an example showing how to convert a UPPER trianglar matrix 'a' to row-based band matrix 'b'. for i in range(0, n): for j in range(i, min(i+k+1, n)): b\[i, j-i\] = a\[i, j\]

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the matrix is an upper or lower triangular matrix. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `Diag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether or not A is unit triangular. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NON_UNIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UNIT:kotlin.Int` |
| --- | --- |
| `K` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of off-diagonals of the matrix A |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F64_2. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F64_2. |
| --- | --- |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |

### ZTPMV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun ZTPMV(
    Uplo: Int, 
    TransA: Int, 
    Diag: Int, 
    Ap: Allocation!, 
    X: Allocation!, 
    incX: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

ZTPMV performs one of the matrix-vector operations x := A\*x or x := A\*\*T\*x or x := A\*\*H\*x Details: http://www.netlib.org/lapack/explore-html/d2/d9e/ztpmv_8f.html Note: For a N\*N matrix, the input Allocation should be a 1D allocation of size dimX = N\*(N+1)/2, The following subroutine can is an example showing how to convert a UPPER trianglar matrix 'a' to packed matrix 'b'. k = 0 for i in range(0, n): for j in range(i, n): b\[k++\] = a\[i, j\]

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the matrix is an upper or lower triangular matrix. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `Diag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether or not A is unit triangular. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NON_UNIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UNIT:kotlin.Int` |
| --- | --- |
| `Ap` | [Allocation](Allocation.md)!: The input allocation contains packed matrix A, supported elements type F64_2. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F64_2. |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| --- | --- |

### ZTPSV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun ZTPSV(
    Uplo: Int, 
    TransA: Int, 
    Diag: Int, 
    Ap: Allocation!, 
    X: Allocation!, 
    incX: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

ZTPSV solves one of the systems of equations A\*x = b or A\*\*T\*x = b or A\*\*H\*x = b Details: http://www.netlib.org/lapack/explore-html/da/d57/ztpsv_8f.html Note: For a N\*N matrix, the input Allocation should be a 1D allocation of size dimX = N\*(N+1)/2, The following subroutine can is an example showing how to convert a UPPER trianglar matrix 'a' to packed matrix 'b'. k = 0 for i in range(0, n): for j in range(i, n): b\[k++\] = a\[i, j\]

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the matrix is an upper or lower triangular matrix. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `Diag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether or not A is unit triangular. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NON_UNIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UNIT:kotlin.Int` |
| --- | --- |
| `Ap` | [Allocation](Allocation.md)!: The input allocation contains packed matrix A, supported elements type F64_2. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F64_2. |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| --- | --- |

### ZTRMM

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun ZTRMM(
    Side: Int, 
    Uplo: Int, 
    TransA: Int, 
    Diag: Int, 
    alpha: Double2!, 
    A: Allocation!, 
    B: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

ZTRMM performs one of the matrix-matrix operations B := alpha\*op(A)\*B or B := alpha\*B\*op(A) op(A) is one of op(A) = A or op(A) = A\*\*T or op(A) = A\*\*H Details: http://www.netlib.org/lapack/explore-html/d8/de1/ztrmm_8f.html

| Parameters ||
|---|---|
| `Side` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the symmetric matrix A appears on the left or right. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#RIGHT:kotlin.Int` |
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether matrix A is upper or lower triangular. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| --- | --- |
| `Diag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether or not A is unit triangular. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NON_UNIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UNIT:kotlin.Int` |
| `alpha` | [Double2](Double2.md)!: The scalar alpha. |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F64_2. |
| --- | --- |
| `B` | [Allocation](Allocation.md)!: The input allocation contains matrix B, supported elements type F64_2. |

### ZTRMV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun ZTRMV(
    Uplo: Int, 
    TransA: Int, 
    Diag: Int, 
    A: Allocation!, 
    X: Allocation!, 
    incX: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

ZTRMV performs one of the matrix-vector operations x := A\*x or x := A\*\*T\*x or x := A\*\*H\*x Details: http://www.netlib.org/lapack/explore-html/d0/dd1/ztrmv_8f.html

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the matrix is an upper or lower triangular matrix. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `Diag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether or not A is unit triangular. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NON_UNIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UNIT:kotlin.Int` |
| --- | --- |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F64_2. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F64_2. |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| --- | --- |

### ZTRSM

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun ZTRSM(
    Side: Int, 
    Uplo: Int, 
    TransA: Int, 
    Diag: Int, 
    alpha: Double2!, 
    A: Allocation!, 
    B: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

ZTRSM solves one of the matrix equations op(A)\*X := alpha\*B or X\*op(A) := alpha\*B op(A) is one of op(A) = A or op(A) = A\*\*T or op(A) = A\*\*H Details: http://www.netlib.org/lapack/explore-html/d1/d39/ztrsm_8f.html

| Parameters ||
|---|---|
| `Side` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the symmetric matrix A appears on the left or right. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#RIGHT:kotlin.Int` |
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether matrix A is upper or lower triangular. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| --- | --- |
| `Diag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether or not A is unit triangular. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NON_UNIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UNIT:kotlin.Int` |
| `alpha` | [Double2](Double2.md)!: The scalar alpha. |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F64_2. |
| --- | --- |
| `B` | [Allocation](Allocation.md)!: The input allocation contains matrix B, supported elements type F64_2. |

### ZTRSV

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun ZTRSV(
    Uplo: Int, 
    TransA: Int, 
    Diag: Int, 
    A: Allocation!, 
    X: Allocation!, 
    incX: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

ZTRSV solves one of the systems of equations A\*x = b or A\*\*T\*x = b or A\*\*H\*x = b Details: http://www.netlib.org/lapack/explore-html/d1/d2f/ztrsv_8f.html

| Parameters ||
|---|---|
| `Uplo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether the matrix is an upper or lower triangular matrix. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UPPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#LOWER:kotlin.Int` |
| `TransA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of transpose applied to matrix A. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NO_TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#TRANSPOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#CONJ_TRANSPOSE:kotlin.Int` |
| `Diag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies whether or not A is unit triangular. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#NON_UNIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#UNIT:kotlin.Int` |
| --- | --- |
| `A` | [Allocation](Allocation.md)!: The input allocation contains matrix A, supported elements type F64_2. |
| `X` | [Allocation](Allocation.md)!: The input allocation contains vector x, supported elements type F64_2. |
| `incX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The increment for the elements of vector x, must be larger than zero. |
| --- | --- |

### create

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun create(rs: RenderScript!): ScriptIntrinsicBLAS!
```

**Deprecated:** *Deprecated in Java.*

Create an intrinsic to access BLAS subroutines.

| Parameters ||
|---|---|
| `rs` | [RenderScript](RenderScript.md)!: The RenderScript context |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS#!` | ScriptIntrinsicBLAS |
