sed -i "s/-Werror//g" src/core/CMakeLists.txt &&
sed -i "s/-Werror//g" src/pyglue/CMakeLists.txt && 
sed -i "s/push(hidden)/push(default)/g" src/core/OCIOYaml.cpp &&

OPTS+=" -DUSE_EXTERNAL_LCMS=1    \
        -DUSE_EXTERNAL_YAML=1    \
        -DUSE_EXTERNAL_TINYXML=1 \
        -DOCIO_BUILD_STATIC=0    \
        -DOCIO_BUILD_PYGLUE=1    \
        -DPYTHON_INCLUDE_DIR=/usr/include/python$(module_version python | cut -c1-3)" &&

default_cmake_build
