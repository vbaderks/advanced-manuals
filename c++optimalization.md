# C++ optimalitzation

## MSVC

The MSVC compiler has a couple of settings to optimize for certain CPUs:

/arch:IA32  
/arch:SSE  
/arch:SSE2  
/arch:AVX  
/arch:AVX2  
/arch:AVX512  

The default mode for x86 and x64 is SSE2.

/arch:[armv8.0-armv8.8]

The default for ARM64 is armv8.0.

see:
https://learn.microsoft.com/en-us/cpp/build/reference/arch-minimum-cpu-architecture

The MSVC compiler can target several CPUs.
The default is /favor:blend.
This seems the best option as the AMD64 and INTEL64 options are unclear.


https://learn.microsoft.com/en-us/cpp/build/reference/favor-optimize-for-architecture-specifics