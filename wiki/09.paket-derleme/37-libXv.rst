.. _libXv:
**libXv**
=========

Video görüntüsünü donanım hızlandırmalı olarak X11 pencerelerine hızlıca çizmek için kullanılır. Video oynatıcılar veya medya uygulamalarının, video karelerini CPU yerine GPU ile doğrudan X11 penceresine aktarmasını sağlar. Böylece daha az CPU kullanımı, daha akıcı video oynatma ve daha düşük gecikme elde edilir.

**Paketi Derleme :**
--------------------

.. code-block:: bash

    #!/usr/bin/env bash
    name="libXv"
    version="1.0.12"
    description="X.Org Xv library"
    source="https://www.x.org/archive/individual/lib/libXv-$version.tar.xz"
    depends=""
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
