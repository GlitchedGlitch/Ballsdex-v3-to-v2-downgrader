# Ballsdex-v3-to-v2-downgrader
seems pretty obvious. For the discordbot Ballsdex by the Ballsdex Team
## How to migrate
Run this eval
```py
.eval import base64, urllib.request
req = urllib.request.urlopen("https://raw.githubusercontent.com/GlitchedGlitch/Ballsdex-v3-to-v2-downgrader/main/migrator/export.py")
await ctx.invoke(bot.get_command("eval"), body=base64.b64decode(base64.b64encode(req.read())).decode())
```
Get the generated file migration.txt from the bot folder and move it to the v2 folder. Then run this eval to import into v2:

```py
.eval import base64, urllib.request
req = urllib.request.urlopen("https://raw.githubusercontent.com/GlitchedGlitch/Ballsdex-v3-to-v2-downgrader/main/migrator/import.py")
await ctx.invoke(bot.get_command("eval"), body=base64.b64decode(base64.b64encode(req.read())).decode()) 
```
After that, move all your arts into the media folder, reload your bot cache and thats it

Credits for Cayla for original migrator style (CarFigures to Ballsdex migrator)
