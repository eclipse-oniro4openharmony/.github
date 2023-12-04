# Welcome to the Eclipse Oniro for OpenHarmony Project

This project is home to add-ons and enhancements for the
[OpenHarmony](https://www.openharmony.cn) project.
For more details on Oniro please see our [project
page](https://oniroproject.org/).

## Quick Start

As prerequisites git-lfs and repo need to be installed. 100GB of free disk space
is recommended for the full build.

**To obtain the source code use the following commands:**

```bash
repo init -u https://github.com/eclipse-oniro4openharmony/manifest.git -b OpenHarmony-4.0-Release --no-repo-verify
repo sync -c
repo forall -c 'git lfs pull'
```

**In the source code directory, fetch the prebuild tools:**

```bash
./build/prebuilts_download.sh
```

**To run the build an isolated docker container is recommended:**

```bash
docker run -it -v $(pwd):/home/openharmony swr.cn-south-1.myhuaweicloud.com/openharmony-docker/docker_oh_standard:3.2

```

**In the Docker instance, run the build:**

Inside the Docker instance, set the target device for the build (e.g. rk3568)
and use ccache to speed up subsequent builds:

```bash
./build.sh --product-name rk3568 --ccache
```
