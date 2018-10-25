
# react-native-aliyun-player

## Getting started

`$ npm install react-native-aliyun-player --save`

### Mostly automatic installation

`$ react-native link react-native-aliyun-player`

### 安卓
```$xslt
app的gradle文件添加
android{
    ...
    packagingOptions {
        pickFirst 'lib/armeabi-v7a/libgnustl_shared.so'
        pickFirst 'lib/arm64-v8a/libgnustl_shared.so'
        pickFirst 'lib/x86_64/libgnustl_shared.so'
        pickFirst 'lib/x86/libgnustl_shared.so'
    }
}

repositories {
    flatDir {
        dirs project(':react-native-aliyun-player').file('libs')
    }
}
```

### Manual installation


#### iOS

1. In XCode, in the project navigator, right click `Libraries` ➜ `Add Files to [your project's name]`
2. Go to `node_modules` ➜ `react-native-aliyun-player` and add `RNAliyunPlayer.xcodeproj`
3. In XCode, in the project navigator, select your project. Add `libRNAliyunPlayer.a` to your project's `Build Phases` ➜ `Link Binary With Libraries`
4. Run your project (`Cmd+R`)<

#### Android

1. Open up `android/app/src/main/java/[...]/MainActivity.java`
  - Add `import com.syan.RNAliyunPlayerPackage;` to the imports at the top of the file
  - Add `new RNAliyunPlayerPackage()` to the list returned by the `getPackages()` method
2. Append the following lines to `android/settings.gradle`:
  	```
  	include ':react-native-aliyun-player'
  	project(':react-native-aliyun-player').projectDir = new File(rootProject.projectDir, 	'../node_modules/react-native-aliyun-player/android')
  	```
3. Insert the following lines inside the dependencies block in `android/app/build.gradle`:
  	```
      compile project(':react-native-aliyun-player')
  	```

#### Windows
[Read it! :D](https://github.com/ReactWindows/react-native)

1. In Visual Studio add the `RNAliyunPlayer.sln` in `node_modules/react-native-aliyun-player/windows/RNAliyunPlayer.sln` folder to their solution, reference from their app.
2. Open up your `MainPage.cs` app
  - Add `using Aliyun.Player.RNAliyunPlayer;` to the usings at the top of the file
  - Add `new RNAliyunPlayerPackage()` to the `List<IReactPackage>` returned by the `Packages` method


## Usage
```javascript
import RNAliyunPlayer from 'react-native-aliyun-player';

// TODO: What to do with the module?
RNAliyunPlayer;
```
