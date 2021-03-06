<p style="text-align: center">
 <img width="160" src="https://i.ibb.co/SJVMwM0/icon.png" alt="icon" border="0" /><br/>
  <h2 align="center">Juan Valdez App</h2>
</p>

### Appendix

- [๐Description](#description)
- [โ Previous requirements](#previous-requirements)
- [๐ฅ Clone Project](#clone-proyect)
- [๐Environment variables](#environment-variables)
- [๐Work Environments](#work-environments)
- [๐ฒ Android Set Up](#android-set-up)
- [๐ iOS Set Up](#ios-set-up)
- [๐ฒ Generate Android APK](#generate-android-apk)
- [๐ฒ Generate iOS TestFlight](#generate-ios-testflight)
- [โ FAQ](#faq)

---

# ๐ Description

Juan Valdez app is a project belonging to the sales area, specifically to coffee products..

---

#### โ Previous requirements

- Install latest LTS Nodejs at [NodeJS.org](https://nodejs.org/es/).
- You must have already installed [React Native CLI](https://reactnative.dev/docs/environment-setup "React Native CLI") on Android / iOS and their dependencies.

Check node and npm versions:

```bash
$ node --version
```

> v16.15.0

```bash
 $ npm --version
```

> 8.5.5

---

#### ๐ฅ Clone Project

```bash
  git clone git@bitbucket.org:tradesystem/juan_valdez_app_v3.git
```

Go to the project directory

```bash
cd juan_valdez_app_v3
```

Install dependencies

```bash
$  npm install
```

---

#### ๐ Environment variables

1. Paste the development variables at location:

> enviroments/dev

2. Paste the production variables at location:

> enviroments/prod

You must request the firebase and keystores environment variables from tech lead.

---

#### ๐ Work Environments

To change the environment you must run:

1. For Development:

```bash
  ./switchenv.sh dev
```

3. For Production:

```bash
  ./switchenv.sh prod
```

#### ๐ฒ Android Set Up

Paste the keyStores at location:

> android/app

Run command the follow command to start the server:

```bash
  npm run android
```

---

#### ๐ iOS Set Up

Install Pods dependencies:

```bash
  pods install
```

Open project in XCode tu run iOS server.

> Notes:
>
> - This process is only for the mobile app.
> - The files that will change are these: `google-services.json`, `GoogleService-Info.plist`,
>   `Info.plist`, `constants.h`, `global.config`, `artisan.ts`, `api.ts`, `strings.xml`, `gradle.properties`.

---

### ๐ฒ Generate Android .apk

Run the follow command:

```bash
  npm run release
```

The generated apk must be at location:

> android/app/build/outputs/apk/release

### ๐ฒ Generate iOS TestFlight

---

### โ FAQ

##### 1.- How to activate / deactivate redux log con console

Get into `constants.ts` file and turn to false LOGGER_ON constant:

> LOGGER_ON = FALSE

##### 2.- Pods Error on iOS install

If the pods were already installed and an error occurred follow the next steps:

1. Deintegrate pods pod deintegrate
2. Clean pods cache pod cache clean --all
3. Clean app build folders rm -rf ~/Library/Developer/Xcode/DerivedData/
4. Install pods again pod install

---
