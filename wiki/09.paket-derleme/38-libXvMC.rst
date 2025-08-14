.. _libXvMC:
**libXvMC**
===========

Video oynatma sırasında video kod çözme işlemlerini donanım hızlandırmalı olarak yapmayı mümkün kılar. Bu, özellikle MPEG video kodeklerinde CPU yükünü azaltmak ve akıcı video oynatımı sağlamak için kullanılır. Yani, video oynatıcıların sadece görüntüyü göstermekle kalmayıp, kod çözme sürecinde GPU desteği almasını sağlar.

**Paketi Derleme :**
--------------------

.. code-block:: bash

    #!/usr/bin/env bash
    name="libXvMC"
    version="1.0.13"
    description="X.Org XvMC library"
    source="https://www.x.org/archive/individual/lib/libXvMC-$version.tar.xz"
    depends="libX11,libXext,libXv,xorgproto"
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
