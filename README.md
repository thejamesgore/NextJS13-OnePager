# NextJS-13-OnePager

Status: live

A landing page created using NextJS 13 & Framer Motion with the intention of understanding the differences between previous versions of NextJS and the new features implemented in version 13.

Also created using SOLID principles for practice.

Live project can be viewed here - https://next-js-13-one-pager.vercel.app/

### Noticable Differences

1. React components are server side componenets by default. Consequence of this is:

- Apps run faster by default
- Apps are more cachefull
- More predictable in size

Means that if there are any aspects of app that must be rendered client side you can add the `"use client"` directive to the very top of the file. E.g `useEffect` or `useState`. If particular components have dependencies that use client side hooks, still need to add `use client` directive.

2. Directory structure is different providing advantages

This impacts routing as one of the advantages of nextJS is it's ability to use file based routing. In NextJS routes are specified using the directory project structure instead of using something like React Router or React Navigation.

However, in NextJS 13 Each path in the route has a dedicated directory with a page.js file that serves as the content entry point.

Example of the differences below:

Route `/` | `pages/index.js` is now `app/page.js`

Route `/blog` | `pages/blog.js` is now `app/blog/page.js`

Route `/blog/new` | `pages/blog/new.js` is now `app/blog/new/page.js`

The new structure enables us to include additional files in each path directory as well as the page.js for a route, such as

layout.js - A system for the path & its sub-paths.
loading.js - A system for an instant loading state using React.
