.. _libjpeg-turbo:
**libjpeg-turbo**
=================

JPEG görüntü kodek kütüphanesidir.

**Paketi Derleme :**
--------------------

.. code-block:: bash

    #!/usr/bin/env bash
    name="libjpeg-turbo"
    version="3.0.3"
    description="MMX, SSE, and SSE2 SIMD accelerated JPEG library"
    source="https://github.com/libjpeg-turbo/libjpeg-turbo/archive/refs/tags/$version.tar.gz"
    depends=""
    group="media.libs"
    
    
    setup(){
        cd $SOURCEDIR
        mkdir build
        cd build
    
        cmake -DCMAKE_INSTALL_PREFIX=/usr \
            -DCMAKE_INSTALL_LIBDIR=/usr/lib64 \
            -DWITH_JPEG8=ON ..
    }
    
    build(){
        make
    }
    
    package(){
        make install DESTDIR=$DESTDIR
        mkdir -p $DESTDIR/lib64
        cd $DESTDIR/lib64
    ln -s ../usr/lib64/libjpeg.so.8 libjpeg.so.8.2.2
    }

**Not:** Burada verilen derleme talimatı(script) **kly Paket Sistemi**'ni kullanarak paketi derler ve oluştur. Oluşan paket(**.kly uzantılı dosya**)  **kly Paket Sistemi** kullanılarak siteme yüklenebilir. **kly Paket Sistemiyle Paket Yapma** konusunu okumak için `tıklayınız. <#klypaketyap>`_


.. raw:: pdf

   PageBreak
