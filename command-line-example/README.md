#  Skia Examples for Command Line with Xcode

> Skia examples running as a CLI application on macOS

# Depdencies

- Xcode 11 over
- libskia.a: build as static libarary without dependecies of multimedia. built with m87 and macOS, and options below

```sh
$ gn gen out/Static --args="is_official_build=true skia_use_system_expat=false skia_use_system_icu=false skia_use_system_libjpeg_turbo=false skia_use_system_libpng=false skia_use_system_libwebp=false skia_use_system_zlib=false extra_cflags_cc=[\"-frtti\"]"
$ ninja -C out/Static skia
```

- to want to build on shell

```sh
$ g++ -std=c++17 SkiaExamples/main.cpp -framework CoreFoundation -framework CoreGraphics -framework CoreText -framework CoreServices -L./lib -lskia -I. -o bin/SkiaExamples
```
# License

Jimmy Moon @ MIT
