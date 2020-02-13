# Flutter plugins that need fixing asap


video_player on ios was killing background music playing.  We have a video with no audio track on our main menu and when it plays, the background music stops.  Even though someone has submitted a pull request, Google just kept asking them to update their fix to the latest version, instead of just taking the code that fixed it and adding it in.

this is the place i found the code that fixed it:
- https://github.com/thesoftwarefanatics/plugins/commit/d45c8ecdc489c138b978edafe3e1cb4e92bde05e

here's the pull request stuck eternally in limbo:
- https://github.com/flutter/plugins/pull/1174

NOTE THIS IS FROM A YEAR AGO.

The bigger the company the slower it moves.

To use this, do this in pubspec.yaml:

video_player: # ^0.10.5+1
    git:
      url: git://github.com/crazedvic/plugins.git
      path: packages/video_player/video_player

The original author is much ambitious than I am, making it optional and everything.  Our app has no sound, so i didn't need that stuff.
