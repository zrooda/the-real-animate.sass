# the-real-animate.sass
**TL;DR** Unlike the rest of the [Animate.css](https://github.com/daneden/animate.css) ports for SASS, this one isn't shit.

- Keyframes are rendered on actual use, no extra imports, no duplicates
- No useless classes, animations are directly attached to styled element
- Nested SASS maps as data source (JSON-like)

```Sass
div
  +animate(fadeIn, 500ms, ease-in)
```
