# Example app with [babel-macros](https://github.com/kentcdodds/babel-macros)

## How to use

### Using `create-next-app`

Execute [`create-next-app`](https://github.com/segmentio/create-next-app) with [Yarn](https://yarnpkg.com/lang/en/docs/cli/create/) or [npx](https://github.com/zkat/npx#readme) to bootstrap the example:

```bash
npx create-next-app --example with-babel-macros with-babel-macros-app
# or
yarn create next-app --example with-babel-macros with-babel-macros-app
```

### Download manually

Download the example:

```bash
curl https://codeload.github.com/zeit/next.js/tar.gz/canary | tar -xz --strip=2 next.js-canary/examples/with-babel-macros
cd with-babel-macros
```

Install it and run:

```bash
npm install
npm run dev
# or
yarn
yarn dev
```

Deploy it to the cloud with [now](https://zeit.co/now) ([download](https://zeit.co/download))

```bash
now
```

## The idea behind the example

This example features how to configure and use [`babel-macros`](https://github.com/kentcdodds/babel-macros) which allows you
to easily add babel plugins which export themselves as a macro without needing
to configure them.

You'll notice the configuration in `.babelrc` includes the `babel-macros`
plugin, then we can use the `preval.macro` in `pages/index.js` to pre-evaluate
code at build-time. `preval.macro` is effectively transforming our code, but
we didn't have to configure it to make that happen!

Specifically what we're doing is we're prevaling the username of the user who
ran the build.
