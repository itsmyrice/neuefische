# CSS Responsive

---
## Mobile First Design

When authoring CSS, it's a very helpful convention to first define all your mobile styles, and then
add media queries to adjust the styles for larger screens. It's easier to reason about, and it
results in a simpler CSS structure. Your code will be more similar to the way other people write
CSS.

When designing, it makes sense to begin designing mobile first, because most users are on mobile
devices. This also helps you to focus on the most important information (you have less space), and
to structure it in a way that makes sense for mobile users.

---

## Responsive Units

Responsive units are units that are relative to the size of the viewport, the current font size, or
the size of their parent element.

- `vh` (viewport height): 1vh is 1% of the viewport height
- `vw` (viewport width): 1vw is 1% of the viewport width
- `em`: 1em is the font size of the current element
- `rem`: 1rem is the font size of the root element
- `%`: is relative to the related property of the parent or current element - every property has
  it's own rules what it is relative to:
  - `width: 1%` is set relative to the parents element width
  - `padding-top: 10%` means 10% of the parents height
  - `font-size: 50%` means half as big as the parent font-size
  - `transform: translateX(50%)` means translate on the x axis by 50% of the current elements width
- `calc()`: allows you to combine multiple units and do math
  - e.g. `calc(100vh - 100px)`
  - or `calc(50% - 10rem)`

---

## Media Queries

Media queries allow you to write CSS for specific media types, screen sizes, orientations and more.

---

### Media Types

You can target a specific media type with the `screen` and `print` media types.

### Screen Size

You can target specific screen sizes with the `min-width` and `max-width` media features.

### Orientation

You can target specific orientations with the `orientation` media feature.

### Pointer

You can target specific pointer types with the `any-pointer` media feature.

### Device Pixel Ratio (Pixel Density)

You can target specific device pixel ratios with the `device-pixel-ratio` media feature.

### Color Scheme

You can target specific color schemes with the `prefers-color-scheme` media feature.

### Reduced Motion

You can target users who are sensitive to animations and movement (and set up their system
accordingly) with the `prefers-reduced-motion` media feature.

### High Contrast

You can target users who prefer a higher contrast with the `prefers-contrast` media feature.

### Other Media Features

There are also media features for other (accessibility) features, like
[`inverted-colors`](https://developer.mozilla.org/en-US/docs/Web/CSS/@media/inverted-colors). The
list of all media features is always growing. Check out
[the full list](https://developer.mozilla.org/en-US/docs/Web/CSS/@media#media_features) on mdn.

### Combining Media Features

You can combine multiple media features with `and`.

### Testing for multiple Media Features

You can use a comma-separated list to apply styles when the user's device matches any one of various
media types using `,`

### Simulating Media Features

You can simulate media features in the browser devtools. For example, you can change your screen
size in the devtools by clicking the device icon in the top left corner of the devtools.

### Common Breakpoints

When using `min-width` media queries it can be helpful to use common breakpoints.

- no media query (default): extra-small, xs, mobile
- `(min-width: 600px)`: small, sm, large mobile
- `(min-width: 900px)`: medium, md, tablet
- `(min-width: 1200px)`: large, lg, desktop
- `(min-width: 1536px)`: extra-large, xl, large desktop

🪄 **Pro Tip**: You can use media queries to redefine the values of CSS custom properties. This way
you can use the property as a value that dynamically changes based on the media query.

---

## Showing different images based on media queries

You can use media queries to show different images based on the screen size.

The html `picture` element allows you to define multiple `source` elements for an image. The browser
will choose the _first_ source that matches the given media query. If no `source` element matches,
the browser will use the `img` element as a fallback.

The `img` element is required, so that there is always a fallback.
