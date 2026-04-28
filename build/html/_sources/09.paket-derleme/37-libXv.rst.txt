.. _libXv:

**libXv**
=========

X11 pencere yönetimi için kullanılır.

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

**Not:** Burada verilen derleme talimatı(script) **kly Paket Sistemi**'ni kullanarak paketi derler ve oluştur. Oluşan paket(**.kly uzantılı dosya**)  **kly Paket Sistemi** kullanılarak siteme yüklenebilir. **kly Paket Sistemiyle Paket Yapma** konusunu okumak için `tıklayınız. <#klypaketyap>`_


.. raw:: pdf

   PageBreak
