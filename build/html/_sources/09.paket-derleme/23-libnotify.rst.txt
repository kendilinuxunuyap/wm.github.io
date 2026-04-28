.. _libnotify:

**libnotify**
=============

Bildirimlerini göstermek için kullanılan bir kütüphanedir. 

**Paketi Derleme :**
--------------------

.. code-block:: bash

    #!/usr/bin/env bash
    name="libnotify"
    version="0.8.2"
    description="Library for sending desktop notifications"
    source="https://download.gnome.org/sources/libnotify/${version%.*}/libnotify-${version}.tar.xz"
    depends=""
    group="x11.libs"
    
    setup(){
    	cd $SOURCEDIR
        meson setup $BUILDDIR --prefix=/usr \
            --libdir=/usr/lib64/ \
            -Dgtk_doc=false     \
            -Dman=false \
    		-Ddefault_library=both
    }
    
    build(){
        ninja -C $BUILDDIR
    }
    
    package(){
        DESTDIR=$DESTDIR ninja -C $BUILDDIR install
    }

**Not:** Burada verilen derleme talimatı(script) **kly Paket Sistemi**'ni kullanarak paketi derler ve oluştur. Oluşan paket(**.kly uzantılı dosya**)  **kly Paket Sistemi** kullanılarak siteme yüklenebilir. **kly Paket Sistemiyle Paket Yapma** konusunu okumak için `tıklayınız. <#klypaketyap>`_


.. raw:: pdf

   PageBreak
