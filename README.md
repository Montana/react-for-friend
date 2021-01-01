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
