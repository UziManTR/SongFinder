# SongFinder 🎧

**A dating app, but for music.** Like, pass, and build a ranked playlist from your taste.

## Features
- Animated, mobile-friendly interface
- Google OAuth sign-in
- Real music-video search through YouTube Data API v3
- Like / dislike / skip controls and live stats
- Playlist size selector (10–50)
- Create a private YouTube playlist from liked results

## Enable the site
On GitHub mobile, open **UziManTR/SongFinder → Settings → Pages**. Under **Build and deployment**, select **Deploy from a branch**, branch `main`, folder `/ (root)`, then Save. Wait for the Pages URL to appear.

## One-time Google setup
1. Open [Google Cloud Console](https://console.cloud.google.com/) and create a project.
2. Open **APIs & Services → Library**, find **YouTube Data API v3**, and enable it.
3. Open **Google Auth Platform** (or **APIs & Services → OAuth consent screen**) and configure the consent screen. If the app is in Testing mode, add your own Google account as a test user.
4. Create an **OAuth client ID** with application type **Web application**.
5. Add this authorized JavaScript origin: `https://uzimantr.github.io` (the GitHub Pages site must use this origin).
6. Copy the OAuth **Client ID** only. Do not paste a client secret anywhere in this public repository.

## Connect in SongFinder
1. Open the published GitHub Pages site.
2. Paste the OAuth Client ID into the field and tap **Connect Google**.
3. Approve the requested YouTube permission.
4. Search an artist, genre, or mood. Like the results you want.
5. Tap **Create YT playlist**. It creates a private playlist in your YouTube account. It should show in YouTube Music under Library → Playlists when the selected videos are music tracks.

## Notes
- The browser stores the Client ID locally. OAuth access tokens are kept in memory and are not written to the repository.
- This static front-end uses the YouTube Data API. API quota, Google consent-screen restrictions, account settings, and video availability can affect results.
- YouTube playlist items are videos, not guaranteed official audio tracks. Review the playlist after creation.
- The playlist size control chooses up to 10–50 liked results; it cannot create more songs than you have liked.
