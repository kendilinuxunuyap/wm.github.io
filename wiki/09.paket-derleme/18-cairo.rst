.. _cairo:

**cairo**
=========

Grafikleri çizimi için kullanılan bir kütüphanedir.

**Paketi Derleme :**
--------------------

.. code-block:: bash

    #!/usr/bin/env bash
    name="cairo"
    version="1.18.0"
    description="A vector graphics library with cross-device output support"
    source="https://gitlab.freedesktop.org/cairo/cairo/-/archive/$version/cairo-$version.tar.gz"
    depends="pixman,libpng,glib,libpcre2,fontconfig,libX11"
    group="x11.libs"
    
    
    setup(){
    	cd $SOURCEDIR
    	meson setup $BUILDDIR --prefix=/usr \
            --libdir=/usr/lib64/ \
            -D b_lto=true \
            -D gtk_doc=false \
            -D spectre=disabled \
            -D symbol-lookup=disabled \
            -D tests=disabled
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
