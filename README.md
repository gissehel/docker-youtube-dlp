What is youtube-dl?
==================

[youtube-dl](https://github.com/rg3/youtube-dl) is a command-line program to download videos from YouTube.com and other video sites.

Reference
=========

* Github page : [https://github.com/gissehel/docker-youtube-dl](https://github.com/gissehel/docker-youtube-dl)
* Docker hub page : [https://hub.docker.com/r/gissehel/youtube-dl/](https://hub.docker.com/r/gissehel/youtube-dl/)

Based on
========

Based on [https://github.com/wernight/docker-youtube-dl](https://github.com/wernight/docker-youtube-dl). ([https://hub.docker.com/r/wernight/youtube-dl/](https://hub.docker.com/r/wernight/youtube-dl/))

How to use this image
=====================

    $ docker run --rm --user $UID:$GID -v $PWD:/downloads ghcr.io/gissehel/youtube-dl <video_url>

  * `--user $UID:$GID` is to run as your current user, and not `root`.
  * `-v $PWD:/downloads` is to store downloaded files in the current working directory.
  * `<video_url>` is the ID of a YouTube video or other arguments to pass to `youtube-dl`.

Note: The entrypoint is set to `youtube-dl`, so do *not* put `youtube-dl` again as argument.

Features of this image
----------------------

  * **Small**: Built based on official [Alpine Linux](https://registry.hub.docker.com/_/alpine/).
  * **Simple**: One command and you should be ready to go. All documented here.
  * **Secure**: Runs as any user.

