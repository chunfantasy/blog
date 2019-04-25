---
layout: post
title: React Native
description: "This note is about hot to use React Native."
modified: 2019-04-01
tags: [Framework]
comments: true
image:
  feature: 2019-04-01-react-native.png
---

# React Native

This note is about how to use React Native.

<div class="social-share" data-initialized="true">
    <a href="#" class="social-share-icon icon-weibo"></a>
    <a href="#" class="social-share-icon icon-qq"></a>
    <a href="#" class="social-share-icon icon-wechat"></a>
</div>
<link rel="stylesheet" href="https://resource.chun.no/sharejs/css/share.min.css">
<script src="https://resource.chun.no/sharejs/js/social-share.min.js"></script>

### &nbsp;

---

## What is React Native

### Definition<sup>[1]</sup>

React Native lets you build mobile apps using only JavaScript.
It uses the same design as React, letting you compose a rich mobile UI using declarative components.

---

## Why use React Native

Some may be against with such mobile native solutions since the ecosystems are already developed very well for iOS and Android.
However, I am not talking about which is better but an alternative for Web developer.

#### An alternative to mobile solution

In stead of using `Objective-C`, `Swift`, `Java` or `Kotlin`,
you can use Web development languages and tools such as `HTML`, `CSS`, `JavaScript`, `Node.js`, `npm`, etc.

``` javascript
import React, {Component} from 'react';
import {Text, View} from 'react-native';

class HelloReactNative extends Component {
  render() {
    return (
      <View>
        <Text>
          If you like React, you'll also like React Native.
        </Text>
        <Text>
          Instead of 'div' and 'span', you'll use native components
          like 'View' and 'Text'.
        </Text>
      </View>
    );
  }
}
```

#### A React Native app is a real mobile app<sup>[1]</sup>

The apps you are building with React Native aren't mobile web apps because React Native uses the same fundamental UI building blocks as regular iOS and Android apps. Instead of using Swift, Kotlin or Java, you are putting those building blocks together using JavaScript and React.

``` javascript
import React, {Component} from 'react';
import {Image, ScrollView, Text} from 'react-native';

class ScrollingImageWithText extends Component {
  render() {
    return (
      <ScrollView>
        <Image
          source={uri: 'https://facebook.github.io/react-native/img/header_logo.png'}
          style={width: 66, height: 58}
        />
        <Text>
          On iOS, a React Native ScrollView uses a native UIScrollView.
          On Android, it uses a native ScrollView.

          On iOS, a React Native Image uses a native UIImageView.
          On Android, it uses a native ImageView.

          React Native wraps the fundamental native components, giving you
          the performance of a native app using the APIs of React.
        </Text>
      </ScrollView>
    );
  }
}
```

#### Save time of recompiling<sup>[1]</sup>

React Native lets you build your app faster. Instead of recompiling, you can reload your app instantly. With Hot Reloading, you can even run new code while retaining your application state. Give it a try - it's a magical experience.

![React Native Recompiling](https://media.giphy.com/media/13WZniThXy0hSE/giphy.gif)

#### 2 for 1

Develop once and can be used for both iOS and Android.
Even more, some shared modules could be used on Web and Desktop, too.

#### Use native code when you need to<sup>[1]</sup>

React Native combines smoothly with components written in Swift, Java, or Objective-C. It's simple to drop down to native code if you need to optimize a few aspects of your application. It's also easy to build part of your app in React Native, and part of your app using native code directly - that's how the Facebook app works.

``` javascript
import React, {Component} from 'react';
import {Text, View} from 'react-native';
import {MapViewComponent} from './your-native-map-implementation';

class CustomMapView extends Component {
  render() {
    return (
      <View>
        <MapViewComponent />
        <Text>
          MapViewComponent could use native Swift, Java, or Objective-C -
          the product development process is the same.
        </Text>
      </View>
    );
  }
}
```

#### No big differenct in performance

<a href="https://medium.com/the-react-native-log/comparing-the-performance-between-native-ios-swift-and-react-native-7b5490d363e2" target="_blank">Comparing the Performance between Native iOS (Swift) and React-Native</a>



---

## UI/UX Components

* <a href="https://github.com/react-bootstrap/react-bootstrap" target="_blank">React Bootstrap</a>
* <a href="https://github.com/mui-org/material-ui" target="_blank">Material-UI</a>
* <a href="https://github.com/GeekyAnts/NativeBase" target="_blank">NativeBase</a>
* <a href="https://github.com/react-native-training/react-native-elements" target="_blank">React Native Elements</a>
* <a href="https://github.com/akveo/kittenTricks" target="_blank">UI Kitten</a>

---

## Quick start

``` bash
$ npm install -g expo-cli
```

``` bash
$ expo init ChunReactNative
```

``` bash
$ npm start
```

---

## Reference

1. https://facebook.github.io/react-native/

---
