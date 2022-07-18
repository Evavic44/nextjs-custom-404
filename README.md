## Customizing the 404 page

To create a custom 404 page create a `404.js` file inside the pages directory of your project. This automatically replaces the default 404 page that comes built-in. This page works the same way as a regular page in a NextJS app, so you can customize it anyhow you want.

## Example Snippet

```js
// pages/404.js
import Head from "next/head";
import Link from "next/link";
import Image from "next/image";
import styles from "../styles/Error.module.css";
import ErrorImage from "../public/error.svg";

export default function Error() {
  return (
    <>
      <Head>
        <title>Oops! Page not found</title>
      </Head>

      <main className={styles.errorContainer}>
        <Image
          className={styles.image}
          src={ErrorImage}
          width={640}
          height={220}
          alt="error image"
        />
        <h1>404</h1>
        <p>Opps! This page is lost in space.</p>

        <Link href="/">
          <a className={styles.btn}>Return home</a>
        </Link>
      </main>
    </>
  );
}
```

<br>
<div align="center">
<img src="public/error.svg" width="400px" alt="error image"> 
</div>
<br><br>

## Getting Started

Follow this guide to run this app locally. <br><br>

This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

```cmd
git clone https://github.com/Evavic44/nextjs-custom-404.git

cd nextjs-custom-404
```

Install the package manager

```bash
npm install
```

Next, run the development server:

```bash
npm run dev
# or
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.
