# Module 2

## What is Gatsby?

### Docs, docs, docs

- [Welcome to Gatsby docs](https://www.gatsbyjs.com/docs/)
- [Cheatsheet](https://www.gatsbyjs.com/docs/cheat-sheet/)
- [Lots of Gatsby resources](https://www.gatsbyjs.com/docs/awesome-gatsby-resources/)

## Pages, Routing and Navigation, Creating Layouts

### [Docs - Pages and layouts](https://www.gatsbyjs.com/docs/recipes/pages-layouts/)

- Project structure [even more on project structure](https://www.gatsbyjs.com/docs/gatsby-project-structure/)
- Creating pages automatically
- Linking between pages [even more on linking pages](https://www.gatsbyjs.com/docs/linking-between-pages/) ([Gatsby API - Link and navigate helper function](https://www.gatsbyjs.com/docs/gatsby-link/))
- Creating a layout component
- Creating pages programmatically with createPage _not covered in this module_

### Notes

- based on React, JSX. Always import React in components/pages
- pages start with lowercase (not reuseable), components start with uppercase (reuseable)
- function declarations are cool, so are arrow functions
- general reminder to destructure props in components - i.e. `({ children })`
- avoid putting assets in /static/, if it's not being rendered by gatsby, gatsby can't see it!
- `ctrl+c` to get out of the npm start (gatsby develop) in terminal
- 404.js page will not render in development but will in production (a link will take you to the custom page in development)
- use the Link component for linking internal pages `<Link to="/">hello</Link>`, clicking on this does a "HTML5 push state" and updates loaded component. Imports like this are called _named imports_ (`{ Link }`). You can also use a navigate helper function in JavaScript instead of a Link component (i.e. imperative use cases)
- `declarative` is _declared stuff_ and `imperative` is _code that happens as a result of something else_
- `ctrl+space` when referencing a component that hasn't been imported will allow you to auto-import!
- `gatsby-browser.js` allows use of [Browser APIs (docs link - scary place)](https://www.gatsbyjs.com/docs/browser-apis/), specifically [wrapPageElement](https://www.gatsbyjs.com/docs/browser-apis/#wrapPageElement) (function/plugin) which sets wrapper components around pages. _Static rendering of pages_
- `gatsby-ssr.js` allows use of [Servering Rendering APIs (docs link - scary place)](https://www.gatsbyjs.com/docs/ssr-apis/), specifically [wrapPageElement](https://www.gatsbyjs.com/docs/ssr-apis/#wrapPageElement). _Server-side rendering of pages_
