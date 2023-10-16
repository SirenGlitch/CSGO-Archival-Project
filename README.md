# CS:GO Install Instructions

Dislike CS:2? Want to go back to the good old days? Welcome Home. After a few days of looking, I have found a method to get CS:GO back, and in theory, it will work after Valve kills off csgo_legacy.

**Note: No official Valve servers are active for CS:GO anymore, so bots are the only possible enemy at the moment, although a CS:GO Dedicated Server might work. As well as this, note that this is in no way endorsed by Valve or Hidden Path Entertainment and may stop working at any time.**

Now, with that out of the way, time to get onto the install instructions.

## Step One: Open Steam Console

Open Run (Win+R) and type `steam://open/console`, this will open Steam with the normally hidden Console menu open.

![Steam Console Tab](image.png)

## Step Two: Depot Download

(Optional): Setup Symlink from default depot download folder to a desired other drive. It is recommended to make the depot download path on the same drive as you plan to store CS:GO on, as it will speed up the movement process later on.

```bat
:: Remove the current depot download folder (backup contents if used before)
rmdir "C:\Program Files(x86)\Steam\steamapps\content\"
:: Make symlink to new folder
mklink /D "C:\Program Files(x86)\Steam\steamapps\content" "<new_path>\content"
```

In the Steam console, enter these two commands:

```steamcmd
download_depot 730 731 718406683749122620
download_depot 730 732 2224497558453288476
```

These will download the CS:GO files to the directories `<depot_download_dir>\app_730\depot_731\` and `<depot_download_dir>\app_730\depot_732\` respectively.

## Step 3: Merge the downloads

SDK-unfriendly install: Create a new folder (preferably) on the same drive as the depot download. Open this folder in one window, and the `depot_download_dir\app_730` in another. Copy/Move the contents of both `depot_731` and `depot_732` to the new folder, you shouldn't get any override warnings, but if you do then override them. However, this install is not the most recommended, as the Counter-Strike: Global Offensive - SDK won't install to this new folder if you want it, however **this is fine if you don't need the SDK.**

SDK-friendly install: Open the `depot_download_dir\app_730` in one window, and `<SteamLibrary_path>\steamapps\common\Counter-Strike Global Offensive` in another (can safely be created if it doesn't already exist). Copy/Move the contents of both `depot_731` and `depot_732` to the `Counter-Strike Global Offensive` folder.

## Step 4: Add to Steam

Anyone who is familiar with adding non-Steam games to their library, you don't need to read this part, as it's exactly the same process.

First, click Games in the top corner of the Steam window, then Add Non-Steam Game to My Library. If the CS:GO download folder is not in your system PATH, then CS:GO most likely won't show up in the Add Non-Steam Game window, so click Browse. From here, navigate to the CS:GO executable, and select it. Then from the Add Non-Steam Game window, make sure csgo is selected, and click Add Selected Programs. Now you can click play on it, and it will launch!

## (Optional) Step 5: Customisation

So, you have CS:GO in your library, but it doesn't look *quite* right. That's fine! Right clicking on the icon in your library and clicking properties allows you to edit the icon and name that is shown in your library, and right clicking on the banner area allows you to add a custom background and logo to its Library page. You can find high quality artwork at [SteamGridDB](https://www.steamgriddb.com).
