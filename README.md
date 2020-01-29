# 🚀react-native-boilerplate 🚀
My first app using React Native

Let's start to create our standard template for React Native:

```
npx react-native init ReactNativeBoilerplate
```

After that I run Metro Bundler with this command:

```
npm run start
```


And in another terminal or tab you can run the app for ios/android:

```
npm run ios
```

or

```
npm run android
```


So for iOS everything worked on the first shot, but not for Android.


First error:

```java
* What went wrong:
Could not compile settings file '/Users/szicar01/Repositories/react-native-boilerplate/android/settings.gradle'.
> startup failed:
  General error during semantic analysis: Unsupported class file major version 57

  java.lang.IllegalArgumentException: Unsupported class file major version 57
```

Solution ([from here](https://github.com/facebook/react-native/issues/26625#issuecomment-560030421z)):

```java
Go to android/gradle/wrapper/gradle-wrapper.properties

Change the following line:

- distributionUrl=https\://services.gradle.org/distributions/gradle-5.5-all.zip
+ distributionUrl=https\://services.gradle.org/distributions/gradle-6.0.1-all.zip
That's what worked for me with the latest versions of everything on MacOS
```

If you have others issues about Android env take a look to this [here](https://facebook.github.io/react-native/docs/getting-started.html#android-development-environment).


## Install React Navigation

I would like to try new version of [React Navigation](https://reactnavigation.org/docs/en/next/getting-started.html).

```
npm install @react-navigation/native@next
```

```
npm install react-native-reanimated react-native-gesture-handler react-native-screens react-native-safe-area-context @react-native-community/masked-view
```

and 

```
npm install @react-navigation/stack@next @react-native-community/masked-view
```

```
npm install @react-navigation/bottom-tabs@next
```

Afte install all package from react-navigation you need to type this [from here](https://reactnavigation.org/docs/en/next/getting-started.html):

```
cd ios
pod install
cd ..
```

Install icons:

```
npm install --save react-native-vector-icons
```

And configure it following [this steps](https://github.com/oblador/react-native-vector-icons#installation) 