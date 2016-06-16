# the-real-animate.sass
**TL;DR** The [animate.css](https://github.com/daneden/animate.css) port to SASS that you're looking for.

- Keyframes are rendered on actual use, no extra imports, no duplicates
- No classes, animations are directly attached to styled element
- Nested SASS maps as data source (JSON-like)

```Sass
@import 'src/the-real-animate'

div
  +animate(fadeIn, 500ms) // default 1s
```
