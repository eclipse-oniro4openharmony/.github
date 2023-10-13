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
repo init -u https://github.com/eclipse-oniro4openharmony/manifest.git -b OpenHarmony-3.2-Release --no-repo-verify
repo sync -c
repo forall -c 'git lfs pull'
```

**In the source code directory, fetch the prebuild tools:**

```bash
./build/prebuilts_download.sh
```

**To run the build an isolated docker container is recommended:**

```bash
docker run -it -v $(pwd):/home/openharmony swr.cn-south-1.myhuaweicloud.com/openharmony-docker/openharmony-docker:1.0.0

```

**In the Docker instance, run the build:**

Select the target device with (e.g.rk3568):

```bash
hb set
```

Start the build:

```bash
hb build
```
