[react-native-qrcode](https://www.npmjs.com/package/react-native-qrcode) ver.0.2.7 is modify for [react-native-webview](https://www.npmjs.com/package/react-native-webview) (seperate from react-native).

---
A react-native component to generate [QRcode](http://en.wikipedia.org/wiki/QR_code)

## Installation
add in package.json
```sh
"react-native-qrcode": "https://github.com/sorayuth10/react-native-qrcode.git",
```
install command
```sh
git+https://github.com/sorayuth10/react-native-qrcode.git,
```
## Usage
```jsx
'use strict';

import React, { Component } from 'react'
import QRCode from 'react-native-qrcode';

import {
    AppRegistry,
    StyleSheet,
    View,
    TextInput
} from 'react-native';

class HelloWorld extends Component {
  state = {
    text: 'http://facebook.github.io/react-native/',
  };

  render() {
    return (
      <View style={styles.container}>
        <TextInput
          style={styles.input}
          onChangeText={(text) => this.setState({text: text})}
          value={this.state.text}
        />
        <QRCode
          value={this.state.text}
          size={200}
          bgColor='purple'
          fgColor='white'/>
      </View>
    );
  };
}

const styles = StyleSheet.create({
    container: {
        flex: 1,
        backgroundColor: 'white',
        alignItems: 'center',
        justifyContent: 'center'
    },

    input: {
        height: 40,
        borderColor: 'gray',
        borderWidth: 1,
        margin: 10,
        borderRadius: 5,
        padding: 5,
    }
});

AppRegistry.registerComponent('HelloWorld', () => HelloWorld);

module.exports = HelloWorld;
```
## Available Props

prop      | type                 | default value
----------|----------------------|--------------
`value`   | `string`             | `http://facebook.github.io/react-native/`
`size`    | `number`             | `128`
`bgColor` | `string` (CSS color) | `"#000"`
`fgColor` | `string` (CSS color) | `"#FFF"`

<img src='qrcode.png' height = '256' width = '256'/>

# Credit

[MIT License](https://github.com/cssivision/react-native-qrcode/blob/master/LICENSE).

## Modfify

By [SRY](https://github.com/sorayuth10/).
