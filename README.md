# Discord-Bot

**ANYTHING WITH [] MEANS IT IS WHATEVER YOU WANT**

import discord
from discord import client
from discord import channel
from discord import member
from discord.client import Client
from discord.ext import commands
import json
from webserver import keep_alive
import os

###### Prefix

bot = commands.Bot(command_prefix='[PREFERED PREFIX]'))

###### Status and custom status

@bot.event
async def on_ready():
    activity = discord.Game(name="[CUSTOM_STATUS]", type=3)
    await bot.change_presence(status=discord.Status.online, activity=activity)
    print("Bot is ready!")

###### Purge Command
@bot.command()
@commands.has_any_role("[WHATEVER ROLES YOU WANT TO INSERT (e.g "owner, admin"]")
async def rid(ctx, amount=10):
    await ctx.channel.purge(limit=amount)
    
###### Bot Commands

**Replying to the users message**
@bot.command()
async def [](ctx):
    await ctx.reply("[]")
    
**Just sending a message**
@bot.command()
async def [](ctx):
    await ctx.send("[]")
    
###### Entering the bots token (after setting it up(if you want to know how to use [this tutorial from 00:00 to 00:32](https://www.youtube.com/watch?v=Gqurhm2QxA0)))
bot.run('[INSERT TOKEN HERE]')
