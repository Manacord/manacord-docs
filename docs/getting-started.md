## Navigating
?> The user permissions required to run certain commands will be mentioned like <span class="user-permissions">this</span>.                                     


## Basic Configuration
?> Use the **`/settings`** command to configure the bot easily.

This guide will cover everything you need to do to get started with the basics of what carlbot offers.


+ ### Logs
By default, Manacord will log **nothing**. This isn't always what you want so let's say that you don't care about message edits.

The `/settings set log <type> <channel>` command turns on certain logs.

The `/settings set log-aio` command turns on everything at once. The bot will automatically create a logging category with 6 log channels and cleverly divide all logs between these channels.

Another thing you can do is ignore logs only in certain channels. For that you can use `/settings set log-ignore <channel>` to ignore all events from that channel. Logs are very customizable so make sure to head over that section for full information.


+ ### Team Roles
By using `/settings set perms team <role>` you can set a exsiting role as staff role. You may want to add more than one role.

!> At least one role must be set in order to use the Temp Voice system.

+ ### Member Role
By using `/settings set perms member <role>` you can set a exsiting role as member role.

!> Also necessary for the temp voice system.

+ ### Mute Role
By using `/settings set perms mute` you can set a exsiting role as mute role.
By using `/settings create muterole` you can create a role with the permission <span style="color: red;">Send Messages</span> denied in every channel. Users can now be muted using `/mod mute <@member> [time] [reason]`. The default time is 48 hours for a time.

!> Also necessary for the temp voice system.<br>
Any future channels created will not be covered by Mute Role.


?> But more on the temp voice system later.


+ ### Welcome Message
You can set the welcome message that would be sent in the set channel using `/settings set welcome`.


+ ### Prefix
By default, Manacord responds to `m?` *(In rare cases)* prefixes as well as `/` slash commands. To make the bot respond to another prefix, `!` for example, you can use `/settings set prefix !`.


This is far from everything Manacord has to offer but at this point you will have set up the crucial things that you can set up.


## FAQ

### How do I get the Message ID? {docsify-ignore}
**Right Click** the message and select **Copy ID**

?> To enable this option you would need to do the following:<br>
Discord Settings > Advanced > Developer Mode > Enable

![Discord ID](_images/faq_discordid.png ':size=75%')


### Why does the bot complain about requiring more permissions? {docsify-ignore}
The way Discord decides if you can add a role or not is based on two things:
* Does the Member adding the role have Administrator permission?
* Is the member trying to add a role higher in the role heirarchy than the bot's role?

To avoid problems, it is best to set the permissions to <span style="color: red;">administrator</span> by default.


### What is the drama channel? {docsify-ignore}
This is a feature that aims to streamline your server's moderation. Automod is nice but it is not perfect as sometimes false positives happen. This feature was made for that exact reason. You need to:
- Set up the drama channel with the command `/settings set drama <channel>`.

![Drama Channel](_images/faq_drama.png ':size=75%')
