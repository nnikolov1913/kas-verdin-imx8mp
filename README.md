# build the image
Prerequisites:

Install docker engine:
https://docs.docker.com/engine/install/

Install kas:
https://kas.readthedocs.io/en/latest/userguide.html

How to build:

kas-container should be used as the YAML files are written for such a usage.
After cloning this repo, execute these commands:
```
cd beagleplay
kas-container checkout verdin-imx8mp.yml
kas-container shell verdin-imx8mp.yml
```
After the last comand, docker container should be started and promt should be inside it already.
In the container build the image:
```
bitbake core-image-minimal
```
After some time(usually it takes 1-2 hours or more) image should be ready in tmp/deploy/images/verdin-imx8mp.
Name is somethig like core-image-minimal-verdin-imx8mp.rootfs-XXXXXXXXXXXX-Tezi...
Flash the image into a module using ToradexEasyInstaller for example.

