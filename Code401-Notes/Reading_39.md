# Reading Notes Day 39 --> React 3 & NextJs

## Reading
* [NextJs](https://nextjs.org/learn/basics/create-nextjs-app)
* [React Context for Beginners](https://www.freecodecamp.org/news/react-context-for-beginners/)
<hr/>

* NextJs is a React Framework. 
* To create a Next.js app:
  * The `create-next-app`: bootstraps a Next.js app for you
  * Invoke the use of a template with the `--example` flag
```text
npx create-next-app nextjs-blog --use-npm --example "https://github.com/vercel/next-learn/tree/master/basics/learn-starter"
```
* `cd` into your new directory `nextjs-blog`
  * run `npm run dev`
  * You should then see a "Welcome" page
  * To edit this new page, open `pages/next.js` with your IDE
  * Locate the text under the `<h1>` tag that says "Welcome to" and change it to "Learn"
  * When this new change is saved, the page is updated automatically
* Pages are associated with a route based on the file name. For ex;
  * `pages/index.js` is associated with the `/` route
  * `pages/posts/first-post.js` is associated with the `/posts/first-post.js`
  * To create a new page, create a new file and place the following content:
  ```text
    export default function FirstPost() {
        return <h1> First Post</h1>;
    }
  ```
  * The component can have any name but, ***MUST*** be exported as `default`


## Videos
* [Why I'm using NextJs in 2020](https://www.youtube.com/watch?v=rtgbaKBhdkk)
* [Learn useContext in 13 minutes](https://www.youtube.com/watch?v=5LrDIWkK_Bc)

### Bookmark & Review
*[NextJs Examples](https://github.com/vercel/next.js/tree/canary/examples)
