# ![alt tag](http://i.imgur.com/mVqUtca.png)
can be used for persist rehydrate the redux store,
# WIP
### Why Redux-recovery
Today to benefit from all the features of redux is to have an SPA, so you have to provide a router. With redux-recovery one can take advantage of redux in a web page and do exactly what offers redux for a SPA. In addition, redux-recovery is simple to use, it has a simple and reliable approach.

### Installation
To install the stable version:

```js
npm install --save redux-recovery
```
This assumes you are using npm as your package manager.


### Usage

```js
import createStore from 'redux';
import ReduxRecovery from 'redux-recovery';

const reduxRecovery = new ReduxRecovery({
    recordAction: true,
    nbSavedActions: 10
});
const middlewares = [reduxRecovery.start];
const store = createStore(reducer, {...initialState}, 
  applyMiddleware(...middlewares),
));
```


### API

`Force state persistence`: store.dispatch({ type: 'PERSIST_STORE' });

`Retrieve the persistence of the state`: reduxRecovery.getPersistState();
