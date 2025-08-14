.. _cairo:
**cairo**
=========

2D vektör grafikleri çizimi için kullanılan açık kaynaklı bir kütüphanedir. Çizgiler, şekiller, metinler ve görüntüler gibi grafiksel öğeleri oluşturmak ve işlemek için platformdan bağımsız bir API sunar. Linux, Windows ve macOS gibi farklı platformlarda çalışır ve genellikle GTK+, Firefox gibi uygulamalarda kullanılır. Hafif, esnek ve yüksek kaliteli grafik çıktıları üretir.

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

.. raw:: pdf

   PageBreak
