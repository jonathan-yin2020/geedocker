GEE repository: https://github.com/google/earthenterprise

# GEEDocker


Build and run Google Earth Enterprise with docker

To create all of the images run runChain.sh\
The script runChain.sh accepts the following flags:\
--test (for running the GEE tests to check that the build was successful)\
--tutorial (for creating an additional fusion image with the tutorial files)

If you wish to create each image independantly you may do so with the given scripts as following:

For the basic build run:
```sh
cd geeBuild
bash build.sh
```
\
For the GEE server run:
```sh
cd server
bash install.sh
```
\
For the GEE fusion run:
```sh
cd fusion
bash install.sh
```
\
For the GEE fusion with tutorial files run:
```sh
cd fusion/tutorial
bash install.sh
```

# Running GEE


Start server:
```sh
cd server
bash run.sh
```
** make sure the server is running before starting fusion\
\
\
Start fusion:
```sh
cd fusion
bash run.sh
```
\
Start fusion with tutorial:
```sh
cd fusion/tutorial
bash run.sh
```
\
To start gee fusion or tutorial with bash entrypoint add --entrypoint flag:
```sh
bash fusion/run.sh --entrypoint
bash fusion/tutorial/run.sh --entrypoint
```


# Remove images and containers

Remove all of the images and containers created by running the script removeAll.sh

Remove individual images by running the script removeImage.sh as such:
```sh
bash removeImage.sh <image_name:tag>
```
\
Remove containers by running the script removeContainer.sh as such:
```sh
bash removeContainer.sh <container_name>
```
