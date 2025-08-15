.. _libXcomposite:
**libXcomposite**
=================

X11 sisteminde pencere kompozisyonunu desteklemek için kullanılan bir yazılım kütüphanesidir. Pencerelerin içeriklerini ayrı ayrı bellek tamponlarında tutarak, bu pencerelerin birleşiminin yapılmasını sağlar. Şeffaflık, gölgeler, geçiş efektleri gibi gelişmiş görüntü özelliklerinin sağlanmasını mümkün kılar.

**Paketi Derleme :**
--------------------

.. code-block:: bash

    #!/usr/bin/env bash
    name="libXcomposite"
    version="0.4.6"
    description="X.Org Xcomposite library"
    source="https://gitlab.freedesktop.org/xorg/lib/libxcomposite/-/archive/libXcomposite-$version/libxcomposite-libXcomposite-$version.tar.gz"
    depends=""
    group="x11.libs"
    
    setup(){
    	cd $SOURCEDIR
    	autoreconf -fvi
        ./configure --prefix=/usr \
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
