This Bukkit plugin allows people with a free or paid New Relic account to send performance data about their Minecraft server and details about core events that occur on their server to New Relic's platform for analysis and graphing.

# Installation

* Download the latest New Relic Java Agent for manual installs
* Unzip the archive in the root directory of your minecraft server. The same location as your Craftbukkit jar.
* Add "-javaagent:newrelic/newrelic.jar" to the java launch command that you use for your server.
* Add the newrelic-api.jar to your launch classpath with something like "-cp craftbukkit.jar:newrelic/newrelic-api.jar"
    * Note: that if you were using "-jar craftbukkit.jar" to launch craftbukkit, you will want to remove this and replace it with "-cp   craftbukkit.jar:newrelic/newrelic-api.jar org.bukkit.craftbukkit.Main"
    * We don't include this as you might already be using New Relic, and we must ensure the newrelic jar and the newrelic-api jar are    the same version.
* Edit newrelic/newrelic.yml and at a minimum ensure that your *license_key* and *app_name* are set appropriately.

# Features

* Enable and disable reporting
* Control which events you want to submit data about.

# Commands

* */nrenable* - enable reporting to New Relic
* */nrdisable* - disable reporting to New Relic

# Permissions

* newrelic.admin: false
    * Allows you to enable or disable reporting

# Configuration

```
track:
  entity:
    death: true
  creature:
    spawn: true
  player:
    death: true
    join: true
    kick: true
    quit: true
    respawn: true
    teleport: true
  block:
    place: true
    break: true
  server:
    command: true
    remotecommand: true
  chunk:
    load: true
    unload: true
```

# Acknowledgements

This plugin is the results of a lot of things, including:
* Being the father of 3 children, 2 of which play Minecraft.
* Working at New Relic
* A [blog](http://blog.newrelic.com/2014/06/17/instrumenting-minecraft-new-relic-insights/) I wrote for New Relic as a Proof-of-Concept about this work
* The [Reddit admincraft community's encouragement](http://www.reddit.com/r/admincraft/comments/28gplh/analyzing_minecraft_with_new_relic_insights/) to create a real plugin.
* [StromCoreFilms great Bukkit Tutorials on YouTube](https://www.youtube.com/playlist?list=PLlmh-IYCohJ931R6Yv8uNAZoZEPQj5kPR)


**NOTE:** Comments can be posted on bukkit.org

