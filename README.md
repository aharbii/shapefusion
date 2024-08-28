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

# id3tag library
1. Run the following commands
```bash
wget https://downloads.sourceforge.net/project/mad/libid3tag/0.15.1b/libid3tag-0.15.1b.tar.gz
tar -xzvf libid3tag-0.15.1b.tar.gz
cd libid3tag-0.15.1b/
wget -O config.guess https://git.savannah.gnu.org/cgit/config.git/plain/config.guess
wget -O config.sub https://git.savannah.gnu.org/cgit/config.git/plain/config.sub
mkdir build
cd build
../configure --enable-debug --disable-shared
mkdir ~/id3tag
cp -r . ~/id3tag
```