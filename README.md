# DiscordMusicBot
A Discord Music bot so that I don't have to compete bandwidth with others. Eventually planned to be more than
a music bot.

v1.3.1

Written by Albion Fung

Current Features:
- Play from name or URL on Youtube
- Pause, skip, resume
- Fix incorrectly queued songs from the bot by going through other query results
- List songs in queue, remove songs from queue, clearing the queue
- Show now playing
- Shorthand commands for all commands
- A cache to keep the 100 most played song data, based on # of plays and recency. Reduces # of API calls

Upcoming Features:
Please see issues board.

Refs:
1. https://gabrieltanner.org/blog/dicord-music-bot
2. https://www.online-tech-tips.com/fun-stuff/how-to-make-your-own-discord-music-bot/
3. https://dev.to/galnir/how-to-write-a-music-command-using-the-discord-js-library-462f
4. https://stackoverflow.com
5. https://github.com (issues)

Reqs: Make sure to have a file config.json in the project's root folder. It must contain:
- prefix for the bot
- developerPrefix for the testing bot (can be the same as above prefix if not using a test bot)
- token for the bot
- developerToken for the testing bot (can be the same as above token if not using a test bot)
- API Key for Youtube API v3
- Path to save cache JSON file

You may freely distribute and use my code as long as your code is:
- open source
- credit me
- credit above refs when using my code
- follow the licenses of the modules used, unless you have your own replacement and do
not use the modules I use
- do not directly charge customers for using an application that uses this code base *
- have this same clause for the distribution and integration of your code

*: The code may still be used in a commercial operation as long as it is offered free.
   For example, you may make use of this code in an operation that makes a profit off of
   advertisements, as long as you do not charge users to pay for this code's functionality
   - including the functionality of this code "free" to certain tiers of purchase but not
   others is considered charging the user directly.
   
   Note: highWaterMark in ytdl's call gives it 32MB of buffer. If that's too much, please change it
   manually for your use case.

Contributors:
- Conanap
- cf-law 
   
__________________________________________________________________________________________________________
Change Log:

   v1.3.1 - 9 June, 2020
   - Refactored 'message' part of code, added list for non-music related commands that should work
   without bot in voice channel.

   v1.3 - 10 Apr, 2020
   - Implemented a Now Playing command.

   v1.2.3 - 10 Apr, 2020
   - Queries with URLs passed as an argument no longer sends a GET request to YouTube API v3. 
   
   v1.2.2 - 9 Apr, 2020
   - Remove song from queue and clear queue can now be done. 
   - Added some much needed comments.
    
   v1.2.1 - 9 Apr, 2020
   - List queue feature added. 
   
   v1.2 - 9 Apr, 2020
   - Implemented a caching functionality to reduce the number of API calls to YouTube API v3. 
   
   v1.1 - 8 Apr, 2020
   - Allow users to select the next best result from their last query if the songbot didn't pick the right one.
   - Fixed a bug where no results or error response from Youtube API crashes the bot.
   
   v1.0 - 8 Apr, 2020
   - Initial release.
