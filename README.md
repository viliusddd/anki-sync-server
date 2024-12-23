# Self-Hosted Anki Sync Server

# Reason behind the repo

I need to sync my Mac and iPhone without an internet connection.
Bonus: decks can be backed up to your cloud of choice (when your Mac/PC returns online). Set `USER_BASE` to your cloud dir.

# Requirements

- Docker Desktop
- Anki Desktop

# Setup

1. Clone this repo.
2. Rename `.env.example` to `.env`, and change the default values:
   1. `USER_BASE` is where your synced data will be saved. If you want, for example, to save your files to iCloud, then you can have `SYNC_BASE='/Users/<your-username>/Library/Mobile Documents/com~apple~CloudDocs/AnkiSync'`.
3. Run `docker compose up`.
4. Go to Anki App -> Preferences... -> Syncing -> Self-hosted sync server: http://localhost:3033 . Use `USER_PORT` with server url. `SYNC_PORT` is used only inside the container.
5. Press `Sync` in the main app window. It will ask for username details: input details from `SYNC_USER1`.

> Official guide: https://docs.ankiweb.net/sync-server.html
