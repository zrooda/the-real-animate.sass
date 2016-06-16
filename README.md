# the-real-animate.sass
**TL;DR** The [animate.css](https://github.com/daneden/animate.css) port to SASS that you're looking for.

- Keyframes are rendered automatically on first use, no extra imports needed, no duplicates
- No classes, animations are directly attached to styled element
- Automatic optimization for animated properties
- Nested SASS maps as data source (JSON-like)

```Sass
@import 'src/the-real-animate'

my-widget

  &.coming-in-hot
    +animate(bounceInLeft) // default 1s

  &.going-bye-bye
    +animate(fadeOut, 500ms)
```

```Css
my-widget.coming-in-hot {
  animation-name: bounceInLeft;
  animation-duration: 1000ms;
  animation-fill-mode: both;
  will-change: opacity, transform; }

@keyframes bounceInLeft { ... }

my-widget.going-bye-bye {
  animation-name: fadeOut;
  animation-duration: 500ms;
  animation-fill-mode: both;
  will-change: opacity; }

@keyframes fadeOut { ... }

```
