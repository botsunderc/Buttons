# Buttons

### Contents
- Buttons
- Disabling Buttons

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
```
The prefix for our Source Bot is `!source `.

```python
# The button class
class Button(discord.ui.View):
    @discord.ui.button(label="Button", row=0)
    async def on_submit(self, interaction: discord.Interaction, button: discord.ui.Button):
        member = guild.get_member(interaction.user.id)

# Command to evoke the button
@source_bot.command(name="button")
async def buttons(ctx):
    await ctx.send(view=Button())
```
Naturally, the button will fail as it leads to nothing. 

<img src="/Images/button1.png">
<img src="/Images/failed.png">

Now, let's make it respond when a user presses the button. 
```python
class Button(discord.ui.View):
    @discord.ui.button(label="Button", row=0)
    async def button_callback1(self, interaction: discord.Interaction, button: discord.ui.Button):
        await interaction.response.send_message("hi")
```
<img src="/Images/response.png">

There are multiple styles of buttons available, as you can see in Pycord's documentations: https://guide.pycord.dev/interactions/ui-components/buttons

<img src="/Images/pycord.png">

- Primary - Blue 
- Secondary - Grey
- Success - Green 
- Danger - Red


```python
class Button(discord.ui.View):

    @discord.ui.button(label="Button", style=discord.ButtonStyle.primary, row=0)
    async def button_callback1(self, interaction: discord.Interaction, button: discord.ui.Button):
        await interaction.response.send_message("hi")

    @discord.ui.button(label="Button", style=discord.ButtonStyle.secondary, row=0)
    async def button_callback2(self, interaction: discord.Interaction, button: discord.ui.Button):
        await interaction.response.send_message("hi")

    @discord.ui.button(label="Button", style=discord.ButtonStyle.success, row=0)
    async def button_callback3(self, interaction: discord.Interaction, button: discord.ui.Button):
        await interaction.response.send_message("hi")

    @discord.ui.button(label="Button", style=discord.ButtonStyle.danger, row=0)
    async def button_callback4(self, interaction: discord.Interaction, button: discord.ui.Button):
        await interaction.response.send_message("hi")
```

<img src="/Images/four.png">
