# NodeBB Youtube Embed Plugin

The Youtube Embed plugin allows users to embed Youtube videos into NodeBB posts. Simply add the
link to the video on its own line.

In order to get title and duration information, the plugin needs to be configured with an API
key. See here for details on acquiring one:

https://developers.google.com/youtube/v3/getting-started

This plugin was forked from [nodebb-plugin-youtube-lite](https://github.com/a5mith/nodebb-plugin-youtube-lite).

## Installation

Search in the 

    npm install nodebb-plugin-youtube-embed

## Changes
    0.6.9
     - Fixed db require
    0.6.8
     - Compatibility update to 1.13
    0.6.7
     - Exception handling for parsing API requests.
     - Unavailable videos don't have a channel name, replaceAll checks for no text.
    0.6.6
     - Rejected videos lack thumbnails, too.
    0.6.5
     - Defensive coding in case Youtube returns a video item that
       doesn't have contentDetails.
    0.6.4
     - Don't falsely report an error for 0s duration
    0.6.3
     - Parse durations that do not have a time component
    0.6.2
     - Don't crash if we can't parse the duration sent by Youtube
    0.6.1
     - Added transparent background and hover effect for play button
     - Max-width style to the main div for small screens and narrow styles
    0.6.0
     - Works with NodeBB 1.0
     - Moved most of the work to the server, to include API calls (keeps API key
       from being exposed to users).
     - LRU cache to reduce quota usage.
     - Supports `t=`, '`start=`', `end=` query string parameters
     - With valid API key displays title, channel and duration information
     - Support `#` in query strings
    0.5.0
        - Plugin now supports [Youtube API v3](https://developers.google.com/youtube/v3/?hl=en)
    0.4.7
     - Changes to Desktop Video Size & Fixed CSS Issues
    0.4.5
     - Fixed how the video displays on mobiles. Should no longer extend past the viewport.
    0.4.4
     - Upgraded Regex so it doesn't match ANY 11 character string. Includes support for rel="nofollow". 
    0.4.1
     - Works with latest 0.7.x and hopefully beyond. Should also support time stamps. 
    0.3.1
     - Removed forced http from api and pre loaded image. 
