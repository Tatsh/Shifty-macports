# Shifty

Shifty was made to expand the capabilities of the built in Night Shift feature in macOS. You can disable Night Shift for specific apps, websites, and custom time periods. It also provides easy access to a slider to fine tune your color temperature. With Shifty, Night Shift becomes a power user feature!

Website shifting supports Safari, Chrome, and Vivaldi.

<img src='docs/en/images/shifty-screenshot-large.png' width=70%>

Shifty is customizable! Make it easier to toggle Night Shift with Quick Toggle or set dark mode based on the schedule. For common Shifty actions, you can set global keyboard shortcuts.

<img src="docs/en/images/prefs-general-screenshot-shadow.png" width=60%/>

## System requirements

* macOS 10.12 or later
* Your system must [support Night Shift](https://support.apple.com/en-us/HT207513#requirements)

## Building from source

### Command line

```sh
cd where-shifty-is-cloned-to/
mkdir data-path
xcodebuild -workspace Shifty.xcworkspace/ \
    -scheme Shifty \
    -derivedDataPath data-path \
    -configuration Release \
    install \
    INSTALL_PATH=./test/ \
    CODE_SIGN_IDENTITY=- \
    CODE_SIGN_STYLE=Manual \
    ENABLE_HARDENED_RUNTIME=NO \
    ARCHS=x86_64
```

In one line:

```sh
cd where-shifty-is-cloned-to/ && mkdir data-path && xcodebuild -workspace Shifty.xcworkspace/ -scheme Shifty -derivedDataPath data-path -configuration Release install INSTALL_PATH=/Applications/ CODE_SIGN_IDENTITY=- CODE_SIGN_STYLE=Manual ENABLE_HARDENED_RUNTIME=NO ARCHS=x86_64
```

## License

Shifty is free and open source, licensed under GPLv3. Feel free to make a pull request!

If you'd like to help translate Shifty into other languages, you can contribute [here](https://shifty.natethompson.io/translate).
