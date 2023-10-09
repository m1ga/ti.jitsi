# ti.jitsi

Basic Jitsi Meet module for Android.

## Method

* **startConference**:
  * Properties:
    * **server** (String): your Jitsi server (default: https://meet.jit.si)
    * **room** (String): room name to join


## Setup

build.gradle
```
repositories {
    maven {
        url "https://github.com/jitsi/jitsi-maven-repository/raw/master/releases"
    }
}
```

tiapp.xml

```xml
<!-- needs minSDK 24 -->
<uses-sdk android:minSdkVersion="24"/>

<application>
  <activity android:name="ti.jitsi.JitsiActivity" android:exported="false"/>
</application>
```

## Example

```js
var ti_jitsi = require('ti.jitsi');

ti_jitsi.startConference({
	room: "this_is_a_test_ti_room"
});
```
