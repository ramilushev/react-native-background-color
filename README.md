## React Native Background Color
  This module alows you to set the root backgound color of your react-native app from JS.

**Supports only Android at the moment.**

### Installation

#### Using npm:

```sh
$ npm install --save react-native-background-color
```

#### Using yarn:

```sh
$ yarn add react-native-background-color
```

#### Link module

```sh
$ react-native link
```

### Usage

```jsx
import React, { Component } from 'react';

import BackgroundColor from 'react-native-background-color';

export default class Row extends Component {
  componentWillMount() {
    BackgroundColor.setColor('#FFFFFF');
  }

  render() {
    return (
      <View></View>
    );
  }
}

```
