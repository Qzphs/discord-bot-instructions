# Instructions for using Discord bot

These instructions should work for Discord bot projects that I've recently
created.


## Create bot

If you don't have a Discord bot, you need to create one. You only need to do
this once.

[This guide](https://discordpy.readthedocs.io/en/stable/discord.html) is pretty
good and tells you everything you need to do; the only thing I'd do differently
is turn off **Public Bot**.


## Set up token and venv

You need to follow the instructions in this section the before you run the bot
code. You only need to do this once per project.

Copy your bot token from the
[Discord Developer Portal](https://discord.com/developers/applications). Create
a new text file in the project folder called **words.txt** and paste your token
into it.

Discord only lets you copy your bot token once. If you did this for a different
project already, you can just copy the token from the **words.txt** in that
project instead of the portal.

If you don't see a folder called **venv** inside of the project folder, then
you also need to run the three commands below.


### Create virtual environment

Windows:
```
py -m venv venv
```

macOS:
```
python3 -m venv venv
```

(**venv** folder should appear)


### Activate virtual environment

Windows:

```
venv\Scripts\activate.bat
```

macOS:

```
source venv/bin/activate
```

### Install discord.py

Windows:
```
py -m pip install discord.py
```

macOS:
```
python3 -m pip install discord.py
```


## Run bot code

You need to first activate the virtual environment unless you already did that
and haven't closed the terminal yet. It doesn't hurt to enter the command again
if you're not sure.

Then, run the bot.

Windows:
```
py -m bot.py
```

macOS:
```
python3 -m bot.py
```


### Sync bot commands

You might need to do this if it's your first time running the bot, or if the
last bot you ran was a different bot. Use this command instead of the normal run
command if there's no error message, but the bot's commands don't show up on
Discord.

Windows:
```
py bot.py --sync
```

macOS:
```
python3 bot.py --sync
```

If this still doesn't fix the missing commands, then try restarting your own
Discord.


### Quit bot

You should use the bot's **/quit** command if possible.

If that's not working for some reason, you can also force quit the bot on your
side by typing Ctrl-C into the terminal (same for both Windows and macOS).
