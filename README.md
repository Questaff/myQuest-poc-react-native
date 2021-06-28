# myQuest Backend
This is the React Native POC mobile app of myQuest !

![](https://cdn.discordapp.com/attachments/584465372489449608/833542286419689472/Webp.net-resizeimage_4.png) [Find us on discord](https://discord.gg/uh6FudeY9Q)

# Installation

## Prerecquisites
* Install [npm](https://docs.npmjs.com/about-npm-versions) or [yarn](https://yarnpkg.com/getting-started/install)
* Install [nodejs](https://nodejs.org/en/download/) v12 or greater

## Install & Initialize :
This installation instructions assumes that you have already installed the prerecquisites above.

### Using Expo CLI
1. Run `yarn global add expo-cli` or `npm install -g expo-cli` depending of which package installer you have to install expo-cli.
2. Run `yarn start` to run the project.

### Using Android Emulator
To make this works, you'll need to do the above instructions to install and run expo before.

1. Install [Android Studio](https://developer.android.com/studio). During the installation wizard select at least one version of the "Android SDK Build-Tools". If you have already android studio installed, make sure it is installed in `Settings > System settings > Android SDK`.
2. Copy your Android SDK Location path from the path above and paste in your `~/.bashrc` or `~/.bash_profile` or whatever bash or shell file depending of your system the following :
```
export ANDROID_SDK=/your/path/here
``` 
If you are on MacOS only, in the same file add the following :
```
PATH=/your/path/here:$PATH
```
Then run `source <your file>`. exemple : `source ~/.bashrc`.

3. Setup an android emulator from the AVD Manager of android studio. You'll need an android version with (Google APIs) but you are free to choose the android 10+ version and whatever device you prefer. Run your emulator.

# Project
You can download the [Expo App](https://play.google.com/store/apps/details?id=host.exp.exponent) from your smarthpone so you can test it directly from it by scanning the QR Code given by expo when you run the project.

## Using Expo CLI
Run `yarn start` to run the project.

When starting the project, the expo web page will open in your browser with everything to works with. The next command can be used anytime in console :

```
› Press a │ open Android
› Press w │ open web

› Press r │ reload app
› Press m │ toggle menu
› Press d │ show developer tools
› shift+d │ toggle auto opening developer tools on startup (enabled)

› Press ? │ show all commands
```

## Using Android Studio Emulator
Start your emulator, then on expo app clic `Run on Android device/emulator` button or press `a` from your terminal where you have started expo.

## Troubleshooting
- When you install expo you may have an error with nodejs if you already have node on your system but the version is under node v12. To fix this :

1. Run `sudo yarn cache clean -f`
2. Then run `sudo yarn global add n`
3. Finally run `sudo n stable`

You may verify the version now is above v12 with `node -v`.

- You may have an adb error if the version of your system differ from the SDK platform-tools one. In result you'll get an error like `adb server version (xx) doesn't match this client (xx); killing...`
To fix it run :
`adb version` to check your system version.
`cd ~/Library/Android/sdk/platform-tools` and `./adb version` to check if the version is different.
`sudo cp ~/Library/Android/sdk/platform-tools/adb /usr/bin` to fix it

- If nothing happen and the android device is not found when you try to run the app via android emulator, you should verify that :
  - Your android emulator is running
  - Your android emulator has debugging mode activate
  - Your android image has (Google APIs) tag.
  - adb server is running, run `adb kill-server` and `adb start-server`.
  - If is not sufficient, try to wipe data of the android emulator and to uninstall expo app. Also check that the profile file depending on which system and bash/shell you are using (~/.bashrc, ~/.bash_profile, ~/.zshenv etc...) has everything according to the installation instruction and that they are sourced (`source ~/.bashrc` or restart your system).
It should works now!

## Version
- React Native 0.63.2
- React 16.9.35
- Expo 41
- Typescript 4.0.0