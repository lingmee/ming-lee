# El Discord
An alert plugin using Discord webhooks.

# What?

El Discord will mention you on Discord when certain scenarios happen in game:
* Someone says "bot" in the game chat.
* Your account dies.
* Your account logs out.
* Your account has been idle for longer than a minute.

# Setup

## Creating a Discord server and getting the Webhook URL.
![Add a Server](https://cdn.discordapp.com/attachments/782635296030064660/813045867313496124/unknown.png)

Firstly, create a new server. (If you already have one skip this step)

![Server Settings](https://cdn.discordapp.com/attachments/782635296030064660/813046287238692874/unknown.png)

Next, open up your Server Settings.

![Integrations Tab](https://cdn.discordapp.com/attachments/782635296030064660/813046480759423036/unknown.png)

Then, open up the Integrations tab.

![Create Webhook](https://cdn.discordapp.com/attachments/782635296030064660/813046533024514048/unknown.png)

On this page click `Create Webhook`.

![Webhook Setup](https://cdn.discordapp.com/attachments/782635296030064660/813046621516202024/unknown.png)

Choose which channel you would like the messages to go to, default: `#general`.

![Copy Webhook](https://cdn.discordapp.com/attachments/782635296030064660/813046707436388362/unknown.png)

When you are finished select 'Copy Webhook URL'. You will be given a link that looks something similar to this:
`https://discord.com/api/webhooks/813046551836360774/yLOQ4JH35nhxDd7w0DR70XPmQHYcHQZrfZs4vrbDgBXQ5IqcENSEgs6EwlZopQ9-bmZ3`

## Getting your Discord User ID

![User Settings](https://cdn.discordapp.com/attachments/782635296030064660/813046882490253382/unknown.png)

At the bottom left of the Discord client, click on the cog next to your username to go to `User Settings`.

![Copy ID](https://cdn.discordapp.com/attachments/782635296030064660/813046919320436746/unknown.png)

On `MY ACCOUNT`, click the three dots and then `Copy ID`. Your user ID will look similar to this:
`154694161105289223`