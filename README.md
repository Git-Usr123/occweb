# OCCWeb terminal (Fork)

### A web terminal for admins to launch Nextcloud's occ commands

![occweb](https://github.com/Adphi/OCCWeb/raw/main/appinfo/screenshot.png)

## About this fork

This is a maintained fork of the original [Adphi/OCCWeb](https://github.com/Adphi/OCCWeb) project. The upstream project was marked as deprecated by its original author, but this fork continues to be developed and kept compatible with current Nextcloud versions.

## Install

Place this app in **nextcloud/apps/**

## ⚠️ Warnings ⚠️

- The application is not a real interactive terminal and does not support long running tasks.
  So if your instance is pretty big, commands like `occ files:scan` will time out and fail.
- Do not use `occ maintenance:mode --on`, obvious...

### Background on the async limitation

Nextcloud has no native support for asynchronous operations through PHP web requests without introducing additional dependencies (e.g. websockets). This means long-running or interactive occ tasks can't be fully supported in a web terminal, and running them against large/voluminous instances can lead to serious issues if they time out mid-operation. [This issue](https://github.com/nextcloud/server/issues/16726) has some background on this limitation.

## TODOs

See [open issues](https://github.com/Git-Usr123/occweb/issues)
