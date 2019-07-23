# TwitchDeathCounter
Twitch Bot that allows chat to keep track of a Death Counter 

---

# Explanation
When the bot has started, it will start listening to chat messages in the channel listed in the settings.txt file. People in this chat will be able to monitor and upkeep a death counter, so that they may follow the progress of the streamer.

---
# Usage
Commands:
<pre><b>!deaths/!deathcounter
</b></pre>
Get the current death counter. Everyone can perform this command.
<pre><b>!death
</b></pre>
Increment the death counter. Subs onwards can perform this command.
<pre><b>!setdeaths 8
</b></pre>
Set the death counter to 8 (for this example). Mods onwards can use this command.

There is a japanese mode, and a normal mode. The former was designed for the game [Sekiro: Shadows Die Twice](https://en.wikipedia.org/wiki/Sekiro:_Shadows_Die_Twice), and the outputs will look like:
<pre><b>Death Counter: 二十六 (26)</b></pre>
If Japanese mode is false, the result will look like:
<pre><b>Death Counter: 26</b></pre>

You can also set a prefix, which allows you to change the Death Counter into a streamer or boss specific counter:
<pre><b>Nameless King Death Counter: 26</b></pre>

---

# Requirements
* TwitchWebsocket

Install this using `pip install git+https://github.com/CubieDev/TwitchWebsocket.git`

This last library is my own [TwitchWebsocket](https://github.com/CubieDev/TwitchWebsocket) wrapper, which makes making a Twitch chat bot a lot easier.
This repository can be seen as an implementation using this wrapper.

---

# Settings
This bot is controlled by a settings.txt file, which looks like:
```
{
    "Host": "irc.chat.twitch.tv",
    "Port": 6667,
    "Channel": "#<channel>",
    "Nickname": "<name>",
    "Authentication": "oauth:<auth>",
    "Prefix": "",
    "Japanese": false
}
```

| **Parameter**        | **Meaning** | **Example** |
| -------------------- | ----------- | ----------- |
| Host                 | The URL that will be used. Do not change.                         | "irc.chat.twitch.tv" |
| Port                 | The Port that will be used. Do not change.                        | 6667 |
| Channel              | The Channel that will be connected to.                            | "#CubieDev" |
| Nickname             | The Username of the bot account.                                  | "CubieB0T" |
| Authentication       | The OAuth token for the bot account.                              | "oauth:pivogip8ybletucqdz4pkhag6itbax" |
| Prefix | What should be in front of "Death Counter" in the output. Eg a boss or a streamer. | "Nameless King" |
| Japanese         | If the Japanese output mode should be used. (See Usage) | false |

*Note that the example OAuth token is not an actual token, but merely a generated string to give an indication what it might look like.*

I got my real OAuth token from https://twitchapps.com/tmi/.

---

# Other Twitch Bots

* [TwitchGoogleTranslate](https://github.com/CubieDev/TwitchGoogleTranslate)
* [TwitchMarkovChain](https://github.com/CubieDev/TwitchMarkovChain)
* [TwitchRhymeBot](https://github.com/CubieDev/TwitchRhymeBot)
* [TwitchCubieBotGUI](https://github.com/CubieDev/TwitchCubieBotGUI)
* [TwitchCubieBot](https://github.com/CubieDev/TwitchCubieBot)
* [TwitchUrbanDictionary](https://github.com/CubieDev/TwitchUrbanDictionary)
* [TwitchWeather](https://github.com/CubieDev/TwitchWeather)
* [TwitchSuggestDinner](https://github.com/CubieDev/TwitchSuggestDinner)
* [TwitchPickUser](https://github.com/CubieDev/TwitchPickUser)
* [TwitchSaveMessages](https://github.com/CubieDev/TwitchSaveMessages)
* [TwitchMMLevelPickerGUI](https://github.com/CubieDev/TwitchMMLevelPickerGUI) (Mario Maker 2 specific bot)
* [TwitchMMLevelQueueGUI](https://github.com/CubieDev/TwitchMMLevelQueueGUI) (Mario Maker 2 specific bot)
* [TwitchPackCounter](https://github.com/CubieDev/TwitchPackCounter) (Streamer specific bot)
* [TwitchDialCheck](https://github.com/CubieDev/TwitchDialCheck) (Streamer specific bot)
* [TwitchSendMessage](https://github.com/CubieDev/TwitchSendMessage) (Not designed for non-programmers)
