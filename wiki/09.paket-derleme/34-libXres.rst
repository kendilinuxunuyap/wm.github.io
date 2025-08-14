.. _libXres:
**libXres**
===========

X sunucusundaki kaynak (resource) kullanımını izlemek için kullanılır.

Özellikle her X11 istemcisinin, ne kadar grafik kaynağı kullanıyor, kaç pencere kaç grafik nesnesi oluşturuyor, hangi istemci ne kadar kaynak tüketiyor öğrenmeyi sağlar.

**Paketi Derleme :**
--------------------

.. code-block:: bash

    #!/usr/bin/env bash
    name="libXres"
    version="1.2.2"
    description="X.Org XRes library"
    source="https://www.x.org/archive/individual/lib/libXres-$version.tar.xz"
    depends="libX11,libXext,xorgproto"
    group="x11.libs"
    
    
    setup(){
        $SOURCEDIR/configure --prefix=/usr \
            --libdir=/usr/lib64/
    }
    
    build(){
        make
    }
    
    package(){
        make install DESTDIR=$DESTDIR
    }

.. raw:: pdf

   PageBreak
