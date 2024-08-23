# macOS installation
1. download wxWidgets source code from [wxWidgets](https://github.com/wxWidgets/wxWidgets/releases/download/v3.2.5/wxWidgets-3.2.5.tar.bz2)
2. extract the source code
3. open terminal and navigate to the extracted folder
4. run the following commands:
```bash
mkdir build-cocoa-debug
cd build-cocoa-debug
../configure --disable-shared --enable-debug
make
```
5. build the samples and demos:
```bash
cd samples
make
cd ..
cd demos
make
cd ..
```
6. copy the build-cocoa-debug folder to the user's home directory and rename it to wxWidgets:
```bash
mkdir ~/wxWidgets
cp -r . ~/wxWidgets
cp -r ../include ~/wxWidgets/include
```
7. open ShapeFusion.xcodeproj
8. build and run the project