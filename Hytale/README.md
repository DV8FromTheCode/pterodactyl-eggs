# Unofficial Hytale Pterodactyl Egg

This is a custom Pterodactyl egg designed to host a **Hytale** server. It utilizes the official Hytale Downloader to handle server installation and updates.

## ⚠️ Important Disclaimer
**Hytale is currently unreleased.** 
This egg is designed based on the available `hytale-downloader` tool and official documentation. However, because the game servers are not yet public:
- **Authentication required:** You cannot fully complete the installation process without a valid Hytale account that has official access to the game.
- **Testing is limited:** The egg installs dependencies and attempts to run the downloader, but full end-to-end functionality (server boot, gameplay) cannot be verified until you have valid access.

## Features
- **Java 25 Support:** Uses the `ghcr.io/ptero-eggs/yolks:java_25` image.
- **Automated Installation:** Script automatically downloads the Hytale Downloader, installs dependencies (`curl`, `unzip`), and attempts to fetch server files.
- **Alpine Linux:** Lightweight installation container for faster deployment.

## Installation
1. Download `egg-hytale.json`.
2. Navigate to your Pterodactyl Panel **Admin View**.
3. Go to **Nests** > **Import Egg**.
4. Select the `egg-hytale.json` file and import it into the desired Nest.

## Configuration
| Variable | Description | Default |
|----------|-------------|---------|
| `SERVER_JARFILE` | The name of the server jar file. | `HytaleServer.jar` |
| `ASSETS_PATH` | Path to the assets zip file. | `Assets.zip` |
| `PATCHLINE` | specific download channel (e.g. `pre-release`). | *(empty)* |
