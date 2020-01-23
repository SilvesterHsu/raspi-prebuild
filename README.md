# raspi-prebuild
Here I have pre-built wheel for raspberry pi. All wheels are in the `prebuild` folder.

Here is a list for builted wheels.
* `matplotlib`
* `numpy`
* `pandas`
* `Pillow`
* `torch`
* `torchvision`
* `scipy`


For more details, follow my Blog [here](https://medium.com/@live459745355/how-do-i-successfully-install-pytorch-numpy-pandas-and-scipy-on-raspberry-pi-4-3b9b0fd739a2)
## Install packages
### wheel file
Use `wget` to download file, and install via `pip`.

For example,
```
wget https://github.com/SilvesterHsu/raspi-prebuild/blob/master/prebuild/Pillow-6.2.2-cp36-cp36m-linux_aarch64.whl
pip install Pillow*.whl
```
### egg file
The scipy is egg file, use `easy_install` to install it.
```
wget https://github.com/SilvesterHsu/raspi-prebuild/tree/master/prebuild/scipy-1.2.3-py3.6-linux-aarch64.egg
easy_install *.egg
```
## Docker
I also offer the Docker file to build images. For newly installed raspberry pi system (ubuntu 64-bit kernel), you can directly build docker images.
```Docker
git clone https://github.com/SilvesterHsu/raspi-prebuild.git
cd raspi-prebuild
docker build -t raspi-prebuild .
```
Because of the use of pre-built files, the time to create the system will be greatly reduced, usually about 10 minutes, and I will also upload the image I created to DockerHub later.
