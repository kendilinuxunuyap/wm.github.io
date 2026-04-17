.. _libXpresent:
**libXpresent**
===============

X11 sistemlerinde “Present” (sunum) uzantısını kullanan kütüphanedir.

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

**Not:** Burada verilen derleme talimatı(script) **kly Paket Sistemi**'ni kullanarak paketi derler ve oluştur. Oluşan paket(**.kly uzantılı dosya**)  **kly Paket Sistemi** kullanılarak siteme yüklenebilir. **kly Paket Sistemiyle Paket Yapma** konusunu okumak için `tıklayınız. <#klypaketyap>`_


.. raw:: pdf

   PageBreak
