# Changelog
## v4.0.0 - 00/00/00
Coming soon...

## v3.0.0 - 08/19/2021
```
npm i dbd.ts@3.0.0
```
### Additions
- Added plugins support
- Added `reverseReading` client option
- Added `insensitive` property to bot/command options
- Added `$addCmdReactions`
- Added `$getUserBadges`
- Added `$getVar and $setVar`
- Added `$archiveThread`
- Added `$unarchiveThread`
- Added `$banCount`
- Added `$numberSeparator`
- Added `$userExists`
- Added `$channelExists`
- Added `$memberExists`
- Added `$memberCount approximate(Presence/Member)`
- Added `$serverChannelExists`
- Added `$serverExists`
- Added `$endsWith`
- Added `$startsWith`
- Added `$deleteChannels`
- Added `$getVarsWithType`
- Added NodeJS version checks
- Added `$isNumber`
- Added `$cloneChannel`
- Added `$getChannelSlowmode`
- Added `$fetchGuildMembers`
- Added `$clearMessages`
- Added `$clearUserMessages`
- Added `$deleteRoles`
- Added `$deleteEmojis`
- Added `$while` loop
- Added `$channelNSFW`
- Added `$messageType`
- Added `$sliceText`
- Added `$indexOf`
- Added `$lastIndexOf`
- Added `$createContextMenuApplication`

### Breaking Changes
- `$serverMFA` -> `$serverMFALevel`
- `$serverNSFW` -> `$serverNSFWLevel`

### Fixed/Improved
- Added 'inline' field to `$addField`
- Fixed `$channelName`
- Bumped [`DBD.TS`](https://npmjs.com/package/dbd.ts) version
- Updated README.md

## v2.1.0 - 08/02/2021
```
npm i dbd.ts@2.1.0
```
### Additions
- Added `$voiceID`
- Added `$isVoiceDeaf`
- Added 'type' field to `$ban`
- Added `$setSlashCommands`
- Added `$startThread`
- Added `$joinThread`
- Added `$leaveThread`
- Added `$removeThreadMember`
- Added `$addThreadMember`
- Added 'reason' field to `$removeThreadMember`/`$addThreadMember`
- Added `$hasPerm`
- Added [`dbdts.db`](https://npmjs.com/package/dbdts.db) support
- Added `bot.addVariable`/`bot.variables.add`

### Fixed/Improved
- Better README/design
- Corrected server invite
- Changed [`discord.js`](https://discord.js.org/) version