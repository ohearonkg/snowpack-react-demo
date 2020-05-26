# Snowpack React Demo

This repository is a simple example of how to use the [snowpack build tool](https://www.snowpack.dev/)
to build your react application without needing to bundle your source code!

## Installation Steps

1. Clone the repository
2. Change into the newly cloned repository
3. Install dependencies using `npm install` or `yarn install`
4. Run the application using `npm start` or `yarn start`

### Installing Additional Packages

For snowpack to work correctly each additional dependency must be in ESM format.
A list of available packages can be found [here](https://www.pika.dev/search).

After installing your desired dependencies, run:`npm snowpack` or `yarn snowpack` as
appropriate to copy your new dependencies into the `web_modules` folder.

### Common Gotchas

#### File Extension Required

Since we are using ECMAscript modules, when importing we must also add the
extension of our files. For example

```
// App.js
import React from "react";

const App = () => <h1>Hello From Snowpack!</h1>;

export default App;

```

```
// index.js
import React from "react";
import ReactDOM from "react-dom";

import App from './App.js'

ReactDOM.render(<App />, document.getElementById("app"));

```
