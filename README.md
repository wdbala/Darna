<div align="center">
<img width="1200" height="475" alt="GHBanner" src="https://ai.google.dev/static/site-assets/images/share-ais-513315318.png" />
</div>

# Darna

Darna is a React community app for Sudanese diaspora groups. Authentication and application data use Firebase Authentication and Cloud Firestore.

## Firebase setup

1. Create a Firebase project and register a Web app.
2. Enable Email/Password under Authentication sign-in providers.
3. Create a Cloud Firestore database.
4. Copy `.env.example` to `.env.local` and fill in the Firebase Web app values.
5. Select the Firebase project with `firebase use <project-id>` and publish the rules with `firebase deploy --only firestore:rules`, or paste `firestore.rules` into the Firebase Console.

The Web app configuration is public client configuration, not a service-account key. Never put Admin SDK credentials in `VITE_*` variables. The current Sudanese-community checkbox is self-attestation; it does not verify identity.

## Run locally

Prerequisite: Node.js 22 or newer.

```sh
npm install
npm run dev
```

## Checks

```sh
npm test
npm run lint
npm run build
```
