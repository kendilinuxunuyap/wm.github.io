.. _libXaw3d:
**libXaw3d**
============

X Window System (X11) için geliştirilmiş bir grafik kullanıcı arayüzü (GUI) kitaplığı olan X Athena Widgets (Xaw) kütüphanesinin 3 boyutlu (3D) görünümlü bir türevidir.

**Paketi Derleme :**
--------------------

.. code-block:: bash

    #!/usr/bin/env bash
    name="libXaw3d"
    version="1.6.4"
    description="X.Org Xaw3d library"
    source="https://www.x.org/archive/individual/lib/libXaw3d-$version.tar.gz"
    depends="libX11,libXt,libXmu,libXext"
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
