## Add flags to cmake
Compile without avx512 accelerator
```
cmake -DCMAKE_CXX_FLAGS="-mno-avx512f"
```