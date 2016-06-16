# the-real-animate.sass
**TL;DR** The [animate.css](https://github.com/daneden/animate.css) port to SASS that you're looking for.

- Keyframes are rendered on first use, no extra imports needed, no duplicates
- No classes, animations are directly attached to styled element
- Nested SASS maps as data source (JSON-like)
- Automatic property caching (3<sup>rd</sup> param `$cache`)

```Sass
@import 'src/the-real-animate'

my-widget

  &.coming-in-hot
    +animate(bounceInLeft) // default 1s, caching on

  &.going-bye-bye
    +animate(fadeOut, 500ms, false)
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
  animation-fill-mode: both; }

@keyframes fadeOut { ... }

```
