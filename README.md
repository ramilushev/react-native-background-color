## React Native Background Color
  This module alows you to set the root backgound color of your react-native app from JS. Supports only Android at the moment.

### Installation

#### Using npm:

```sh
$ npm install --save react-native-background-color
```

#### Using yarn:

```sh
$ yarn add react-native-background-color
```

#### Link module in Android

   * Add the following to `android/settings.gradle`:
        ```
        include ':react-native-background-color'
        project(':react-native-background-color').projectDir = new File(settingsDir, '../node_modules/react-native-background-color/android')
        ```

    * Add the following to `android/app/build.gradle`:
        ```xml
        ...

        dependencies {
            ...
            compile project(':react-native-background-color')
        }
        ```
    * Add the following to `android/app/src/main/java/**/MainApplication.java`:
        ```java
        import io.rado.backgroundcolor.BackgroundColor;  // add this for react-native-background-color

        public class MainApplication extends Application implements ReactApplication {

            @Override
            protected List<ReactPackage> getPackages() {
                return Arrays.<ReactPackage>asList(
                    new MainReactPackage(),
                    new BackgroundColor()     // add this for react-native-background-color
                );
            }
        }
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
