.. _gdk-pixbuf:
**gdk-pixbuf**
==============

GTK+ kütüphanesinin bir parçası olan pakettir.

**Paketi Derleme :**
--------------------

.. code-block:: bash

    #!/usr/bin/env bash
    name="gdk-pixbuf"
    version="2.42.10"
    description="gdk-pixbuf Image loading library for GTK+ "
    source="https://download.gnome.org/sources/gdk-pixbuf/${version%.*}/gdk-pixbuf-$version.tar.xz"
    depends="libjpeg-turbo,shared-mime-info,gi-docgen,libtiff,libpng,glib"
    group="x11.libs"
    
    
    setup(){
    	cd $SOURCEDIR
        meson setup $BUILDDIR --prefix=/usr \
            --libdir=/usr/lib64/ \
            -Db_lto=true \
            -D builtin_loaders=all \
            -Dman=false \
            -D installed_tests=false \
            -D tiff=enabled \
            -D introspection=enabled \
            -D tests=false
    
    }
    
    build(){
    	meson compile -C $BUILDDIR
        #ninja -C $BUILDDIR
    }
    
    package(){
    	DESTDIR="$DESTDIR" meson install -C $BUILDDIR
    
    }
    
Ek dosyaları indirmek için `tıklayınız. <https://kendilinuxunuyap.github.io/_static/files/gdk-pixbuf/files.tar>`_

**Not:** Burada verilen derleme talimatı(script) **kly Paket Sistemi**'ni kullanarak paketi derler ve oluştur. Oluşan paket(**.kly uzantılı dosya**)  **kly Paket Sistemi** kullanılarak siteme yüklenebilir. **kly Paket Sistemiyle Paket Yapma** konusunu okumak için `tıklayınız. <#klypaketyap>`_


.. raw:: pdf

   PageBreak
