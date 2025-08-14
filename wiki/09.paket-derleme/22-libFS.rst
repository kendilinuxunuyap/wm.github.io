.. _libFS:
**libFS**
=========

X Window System'de yazı tipi sunucusu (font server) ile istemciler arasındaki iletişimi sağlayan bir kütüphanedir. X11 uygulamalarının uzak veya yerel yazı tipi sunucularından yazı tipi verilerine erişmesini sağlar. Hafif bir yapıya sahip olup, Xorg sistemlerinde yazı tipi yönetimini kolaylaştırır. Genellikle modern sistemlerde doğrudan kullanım yerine X sunucusuyla entegre çalışır.
.. _ :

**Paketi Derleme :**
--------------------

.. code-block:: bash

    #!/usr/bin/env bash
    name="libFS"
    version="1.0.9"
    description="X.Org FS library"
    source="https://www.x.org/archive/individual/lib/libFS-$version.tar.xz"
    depends="xorgproto"
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
