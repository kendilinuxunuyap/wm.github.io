.. _libXxf86vm:

**libXxf86vm**
==============

Ekran çözünürlüğü, yenileme hızı gibi işlemlerin değiştirmesini sağlar.

**Paketi Derleme :**
--------------------

.. code-block:: bash

    #!/usr/bin/env bash
    name="libXxf86vm"
    version="1.1.5"
    description="X.Org Xxf86vm library"
    source="https://www.x.org/archive/individual/lib/libXxf86vm-$version.tar.xz"
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
