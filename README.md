# NextJS-13-OnePager

A landing page created using NextJS 13 & Framer Motion with the intetion of understanding the differences between previous versions of NextJS and the new features implemented in version 13.

Also created using SOLID principles for practice.

Live project can be viewed here - https://next-js-13-one-pager.vercel.app/

### Noticable Differences

React components are server side componenets by default. Consequence of this is:
- Apps run faster by default
- Apps are more cachefull
- More predictable in size

Means that if there are any aspects of app that must be rendered client side you can add the `"use client"` directive to the very top of the file. E.g `useEffect` or `useState`. If particular components have dependencies that use client side hooks, still need to add `use client` directive.