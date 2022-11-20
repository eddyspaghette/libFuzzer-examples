# How to build

## Prerequisities & Dependencies:
- clang (ver 9 or above for libFuzzer)
- cMake
- Ubuntu 18.04 LTS


1) follow instructions in cJSON folder on how to install / build the library using cMake/make



2) if needed, run the command below to refresh library cache after installing/building cJSON

```
sudo ldconfig
```




3) build the executable (default called ./a.out in build directory) using the following command

```
clang++ -g -fsanitize=fuzzer,address libcjson.so libcjson.so.1 example.cc
```
