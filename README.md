# steamwebapi

> A simplified wrapper for the steam web api

This is a simple and lightweight wrapper for the steam web api. Created because the other options weren't simple enough for me.

## Documentation

### Installation

```
npm install https://github.com/DevNvll/steamwebapi.git
```

or

```
yarn add https://github.com/DevNvll/steamwebapi.git
```

### Usage

```javascript
const Steam = require('steamwebapi')
const api = new Steam(API_KEY_HERE)

const id = 76561198052893297 || 'cmdline' // You can use steamID64 or the vanity url

api.getPlayerSummary(id).then(data => {
  console.log(data)
})
```

### Methods

```javascript
resolveId(id) // resolves vanity url to steamID64
getNewsForApp(appid, (count = 3), (maxLength = 300))
getGlobalAchievementPercentagesForApp(appid)
getGlobalStatsForGame(appid, (count = 1), (achievements = []))
getPlayerSummary(id)
getOwnedGames(id)
getRecentlyPlayedGames(id)
getPlayerBans(id)
getPlayerAchievements(id, appid)
getUserStatsForGame(id, appid)
getFriendList(id)
isPlayingSharedGame(id, appid)
getSchemaForGame(appid)
getAppList()
getAppInfo(appid)
```

More info: https://developer.valvesoftware.com/wiki/Steam_Web_API

## License

MIT
