# hydro

This is an experiment that tries to implement a minimal [hydra](https://github.com/hydra-synth/hydra-synth) in a single self-contained HTML file. The GLSL compiler is implemented with a stripped down version of [@kabelsalat/core](https://github.com/felixroos/kabelsalat/tree/main/packages/core).

## Examples

Many of these examples are taken from the hydra examples to be able to compare both + I've added some of my own

- [dragon tails](https://felixroos.github.io/schattenspiel/hydro/#c2hhcGUoMiwgKCkgPT4gTWF0aC5zaW4odGltZSkvNCsuMjUsIC41KQoucmVwZWF0KDEsNSkKLmNvbG9yKC42LDAsLjgpCi5tb2R1bGF0ZShub2lzZSgyLC4zKSwuMDUpCi8vLm1vZHVsYXRlUm90YXRlKG5vaXNlKDEwLC4zKSwuMikKLnJvdGF0ZSgxLjUsMC4xKQouY29sb3JhbWEoKQouZGlmZihvMCkKLmNvbG9yYW1hKCkKLmJyaWdodG5lc3MoLjQpCi5odWUoKCkgPT4gTWF0aC5zaW4odGltZS84KSkKLmJsZW5kKG8wLC40KQoucG9zdGVyaXplKDQpCi5tb2R1bGF0ZShvc2MoKSwuMDAwNSkKLm91dChvMCk=)
- [nyan worm](https://felixroos.github.io/schattenspiel/hydro/#c2hhcGUoNDAsLjEsLjIpCi5yZXBlYXQoNCwgNCkKLm1vZHVsYXRlKG5vaXNlKDIsLjUpLC4wOCkKLnJvdGF0ZSgwLC4xKQouZGlmZihzcmMobzApLC45OSkKLmNvbG9yYW1hKCkKLmJsZW5kKHNyYyhvMCksLjQpCi5waXhlbGF0ZSgyNTYsMjU2KQoub3V0KG8wKTs=)
- [jelly fountain](https://felixroos.github.io/schattenspiel/hydro/#c3JjKG8wKS5ibGVuZChzcmMobzApKQoubW9kdWxhdGUobm9pc2UoOCksMC4wMDUpCi5ibGVuZChzaGFwZSgzLC4zLC4zKSwwLjAxKQoucm90YXRlKDAuMDEpCi5jb2xvcmFtYSgpCi5vdXQobzAp)
- [comic eye soup](https://felixroos.github.io/schattenspiel/hydro/#b3NjKDIwLC4xLDIpCi5tb2R1bGF0ZShub2lzZSgzKSwwLjI1KQoudGhyZXNoKC40KQoubW9kdWxhdGUob3NjKDEwKS5yb3RhdGUoTWF0aC5QSS8yKSwuNykKLm1vZHVsYXRlS2FsZWlkKG5vaXNlKDQpKQoub3V0KCk=)
- [ojack demo patch](https://felixroos.github.io/schattenspiel/hydro/#Ly8gbGljZW5zZWQgd2l0aCBDQyBCWS1OQy1TQSA0LjAgaHR0cHM6Ly9jcmVhdGl2ZWNvbW1vbnMub3JnL2xpY2Vuc2VzL2J5LW5jLXNhLzQuMC8KLy8gYnkgT2xpdmlhIEphY2sKLy8gaHR0cHM6Ly9vamFjay5naXRodWIuaW8KCm9zYygxMDAsIDAuMDEsIDEuNCkKICAucm90YXRlKDAsIDAuMSkKICAubXVsdChvc2MoMTAsIDAuMSkubW9kdWxhdGUob3NjKDEwKS5yb3RhdGUoMCwgLTAuMSksIDEpKQogIC5jb2xvcigyLjgzLCAwLjkxLCAwLjM5KQogIC5vdXQoKTs=)
- [Puertas III (almost)](https://felixroos.github.io/schattenspiel/hydro/#Ly8gbGljZW5zZWQgd2l0aCBDQyBCWS1OQy1TQSA0LjAgaHR0cHM6Ly9jcmVhdGl2ZWNvbW1vbnMub3JnL2xpY2Vuc2VzL2J5LW5jLXNhLzQuMC8KLy8gUHVlcnRhcyBJSUkKLy8gcG9yIENlbGVzdGUgQmV0YW5jdXIKLy8gaHR0cHM6Ly9naXRodWIuY29tL2Vzc3RlYmFuCiAKb3NjKDQwLDAuMiwxKQogIC5tb2R1bGF0ZVNjYWxlKG9zYyg0MCwwLDEpLmthbGVpZCg4KSkKICAucmVwZWF0KDIsNCkKICAubW9kdWxhdGUoc3JjKG8wKSwwLjA1KQogIC5tb2R1bGF0ZUthbGVpZChzaGFwZSg0LDAuMSwxKSkKICAub3V0KG8wKQ==)
- [feedback example](https://felixroos.github.io/schattenspiel/hydro/#c3JjKG8wKQoubW9kdWxhdGUobm9pc2UoOCksMC4wMDUpCi5ibGVuZChzaGFwZSg0KSwwLjAxKQoucm90YXRlKDAuMDEpCi5vdXQobzAp)
- [trypophobia](https://felixroos.github.io/schattenspiel/hydro/#Ly8gbGljZW5zZWQgd2l0aCBDQyBCWS1OQy1TQSA0LjAgaHR0cHM6Ly9jcmVhdGl2ZWNvbW1vbnMub3JnL2xpY2Vuc2VzL2J5LW5jLXNhLzQuMC8KLy9yYW5kb20gdHJ5cG9waG9iaWEgLSBjaGFuZ2VzIGV2ZXJ5dGltZSB5b3UgbG9hZCBpdCEKLy9ieSBSaXRjaHNlCi8vIG1vZGlmaWVkIGJ5IGZyb29zIHRvIHdvcmsgaW4gaHlkcm8KLy9pbnN0YWdyYW0uY29tL3JpdGNoc2UKIApmdW5jdGlvbiByKG1pbj0wLG1heD0xKSB7IHJldHVybiBNYXRoLnJhbmRvbSgpKihtYXgtbWluKSttaW47IH0KIApzb2xpZCgxLDEsMSkKLmRpZmYoIHNoYXBlKCA0LCByKDAuNiwwLjkzKSwgLjA5KS5yZXBlYXQoMjAsMTApICkKLm1vZHVsYXRlU2NhbGUob3NjKDgpLnJvdGF0ZShyKC0uNSwuNSkpLC41MikKLmFkZChzcmMobzApLnNjYWxlKDAuOTY1KS5yb3RhdGUoLjAxMiooTWF0aC5yb3VuZChyKC0yLDEpKSkpCi5jb2xvcihyKCkscigpLHIoKSkKLm1vZHVsYXRlUm90YXRlKHNyYyhvMCkscigwLDAuNSkpCi5icmlnaHRuZXNzKC4xNSkKLC43KQoub3V0KCkK)
- [floaty shards](https://felixroos.github.io/schattenspiel/hydro/#CnNyYyhvMCkKLmJsZW5kKHNoYXBlKDMpLnNjYWxlKDIpLmNvbG9yKDAsLjksLjUpKQoubW9kdWxhdGUodm9yb25vaSgzKSwuNSkKLm1vZHVsYXRlU2NhbGUob3NjKDEwKSwuMSkKLm1vZHVsYXRlUm90YXRlKG9zYygxMCksLjEpCi8vLmNvbG9yYW1hKCkKLm91dChvMCk=)
- [Nelson Vera (not quite)](https://felixroos.github.io/schattenspiel/hydro/#Ly8gbGljZW5zZWQgd2l0aCBDQyBCWS1OQy1TQSA0LjAgaHR0cHM6Ly9jcmVhdGl2ZWNvbW1vbnMub3JnL2xpY2Vuc2VzL2J5LW5jLXNhLzQuMC8KLy8gYnkgTmVsc29uIFZlcmEKLy8gdHdpdHRlcjogQG5lbF9zb25vbG9naWEKCm9zYyg4LC0wLjUsIDEpLmNvbG9yKC0xLjUsIC0xLjUsIC0xLjUpLmJsZW5kKHNyYyhvMCkpLnJvdGF0ZSgtMC41LCAtMC41KS5tb2R1bGF0ZShzaGFwZSg0KS5yb3RhdGUoMC41LCAwLjUpLnNjYWxlKDIpLnJlcGVhdFgoMiwgMikKLy8ubW9kdWxhdGUoc3JjKG8wKSwgbW91c2VYLCAwLjAwMDAwNSkKLnJlcGVhdFkoMiwgMikpLm91dChvMCk=)
- [Sumet](https://felixroos.github.io/schattenspiel/hydro/#Ly8gbGljZW5zZWQgd2l0aCBDQyBCWS1OQy1TQSA0LjAgaHR0cHM6Ly9jcmVhdGl2ZWNvbW1vbnMub3JnL2xpY2Vuc2VzL2J5LW5jLXNhLzQuMC8KLy8gU3VtZXQKLy8gYnkgUmFuZ2dhIFB1cm5hbWEgQWppCi8vIGh0dHBzOi8vcmFuZ2dhcHVybmFtYWFqaTEud2l4c2l0ZS5jb20vcG9ydGZvbGlvCgpvc2MoMC41LDEuMjUpLm11bHQoc2hhcGUoMSwwLjA5KS5yb3RhdGUoMS41KSkKICAuZGlmZihncmFkaWVudCgpKQogIC5hZGQoc2hhcGUoMiwyKS5ibGVuZChncmFkaWVudCgxKSkpCiAgLm1vZHVsYXRlKG5vaXNlKCkKICAgICAgICAgICAgLm1vZHVsYXRlKG5vaXNlKCkuc2Nyb2xsWSgxLDAuMDYyNSkpKQogIC5ibGVuZChzcmMobzApKQogIC5jb2xvcigxLC0wLjUsLTAuNzUpCiAgLm91dCgpCg==)
- [Dreamy Diamond](https://felixroos.github.io/schattenspiel/hydro/#Ly8gbGljZW5zZWQgd2l0aCBDQyBCWS1OQy1TQSA0LjAgaHR0cHM6Ly9jcmVhdGl2ZWNvbW1vbnMub3JnL2xpY2Vuc2VzL2J5LW5jLXNhLzQuMC8KLy8gRHJlYW15IERpYW1vbmQKLy8gYnkgUmFuZ2dhIFB1cm5hbWEgQWppCi8vIGh0dHBzOi8vcmFuZ2dhcHVybmFtYWFqaTEud2l4c2l0ZS5jb20vcG9ydGZvbGlvCgpvc2MoNywtMC4xMjUpLm1vZHVsYXRlKHZvcm9ub2koMSkpLmRpZmYodm9yb25vaSgxKS5tdWx0KGdyYWRpZW50KC0xKS5sdW1hKDAuMTI1KSkpCiAgLmx1bWEoMC4xMjUpCiAgLmFkZChzaGFwZSg3LCAwLjUpCiAgICAgICAubXVsdCh2b3Jvbm9pKDEwLDIpLmJsZW5kKHNyYyhvMCkpLmRpZmYoZ3JhZGllbnQoMSkpLm1vZHVsYXRlKHZvcm9ub2koKSkpKQogIC5zY3JvbGxZKC0wLjEpCiAgLnNjcm9sbFgoMC4xMjUpCiAgLmJsZW5kKHNyYyhvMCkpCiAgLmJsZW5kKHNyYyhvMCkpCiAgLm91dCgpCgo=)
- [Zach Krall Disks](https://felixroos.github.io/schattenspiel/hydro/#Ly8gbGljZW5zZWQgd2l0aCBDQyBCWS1OQy1TQSA0LjAgaHR0cHM6Ly9jcmVhdGl2ZWNvbW1vbnMub3JnL2xpY2Vuc2VzL2J5LW5jLXNhLzQuMC8KLy8gYnkgWmFjaCBLcmFsbAovLyBodHRwOi8vemFjaGtyYWxsLm9ubGluZS8KCm9zYyggMjE1LCAwLjEsIDIgKQoubW9kdWxhdGUoCiAgb3NjKCAyLCAtMC4zLCAxMDAgKQogIC5yb3RhdGUoMTUpCikKLm11bHQoCiAgb3NjKCAyMTUsIC0wLjEsIDIpCiAgLnBpeGVsYXRlKCA1MCwgNTAgKQopCi5jb2xvciggMC45LCAwLjAsIDAuOSApCi5tb2R1bGF0ZSgKICBvc2MoIDYsIC0wLjEgKQogIC5yb3RhdGUoIDkgKQopCi5hZGQoCiAgb3NjKCAxMCwgLTAuOSwgOTAwICkKICAuY29sb3IoMSwwLDEpCikKLm11bHQoCiAgc2hhcGUoOTAwLCAwLjIsIDEpCiAgLmx1bWEoKQogIC5yZXBlYXRYKDIpCiAgLnJlcGVhdFkoMikKICAuY29sb3JhbWEoMTApCikKLm1vZHVsYXRlKAogIG9zYyggOSwgLTAuMywgOTAwICkKICAucm90YXRlKCA2ICkKKQouYWRkKAogIG9zYyg0LCAxLCA5MCkKICAuY29sb3IoMC4yLDAsMSkKKQoub3V0KCkKCg==)
- [Eye in the Sky](https://felixroos.github.io/schattenspiel/hydro/#Ly8gbGljZW5zZWQgd2l0aCBDQyBCWS1OQy1TQSA0LjAgaHR0cHM6Ly9jcmVhdGl2ZWNvbW1vbnMub3JnL2xpY2Vuc2VzL2J5LW5jLXNhLzQuMC8KLy8gZWVfMSAuIEVZRSBJTiBUSEUgU0tZCi8vZXhhbXBsZSBvZiBtYXNrIGFuZCBmdW5jdGlvbiBtb2R1bGF0aW9uCi8vIGVfZSAvLyBAZWVyaWVfZWFyCm5vaXNlKDE4KQogIC5jb2xvcmFtYSgxKQogIC5wb3N0ZXJpemUoMikKICAua2FsZWlkKDUwKQogIC5tYXNrKAogICAgc2hhcGUoMjUsIDAuMjUpLm1vZHVsYXRlU2NhbGUoCiAgICAgIG5vaXNlKDQwMC41LCAwLjUpCiAgICApCiAgKQogIC5tYXNrKHNoYXBlKDQwMCwgMSwgMi4xMjUpKQogIC5tb2R1bGF0ZVNjYWxlKG9zYyg2LCAwLjEyNSwgMC4wNSkua2FsZWlkKDUwKSkKICAubXVsdChvc2MoMjAsIDAuMDUsIDIuNCkua2FsZWlkKDUwKSwgMC4yNSkKICAuc2NhbGUoMS43NSwgMC42NSwgMC41KQogIC5tb2R1bGF0ZShub2lzZSgwLjUpKQogIC5zYXR1cmF0ZSg2KQogIC5wb3N0ZXJpemUoNCwgMC4yKQogIC5zY2FsZSgxLjUpCiAgLm91dCgpOwoK)
- [by Débora Falleiros Gonzales](https://felixroos.github.io/schattenspiel/hydro/#Ly8gbGljZW5zZWQgd2l0aCBDQyBCWS1OQy1TQSA0LjAgaHR0cHM6Ly9jcmVhdGl2ZWNvbW1vbnMub3JnL2xpY2Vuc2VzL2J5LW5jLXNhLzQuMC8KLy8gYnkgROlib3JhIEZhbGxlaXJvcyBHb256YWxlcwovLyBodHRwczovL3d3dy5nb256YWxlc2RlYm9yYS5jb20vCgpvc2MoNSkuYWRkKG5vaXNlKDUsIDIpKS5jb2xvcigwLCAwLCAzKS5jb2xvcmFtYSgwLjQpLm91dCgpCg==)
- [trying to get closer by Ritchse](https://felixroos.github.io/schattenspiel/hydro/#Ly8gbGljZW5zZWQgd2l0aCBDQyBCWS1OQy1TQSA0LjAgaHR0cHM6Ly9jcmVhdGl2ZWNvbW1vbnMub3JnL2xpY2Vuc2VzL2J5LW5jLXNhLzQuMC8KLy90cnlpbmcgdG8gZ2V0IGNsb3NlcgovL2J5IFJpdGNoc2UKLy9pbnN0YWdyYW0uY29tL3JpdGNoc2UKIApvc2MoNjAsLTAuMDE1LDAuMykuZGlmZihvc2MoNjAsMC4wOCkucm90YXRlKE1hdGguUEkvMikpCgkubW9kdWxhdGVTY2FsZShub2lzZSgzLjUsMC4yNSkubW9kdWxhdGVTY2FsZShvc2MoMTUpLnJvdGF0ZSgwLC4yKSksMC42KQoJLmNvbG9yKDEsMC41LDAuNCkuY29udHJhc3QoMS40KQoJLmFkZChzcmMobzApLm1vZHVsYXRlKHNyYyhvMCksLjA0KSwuNikKCS5pbnZlcnQoKS5icmlnaHRuZXNzKDAuMSkuY29udHJhc3QoMS4yKQoJLm1vZHVsYXRlU2NhbGUob3NjKDIpLC0wLjIpCiAgLm91dCgpCg==)
- [CNSD](https://felixroos.github.io/schattenspiel/hydro/#Ly8gbGljZW5zZWQgd2l0aCBDQyBCWS1OQy1TQSA0LjAgaHR0cHM6Ly9jcmVhdGl2ZWNvbW1vbnMub3JnL2xpY2Vuc2VzL2J5LW5jLXNhLzQuMC8KLy9DTkRTRAovL2h0dHA6Ly9tYWxpdHppbmNvcnRlcy5uZXQvCi8vYW1lYmEKCm9zYygxNSwgMC4wMSwgMC4xKS5tdWx0KG9zYygxLCAtMC4xKS5tb2R1bGF0ZShvc2MoMikucm90YXRlKDQsMSksIDIwKSkKLmNvbG9yKDAsMi40LDUpCi5zYXR1cmF0ZSgwLjQpCi5sdW1hKDEsMC4xLCA2KQouc2NhbGUoMC43LCAwLjcpCi5kaWZmKHNyYyhvMCkpLy8gbzAKLm91dChvMCkvLyBvMQo=)
- [moire](https://felixroos.github.io/schattenspiel/hydro/#Ly8gbGljZW5zZWQgd2l0aCBDQyBCWS1OQy1TQSA0LjAgaHR0cHM6Ly9jcmVhdGl2ZWNvbW1vbnMub3JnL2xpY2Vuc2VzL2J5LW5jLXNhLzQuMC8KLy8gbW9pcmUKLy8gYnkgT2xpdmlhIEphY2sKLy8gdHdpdHRlcjogQF9vamFja18KCnBhdHRlcm4gPSAoKSA9PiBvc2MoMjAwLCAwKS5rYWxlaWQoMjAwKS5zY2FsZSgxLCAwLjQpCi8vCnBhdHRlcm4oKQogIC5zY3JvbGxYKDAuMSwgMC4wMSkKICAubXVsdChwYXR0ZXJuKCkpCiAgLm91dCgpCg==)

## Shuffle

You can open the browser console and enter `shuffle()` to load a random hydra example.

## Completeness

Not all hydra functions / features work, and probably never will, as this is mostly an experiment out of curiosity.
The initial goal was to see if @kabelsalat/core could be used to compile an existing DSL that also targets another language (GLSL) + another domain (visual). It seems to work out nicely for the moment.

Here's a feature list anyway:

### Language Features

- [x] Method-Chaining DSL
- [x] Array Arguments
- [x] Function Arguments
- [x] Multiple Outputs with Feedback

### Source

- [x] o0...o3
- [ ] s0...s3
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
- [x] width
- [x] height
- [x] time
- [x] mouse

### Array

- [ ] fast
- [ ] smooth
- [ ] ease
- [ ] offset
- [ ] fit
