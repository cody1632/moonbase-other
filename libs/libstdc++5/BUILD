mkdir BUILD &&
cd BUILD &&

../configure --host=$BUILD             \
             --enable-languages=c++    \
             --prefix=/usr             \
             --infodir=/usr/share/info \
             --mandir=/usr/share/man   \
             --enable-__cxa_atexit     \
             --enable-threads          \
             --disable-nls             \
             --enable-target-optspace  \
             --with-gnu-ld             \
             --with-system-zlib        \
             --enable-shared          &&

make CFLAGS='-O' LIBCFLAGS='-g -O2' LIBCXXFLAGS='-g -O2 -fno-implicit-templates' bootstrap-lean &&

prepare_install &&

make DESTDIR=$(pwd -P)/ROOT install-target-libstdc++-v3 &&

install -v $(pwd -P)/ROOT/usr/lib/libstdc++.so.5 /usr/lib/
