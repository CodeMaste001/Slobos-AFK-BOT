# Minecraft AFK Bot

A Mineflayer-based bot that keeps an Aternos Minecraft server online 24/7 by staying connected and preventing idle shutdowns.

## How to run

**Start:** Click the Run button (or use the "Start application" workflow). The bot connects automatically.

**Dashboard:** The preview pane shows a live status page with connection status, uptime, and bot coordinates.

## Configuration

All settings are in `settings.json`:

| Setting | Description |
|---|---|
| `server.ip` | Aternos server address |
| `server.port` | Server port |
| `server.version` | Minecraft version (e.g. `"1.21.11"`) |
| `bot-account.username` | Bot's in-game name |
| `utils.anti-afk` | Jumps periodically to avoid AFK kicks |
| `utils.chat-messages` | Optional recurring chat messages |
| `utils.periodic-rejoin` | Leaves and rejoins on a random interval |
| `discord` | Discord webhook notifications (set `enabled: true` and add `webhookUrl`) |

## Stack

- **Runtime:** Node.js 22
- **Bot:** [Mineflayer](https://github.com/PrismarineJS/mineflayer)
- **Pathfinding:** mineflayer-pathfinder
- **Web server:** Express (port 5000) — serves the status dashboard and `/health` endpoint

## User preferences

<!-- Add any preferences here -->
