# TabNavigator [![Slack](http://slack.exponentjs.com/badge.svg)](http://slack.exponentjs.com)
A tab bar that switches between scenes, written in JS for cross-platform support. It works on iOS and Android.

To use this component, you will need to enable the following Babel options:
 - es7.decorators
 - es7.classProperties
 - es6.modules

The look and feel is slightly different than the native navigator but it is better in some ways. Also it is pure JavaScript.

The API of this component may change in the future to be more like Navigator's, which works great once there is better support for nested Navigators in React Native.

## Usage

```js
<TabNavigator>
  <TabNavigator.Item
    selected={this.state.selectedTab === 'home'}
    title="Home"
    renderIcon={() => <Image source={...} />}
    renderSelectedIcon={() => <Image source={...} />}
    badgeText="1"
    onPress={() => this.setState({ selectedTab: 'home' })}>
    {homeView}
  </TabNavigator.Item>
  <TabNavigator.Item
    selected={this.state.selectedTab === 'profile'}
    title="Profile"
    renderIcon={() => <Image source={...} />}
    renderSelectedIcon={() => <Image source={...} />}
    renderBadge={() => <CustomBadgeView />}
    onPress={() => this.setState({ selectedTab: 'profile' })}>
    {profileView}
  </TabNavigator.Item>
</TabNavigator>
```

See TabNavigatorItem's supported props for more info.
