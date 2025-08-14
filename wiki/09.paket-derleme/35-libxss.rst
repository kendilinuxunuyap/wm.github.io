.. _libxss:
**libxss**
==========

X11 (X Window System) için geliştirilmiş, ekran koruyucu (screen saver) durumunu izlemeye ve kontrol etmeye yarayan bir kütüphanedir.

**Paketi Derleme :**
--------------------

.. code-block:: bash

    #!/usr/bin/env bash
    name="libxss"
    version="1.2.4"
    description="X11 Screen Saver extension library"
    source="https://xorg.freedesktop.org/releases/individual/lib/libXScrnSaver-${version}.tar.xz"
    depends="libXext,util-macros,xorgproto"
    group="x11.libs"
    
    
    
    setup(){
        autoreconf -fvi
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
