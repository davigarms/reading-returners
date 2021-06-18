# Reading Returners

An app to allow a person to search for books and build their own personal reading list.

## Features to be included:

- Search for books by title
- Add a book to your personal reading list
- Ability to remove a book from your own personal reading list
- Mark a book as having been read and leave a review

## App access

**The app can be accessed in the following URL:**

- https://d1grde2885ktde.cloudfront.net

**Other URLs so far:**

To access a book directly, add an id as a parameter, as follows:

- https://d1grde2885ktde.cloudfront.net/[id]

E.g.

- https://d1grde2885ktde.cloudfront.net/60b7ccf5916a6f120fec86e5

## API

**APIs are located in:**

- https://d1grde2885ktde.cloudfront.net/api/

**Books**

`GET`

- https://d1grde2885ktde.cloudfront.net/api/books
- https://d1grde2885ktde.cloudfront.net/api/book/[id]

## Getting Started

This is a [Next.js](https://nextjs.org/ 'Next.js') project bootstrapped with create-next-app.

**First, run the development server:**

```bash
npm run dev
# or
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `pages/index.js`. The page auto-updates as you edit the file.

[API routes](https://nextjs.org/docs/api-routes/introduction) can be accessed on [http://localhost:3000/api/hello](http://localhost:3000/api/). This endpoint can be edited in `pages/api`.

The `pages/api` directory is mapped to `/api/*`. Files in this directory are treated as [API routes](https://nextjs.org/docs/api-routes/introduction) instead of React pages.

## Database

MongoDB and Mongoose are used to store and model application data. A MongoDB URI should be defined in a `.env` file, according to the example provided.

## Styling

[Styled JSX](https://github.com/vercel/styled-jsx 'Styled JSX') is utilised for declarative CSS-in-JS styling.

[Figmagic](https://github.com/mikaelvesavuori/figmagic 'Figmagic') and [Amazon Styles Dictionary](https://amzn.github.io/style-dictionary/ 'Amazon Styles Dictionary') are employed to generate the design tokens to style the app.

Figmagic fetches a document directly from Figma and generates JSON files with design tokens, while Styles Dictionary exports them in a JS module, allowing the application of the defined values consistently across the app.

Please note that Figmagic requires a Figma document including the tokens. A template can be found at:

https://www.figma.com/community/file/821094451476848226/Figmagic-%E2%80%94-Design-System-for-Tokens.

You will also need a Figma API key and the URL id of the document with the tokens. More information can be found in the[ Figmagic documentation](https://github.com/mikaelvesavuori/figmagic ' Figmagic documentation').

The JSON files are located in `figmagic/dictionary` folder.

**To fetch Figma tokens and update the JSON files, run:**

```bash
npm run fetch-figma
# or
yarn fetch-figma
```

Tokens can also be generated directly from the JSON files using Styles Dictionary. You can edit them manually without the use of Figma API.

**To generate the JS module from the JSON files, run:**

```bash
npm run build-dictionary
# or
yarn build-dictionary
```

**You can also run Figmagic and Styles Dictionary in a single command using:**

```bash
npm run build-figma
# or
yarn build-figma
```

## Deployment

[Serverless Next.js Component](https://github.com/serverless-nextjs/serverless-next.js 'Serverless Next.js Component') is used for deployment in AWS using S3, Lamba@Edge and CloudFront, for static pages, APIs and fast content delivery.

The configuration is defined in the `serverless.yml` file, following the example provided.

You should also use this file to add and access environment variables at build time.

**To deploy this project, run:**

```bash
  npm run deploy
  # or
  yarn deploy
```

## Authors

- [@Davi Garms](https://www.github.com/davigarms)
