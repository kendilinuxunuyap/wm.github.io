.. _libXtst:
**libXtst**
===========

Klavye ve fare girdilerini simüle etmek için kullanılır. Programların veya test otomasyonlarının, gerçek kullanıcı girişi olmadan fare hareketi, tıklama veya tuş vuruşu gibi eylemleri taklit etmesini sağlar. Ekran kayıt, otomasyon, uzaktan kumanda yazılımları tarafından yaygın kullanılır.

**Paketi Derleme :**
--------------------

.. code-block:: bash

    #!/usr/bin/env bash
    name="libXtst"
    version="1.2.4"
    description="X.Org Xlib-based client API for the XTEST & RECORD extensions library"
    source="https://www.x.org/archive/individual/lib/libXtst-$version.tar.xz"
    depends="libX11,libXext,xorgproto,libXi"
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
