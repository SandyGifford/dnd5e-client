# DnD5e TypeScript APi (client edition)

This repo offers typings and function endpoints to the [DnD 5e API](http://www.dnd5eapi.co/).  It is based on the [dnd5e](https://github.com/SandyGifford/dnd5e) package and is designed to be used with the [dnd5e-server](https://github.com/SandyGifford/dnd5e-server) package.

## installation

### Yarn
```
yarn add dnd5e-client
```

### NPM
```
npm install dnd5e-client
```

## use

After installing you can import normally:

```typescript
import * as DnD from "dnd5e-client";

// -- or --

import {AbilityScore} from "dnd5e-client";
```

<quote>**note:** this package requires that you have setup the Express middleware from the [dnd5e-server](https://github.com/SandyGifford/dnd5e-server) package.  It is not stand-alone.</quote>

### accessing the endpoints

Once you have the middleware setup, and your server running, you can find all endpoints under `ClientEndpoints`

```typescript
import * as DnD from "dnd5e-client";

DnD.ClientEndpoints.skills()
	.then(console.log);
```

Every endpoint in `ClientEndpoints` returns a promise that resolves to a JSON object (typed).  For more information on individual endpoints, see the JSDocs, or the [DnD 5e API docs](http://www.dnd5eapi.co/docs/).
