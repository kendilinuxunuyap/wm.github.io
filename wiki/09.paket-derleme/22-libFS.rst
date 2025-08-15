.. _libFS:
**libFS**
=========

X Window System'de yazı tipi sunucusu (font server) ile istemciler arasındaki iletişimi sağlayan bir kütüphanedir. X11 uygulamalarının uzak veya yerel yazı tipi sunucularından yazı tipi verilerine erişmesini sağlar. Hafif bir yapıya sahip olup, Xorg sistemlerinde yazı tipi yönetimini kolaylaştırır. Genellikle modern sistemlerde doğrudan kullanım yerine X sunucusuyla entegre çalışır.

**Paketi Derleme :**
--------------------

.. code-block:: bash

    #!/usr/bin/env bash
    name="libFS"
    version="1.0.9"
    description="X.Org FS library"
    source="https://www.x.org/archive/individual/lib/libFS-$version.tar.xz"
    depends="xorgproto"
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
