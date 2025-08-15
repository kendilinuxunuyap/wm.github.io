.. _libXvMC:
**libXvMC**
===========

Video oynatma sırasında video kod çözme işlemlerini donanım hızlandırmalı olarak yapmayı mümkün kılar. Bu, özellikle MPEG video kodeklerinde CPU yükünü azaltmak ve akıcı video oynatımı sağlamak için kullanılır. Yani, video oynatıcıların sadece görüntüyü göstermekle kalmayıp, kod çözme sürecinde GPU desteği almasını sağlar.

**Paketi Derleme :**
--------------------

.. code-block:: bash

    #!/usr/bin/env bash
    name="libXvMC"
    version="1.0.13"
    description="X.Org XvMC library"
    source="https://www.x.org/archive/individual/lib/libXvMC-$version.tar.xz"
    depends="libX11,libXext,libXv,xorgproto"
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
