# React Native Component for ijkplayer

How to build Example
```
git clone https://github.com/uimeet/react-native-ijkplayer-example.git
cd react-native-ijkplayer-example
npm install
react-native run-android
```
A react native component for [ijkplayer](https://github.com/Bilibili/ijkplayer)

### iOS

iOS build need IJKMediaFramework.framework first,
which can be build following instructions on https://github.com/Bilibili/ijkplayer,
and generate IJKMediaFramework.framework

```
cd /Users/cong/Library/Developer/Xcode/DerivedData/IJKMediaDemo-ffgcszbckhcejffronccjzcppdbz/Build/Products/
lipo -create Release-iphoneos/IJKMediaFramework.framework/IJKMediaFramework Release-iphonesimulator/IJKMediaFramework.framework/IJKMediaFramework -output IJKMediaFramework
cp IJKMediaFramework Release-iphoneos/IJKMediaFramework.framework/
cp -R Release-iphoneos/IJKMediaFramework.framework react-native-ijkplayer/ios/
```

After IJKMediaFramework.framework placed under react-native-ijkplayer/ios/ , Example is ready to build.
```
cd react-native-ijkplayer/Example/ios
open Example.xcodeproj
```

### Android

ijk dependencies is satisfied using gradle for Android

```
cd react-native-ijkplayer/Example/android
./gradlew installDebug
```

### Usage

 ```js
import IJKPlayer from "react-native-ijkplayer";
 () => (
     <IJKPlayer
         style={{}}
         headers={{}}
         source={{
             uri: "http://techslides.com/demos/sample-videos/small.mp4"
         }}
         paused={false}
         muted={flase}
         paused={true}
         volume={1.0}
         onLoadStart={}
         onLoad={}
         onBuffer={}
         onError={}
         onProgress={}
         onPause={}
         onStop={}
         onEnd={}
     />
 );
 ```

 ### Building

 Build for iOS following the instructions at https://github.com/Bilibili/ijkplayer. You must create release builds for both iOS and the simulator.

 ```bash
 cd ~/Library/Developer/Xcode/DerivedData/IJKMediaDemo-*/Build/Products/
 lipo -create Release-iphoneos/IJKMediaFramework.framework/IJKMediaFramework Release-iphonesimulator/IJKMediaFramework.framework/IJKMediaFramework -output IJKMediaFramework
 cp IJKMediaFramework Release-iphoneos/IJKMediaFramework.framework/
 cp -R Release-iphoneos/IJKMediaFramework.framework react-native-ijkplayer/ios/
 ```
