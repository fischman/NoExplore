# NoExplore
Disable distractions in the Instagram Android app beyond chat &amp; friends' posts.

## Motivation
I want to use Instagram to see friends' posts & stories, and chats. I
don't want to spend time watching strangers' Reels and posts.

## What it does
When the `Reels` or `Explore and search` icons in the app's home view are
tapped, a fake "back" swipe will be performed to go back to the home
view. When scrolling the main feed and reaching `Suggested Posts` a fake
"up" swipe will be performed, refreshing the feed and jumping to its
top.

## How it works
This "app" registers an [Android Accessibility Service](https://developer.android.com/guide/topics/ui/accessibility/service) that watches
actions taken in the Instagram app and perform the back or up swipes
depending on what it sees. There's no user interface or activity for
this app itself, it's purely a background process.

After installing, you'll have to enable this using: `Settings` ->
`Accessibility` -> tap `Disable Instagram Distractions` -> enable the main
toggle, and leave the shortcut-related disabled.  Note that
accessibility services have a tremendous level of access, so enabling
per above will show a scary consent screen.

## How to install
This isn't (yet?) available in Google's Play app store.

Either build using Android Studio (or gradle) from source, or download
the latest [release](https://github.com/fischman/NoExplore/releases) APK and install via adb or your side-loading
mechanism of choice.
