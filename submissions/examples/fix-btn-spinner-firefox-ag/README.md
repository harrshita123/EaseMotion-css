# Fix Button Loading Spinner Firefox Overflow

## What does this do?
Fixes the loading spinner on `.ease-btn` overflowing the button border-radius in Firefox using `isolation: isolate` and `transform: translateZ(0)`.

## How is it used?
```html
<button class="ease-btn ease-btn--loading" disabled>Loading...</button>
```

## Why is it useful?
Firefox does not reliably clip absolutely-positioned pseudo-elements with `overflow: hidden` + `border-radius`. `isolation: isolate` forces a new stacking context and `transform: translateZ(0)` triggers GPU compositing, both enforcing the clip reliably in Firefox. Fixes #32722.
