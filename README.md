PRSEK is a custom-built Twitch bot designed to seamlessly interface with the Songify Windows application, enabling real-time song requests and playback control directly from a Twitch chat. This bot enhances viewer engagement by allowing your audience to influence the music played during your live streams.

Features
Song Requests: Viewers can request songs using chat commands.

Queue Management: Maintains a queue of requested songs and plays them in order.

Moderation Tools: Streamers and moderators can blacklist songs, ban users, and manage the queue.

Real-Time Feedback: Provides instant feedback in chat for song requests, skips, and playback status.

Customizable Commands: Configure command prefixes, cooldowns, and permissions.

Error Handling: Robust error handling and logging for troubleshooting.

Installation
Prerequisites
Python 3.8 or higher

A Twitch account with a registered bot account

The Songify Windows application installed and running

Twitch Developer credentials (Client ID and Client Secret)

Steps
Clone the Repository:

```bash
Copy
git clone https://github.com/yourusername/PRSEK.git
cd PRSEK
Install Dependencies:

```bash
Copy
pip install -r requirements.txt
Configure the Bot:

Rename config.example.json to config.json.

Fill in the required fields:

```json
{
  "twitch_client_id": "YOUR_TWITCH_CLIENT_ID",
  "twitch_client_secret": "YOUR_TWITCH_CLIENT_SECRET",
  "twitch_bot_username": "YOUR_BOT_USERNAME",
  "twitch_bot_token": "YOUR_BOT_OAUTH_TOKEN",
  "twitch_channel": "YOUR_TWITCH_CHANNEL",
  "songify_api_key": "YOUR_SONGIFY_API_KEY",
  "command_prefix": "!",
  "max_queue_length": 10,
  "request_cooldown": 30
}

```Run the Bot:

```bash
Copy
python prsek.py
Usage
Viewer Commands
!songrequest <song_name> or !sr <song_name> - Request a song.

!queue or !q - View the current song queue.

!currentsong or !nowplaying - Display the currently playing song.

!skip - Vote to skip the current song (if enabled).

!mysong - Check the position of your requested song in the queue.

!help - List available commands.

Streamer/Moderator Commands
!addsong <song_name> - Manually add a song to the queue.

!skipsong - Skip the current song.

!clearsong <song_name> - Remove a specific song from the queue.

!clearqueue - Clear the entire song queue.

!pause - Pause the current song.

!resume - Resume playback.

!volume <level> - Adjust the volume (if supported).

!blacklist <song_name> - Blacklist a song.

!unblacklist <song_name> - Remove a song from the blacklist.

!banuser <username> - Ban a user from making requests.

!unbanuser <username> - Unban a user.

!setcooldown <seconds> - Set a cooldown for song requests.

!setmaxqueue <number> - Set the maximum queue length.

!togglecommands - Enable or disable viewer commands.

!reloadconfig - Reload the bot's configuration.

Admin Commands
!restartbot - Restart the bot.

!updatebot - Check for and apply updates.

!shutdownbot - Shut down the bot.

!logs - View or export bot logs.

Configuration
The bot's behavior can be customized via the config.json file. Key settings include:

Command Prefix: Change the prefix for commands (e.g., !, ?).

Rate Limits: Adjust rate limits for chat messages and API requests.

Permissions: Set permissions for commands (viewer, mod, streamer-only).

Logging: Enable or disable logging and specify log file locations.

Contributing
We welcome contributions to PRSEK! If you'd like to contribute, please follow these steps:

Fork the repository.

Create a new branch for your feature or bugfix.

Commit your changes and push to your fork.

Submit a pull request with a detailed description of your changes.

Support
If you encounter any issues or have questions, please:

Open an issue on GitHub.

Join our Discord server for community support.

License
PRSEK is licensed under the MIT License. See the LICENSE file for details.

Acknowledgements
TwitchIO - For the Twitch API interaction library.

Songify - For the music playback application.

You! - For using PRSEK and supporting the project!

Happy Streaming! 🎶
