---
title: Authentication
---

# Authentication

Our endpoints require an API Key that is associated with your account. Keep it private (your secret). If your API Key is no longer a secret, get a new one inside your <a href="javascript:alert('Imagine we just sent you to your account settings.')">Account Settings</a>. The API Key is specific to your datacenter equipment and only returns information about your equipment.


Of course all of this is just for fun: because CloudUla is a **fictitious** company and this portal is just an example of how to use the <a href="https://www.redoc.ly/developer-portal">Redocly Developer Portal</a> and API documentation tools, all part of their docs-as-code implementation.

Because we are a **fictitious** company we have a **fictitious** API Key for you. It will actually work, please give it a try as our mock server awaits.

## Fictitious API Key
```
DEMO_KEY_FOR_ME
```

## Using your API Key

We made it simple, every call you make must include your API Key in the Header parameters. Here is how it might look in a <b>AXIOS</b> javascript call.

```javascript
const axios = require('axios');
 
// Make a request for a server with a given id, using version 1 of the APIs
axios.get('https://apis.cloudula.io/v1/server?id=12345', 
    {headers: {'api_key': 'DEMO_KEY_FOR_ME'}
  })
  .then(function (response) {
    console.log(response);
  })
  .catch(function (error) {
    console.log(error);
  });
```

As you go through the API Reference section you will notice the API Key in use with each example.
