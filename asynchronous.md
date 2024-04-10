# Asynchronous JavaScript and APIs

## Promises
```js
const myData = getData() // if this is refactored to return a Promise...

myData.then(function(data){ // .then() tells it to wait until the promise is resolved
  const pieceOfData = data['whatever'] // and THEN run the function inside
})
```
> A callback function is a function passed into another function as an argument, which is then invoked inside the outer function to complete some kind of routine or action.

```js
const fetchData = () => {
    fetch('https://api.weatherapi.com/v1/current.json?key=' + key + '&q=' + city)
    .then(function(response) {
        return response.json();
    })
    .then(function(response) {
        console.log(response.location);
    })
    .catch(function(err) {
        console.log('Error');
    });

}

fetchData();
```

Example sending a `POST` request to the GraphQL Shopify [Storefront API](https://shopify.dev/docs/api/storefront) endpoint:

```sh
# create the app
mkdir app-name && cd app-name
npm init -y
echo > server.js 
echo > .gitignore 
echo > .env 
echo > README.md
npm install express
npm i dotenv
npm i node-fetch@2
```

The `server.js` file:

```js
require('dotenv').config();
const fetch = require('node-fetch');
const { SHOPIFY_STORE_URL, SHOPIFY_ACCESS_TOKEN } = process.env;

const fetchProducts = () => {
    const query = `
      {
        products(first: 5) {
          edges {
            node {
              id
              title
              handle
              description
              variants(first: 1) {
                edges {
                  node {
                    id
                    title
                  }
                }
              }
            }
          }
        }
      }
    `;
    fetch(`https://${SHOPIFY_STORE_URL}/api/2024-04/graphql.json`, {
        method: 'POST',
        headers: {
          'Content-Type': 'application/json',
          'X-Shopify-Storefront-Access-Token': SHOPIFY_ACCESS_TOKEN,
        },
        body: JSON.stringify({ query }),
      })
    .then(function(response) {
        return response.json();
    })
    .then(function(response) {
        console.log(response);
    })
    .catch(function(err) {
        console.log('Error');
    });

};

fetchProducts();
```

//OR//

```js
require('dotenv').config();
const express = require('express');
const fetch = require('node-fetch');
const app = express();
const port = 3000;

const { SHOPIFY_STORE_URL, SHOPIFY_ACCESS_TOKEN } = process.env;

app.get('/products', async (req, res) => {
  try {
    const graphqlEndpoint = `https://${SHOPIFY_STORE_URL}/api/2024-04/graphql.json`;
    const query = `
      {
        products(first: 5) {
          edges {
            node {
              id
              title
              handle
              description
              variants(first: 1) {
                edges {
                  node {
                    id
                    title
                  }
                }
              }
            }
          }
        }
      }
    `;

    const response = await fetch(graphqlEndpoint, {
      method: 'POST',
      headers: {
        'Content-Type': 'application/json',
        'X-Shopify-Storefront-Access-Token': SHOPIFY_ACCESS_TOKEN,
      },
      body: JSON.stringify({ query }),
    });

    const data = await response.json();
    res.json(data);
  } catch (error) {
    console.error('Error fetching products:', error);
    res.status(500).json({ error: 'Internal Server Error' });
  }
});

app.listen(port, () => {
  console.log(`Server is listening at http://localhost:${port}`);
});
```
