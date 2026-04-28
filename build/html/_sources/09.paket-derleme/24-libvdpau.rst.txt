.. _libvdpau:

**libvdpau**
============

NVIDIA'nın VDPAU arayüzünü için kütüphanedir.

**Paketi Derleme :**
--------------------

.. code-block:: bash

    #!/usr/bin/env bash
    name="libvdpau"
    version="1.5"
    description="VDPAU wrapper and trace libraries"
    source="https://gitlab.freedesktop.org/vdpau/libvdpau/-/archive/$version/libvdpau-$version.tar.gz"
    depends="libXext"
    group="x11.libs"
    
    
    setup(){
    	cd $SOURCEDIR
        meson setup $BUILDDIR --prefix=/usr \
            -Ddefault_library=both \
            --libdir=/usr/lib64 \
            -Ddri2=true
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
