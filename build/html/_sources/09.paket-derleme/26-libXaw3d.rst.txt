.. _libXaw3d:

**libXaw3d**
============

Xaw için 3D kütüphanesidir.

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

**Not:** Burada verilen derleme talimatı(script) **kly Paket Sistemi**'ni kullanarak paketi derler ve oluştur. Oluşan paket(**.kly uzantılı dosya**)  **kly Paket Sistemi** kullanılarak siteme yüklenebilir. **kly Paket Sistemiyle Paket Yapma** konusunu okumak için `tıklayınız. <#klypaketyap>`_


.. raw:: pdf

   PageBreak
