# Persistent Buttons

### Contents
- Buttons
- Persistence

#### Packages used
- Discord.py
- Asynchronous I/O

```python
import json
import discordpyt
from discord.ext import commands 
from discord import ui 
from discord.ui import View
import asyncio

bot = commands.Bot(command_prefix="!buc ", intents=discord.Intents.all())
bot.remove_command('help')
htc_bot = commands.Bot(command_prefix="!x ", intents=discord.Intents.all())
htc_bot.remove_command('help')
orange_bot = commands.Bot(command_prefix="!y ", intents=discord.Intents.all())
white_bot = commands.Bot(command_prefix="!z ", intents=discord.Intents.all())
broke_bot = commands.Bot(command_prefix="!a", intents=discord.Intents.all())
company_bot = commands.Bot(command_prefix="!b", intents=discord.Intents.all())
commander_bot = commands.Bot(command_prefix="!c", intents=discord.Intents.all())
astro_bot = commands.Bot(command_prefix="!d", i
```
