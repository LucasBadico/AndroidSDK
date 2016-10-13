# AndroidSDK

Android SDK Docker Image

[![](https://img.shields.io/badge/Docker%20Hub-info-blue.svg)](https://hub.docker.com/r/thyrlian/android-sdk/)

<img src="https://github.com/thyrlian/AndroidSDK/blob/master/Images/AndroidSDK.png?raw=true" width="200">

## Notes

* Run Android SDK update directly from the **Dockerfile** or inside the **container** would fail with the default `AUFS` storage driver, due to some file operations are not supported by this storage driver, but change it to `Btrfs` would work.  You can check your current storage driver option by `docker info | grep 'Storage Driver'`.  To check which filesystems are supported by the host kernel, just run `cat /proc/filesystems`.
