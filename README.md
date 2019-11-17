# react-pull-to-refresh

> Pull To Refresh for Progressive Web Application (only Mobile) React JS

[![NPM](https://img.shields.io/npm/v/react-pull-to-refresh.svg)](https://www.npmjs.com/package/react-pull-to-refresh) [![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)

## Install

```bash
npm i pull-to-refresh-react
```

##### [Pull To Refresh NPM](https://www.npmjs.com/package/pull-to-refresh-react)


##### [Pull To Refresh Github](https://github.com/CuongStf/pull-to-refresh-react)

## Usage

```jsx
import React, { Component } from 'react'

import PullToRefresh from "pull-to-refresh-react";

export default class App extends Component {
  onRefresh() {
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve();
      }, 5000);
    });
  }

  render() {
    return (
      <PullToRefresh options={{ height: 60 }} onRefresh={this.onRefresh}>
        <div
          style={{
            height: "500px",
            width: "100%",
            backgroundColor: "black"
          }}
        ></div>
      </PullToRefresh>
    );
  }
}
```

## Prop

| Prop                  | Type                                | Default | Description |
| :---------            | :-------:                           | :-----: | :----------- |
| onRefresh             | `async function (required)`                     | -       | Function happend when onRefresh |
| textError             | `string (optional)`                     | `Error`       | Text display when error |
| textStart    | `string (optional)`      | `Start`       | Text display when start touch |
| textReady           | `string (optional)`                            | `Ready`    | Text display when ready onRefresh |
| textRefresh             | `string (optional)`                     | `Refresh`       | Text display when refreshing |
| options             | `object (optional)`                     | `{ height: 60 }`       | { height: height of Pull Down }  |



## License

MIT © [CuongStf](https://github.com/CuongStf)
