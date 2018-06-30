# What is froyok-perforce ?
This is a "fork" of the following Docker image : https://github.com/ambakshi/docker-perforce/tree/master/perforce-server

The goal of this reopsitory is to provides files that allow to build a Docker image to install a Perfoce server suited for **Unreal Engine 4** projects.

# How to build ?
Use the following steps :
1. Download the files into an empty folder
2. Run to build : **docker build . -t=froyok-perforce --no-cache**
3. Run to package : **docker save  froyok-perforce > froyok-perforce.tar**

You will end-up with a **froyok-perforce.tar** file that can be installed on a Docker system. This is compatible with Docker on Synology NAS for example.
