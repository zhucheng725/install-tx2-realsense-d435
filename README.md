# install-tx2-realsense-d435
install tx2 realsense d435



### 1.Install<br>
Follow the nvidia dev website: https://devtalk.nvidia.com/default/topic/1065522/jetson-tx2/realsense-d435-with-jetson-tx2-depth-stop-working-freezes-after-time/post/5401724/#5401724<br>

```
sudo apt-key adv --keyserver keys.gnupg.net --recv-key F6E65AC044F831AC80A06380C8B3A55A6F3EFCDE || sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:8$

sudo add-apt-repository "deb http://realsense-hw-public.s3.amazonaws.com/Debian/apt-repo bionic main" -u

sudo apt-get install librealsense2-utils

sudo apt-get install librealsense2-dev

sudo apt-get install librealsense2-dbg

git clone https://github.com/IntelRealSense/librealsense.git

cd librealsense

mkdir build

cd build

cmake ../ -DBUILD_PYTHON_BINDINGS:bool=true

make -j4

sudo make install

cd /usr/local/lib

sudo cp librealsense2.so pyrealsense2.cpython-36m-aarch64-linux-gnu.so /usr/lib/python3.6/site-packages/
```


