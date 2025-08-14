.. _libXfont:
**libXfont**
============

X sunucusunun font (bitmap veya outline tabanlı) dosyalarını yüklemesini, analiz etmesini ve istemcilere sunmasını sağlar.X sunucusu ile istemciler arasındaki yazı tipi işlemlerini destekler, ancak doğrudan uygulamalar tarafından kullanılmaz. Genellikle X sunucusunun içinde veya onunla birlikte çalışan font sunucularında kullanılır.

**Paketi Derleme :**
--------------------

.. code-block:: bash

    #!/usr/bin/env bash
    name="libXfont"
    version="1.5.4"
    description="X.Org Xfixes library"
    source="https://www.x.org/archive/individual/lib/libXfont-$version.tar.gz"
    depends="libfontenc,freetype"
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
