# Emscripten

## Build

```
cd linux
emmake make
```

## Link

```
emcc -flto -O3 -fno-rtti -fno-exceptions *.o */*.o */*/*.o -o index.html -sUSE_SDL=2 -sUSE_SDL_MIXER=2 -sSDL2_MIXER_FORMATS='["wav","mod"]' -sASYNCIFY -sENVIRONMENT=web --preload-file ../resources/@. --closure 1 -sEXPORTED_RUNTIME_METHODS=['allocate']
```
