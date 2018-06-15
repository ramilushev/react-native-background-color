## React Native Background Color
  This module alows you to set the root backgound color of your react-native app from JS.
  
  This calls `setBackgroundColor` on the root view, which will remove overwrites/removes any existing background resource, including any borders, corners, padding, etc. This is very good for if you set a splash screen in Android following this popular way - [Medium :: Andrey Nikishaev - Change splash screen in React Native Android app](https://medium.com/react-native-development/change-splash-screen-in-react-native-android-app-74e6622d699). That tutorial recommends setting a solid color on the root view to just cover the splash image. However when the keyboard shows, it shows the background view for a split second, and your splash image is visible. So by using `setBackgroundColor` from this module, you can erase that image from the back.

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
