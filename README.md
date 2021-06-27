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

### Using React Native CLI
<!-- https://docs.expo.io/workflow/android-studio-emulator/?redirected -->

# Project
## Using Expo CLI
Run `yarn start` to run the project.

When starting the project, the expo web page will open in your browser with everything to works with. The next command can be used anytime in console :

› Press a │ open Android
› Press w │ open web

› Press r │ reload app
› Press m │ toggle menu
› Press d │ show developer tools
› shift+d │ toggle auto opening developer tools on startup (enabled)

› Press ? │ show all commands

## Using React Native CLI
<!-- Connect your device (physical smartphone or emulator) and run `npx react-native run-android`

To reload the app press "r"
To open developer menu press "d" -->

## Troubleshooting
- When you install expo you may have an error with nodejs if you already have node on your system but the version is under node v12. To fix this :

1. Run `sudo yarn cache clean -f`
2. Then run `sudo yarn global add n`
3. Finally run `sudo n stable`

That's it. You may verify the version now is above v12 with `node -v`.

## Version
- React Native 0.63.2
- React 16.9.35
- Expo 41
- Typescript 4.0.0