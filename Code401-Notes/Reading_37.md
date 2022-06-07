# Reading Notes For Day 37 --> React 1

## Readings / Videos

### ES6 Overview
* [ES6 Syntax & Feature Overview](https://www.taniarascia.com/es6-syntax-and-feature-overview/)

### React
* [React - Hello World](https://reactjs.org/docs/hello-world.html)
* [React - JSX](https://reactjs.org/docs/introducing-jsx.html)
* [React - Rendering Elements](https://reactjs.org/docs/rendering-elements.html)
* [React - Components & Props](https://reactjs.org/docs/components-and-props.html)
* [React - State & Lifecycle](https://reactjs.org/docs/state-and-lifecycle.html)
* [React - Handling Events](https://reactjs.org/docs/handling-events.html)
<hr/>

* JSX is a syntax extension to JavaScript and produces React "elements".
* React separates "concerns" coupled with units called "components" instead of ***technologies***
* For readability, split JSX over multiple lines and wrap it in parentheses to avoid the pitfalls of `automatic 
  semicolon insertion`
* After compilation, JSX expressions become regular JavaScript
<hr/>

### Tailwind CSS
* [Utility First CSS](https://tailwindcss.com/docs/utility-first)
* [Tailwind in 15 Minutes](https://www.youtube.com/watch?v=6zIuAyLZPH0) ***Video not available***
<hr/>

* Tailwind CSS works by scanning all of your HTML files, JS components, and any other templates for class names, 
  generating the corresponding styles and then writing them to a static CSS file.
* Install Tailwind CSS via npm and create your file tailwind.config.js
```text
npm install -D tailwindcss
npx tailwindcss init
```

* Add the `tailwind.config.js` to all of your template files
```text
module.exports = {
  content: ["./src/**/*.{html,js}"],
  theme: {
    extend: {},
  },
  plugins: [],}
```

* Add the `@tailwind` directives for each of Tailwind's layers to the main CSS file
```text
@tailwind base;
@tailwind components;
@tailwind utilities;
```

* Start the Tailwind CLI build process
```text
npx tailwindcss -i ./src/input.css -o ./dist/output.cess --watch
```

* Start using Tailwind in HTML. Add the compiled CSS file to the `<head>` and start using the Tailwind utility 
  classes to style your content.
```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="/dist/output.css" rel="stylesheet">
  <title>Tailwind</title>  
</head>
<body>
  <h1 class="text-3xl font-bold underline">
    Hello world!
  </h1>
</body>
</html>
```

<hr/>

### Next.js
* [Learn Next.js](https://nextjs.org/learn/basics/create-nextjs-app)
* [Why use Next.js?](https://www.youtube.com/watch?v=rtgbaKBhdkk)
<hr/>

* Next.js provides a solution to:
  * Bundling code using like webpack and transforming it using a compiler like Babel.
  * You need to do production optimization such as code splitting.
  * For performance and SEO, you may want to statically pre-render some pages.
  * Needing to write server-side code to connect your React app to your data store.
* Next.js built-in features include:
  * An intuitive page-based routing system (with support for dynamic routes).
  * Pre-rendering, both static generation and server-side rendering are supported on a per-page basis.
  * Automatic code splitting for faster page loads
  * Client-side routing with optimized prefetching
  * Built-in CSS and SaSS support
  * Development environment for fast refresh support
  * API routes to build API endpoint with Serverless functions
  * Fully extendable
* Setup:
  * Make sure you have [Node.js](https://nodejs.org/en/), you can install it from the link
  * Create a Next.js app
```text
npx create-next-app nextjs-blog --use-npm --example "https://github.com/vercel/next-learn/tree/master/basics/learn-starter"
```

  * Run the development server:
    * `cd` into the directory 
    * use the command `npm run dev` - This starts your development server on port `https://localhost:3000`
