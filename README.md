
# Kingriders App
>ANDROID Verison 6.3.0
##### Follow these commands:

    For build apk, run `phonegap build android --debug --buildConfig=path/to/build.json`.

    install on phone `adb install -r platforms/android/build/outputs/apk/android-debug.apk`

    update android:
    - phonegap plateform add android@6.3.0
    - phonegap plateform remove android@6.3.0
    - phonegap plateform update android@6.3.0

  

#### Key generation

> HELP:

    https://stackoverflow.com/questions/26449512/how-to-create-a-signed-apk-file-using-cordova-command-line-interface

    http://docs.phonegap.com/phonegap-build/signing/android/

  

1. keytool -genkey -v -keystore [keystore_name].keystore -alias [alias_name] -keyalg RSA -keysize 2048 -validity 10000

example:

- keytool -genkey -v -keystore solutionwin.keystore -alias kingriders -keyalg RSA -keysize 2048 -validity 10000

2. jarsigner -verbose -sigalg SHA1withRSA -digestalg SHA1 -keystore <keystorename>  <Unsigned  APK  file>  <Keystore  Alias  name>

example:

- jarsigner -verbose -sigalg SHA1withRSA -digestalg SHA1 -keystore NAME-mobileapps.keystore Example-release-unsigned.apk xxxxxmobileapps