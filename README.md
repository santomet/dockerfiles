Qt toolchain images
===================
* qt:5.12-desktop currently Qt 5.12.3


Usage:
------

1. Install required specific dependencies:

  ```sh
sudo apt-get -qq update && sudo apt-get install -qq -y <packages>
```
2. Clone repo with source

  ```sh
git clone --recursive <repo> ~/src
```
3. Make build dir & cd into

  ```sh
mkdir ~/build && cd ~/build
```
4. Run qmake

  ```sh
qmake -r ~/src
```
5. Run make

  ```sh
make -j4
```
6. Run make install 

  ```sh
make install INSTALL_ROOT=$HOME/dist
```
7. *Android*: run apk creation

  ```sh
androiddeployqt --input ~/src/<android json> --output ~/dist --deployment bundled --gradle --release
```

Links
-----

Used extract-qt script from https://github.com/benlau/qtci/blob/master/bin/extract-qt-installer
