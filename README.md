<p style="text-align: center">
 <img width="160" src="https://i.ibb.co/SJVMwM0/icon.png" alt="icon" border="0" /><br/>
  <h2 align="center">Juan Valdez App</h2>
</p>

### Appendix

- [📚Description](#description)
- [✅ Previous requirements](#previous-requirements)
- [📥 Clone Project](#clone-proyect)
- [📌Environment variables](#environment-variables)
- [📁Work Environments](#work-environments)
- [📲 Android Set Up](#android-set-up)
- [🍎 iOS Set Up](#ios-set-up)
- [📲 Generate Android APK](#generate-android-apk)
- [📲 Generate iOS TestFlight](#generate-ios-testflight)
- [❓ FAQ](#faq)

---

#### 📚 Description

Juan Valdez app is a project belonging to the sales area, specifically to coffee products..

---

#### ✅ Previous requirements

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

#### 📥 Clone Project

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

#### 📌 Environment variables

1. Paste the development variables at location:

> enviroments/dev

2. Paste the production variables at location:

> enviroments/prod

You must request the firebase and keystores environment variables from tech lead.

---

#### 📁 Work Environments

To change the environment you must run:

1. For Development:

```bash
  ./switchenv.sh dev
```

3. For Production:

```bash
  ./switchenv.sh prod
```

#### 📲 Android Set Up

Paste the keyStores at location:

> android/app

Run command the follow command to start the server:

```bash
  npm run android
```

---

#### 🍎 iOS Set Up

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

### 📲 Generate Android .apk

Run the follow command:

```bash
  npm run release
```

The generated apk must be at location:

> android/app/build/outputs/apk/release

### 📲 Generate iOS TestFlight

---

### ❓ FAQ

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
