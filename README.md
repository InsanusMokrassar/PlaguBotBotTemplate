# PlaguBot Bot Template

1. Update your dependencies [here](https://github.com/InsanusMokrassar/PlaguBotBotTemplate/blob/master/build.gradle#L27-L30). Usually in gradle projects/readmes developers define names of
their dependencies
2. Edit [config](config.json). The main points
([full list of parameters with explanation](https://github.com/InsanusMokrassar/PlaguBot/blob/master/template.config.json):
    * Change [database](https://github.com/InsanusMokrassar/PlaguBotBotTemplate/blob/master/config.json#L2-L4) section
    * Change [bot token](https://github.com/InsanusMokrassar/PlaguBotBotTemplate/blob/master/config.json#L5)
    * Change [list of plugins](https://github.com/InsanusMokrassar/PlaguBotBotTemplate/blob/master/config.json#L6-L11):
        * Field `type` - it is name of the plugin provided by developer/dependency
        * Other fields are parameters of plugin and must be provided directly
        * Example is available in the [example section](https://github.com/InsanusMokrassar/PlaguBotBotTemplate/blob/master/config.json#L6-L11): here `Hello` is name of plugin and
        `parameter` is its configuration parameter

## How to launch

There are two main ways to launch it:

* Run `./gradlew build && ./gradlew run --args="PATH_TO_YOUR_CONFIG"` with replacing of `PATH_TO_YOUR_CONFIG`
* Run `./gradlew build` and get [zip of bot](build/distributions/bot.zip) and unarchive it somewhere you need. In this
archive there is an executable files `bot.bat` (for windows) and `bot` (for linux) by the path inside of archive
`/bot/bin`. After unarchiving you can just launch executable file with one argument: path to the config
