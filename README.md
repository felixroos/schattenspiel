# schattenspiel

schattenspiel (= german for "shadow play") is a minimal, single-html-file shader live coding editor using the same format as shadertoy.

You can use it here: <https://felixroos.github.io/schattenspiel/>

## Usage

Like shadertoy, your code is expected to define `mainImage` like this:

```js
void mainImage( out vec4 fragColor, in vec2 fragCoord )
{
    // Normalized pixel coordinates (from 0 to 1)
    vec2 uv = fragCoord/iResolution.xy;
    // Time varying pixel color
    vec3 col = 0.5 + 0.5*cos(iTime+uv.xyx+vec3(0,2,4));
    // Output to screen
    fragColor = vec4(col,1.0);
}
```

- When you make a change, you can update the shader by pressing `ctrl+Enter`.
- The URL will reflect your latest code change, so you can share the URL / refresh the page

Many shadertoy examples work here, just note that only a subset of uniforms is defined:

### Uniforms

The following uniforms are defined from the outside:

- `uniform vec2 iResolution`: width and height of the canvas
- `uniform float iTime`: Elapsed time in seconds
- `uniform vec2 iMouse`: X,Y Mouse position

## Examples

## Credits

- [WebGLFundamentals shadertoy example](https://webglfundamentals.org/webgl/lessons/webgl-shadertoy.html)
- [shadertoy](https://www.shadertoy.com/)
