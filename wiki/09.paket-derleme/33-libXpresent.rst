.. _libXpresent:
**libXpresent**
===============

X Present Extension'ın istemci tarafı API’sini sağlar. Bu eklenti, daha düzgün, yırtılmasız (tearing-free) grafik güncellemeleri için ekran sunumlarını (presentation) kontrol etmeye yarar.

Uygulamaların (özellikle oyunlar, video oynatıcılar, pencere yöneticileri) tam ekran veya pencere içi çizimlerini ekranla senkronize bir şekilde sunmalarını sağlar.

Bu, klasik X11 sistemlerinde sık görülen ekran yırtılması (tearing) sorununu azaltmaya yardımcı olur.

VSync benzeri işlevler için altyapı sağlar.

**Paketi Derleme :**
--------------------

.. code-block:: bash

    #!/usr/bin/env bash
    name="libXpresent"
    version="1.0.1"
    description="X Present Extension C Library"
    source="https://www.x.org/archive/individual/lib/libXpresent-$version.tar.xz"
    depends="libX11,xorgproto,libXext,libXfixes,libXrandr"
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
