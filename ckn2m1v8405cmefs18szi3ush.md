## Still using ExpressJS? Time to switch backend frameworks!

Hey everyone! Welcome to this blog on switching your backend frameworks in JS.

So, here's the thing, We all know ExpressJS is indeed popular and probably one of the first backend frameworks, But that doesn't give a proper reason to use it, when you get something better and new. I've seen most of the JS community isn't much aware of the new Awesome backend framework called `Fastify`.

But, It's time to change. Why? because it's better. 

Now, How am I saying that? Because here's a ton of points that makes it awesome, and really cool to use!

## Simpleness

Relatively, ExpressJS has been always the same.

```js

const express = require('express')
const app = express()
const port = 3000

app.get('/', (req, res) => {
  res.send('Hello World!')
})

app.listen(port, () => {
  console.log(`Example app listening at http://localhost:${port}`)
})
```
But Fastify makes it simple.

- Require and configure
- Run!

Here's the same thing, but for fastify

```js
// Require the framework and instantiate it
const fastify = require('fastify')({
  logger: true
})

// Declare a route
fastify.get('/', function (request, reply) {
  reply.send({ hello: 'world' })
})

// Run the server!
fastify.listen(3000, function (err, address) {
  fastify.log.info(`server listening on ${address}`)
})
```
You even get lightweight choices, but robust configuration, one of them being the awesome logging. Now this is some real thing. This being simple affects it a lot, which brings us to out second point!

## Performance

As a comparison of their code, ExpressJS has a ton of code, while fastify does just few files, hence keeping light and easy to get started and use.

You might be wondering, "Soo.... How does it even affect?"

It does. A lot. When there's a lot of things going in the backend, they have to process everything, after reading, and interpreting. Basically that increases the time taken, and makes it slower. Fastify did make a interesting decision to fix this, we'll be talking about that. But for now, It's pretty lightweight and the same thing is done in fewer lines of code, and Yet it didn't stop from providing power in your hands. Here's what It can do without any additional dependencies, or anything.

![Screenshot from 2021-04-02 14-33-42.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1617354233775/STzzOgmtv.png)

Here's the benchmark too!

![Screenshot from 2021-04-04 12-51-59.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1617520963092/mcVPYPzw1.png)

It even outperformed all other frameworks by 4 or 5 times :D

Isn't it crazy? Yeah, that's the the outer thing, wait for to explore more :)

## Async and speed

Fastify has better grasp over async, allowing multiprocessing instead of threading, and running it in coroutines to speed things in the background.

Here's a Tip: Use async more, The reasons to do so:

- Speed
- Multiple processing at once
- Coroutines
- The code is less and easier!

```js
const fastify = require('fastify')({
  logger: true
})

fastify.get('/', async (request, reply) => {
  return { hello: 'world' }
})

const start = async () => {
    await fastify.listen(3000)
}
start()
```

This is Just even simpler.

## Extensibility and ecosystem

Yay! Time to discuss fastify ecosystem. But before we do that, Here's the thing


![Screenshot from 2021-04-02 14-44-28.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1617357435841/1u7AoX_Gw.png)

As you see in the diagram, ExpressJS has a single package only with everything cluttered and included which tries to make people to use it because it has everything bundled together.

But that's not the case with fastify. They have a ecosystem, and make separate packages for each thing, keeping each thing lightweight, and transparent. You realize what's being used, what's needed and other stuff. They have "Plugins" to do things which you want to do, but isn't unfortunately available in root package, Hence this way everything's organized, and clean. Even if you can't find plugin for your job, It's damn easy to make one, trust me.

![Screenshot from 2021-04-02 14-48-45.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1617355150225/JKEw0CLl5.png)

They're extensible, light, easy to use, and make! You can even contribute to community by making your own plugins!

## Logging

Probably one of the best and easiest ways to do this in fastify. It's easy, customizable and handy.

Here's how to get started

```js
const fastify = require('fastify')({
  logger: true
})

