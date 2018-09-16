# What is froyok-perforce ?
This is a "fork" of the following Docker image : https://github.com/ambakshi/docker-perforce/tree/master/perforce-server

The goal of this repository is to provides files that allow to build a Docker image ready install a Perfoce server suited for **Unreal Engine 4** projects.

# What has been changed from the original Docker image ?
Here are the changes that have been made in the bash script :
 * Added comments to make it easier to read
 * Modifer the **configure-helix-p4d.sh** command line to add **--case 1** (force case-insensitive)
 * Added 3 configure command to hide user list, hide config files and disable automatic user creation
 * Added multiple Typemap setup to match the UE4 list : https://docs.unrealengine.com/en-us/Engine/Basics/SourceControl/Perforce

# How to build ?
Use the following steps :
1. Download the files into an empty folder
2. Run to build : **docker build . -t=froyok-perforce --no-cache**
3. Run to package : **docker save  froyok-perforce > froyok-perforce.tar**

You will end-up with a **froyok-perforce.tar** file that can be installed on a Docker system. This is compatible with Docker on Synology NAS for example.

For further details see : http://www.froyok.fr/blog/2018-09-setting-up-perforce-with-docker-for-unreal-engine-4
