.. _libxkbcommon:
**libxkbcommon**
================

Klavye için gerekli kütüphane.

**Paketi Derleme :**
--------------------

.. code-block:: bash

    #!/usr/bin/env bash
    name="libxkbcommon"
    version="1.7.0"
    description="keymap handling library for toolkits and window systems"
    source="https://github.com/xkbcommon/libxkbcommon/archive/refs/tags/xkbcommon-$version.tar.gz"
    depends="libxml2,libxcb,xkeyboard-config,wayland-protocols,wayland"
    makedepend="bison,wayland-protocols,wayland"
    group="x11.libs"
    
    setup(){
    cd $SOURCEDIR
        meson setup $BUILDDIR \
            --prefix=/usr \
            --libdir=/usr/lib64/ \
            --libexecdir=/usr/lib64/ \
            -Denable-docs=false \
            -Denable-wayland=true
    }
    
    build(){
        ninja -C $BUILDDIR 
    }
    
    package(){
        DESTDIR=$DESTDIR ninja -C $BUILDDIR install
    }

**Not:** Burada verilen derleme talimatı(script) **kly Paket Sistemi**'ni kullanarak paketi derler ve oluştur. Oluşan paket(**.kly uzantılı dosya**)  **kly Paket Sistemi** kullanılarak siteme yüklenebilir. **kly Paket Sistemiyle Paket Yapma** konusunu okumak için `tıklayınız. <#klypaketyap>`_


.. raw:: pdf

   PageBreak
