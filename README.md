AJislive3 is a React Native/Expo communication app.

Included: chat UI, Supabase realtime/chat service, Supabase document-storage service, voice/video call entry points, database schema and Row Level Security, environment template.

Backend setup: create a Supabase project; run supabase/schema.sql; create a Storage bucket named documents and configure storage policies; copy .env.example to .env and add the project URL and anon key. For real video/voice, configure LiveKit/WebRTC and a secure server-side token endpoint. Never put a LiveKit API secret in the mobile app.

The repository contains no private service keys.
