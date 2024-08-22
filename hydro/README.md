# hydro

this is an experiment that tries to compile a hydra patch using @kabelsalat/core.

## Examples

- [comic eye soup](https://felixroos.github.io/schattenspiel/hydro/#b3NjKDIwLC4xLDIpCi5tb2R1bGF0ZShub2lzZSgzKSwwLjI1KQoudGhyZXNoKC40KQoubW9kdWxhdGUob3NjKDEwKS5yb3RhdGUoTWF0aC5QSS8yKSwuNykKLm1vZHVsYXRlS2FsZWlkKG5vaXNlKDQpKQoub3V0KCk=)
- [ojack demo patch](https://felixroos.github.io/schattenspiel/hydro/#Ly8gbGljZW5zZWQgd2l0aCBDQyBCWS1OQy1TQSA0LjAgaHR0cHM6Ly9jcmVhdGl2ZWNvbW1vbnMub3JnL2xpY2Vuc2VzL2J5LW5jLXNhLzQuMC8KLy8gYnkgT2xpdmlhIEphY2sKLy8gaHR0cHM6Ly9vamFjay5naXRodWIuaW8KCm9zYygxMDAsIDAuMDEsIDEuNCkKICAucm90YXRlKDAsIDAuMSkKICAubXVsdChvc2MoMTAsIDAuMSkubW9kdWxhdGUob3NjKDEwKS5yb3RhdGUoMCwgLTAuMSksIDEpKQogIC5jb2xvcigyLjgzLCAwLjkxLCAwLjM5KQogIC5vdXQoKTs=)
- [Puertas III (almost)](https://felixroos.github.io/schattenspiel/hydro/#Ly8gbGljZW5zZWQgd2l0aCBDQyBCWS1OQy1TQSA0LjAgaHR0cHM6Ly9jcmVhdGl2ZWNvbW1vbnMub3JnL2xpY2Vuc2VzL2J5LW5jLXNhLzQuMC8KLy8gUHVlcnRhcyBJSUkKLy8gcG9yIENlbGVzdGUgQmV0YW5jdXIKLy8gaHR0cHM6Ly9naXRodWIuY29tL2Vzc3RlYmFuCiAKb3NjKDQwLDAuMiwxKQogIC5tb2R1bGF0ZVNjYWxlKG9zYyg0MCwwLDEpLmthbGVpZCg4KSkKICAucmVwZWF0KDIsNCkKIC8vIC5tb2R1bGF0ZShvMCwwLjA1KQogIC5tb2R1bGF0ZUthbGVpZChzaGFwZSg0LDAuMSwxKSkKICAub3V0KCkK)
- [feedback example](https://felixroos.github.io/schattenspiel/hydro/#c3JjKCkKLm1vZHVsYXRlKG5vaXNlKDgpLDAuMDA1KQouYmxlbmQoc2hhcGUoNCksMC4wMSkKLnJvdGF0ZSgwLjAxKQoub3V0KCk=)
- [trypophobia](https://felixroos.github.io/schattenspiel/hydro/#Ly8gbGljZW5zZWQgd2l0aCBDQyBCWS1OQy1TQSA0LjAgaHR0cHM6Ly9jcmVhdGl2ZWNvbW1vbnMub3JnL2xpY2Vuc2VzL2J5LW5jLXNhLzQuMC8KLy9yYW5kb20gdHJ5cG9waG9iaWEgLSBjaGFuZ2VzIGV2ZXJ5dGltZSB5b3UgbG9hZCBpdCEKLy9ieSBSaXRjaHNlCi8vIG1vZGlmaWVkIGJ5IGZyb29zIHRvIHdvcmsgaW4gaHlkcm8KLy9pbnN0YWdyYW0uY29tL3JpdGNoc2UKIApmdW5jdGlvbiByKG1pbj0wLG1heD0xKSB7IHJldHVybiBNYXRoLnJhbmRvbSgpKihtYXgtbWluKSttaW47IH0KIApzb2xpZCgxLDEsMSkKLmRpZmYoIHNoYXBlKCA0LCByKDAuNiwwLjkzKSwgLjA5KS5yZXBlYXQoMjAsMTApICkKLm1vZHVsYXRlU2NhbGUob3NjKDgpLnJvdGF0ZShyKC0uNSwuNSkpLC41MikKLmFkZChzcmMobzApLnNjYWxlKDAuOTY1KS5yb3RhdGUoLjAxMiooTWF0aC5yb3VuZChyKC0yLDEpKSkpCi5jb2xvcihyKCkscigpLHIoKSkKLm1vZHVsYXRlUm90YXRlKHNyYyhvMCkscigwLDAuNSkpCi5icmlnaHRuZXNzKC4xNSkKLC43KQoub3V0KCkK)

## Completeness

Not all hydra functions / features work, and probably never will, as this is mostly an experiment out of curiosity.
The initial goal was to see if @kabelsalat/core could be used to compile an existing DSL that also targets another language (GLSL) + another domain (visual). It seems to work out nicely. I still haven't figured out how to do feedback with WebGL..

Here's a list anyway:

### Language Features

- [x] Method-Chaining DSL
- [ ] Array Arguments
- [ ] Function Arguments
- [x] Multiple Outputs with Feedback

### Source

- [x] noise
- [x] voronoi
- [x] osc
- [x] shape
- [x] gradient
- [x] src
- [x] solid
- [ ] prev

### Geometry

- [x] rotate
- [x] scale
- [x] pixelate
- [x] repeat
- [x] repeatX
- [x] repeatY
- [x] kaleid
- [x] scroll
- [x] scrollX
- [x] scrollY

### Color

- [x] posterize
- [x] shift
- [x] invert
- [x] contrast
- [x] brightness
- [x] luma
- [x] thresh
- [x] color
- [x] saturate
- [x] hue
- [x] colorama
- [ ] sum
- [x] r
- [x] g
- [x] b
- [x] a

### Blend

- [x] add
- [x] sub
- [x] layer
- [x] blend
- [x] mult
- [x] diff
- [x] mask

### Modulate

- [x] modulateRepeat
- [x] modulateRepeatX
- [x] modulateRepeatY
- [x] modulateKaleid
- [x] modulateScrollX
- [x] modulateScrollY
- [x] modulate
- [x] modulateScale
- [x] modulatePixelate
- [x] modulateRotate
- [x] modulateHue

### External Sources

- [ ] initCam
- [ ] initImage
- [ ] initVideo
- [ ] init
- [ ] initStream
- [ ] initScreen

### Synth Settings

- [x] render
- [ ] update
- [ ] setResolution
- [ ] hush
- [ ] setFunction
- [ ] speed
- [ ] bpm
- [ ] width
- [ ] height
- [ ] time
- [ ] mouse

### Array

- [ ] fast
- [ ] smooth
- [ ] ease
- [ ] offset
- [ ] fit
