# Tesfy Example

[Tesfy](https://tesfy.io/) allows you to create **unlimited** A/B Tests and Feature Flags for **free** using a [web app](https://app.tesfy.io/) or by your self.

This example shows how to integrate [react-tesfy](https://github.com/andresz1/react-tesfy) in Next.js.

To use Tesfy there are only two mandatory things needed. A `userId` and a configuration file known as `datafile`. In the `_app.js` you will notice that those are being get.

The `userId` must uniquely identify a user even if not logged in, for that reason a [uuid](https://en.wikipedia.org/wiki/Universally_unique_identifier) is created and stored in a cookie so the next time a page is requested a new `userId` won't be created, instead the cookie one will be used.

The `datafile` is just a `json` that defines the configuration of the experiments and features avaliable. It must be fetched from Tesfy CDN or from your own servers at least everytime a request is performed, later on this configuration could also be fetched if wanted (e.g. during page transitions).

## Deploy your own

Deploy the example using [Vercel](https://vercel.com):

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/import/project?template=https://github.com/vercel/next.js/tree/canary/examples/with-tesfy)

## How to use

### Using `create-next-app`

Execute [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app) with [npm](https://docs.npmjs.com/cli/init) or [Yarn](https://yarnpkg.com/lang/en/docs/cli/create/) to bootstrap the example:

```bash
npx create-next-app --example with-tesfy with-tesfy-app
# or
yarn create next-app --example with-tesfy with-tesfy-app
```

### Download manually

Download the example:

```bash
curl https://codeload.github.com/vercel/next.js/tar.gz/canary | tar -xz --strip=2 next.js-canary/examples/with-tesfy
cd with-tesfy
```

Install it and run:

```bash
npm install
npm run dev
# or
yarn
yarn dev
```

Deploy it to the cloud with [Vercel](https://vercel.com/import?filter=next.js&utm_source=github&utm_medium=readme&utm_campaign=next-example) ([Documentation](https://nextjs.org/docs/deployment)).
