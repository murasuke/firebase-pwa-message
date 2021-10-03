# PWA始めの一歩(firebase-pwa-message)

## cra-template-pwa-typescriptテンプレートでreactのひな形を作成する

```bash
npx create-react-app pwa-proto --template cra-template-pwa-typescript
```
## firebaseコンソールでプロジェクトを作成する

* プロジェクトを新規作成
* アプリを追加
* Firestoreの作成


## firebaseの設定を行う

* firebase-toolsをインストール後にログイン
```bash
$ npm install -g firebase-tools
```
## Firebase CLIで、Firebase プロジェクトを初期化

```
$ firebase init

     ######## #### ########  ######## ########     ###     ######  ########
     ##        ##  ##     ## ##       ##     ##  ##   ##  ##       ##
     ######    ##  ########  ######   ########  #########  ######  ######
     ##        ##  ##    ##  ##       ##     ## ##     ##       ## ##
     ##       #### ##     ## ######## ########  ##     ##  ######  ########

You're about to initialize a Firebase project in this directory:

  C:\Users\t_nii\Documents\git\firebase\pwa-message

? Are you ready to proceed? Yes
? Which Firebase features do you want to set up for this directory? Press Space to select features, then Enter to confirm your choices.
 ( ) Realtime Database: Configure a security rules file for Realtime Database and (optionally) provision default instance
 (*) Firestore: Configure security rules and indexes files for Firestore
>(*) Functions: Configure a Cloud Functions directory and its files
 (*) Hosting: Configure files for Firebase Hosting and (optionally) set up GitHub Action deploys
 ( ) Hosting: Set up GitHub Action deploys
 ( ) Storage: Configure a security rules file for Cloud Storage
(Move up and down to reveal more choices)

=== Project Setup

First, let's associate this project directory with a Firebase project.
You can create multiple project aliases by running firebase use --add,
but for now we'll just set up a default project.

? Please select an option:
> Use an existing project
  Create a new project
  Add Firebase to an existing Google Cloud Platform project
  Don't set up a default project

? Select a default Firebase project for this directory:
  chousei-firebase-36769 (chousei-firebase)
  myfirstproject-2b5c3 (myFirstProject)
> pwa-messaging-d01da (pwa-messaging)

=== Firestore Setup

Firestore Security Rules allow you to define how and when to allow
requests. You can keep these rules in your project directory
and publish them with firebase deploy.

? What file should be used for Firestore Rules? (firestore.rules)

Firestore indexes allow you to perform complex queries while
maintaining performance that scales with the size of the result
set. You can keep index definitions in your project directory
and publish them with firebase deploy.

? What file should be used for Firestore indexes? (firestore.indexes.json)

=== Functions Setup

A functions directory will be created in your project with sample code
pre-configured. Functions can be deployed with firebase deploy.

? What language would you like to use to write Cloud Functions? TypeScript
? Do you want to use ESLint to catch probable bugs and enforce style? No
+  Wrote functions/package.json
+  Wrote functions/tsconfig.json
+  Wrote functions/src/index.ts
+  Wrote functions/.gitignore
? Do you want to install dependencies with npm now? No

=== Hosting Setup

Your public directory is the folder (relative to your project directory) that
will contain Hosting assets to be uploaded with firebase deploy. If you
have a build process for your assets, use your build's output directory.

? What do you want to use as your public directory? build
? Configure as a single-page app (rewrite all urls to /index.html)? Yes
? Set up automatic builds and deploys with GitHub? No
+  Wrote build/index.html

i  Writing configuration info to firebase.json...
i  Writing project information to .firebaserc...

+  Firebase initialization complete!

```

## プロジェクトをビルドして動作することを確認する

```bash
npm run start
```

## firebase hostingにデプロイ


```json
  "scripts": {
    "deploy": "npm run -s build && firebase deploy --only hosting",
  }
```

```bash
npm run deploy
```
