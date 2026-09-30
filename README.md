# AJislive3

AJislive3 is an Expo React Native messaging app foundation with:

- Email/password signup and login
- Supabase Realtime chat
- Document picker + Supabase Storage document sharing
- Video/voice call buttons prepared for LiveKit
- Dark AJislive3 UI

## Supabase setup

1. Create a Supabase project.
2. Open **SQL Editor** and run `supabase/schema.sql`.
3. The SQL creates the `documents` public bucket and its upload/read policies.
4. In the Expo environment, set:
   - `EXPO_PUBLIC_SUPABASE_URL`
   - `EXPO_PUBLIC_SUPABASE_PUBLISHABLE_KEY` (preferred) or `EXPO_PUBLIC_SUPABASE_ANON_KEY`
5. Start with `npm install` then `npx expo start`.

Do not commit private service-role keys or database passwords.

## Calling

The app UI is prepared for LiveKit voice/video calling. Actual WebRTC calling requires a LiveKit server and a secure backend token endpoint. LiveKit's Expo SDK uses native modules, so a development build is required rather than Expo Go.

See the official docs:
- https://supabase.com/docs/guides/getting-started/quickstarts/expo-react-native
- https://docs.livekit.io/transport/sdk-platforms/expo/

## Current status

Chat and document-sharing code is connected to Supabase and will work after the Supabase project/environment is configured. Voice/video requires LiveKit credentials plus a server-side token endpoint; never put the LiveKit API secret in the mobile app.
