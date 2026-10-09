# Interactive Fractal

A full-screen fractal explorer in a single HTML file (WebGL 2, no dependencies).

**Live:** https://ktnkv.github.io/interactive-fractal/

Type any complex formula `z → f(z)` and it is compiled into a shader on the fly.

- **Move the mouse** — morphs the fractal (changes `c`); hold **Shift** for fine control
- **Drag** — pan, **scroll / pinch** — zoom
- **Click** or **Space** — freeze `c`, **R** — reset the view
- On touch screens: one finger morphs, two fingers pan and zoom

## Formula syntax

| | |
|---|---|
| `z` | the iterated value (starts at the pixel) |
| `c` | the parameter controlled by the mouse |
| `p` | the pixel itself, e.g. `z^2 + p` is the Mandelbrot set |
| `t` | time in seconds, for animated formulas |
| `i`, `pi`, `e` | constants |
| `+ - * / ^` | arithmetic, implicit multiplication (`3z^2`) |
| functions | `sin cos tan sinh cosh tanh exp log sqrt abs arg conj re im fold` |

`fold(z)` is `|re z| + i|im z|` (the Burning Ship trick).

Points that escape are coloured by a smooth iteration count, points that converge
(Newton-style formulas) by the root they reach.
