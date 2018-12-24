# SlugBot
Slugbot is a Discord and Twitch.tv bot primarily focused on, but not limited to, enhancing Dark Souls communities. 
SlugBot Also covers general admin functionality, with Discord server logging, muting, role assignment, Twitch stream notifications, follows and more!

If you'd like to support SlugBot development you can buy The Slug a ~~beer~~ coffee on ko-fi.com!
[![ko-fi](https://www.ko-fi.com/img/donate_sm.png)](https://ko-fi.com/G2G0NP0R)

## Overview
[placeholder]
### SlugBot in Discord
[placeholder]
#### Setup
[placeholder]
#### Commands
[placeholder]


### SlugBot in Twitch
[placeholder]
#### Setup
[placeholder]
#### Commands
[placeholder]


## TODO list

### User Data:
 - [x] rep system: allow users to give other users rep once a day @done (18-12-11 16:03)
 - [x] let discord users link their twitch accounts @done (18-11-16 03:57)
 - [x] generate userData from memberData @done (18-11-16 00:13)
 - [x] generate temp userData from twitchChan data. merge with other userData if discord<>twitch link is made @done (18-11-16 03:57)
 - [x] create userData when new member joins server if needed @done (18-11-16 00:15)
 - [x] create useData when new twitchChan data is created if needed @done (18-11-16 00:15)
 - [ ] viewable profiles for users containing rep, score, rank, builds etc
### Member Events:
 - [x] Sync member events across all servers shared with slugbot. @done (18-10-26 05:09)
 - [x] Sync participants across all servers. @done (18-11-15 02:35)
 - [ ] Link twitch channel if a discord>twitch link is made.
 - [x] Use member's set build to fill in blank member event info if possible @done (18-11-05 18:09)
 - [x] Display participants builds in participant list if possible @done (18-11-15 02:36)
 - [x] compact participant list if it gets too long @done (18-11-15 02:36)
 - [x] Improve location parsing. (string similarity maybe?) @done (18-12-07 23:34)
 - [ ] Add locations (with screenshots) for playable areas without bonfires
 - [x] Delete old reminder when a new one is sent @done (18-12-07 19:34)

### Activity Data:
 - [x] Collect emote usage data. @done (18-11-05 18:09)
 - [x] Display data on emote usage. @done (18-11-21 22:42)
 - [x] Graph activity data per guild. @done (18-10-30 03:11)
 - [x] Graph activity data per member. @done (18-11-21 22:42)
 - [x] Graph activity data per channel. @done (18-11-21 22:42)

### music:
 - [ ] Music queue.
 - [ ] Play, pause, skip, volume.
 - [ ] Mod override.
 - [ ] User permissions.

### Word Censor:
 - [x] let moderators add and remove filter words @done (18-11-05 18:07)
 - [x] store expanded filter word list in database @done (18-11-05 18:08)
 - [x] Allow mods to add regex filters that, when matched, flag the message for deletion @done (18-11-14 03:29)

### ds3 builds:
 - [x] Whenever a soulsPlanner link is sent in a message, add reactions that allow users to preview the build either in a richEmbed or as a screenshot of the page. @done (18-10-30 03:10)
 - [x] Allow discord members to add their builds to a personal build list @done (18-10-30 20:10)
 - [x] Allow discord members to set their current build @done (18-10-30 20:10)
 - [x] Allow discord members to delete builds from their list @done (18-10-30 20:10)
 - [x] Way to display a member's build list. @done (18-10-31 15:42)
 - [x] Use only one reactionCollector per msg @done (18-11-03 20:00)
 - [x] Give better feedback if build processing fails. @done (18-11-15 02:36)
 - [ ] let mods stop builds from displaying in their servers. (does not remove the build from the db)
 - [x] Add basic word censoring for build names. @done (18-11-05 18:09)
 - [x] Show poise in armour field. @done (18-11-13 16:51)
 - [x] port current build to be stored in userData instead of memberData @done (18-11-13 17:26)
   - [x] discord !setbuild saves to userData @done (18-11-13 17:01)
   - [x] twitch !setbuild saves to userData if one is linked to a discord account @done (18-11-13 17:16)
   - [x] discord !build uses userData @done (18-11-13 17:04)
   - [x] twitch !build uses userData if available and twitchData if not @done (18-11-13 17:24)
 - [x] port twitch channel builds over to global userData builds @done (18-11-16 03:58)

### DS3 Tools:
 - [ ] collect all DS3 weapon data and add to DB
   - [x] Attack motionValues @done (18-12-17 01:58)
   - [ ] Weapon art motionValues
   - [x] crit motionValues @done (18-12-17 01:58)
   - [x] base damage @done (18-12-17 01:58)
   - [x] scaling coefficients @done (18-12-17 01:58)
   - [x] curve indexes @done (18-12-17 01:58)
   - [ ] poise health multipliers and poise damage
   - [ ] frame data
 - [ ] user can enter strength, dex, int, faith and get a list of weapons they can use with their AR
 - [x] Add the ability to get statistical info on dice rolls with !roll. @done (18-12-09 03:16)

### Commands:
  User or mod commands for slugbot
 - [x] Add way to limit which channels commands can be used in @done (18-12-21 01:25)
 - [ ] Add way to limit who can use commands.
 - [ ] Better way to list roles for !constraint.
 #### Custom Commands:
  - [x] Store incremental value in customCommand document in db @done (18-11-19 00:20)
  - [x] add replacement flag for increment value. @done (18-11-19 00:20)
  - [x] add replacement flag for username. @done (18-11-19 00:20)
 #### Reminders:
  - [ ] Allow users to set reminders for themselves. SlugBot will DM them with the reminder.
  - [ ] Save reminder time to db. check db every 5 minutes. Cache reminder time in memory if it is due in less than 5 minutes.
  - [ ] Allow twitch mods to add periodic reminders that display every x minutes in chat.
  - [ ] Dont find docs for periodic twitch reminders if stream is not live.
 #### !help:
  - [ ] Separate !commands and !help. display only functional commands in !help. display custom commands with !commands.
  - [ ] Improve !help message. use hover-over link embeding.
  - [ ] Clickable link for each command linking to this page.
 #### !weapon:
  - [ ] Show spellbuff for catalysts instead of R1 damage.
  - [ ] Account for attack damage type when calculating approx damage.
  - [ ] Make sure crit damage is calculated without str 1.5 mult.
  - [ ] Show shield stability.
  - [ ] Menu for poise data.
  - [ ] Synonym lookup.
  - [ ] find best stat spread for specific weapon.
  - [ ] find best infusion for weapon given specific stats.

### Twitch:
 - [x] discord users with a streamer role will automatically have their streams displayed in the #stream channel (as long as their accounts are linked). @done (18-12-07 23:35)
   - [ ] Prompt user to link twitch if they haven't.
   - [x] Add member to streamer list if they link their accounts after getting the streamer role @done (18-12-07 23:37)

### Bugs:
 - [x] Location images not displaying for DS3 member events. @done (18-10-30 02:51)
 - [ ] Location images not displaying for DS1 member events.
 - [ ] Unmuting stops working at seemingly random times.
 - [ ] builds not accept +0 weapons
 - [x] sort out broken names in !weapon (lothric sword) @done (18-12-17 01:59)
