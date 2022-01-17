### Understanding Responsive Design ###

Check 'emmet' for quick shortcuts to type html
https://www.youtube.com/watch?v=V8vizNQKtx0

Breakpoints mean that the design will break into a different layout when the breakpoint is hit.This video explains it well - https://www.youtube.com/watch?v=iC8cxluBSB0&list=PLbGui_ZYuhij_HswuaGK-ABs1vfC5HTKn&index=6



Example set of common media queries based on minimum viewport widths
```
// X-Small devices (portrait phones, less than 576px)
// No media query for `xs` since this is the default in Bootstrap

// Small devices (landscape phones, 576px and up)
@media (min-width: 576px) { ... }

// Medium devices (tablets, 768px and up)
@media (min-width: 768px) { ... }

// Large devices (desktops, 992px and up)
@media (min-width: 992px) { ... }

// X-Large devices (large desktops, 1200px and up)
@media (min-width: 1200px) { ... }

// XX-Large devices (larger desktops, 1400px and up)
@media (min-width: 1400px) { ... }
```

#### More Examples

 min-width media queries(up)
```
@include media-breakpoint-up(sm) { ... }
@media (min-width: 576px) { ... }
```

max-width media query(down)
```
@include media-breakpoint-down(md) { ... }
@media (max-width: 767.98px) { ... }
```

single breakpoint(only)
```
@include media-breakpoint-only(md) { ... }
will result in
@media (min-width: 768px) and (max-width: 991.98px) { ... }
```

Between breakpoints
```
@include media-breakpoint-between(md, xl) { ... }
@media (min-width: 768px) and (max-width: 1199.98px) { ... }
```
