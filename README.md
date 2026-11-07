# Zune

A local music player that runs entirely in your browser. No server, no accounts, no uploads: your tracks stay on your device, stored in the browser itself. The look is inspired by the Xbox 360 "blades" dashboard, and the app opens with a Windows 8.1-style launch animation.

**Languages:** English (default) and Ukrainian (switch with the `EN` / `UA` button next to the logo).

<img width="1919" height="947" alt="image" src="https://github.com/user-attachments/assets/84c17a0c-eb38-44ad-9084-9f4e41af7a28" />


## Features

- **Local library.** Add audio files with the button or by dragging them into the window (mp3, flac, ogg, wav, m4a, aac, opus). Files are saved in the browser's IndexedDB, so they are still there after a reload.
- **Duplicate filter.** A track is skipped if a song with the same artist and title already exists (case, brackets and words like "official" or "lyrics" are ignored), or if a file has the same size and duration. The first copy is kept. **System → Remove duplicates** cleans an existing library the same way.
- **Playlists.** Create, open, play and delete playlists. Add a track with the ＋ button on its row, or tick several tracks at once inside a playlist.
- **Favorites.** Heart any track to collect it in the favorites blade.
- **Player.** Play/pause, next/previous, seek, volume, shuffle and repeat (off / all / one). Media keys and the lock-screen controls work where the browser supports them.
- **Search** across your library.
- **Profile.** Change your name, avatar and interface color (five themes), see your stats, and collect Gamerscore and achievements.
- **Responsive layout** for phones.

## Controls

| Key | Action |
|---|---|
| ← / → | Switch blade |
| ↑ / ↓ | Move selection |
| Enter | Select (play / open) |
| Esc / Backspace | Back (closes an open playlist) |
| Space | Play / pause |
| Y | Heart the current track |

Filenames named `Artist - Title.mp3` are split into artist and title automatically. Anything else is shown as the title with an unknown artist.

## Secrets

There are hidden commands you can type on the keyboard (not into a text field). Type `help` to see the list.

## Where the data lives

| Data | Storage |
|---|---|
| Tracks and playlists | IndexedDB (`metro-music`) |
| Profile, achievements, language | `localStorage` |

Everything stays in the browser you used. A different browser or device starts with an empty library, and clearing the site's data removes everything. There is no sync or backup, so keep your original files.

## Running it

- **Online:** open the published link.
- **Locally:** save the page as a single `.html` file and open it in any modern browser (Chrome, Edge, Firefox, Safari). It has no dependencies and needs no internet connection.

## Limits

- Browser storage quotas apply. A very large library may not fit, and the **System** blade shows how much space your tracks use.
- Duplicates are detected by name, size and duration, not by sound. Two different recordings of the same song with different filenames will both be kept.
- Cover art is generated from the track name. Embedded cover images are not read.
- Private or incognito windows may not keep data after they are closed.

