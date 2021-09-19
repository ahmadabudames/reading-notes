# Dynamic Routes

## Download Starter Code (Optional)

If you’re NOT continuing from the previous lesson, you can download, install, and run the starter code for this lesson below. This sets up a nextjs-blog directory such that it’s identical to the result of the previous lesson.

Again, this is NOT necessary if you’ve just finished the previous lesson.


```
npx create-next-app nextjs-blog --use-npm --example "https://github.com/vercel/next-learn/tree/master/basics/dynamic-routes-starter"
```

## Page Path Depends on External Data


the case where each page path depends on external data. Next.js allows you to statically generate pages with paths that depend on external data. This enables dynamic URLs in Next.js.

![](https://nextjs.org/static/images/learn/dynamic-routes/page-path-external-data.png)


> **How to Statically Generate Pages with Dynamic Routes**

- We want each post to have the path /posts/<id>, where <id> is the name of the markdown file under the top-level posts directory.

- Since we have ssg-ssr.md and pre-rendering.md, we’d like the paths to be /posts/ssg-ssr and /posts/pre-rendering.

## Implement getStaticProps


To do so, open lib/posts.js again and add the following getPostData function at the bottom. It will return the post data based on id:


```
export function getPostData(id) {
  const fullPath = path.join(postsDirectory, `${id}.md`)
  const fileContents = fs.readFileSync(fullPath, 'utf8')

  // Use gray-matter to parse the post metadata section
  const matterResult = matter(fileContents)

  // Combine the data with the id
  return {
    id,
    ...matterResult.data
  }
}
```

## Render Markdown

> **To render markdown content, we’ll use the remark library. First, let’s install it**

```
npm install remark@13 remark-html@13
```

> **Then, open lib/posts.js and add the following imports to the top of the file:**

```
import remark from 'remark'
import html from 'remark-html'
```

## Formatting the Date

To format the date, we’ll use the date-fns library. First, install it:

```
npm install date-fns
```

# Next.js and Vercel


**Vercel** is made by the creators of Next.js and has first-class support for Next.js. When you deploy your Next.js app to Vercel, the following happens by default:

- Pages that use Static Generation and assets (JS, CSS, images, fonts, etc) will automatically be served from the Vercel Edge Network, which is blazingly fast.

- Pages that use Server-Side Rendering and API routes will automatically become isolated Serverless Functions. This allows page rendering and API requests to scale infinitely.

> **Vercel has many more features, such as:**


- **Custom Domains:** Once deployed on Vercel, you can assign a custom domain to your Next.js app. Take a look at our documentation here.

- **Environment Variables:** You can also set environment variables on Vercel. Take a look at our documentation here. You can then use those environment variables in your Next.js app.


- **Automatic HTTPS:** HTTPS is enabled by default (including custom domains) and doesn't require extra configuration. We auto-renew SSL certificates.





