# Walkup DJ

Walk-up music for youth baseball. Walkup DJ announces each batter by name and number in the phone's voice, then plays their walk-up clip from Spotify through any Bluetooth speaker — following your batting order.

## Features

- **Roster** — name, number, optional pronunciation, and a Spotify song with a custom start point and clip length
- **Lineup** — set and reorder the batting order for each game
- **Game screen** — one tap to announce and play; auto-advances to the next batter
- **Announcer** — customizable wording, voice (English or French) and speaking speed
- **Works on any phone** — add it to your home screen; no app store needed
- **Backup** — export and import your roster as a file

## Requirements

- Spotify Premium
- The Spotify app installed on the phone connected to your speaker

## Setup

1. **Publish with GitHub Pages.** In this repository, go to **Settings → Pages**, set the source to **Deploy from a branch**, and choose `main` / root. Your app will be at `https://<your-username>.github.io/walkup-dj/`.
2. **Register a Spotify app.** At [developer.spotify.com/dashboard](https://developer.spotify.com/dashboard), create an app:
   - **Redirect URI:** your GitHub Pages address exactly, including the trailing slash
   - **API:** Web API
   - Copy the **Client ID**, and add your Spotify account's email under **User Management**
3. **Connect.** Open the app on your phone, go to **Settings**, paste the Client ID and tap **Connect Spotify**. Then use **Share → Add to Home Screen**.

## Game day

1. Pair your phone with the Bluetooth speaker.
2. Open the Spotify app and play any song for a second so it's awake.
3. Open Walkup DJ, tap **📡 Speaker** to confirm your phone is selected, and tap **▶ Announce & Play** for each batter.

If a song doesn't start, Spotify has probably gone to sleep in the background — reopen it and try again.

## How it works

Walkup DJ is a single HTML file with no server. It signs in to Spotify using the PKCE flow and remote-controls playback on your phone's Spotify app through the Spotify Web API. Announcements use the browser's built-in text-to-speech. Your roster is stored on your device.

## Note on music licensing

Streaming services license music for personal use. Playing music publicly at games falls under public performance licensing (SOCAN / Re:Sound in Canada). Many leagues and facilities already hold these licences — check with yours.
