## What is this? 

My friend who's learning React needed help on making this component that involved `axios` and `promises` and I offered to help. This is now a public repo, may help others, may not. I figure more open source code out there, the better.

## `promises.js` 

```jsx
import React from 'react';
import axios from 'axios';
import API from '../api';

export default class PersonList extends React.Component {
  handleSubmit = event => {
    event.preventDefault();

    API.delete(`users/${this.state.id}`)
      .then(res => {
        console.log(res);
        console.log(res.data);
      })
  }
}
```

## Other ways to invoke Axios

This `README` is for them to look at and help them understand React better. `Axios` is a Promise based HTTP client for the browser and node.js. There's many ways you can invoke Axios, but in this example in React I just showed you one way. You can also invoke Axios using a CDN. Using something like `jsDelivr` and doing:

```html
<script src="https://cdn.jsdelivr.net/npm/axios/dist/axios.min.js"></script>
```

## Promises 

Axios depends on a native ES6 Promise implementation to be supported. If your environment doesn't support ES6 Promises, you can polyfill.

```javascript
import axios from 'axios';
axios.get('/user?ID=12345');
```
