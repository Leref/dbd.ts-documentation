# Changelog
## v4.0.1 - 10/30/2021
```
npm i dbd.ts@4.0.1
```
- Fixed missing functions folder
- Removed not needed folders

## v4.0.0 - 10/30/2021
```
npm i dbd.ts@4.0.0
```
### Added
- Added `$getMessage`
- Added `$createFile`
- Added `messageDelete` callback
- Added `messageUpdate` callback
- Added `$createTextChannel`
- Added `$wait`
- Added more var oriented functions in `$getCooldownTime`
- Added `$dmChannel` and `$sendDM`
- Added `$makeReturn`
- Added `loopCommand`
- Added functions regarding `$textSplit`
- Added `$findTextSplitElement`
- Added `$joinSplitText`
- Added `memberUpdate` callback
- Added `userUpdate` callback
- Added hyperlinks
- Added `$ignoreCode`
- Added `addMessageReactions`
- Added all `role` callbacks
- Added `$setNickname`
- Added `$findMember`
- Added `$clearAllReactions`
- Added `$clearReaction(s)`
- Added `$channelType`
- Added `$commandInfo`
- Added `$hasRole`
- Added `$getLeaderboardPosition`
- Added `$roleCount`
- Added `$randomTexts`
- Added `$customEmoji`
- Added compacted function `$role`
- Added compacted function `$member`
- Added `$usersWithRole`
- Added `$botCount`
- Added `$charCount`
- Added `onChannel(Create/Delete/Update)` callbacks
- Added `$findServerChannel and $findChannel`
- Added `$argCount`
- Added `$hasEmbeds`
- Added `$messageAttachments`
- Added `$messageExists`
- Added compact function `$client`
- Added `$checkContains`
- Added `$onlyForRoles` and `$onlyForServers`
- Added compact function `$channel`
- Added `voiceStateUpdate` callback
- Added `$packageName`
- Added `$getBotInvite`
- Added `$noMentionMessage`
- Added `$readyTimestamp`
- Added readyEvent log message
- Added persistent timeout function
- Added `$variableCount`
- Added `$shardCount`
- Added `$lerefAvatar`
- Added `$setRoleIcon` 
- Added `$userBanner` 
- Added `$userAccentColor`
- Added `$forEach`
- Added `$replaceTextWithRegex`
- Added `$buffer`
- Added `$userIconURL`
- Added `$functionCount`
- Added `$filter`
- Added `$getUserReactions`
- Added `$akarui`
- Added `$getServerInvite`
- Added `$getBanReason`
- Added `$botLeave`
- Added `$memberAvatar`
- Added `$interactionFollowUp`
- Added `$isBot`
- Added `$isVoiceSelfVideo`
- Added `$isVoiceStreaming`
- Added `$dbPing`
- Added `$randomString`
- Added object functions
- Added colorful logging on `readyEvent`
- Added [discord.js](https://discord.js.org/) v13.3.0 + autocomplete interaction
- Added `$round`

### Fixed/Improved
- Made content optional for `$channelSendMessage`
- Removed useless import
- Implemented ability to reload multiple commands
- Removed :x: error message from `$eval`
- Removed build script
- Improved encoder
- Allowed `$channelID` and `$guildID` in interactions
- Modified `$ram` to show current used ram.
- Modified command handler - Logging debug method
- `$reboot` has been modified
- Fixed `$deleteChannels`
- Added intent and event checkers
- Fixed `$deleteSlashCommand`
- Allowed 2 parameters in `.commands.add`
- Updated database
- Updated readyOn dbd.ts
- Added extended role options
- Allowed files in handler with no keys
- Added rest to `$djsEval`
- Remove trimming from `$argCount`
- Improved compiler
- Forced `channelID` field in `$lavalinkPlay`
- Partially fixed `ignoreAllErrors`
- New design
- Updated Error Handling System
- Fixed lavalink playlist load and message in spam
- Negative indexes now work in `$message`

### Breaking Changes
- Renamed `createFunction` to `createCustomFunction`

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