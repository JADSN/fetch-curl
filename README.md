## Motivation

First the difficulty was making http2 requests on node through an http1 proxy. Libcurl abstracts this for us. So why not curl node With this in mind, I decided to create a lib that uses background curl but with the fetch API syntax

## Installing

To utilize for node.js install the the `npm` module:

```bash
npm i fetch-curl --save
```

## Common Usage

### GET Text

```js
const res = await fetch('https://github.com/');
const body = res.text();

console.log(body)
```

### GET Json

```js
const res = await fetch('https://restcountries-v1.p.rapidapi.com/all');
const json = res.json();

console.log(json)
```

### POST

```js
const res = await fetch('https://foo/', {
        method: 'POST',
        body: {
            name: 'foo',
            email:'foo@foo.com'
        }
    });

const json = res.json();

console.log(json)
```