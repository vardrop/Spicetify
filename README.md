![Logo](LOGO.svg)

[![GitHub release](https://img.shields.io/github/release/khanhas/Spicetify/all.svg?colorB=97CA00?label=version)](https://github.com/khanhas/Spicetify/releases/latest) [![Github All Releases](https://img.shields.io/github/downloads/khanhas/Spicetify/total.svg?colorB=97CA00)](https://github.com/khanhas/Spicetify/releases) [![Join the community on Spectrum](https://withspectrum.github.io/badge/badge.svg)](https://spectrum.chat/spicetify)

## How to use
**1.** Download and install [**Rainmeter**](https://www.rainmeter.net/) (require version >= 4.1)  
**2.** Download and install rmskin package in [**release page**](https://github.com/khanhas/Spicetify/releases)  
**3.** Load Spicetify skin in Rainmeter Manage  
**4.** Choose **Backup** in skin UI to start backing up original Spotify files  
**5.** Pick color scheme, edit CSS then **Apply**  

**Note:** Only Spotify normal version is supported. Windows Store version is under a write permission required folder so I can't make it to work. Normal Spotify installer can be downloaded [here](https://download.scdn.co/SpotifySetup.exe).

![Demo1](https://i.imgur.com/O6IRzlV.png)

## Outline
- [Custom CSS](https://github.com/khanhas/Spicetify#custom-css)
- [Themes](https://github.com/khanhas/Spicetify#themes)
- [Extensions](https://github.com/khanhas/Spicetify#extensions)
- [Apps](https://github.com/khanhas/Spicetify#apps)

## Custom CSS
To sastify any web developer that has experience with CSS, **Inject CSS** option will allow you to customize your Spotify client even more. 

I included in install package my own CSS theme:

![Demo2](https://i.imgur.com/eiAPF6j.png)

**Note:** If you prefer original Spotify UI, please clear user.css file or uncheck **Inject CSS**.

To use color variables, check out [Custom CSS wiki page](https://github.com/khanhas/Spicetify/wiki/Custom-CSS).

## Themes
If you have multiple themes in Themes folder, click at back and next buttons to rotate through all of them. You also can create new theme and duplicate current theme instantly by using right mouse context menu.

![Demo3](https://i.imgur.com/B9NkBU0.png)

## Extensions
Spicetify also allows you inject custom Javascript to support your theme or enhance your Spotify client functionalities. 

I included some extensions in install package you might find useful, activate them in Spicetify then Apply/Re-apply:

- **Auto Skip Videos:**  Videos are unable to play in some regions because of Spotify's policy. Instead of jumping to next song in playlist, it just stops playing. And it's kinda annoying to open up the client to manually click next every times it happens. Use this extension to skip them automatically.

- **Christian Spotify:** Auto skip explicit tracks

![Ext_Christian](https://i.imgur.com/yTUeWWn.png)

- **DJ Mode extension:** Easily setting up the client for your friends or audiences to choose, add song to queue but prevent them to control player. Plays button in album track list/playlist are re-purposed to add track to queue, instead of play track directly. Hide Controls option also allow you to hide all control button in player bar, Play/More/Follow buttons in cards.

![Ext_DJ](https://i.imgur.com/pOFEqtM.png)

- **Queue All:**  You like using Discover, New Releases page to find new music but adding each one of them to queue takes a lot of effort? If so, activate this  extensions and apply. At top of every carousel now has a "Queue All"  button to help you add all of them to queue. Note: Not available for playlist carousels. Just songs, albums ones.

![QueueAll](https://i.imgur.com/D9ytt7K.png)

- **Trash Bin:** Throw songs/artists to trash bin and never hear them again (automatically skip). This extension will append a trash bin button in player bar and one in every artist page header. Button in player bar will immediately skip and add that song to trash list. Button in artist page will add that artist in trash list and skip whenever his/her songs play.

![Ext_Trash1](https://i.imgur.com/k7A7oBI.png) | ![Ext_Trash2](https://i.imgur.com/dVZclSJ.png)
---|---

- **WebNowPlaying Companion**: For Rainmeter user only. Works exactly like [WebNowPlaying Companion for browser](https://github.com/tjhrulz/WebNowPlaying-BrowserExtension), get song information and control player directly with WebNowplaying plugin.

Check out [Extension wiki page](https://github.com/khanhas/Spicetify/wiki/Extension) for list of useful functions, object.

## Apps
Inject custom apps to Spotify and access them in left sidebar.  

I included my own app to demonstrate how to make and inject an app:

- **Reddit**: Fetching top 100 Spotify posts in any subreddit. This app has native feels and behavior just like other Spotify apps: you can follow, save, play, open playlist/track/album directly. Moreover, it also can fetch Youtube posts and play them inside Spotify.  

![Reddit](https://i.imgur.com/OTrW2e8.png)

Check out [App wiki page](https://github.com/khanhas/Spicetify/wiki/App) for some app making tips.

## How it works
Spotify UI is HTML/CSS and runs inside Chromium Embedded Framework<sup>[[1]](https://www.quora.com/How-is-JavaScript-used-within-the-Spotify-desktop-application-Is-it-packaged-up-and-run-locally-only-retrieving-the-assets-as-and-when-needed-What-JavaScript-VM-is-used)</sup>. All CSS files controlling element attributes and interaction are packed in SPA files (they basically are ZIP).  

These CSS files are extracted first then go through a preparation process that finds and replaces almost all colors with specific keywords.  

When user applies his/her own colors scheme, all keywords are replaced with actual colors value, both in hex and RRR,GGG,BBB format. 

After that, modded CSS and remaining files are transferred back to Spotify directory.

## Credit
Thanks ![**actionless**](https://github.com/actionless) for his ![oomoxify](https://github.com/actionless/oomoxify/blob/master/oomoxify.sh) script that this skin is based on.
Thanks ![**tjhrulz**](https://github.com/tjhrulz) for his ![WebNowPlaying Browser Extension](https://github.com/tjhrulz/WebNowPlaying-BrowserExtension) and ![MessagePassing plugin](https://github.com/tjhrulz/MessagePassingForRainmeter).
