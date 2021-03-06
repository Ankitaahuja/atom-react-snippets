# atom-react-redux-react-native-snippets package

React, React-Native, Redux, and Test snippets to help with building your React apps in Atom.

# React

### `imr` Import React
```
import React from "react";
```

### `imrc` Import React with Component
```
import React, { Component } from "react";'
```

### `ed` Export Default
```
export default ${1}
```  

### `rsl` React Stateless Component
```
    import React from 'react';

    const ${1} = () => (

    );

    export default ${1};
```

### `rcon` React Constructor':
```
      constructor(props) {
        super(props);

        this.state = {$1};
      }
```

### `rcom` React Component
```
      import React, { Component } from 'react';

      class $1 extends Component {
        render() {
          return (
            <div>
              <h1>$1 Component</h1>
            </div>
          );
        }
      }

      export default ${1};
```

### `rcwu` React Component Will Mount
```
      componentWillMount() {
        ${1}
      }
```

### `rcdm` React Component Did Mount
```
      componentDidMount() {
        ${1}
      }
```

### `rcwrp` React Component Will Receive Props
```
  componentWillReceiveProps() {
    ${1}
  }
```

### `rcum` React Component Did Unmount
```
      componentDidUnmount() {
        ${1}
      }
```

### `rcwu` React Component Will Update
```
      componentDidWillUpdate() {
        ${1}
      }
```

### `rcdu` React Component Did Update
```
      componentDidDidUpdate() {
        ${1}
      }
```

### `rrat` React-Redux App Template
```
    import React from 'react';
    import ReactDom from 'react-dom';
    import { Provider } from 'react-redux';
    import { createStore, applyMiddleware } from 'redux';
    // install of react-router@3.0.1 or change line below and routing to reflect latest version
    import { Router, Route, IndexRoute, browserHistory} from 'react-router';
    import thunk from 'redux-thunk';
    import App from './components/App';

    import reducers from './reducers';
    const createStoreWithMiddleWare = applyMiddleware(thunk)(createStore);

    ReactDOM.render(
      <Provider store={createStoreWithMiddleware(reducers)}>
        <Router history={browserHistory}>
          <Route path="/" component={App} >
            <IndexRoute component={$1} />
            <Route path="${2}" component={${3}} />
          </Route >
        </Router>
      </Provider>,
      document.getElementById('app')
    );
```

### `rrr` React-Router Route
```
    <Route path="${1}" component={${2}} />
```

# React-Native

### `rncom` React-Native Component
```
      import React, { Component } from 'react';
      import { Text, View } from 'react-native';

      class ${1} extends Component {
        render() {
          return (
            <View>
              <Text>${1} Component</Text>
            </View>
          );
        }
      }

      export default ${1};
```

### `rnsl` React-Native Stateless Component
```
      import React from 'react';
      import { Text, View } from 'react-native';

      const $1 = () => (
        <View>
          <Text>${1} Component</Text>
        </View>
      )

      export default ${1};
```

### `ess` React Native EStyleSheet
```
    import EStyleSheet from 'react-native-extended-stylesheet';

    const styles = EStyleSheet.create({
      ${1}
    });

    export default styles;

```
# Redux

### `rrd` Redux Reducer
```
      export default (state = INITIAL_STATE, action) => {
        switch(action.type) {
          case ${1}:
          default:
            return state;
        }
      }
```
### `rrs` Redux Reducer Initial State
```
    const INITIAL_STATE: {
      ${1}
    };
```
### `rat` Redux Action Type
```
export const ${1} = "${1}"'
```

# Testing

### `tdesc` Test Describe
```
    describe('${1}', () => {
      ${2}
    })
```
### `tit` Test It
```
    it('should ${1}', () => {
      ${2}
    });
```
