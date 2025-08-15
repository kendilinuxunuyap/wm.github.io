.. _libXdamage:
**libXdamage**
==============

Bir pencerenin hangi kısımlarının değiştiğini takip etmek kullanılır. Yani, bir pencere üzerinde sadece değişen (güncellenen) alanları bildirir. Bu sayede:

- Ekran kaydı (screen recording),
- Uzaktan masaüstü paylaşımı (VNC vs.),
- Compositing window manager'lar,
- GPU optimizasyonları,

gibi uygulamalarda sadece değişen pikselleri işleyerek performans kazancı sağlar.

**Paketi Derleme :**
--------------------

.. code-block:: bash

    #!/usr/bin/env bash
    name="libXdamage"
    version="1.1.6"
    description="X.Org Xdamage library"
    source="https://www.x.org/archive/individual/lib/libXdamage-$version.tar.xz"
    depends="libXfixes,libX11"
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
