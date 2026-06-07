The `svg` element is used to draw vector graphics directly inside your HTML. Unlike a PNG or JPG, an SVG is made of math — paths, points, and curves — so it scales perfectly at any size without ever going blurry.

Below is the heart icon we are working with. Try changing `fill="red"` to `fill="crimson"` or `fill="pink"` to see the color update instantly.

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <title>Heart Icon</title>
  </head>
  <body>
    <svg width="24" height="24" viewBox="0 0 24 24" fill="red">
      <path
        d="M12 21s-6-4.35-9.33-8.22C-.5 7.39 3.24 1 8.4 4.28 10.08 5.32 12 7.5 12 7.5s1.92-2.18 3.6-3.22C20.76 1 24.5 7.39 21.33 12.78 18 16.65 12 21 12 21z"
      ></path>
    </svg>
  </body>
</html>
```

Let's break down each key part of this SVG:

---

### The `svg` element

```html
<svg width="24" height="24" viewBox="0 0 24 24" fill="red">
```

The `svg` element is the container for the whole drawing — just like the `<audio>` element is the container for a sound player. Everything you want to draw goes *inside* it.

It has four attributes here:

- **`width="24"`** — sets the actual rendered width on the page in pixels.
- **`height="24"`** — sets the actual rendered height on the page in pixels.
- **`fill="red"`** — sets the default fill color for all shapes drawn inside. Because it is set on the `svg` element, every shape inside inherits this color unless it overrides it.

---

### The `viewBox` attribute

```html
viewBox="0 0 24 24"
```

`viewBox` is one of the most important SVG concepts. It defines the **internal coordinate system** — the imaginary grid the artist used when drawing the shapes.

The four numbers mean:

| Value | Meaning |
|-------|---------|
| `0`   | Start the grid at x = 0 (left edge) |
| `0`   | Start the grid at y = 0 (top edge) |
| `24`  | The grid is 24 units wide |
| `24`  | The grid is 24 units tall |

Think of it like a camera zoom. The artist drew the heart on a 24 × 24 grid. The `width` and `height` attributes then stretch or shrink that grid to fit on your page. You could change `width` to `200` and the heart would scale up perfectly — because the `viewBox` tells the browser how to map the internal coordinates to the screen.

---

### The `path` element

```html
<path d="M12 21s-6-4.35 ..."></path>
```

The `path` element is the most powerful shape in SVG. It can draw *any* shape — curves, straight lines, arcs — all through a single attribute called `d`.

---

### The `d` attribute

```html
d="M12 21s-6-4.35-9.33-8.22C-.5 7.39 3.24 1 8.4 4.28 10.08 5.32 12 7.5 12 7.5s1.92-2.18 3.6-3.22C20.76 1 24.5 7.39 21.33 12.78 18 16.65 12 21 12 21z"
```

The `d` attribute contains a **mini drawing language** made of letters and numbers. Each letter is a command that tells the browser what to draw next. Here are the commands used in this heart:

| Command | Full Name | What it does |
|---------|-----------|--------------|
| `M`     | **Move To** | Picks up the pen and moves to a coordinate without drawing. `M12 21` means "start at x=12, y=21" — the bottom tip of the heart. |
| `s`     | **Smooth Cubic Bézier (relative)** | Draws a smooth curve relative to the current position. The lowercase `s` means the coordinates are *relative* — measured from where the pen currently is, not from the origin. |
| `C`     | **Cubic Bézier Curve (absolute)** | Draws a smooth S-shaped curve using two control points and an end point. Uppercase `C` means the coordinates are *absolute* — measured from the top-left corner (x=0, y=0). |
| `z`     | **Close Path** | Draws a straight line back to the starting point (`M12 21`) and closes the shape, completing the outline. |

**Relative vs Absolute** — the key rule is simple:
- **Uppercase** letter = absolute coordinates (from the top-left of the viewBox)
- **Lowercase** letter = relative coordinates (from where the pen currently sits)

---

### Putting it all together

Here is how the heart is drawn step by step:

1. `M12 21` — the pen starts at the bottom tip of the heart.
2. The `s` and `C` commands draw the two curved lobes upward — one going left, one going right — using Bézier curves to create the smooth heart shape.
3. `z` — the path closes back at the starting point, sealing the shape.
4. Because `fill="red"` is set on the `svg`, the closed shape is automatically filled in with red.

---

### Changing the heart

Here are some things you can try:

- Change `fill="red"` on the `svg` to `fill="crimson"`, `fill="hotpink"`, or any CSS color.
- Change `width="24" height="24"` to `width="100" height="100"` — the heart scales up perfectly with no blur because it is a vector.
- Add `stroke="black" stroke-width="1"` to the `<path>` to add an outline around the heart.

SVG paths look complex at first, but they follow a simple pattern: **move the pen, draw curves, close the shape, and fill it in**. Once you understand `viewBox`, `path`, and `d`, you can read and modify almost any SVG icon you find.