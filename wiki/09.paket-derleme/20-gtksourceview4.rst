.. _gtksourceview4:
**gtksourceview4**
==================

GTK+ tabanlı uygulamalar için gelişmiş bir metin düzenleme bileşenidir. Kaynak kodu düzenleme, sözdizimi vurgulama, satır numaraları, otomatik girintileme gibi özellikler sunar. Programlama dilleri ve betik dosyaları için özelleştirilmiş düzenleme desteği sağlar. Hafif, esnek ve genellikle GNOME tabanlı editörlerde (ör. gedit) kullanılır.

**Paketi Derleme :**
--------------------

.. code-block:: bash

    #!/usr/bin/env bash
    name="gtksourceview4"
    version="4.8.4"
    description="A text widget adding syntax highlighting and more to GNOME"
    source="https://download.gnome.org/sources/gtksourceview/${version%.*}/gtksourceview-${version}.tar.xz"
    depends="gtk3,libxml2,gobject-introspection"
    group="x11.libs"
    
    
    setup(){
    	cd $SOURCEDIR
        meson setup $BUILDDIR --prefix=/usr \
            --libdir=/usr/lib64/ \
            -Db_lto=true \
            -Dgtk_doc=true
    }
    
    build(){
        ninja -C $BUILDDIR
    }
    
    package(){
        DESTDIR=$DESTDIR ninja -C $BUILDDIR install
    }
    
.. raw:: pdf

   PageBreak
