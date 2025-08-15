.. _libXxf86dga:
**libXxf86dga**
===============

Uygulamaların, X sunucusunu atlayarak doğrudan grafik donanımına erişmesini sağlar. Bu sayede özellikle tam ekran uygulamalarda daha hızlı ve düşük gecikmeli grafik çizimi mümkün olur. CPU ve GPU arasında daha hızlı veri aktarımı sağlar.

**Paketi Derleme :**
--------------------

.. code-block:: bash

    #!/usr/bin/env bash
    name="libXxf86dga"
    version="1.1.6"
    description="X.Org Xxf86dga library"
    source="https://www.x.org/archive/individual/lib/libXxf86dga-$version.tar.gz"
    depends=""
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
