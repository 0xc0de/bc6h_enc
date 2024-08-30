# bc6h_enc
## Single file library for BC6H compression with no external dependencies.

Official repository: https://github.com/0xc0de/bc6h_enc

The code is based on BC6HBC7.cpp from DirectXTex and localized into a single header library with no external dependencies.

### How to use:
   
```c
// You can define:
//  for debug logging:
//   #define BC6H_LOG(s) YourPrint(s)
//  for asserts:
//   #define BC6H_ASSERT(expression) YourAssert(expression)
//  to override float<->half packing:
//   #define BC6H_HALF_TO_FLOAT(h) YourImpl(h)
//   #define BC6H_FLOAT_TO_HALF(f) YourImpl(f)
#define BC6H_ENC_IMPLEMENTATION
#include "bc6h_enc.h"
```
##   Public interface:
```c
bc6h_enc::DecodeBC6HU(void* pDest, const void* pSrc);
bc6h_enc::DecodeBC6HS(void* pDest, const void* pSrc);
bc6h_enc::EncodeBC6HU(void* pDest, const void* pSrc);
bc6h_enc::EncodeBC6HS(void* pDest, const void* pSrc);
```
