.. _libXtst:
**libXtst**
===========

Klavye ve fare simüle etmek için kullanılan kütüphane. 

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

**Not:** Burada verilen derleme talimatı(script) **kly Paket Sistemi**'ni kullanarak paketi derler ve oluştur. Oluşan paket(**.kly uzantılı dosya**)  **kly Paket Sistemi** kullanılarak siteme yüklenebilir. **kly Paket Sistemiyle Paket Yapma** konusunu okumak için `tıklayınız. <#klypaketyap>`_


.. raw:: pdf

   PageBreak
