# bing-osx-wallpaper
Bash script to update Yosemite desktop wallpaper with daily image from bing

Use at your own risk.  This script was made to download the latest bing homepage wallpaper on OS X Yosemite.  You should add this as a backround job that processes however frequently you want.  The script is made to be fairly lightweight and should only actually download the file once a day.  So you can have it running every minute, 5 minutes 15 minutes or however often you want.

# Installation
To install you'll need to just add it as a backend job.  OSX allows you to do this via crontab or launchd.  Since I'm not familiar with launchd I'll be using crontab
### Edit your crontab
```
crontab -e
```

### Add a crontab entry
Add something similar to what's below to your crontab.  Obviously change the first command to where you've downloaded the code and the second variable to where your bing wallpapers will be stored
```
# Download bing backgrounds, check every 5 minutes
*/5 * * * * /Users/YOURUSER/src/bing-osx-wallpaper/update_wallpaper.sh -d /Users/YOURUSER/Pictures/bing-wallpapers > /dev/null 2>&1
```

# Troubleshooting
This script assumes that you have a few things installed or available, sed, grep, wget, etc.  Most of these you should be able to install from brew, but if there's a better way to do it, feel free to contribute

# Contributions
Please do! Feel free to fork and change anything.
