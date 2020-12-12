[Problem](https://stackoverflow.com/questions/39988844/docker-compose-up-vs-docker-compose-up-build-vs-docker-compose-build-no-cach)
The following only builds the images, does not start the containers:

```docker-compose build```
The following builds the images if the images do not exist and starts the containers:

```docker-compose up```
If you add the --build option, it is forced to build the images even when not needed:

```docker-compose up --build```
The following skips the image build process:

```docker-compose up --no-build```
If the images aren't built beforehand, it fails.

The ```--no-cache``` option disables the Docker [build cache](https://docs.docker.com/develop/develop-images/dockerfile_best-practices/#leverage-build-cache) in the image creation process. 
This is used to cache each layer in the Dockerfile and to speed up the image creation reusing [layers](https://docs.docker.com/storage/storagedriver/#images-and-layers) (~ Dockerfile lines) previously built for other images that are identical.
