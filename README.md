# the-real-animate.sass
**TL;DR** The [animate.css](https://github.com/daneden/animate.css) port to SASS that you're looking for.

- Keyframes are rendered on actual use, no extra imports, no duplicates
- No classes, animations are directly attached to styled element
- Nested SASS maps as data source (JSON-like)
- Automatic property caching (3<sup>rd</sup> param `$cache`)

```Sass
@import 'src/the-real-animate'

.dialog
  +animate(fadeIn, 500ms)

  &.leaving-us
    +animate(bounceOutLeft) // default 1s
```

```Css
.dialog {
  animation-name: fadeIn;
  animation-duration: 500ms;
  animation-fill-mode: both;
  will-change: opacity; }

@keyframes fadeIn {
  ... }

.dialog.is-leaving-us {
  animation-name: bounceOutLeft;
  animation-duration: 1000ms;
  animation-fill-mode: both;
  will-change: opacity, transform; }

@keyframes bounceOutLeft {
  ... }

```