fastify.get('/', options, function (request, reply) {
  request.log.info('Some info about the current request')
  reply.send({ hello: 'world' })
})
```

You can even customize as you want, and it's damn easy. Here's how

```js
const fastify = require('fastify')({
  logger: {
    prettyPrint: true,
    serializers: {
      res (reply) {
        // The default
        return {
          statusCode: reply.statusCode
        }
      },
      req (request) {
        return {
          method: request.method,
          url: request.url,
          path: request.path,
          parameters: request.parameters,
          headers: request.headers
        };
      }
    }
  }
});
```

## Typescript support

Usually people love working with TypeScript now-a-days, and It's pretty awesome. Fastify has inbuilt support for TypeScript too!!

You just add typescript with fastify, and Just write the code for it, as it is for JS, and it just works fine, Bam!

Fastify is shipped with a typings file, but you may need to install `@types/node`, depending on the Node.js version you are using.

We pass the relevant typings for our http version used.

By passing types we get correctly typed access to the underlying http objects in routes.

If using http2 we'd pass `<http2.Http2Server, http2.Http2ServerRequest, http2.Http2ServerResponse>`.

For https pass http2.Http2SecureServer or http.SecureServer instead of Server.

This ensures within the server handler we also get http.ServerResponse with correct typings on reply.res.

Here's the guide for it: [Fastify TypeScript](https://www.fastify.io/docs/latest/TypeScript/)

## Schema, Validations and Hooks

This is probably one of the exciting and amazing features in fastify. Of course, Fastify can do much more than this.

For example, you can easily provide input and output validation using JSON Schema and perform specific operations before the handler is executed:

```js
const fastify = require('fastify')({ logger: true })

fastify.route({
  method: 'GET',
  url: '/',
  schema: {
    // request needs to have a querystring with a `name` parameter
    querystring: {
      name: { type: 'string' }
    },
    // the response needs to be an object with an `hello` property of type 'string'
    response: {
      200: {
        type: 'object',
        properties: {
          hello: { type: 'string' }
        }
      }
    }
  },
  // this function is executed for every request before the handler is executed
  preHandler: async (request, reply) => {
    // E.g. check authentication
  },
  handler: async (request, reply) => {
    return { hello: 'world' }
  }
})
```

This features reduces code, Keeps it DRY, and makes working even easier! Just awesome!

## Activity on the projects

Being active, and maintained projects should be preferred more, because of patches, bug fixes and constantly new features out of the oven. On the date of the writing, here are the stats:

#### ExpressJS

Latest commit:

![Screenshot from 2021-04-02 15-10-31.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1617356458951/0zy9Nh0pW.png)

Latest release:

![Screenshot from 2021-04-02 15-11-17.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1617356490888/gJzB4mS7v.png)

#### Fastify

Latest commit:

![Screenshot from 2021-04-02 15-11-56.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1617356533642/7dGTlrP40.png)

Latest release:

![Screenshot from 2021-04-02 15-11-59.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1617356542992/Kx3xyUbyR.png)

## Documentation

> Anyone can write documentation, but the best documentation, always stands out as the best.

This proverb shows the importance of good documentation, and It is actually true in case of fastify.
The documentation is so simple, that you can't resist learning. It's easy and you can learn the technlogy in pretty simple and quick manner. It's lucid, simple and one of the best.

![Screenshot from 2021-04-02 15-20-05.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1617357017726/n72LmDbL3.png)

Everything's written and explained in an easy to understand way, and it's not too cluttered. Things are left clean, and the actual thing, that is documentation is more focused on.

These are the points I have, why to use Fastify.

**Do you need more reason to show it's better?**
**Add a star to show support towards the community and spread the word!**

It's gonna be the future, I predict. Anything that's good, always survives the situations, and fastify will do it for sure!

**Important Links**
- [Fastify docs](https://fastify.io)
- [Fastify github](https://github.com/fastify/fastify)
- [Fastify ecosystem](https://fastify.io/ecosystem)

Thank you so much for reading this article, I hope you loved it, and learnt something awesome! If you have any queries or feedback, Hit me up in my twitter handle at [@JanaSunrise](https://twitter.com/janaSunrise)! Have a great day, See you later!

