.. _libvdpau:
**libvdpau**
============

NVIDIA'nın VDPAU (Video Decode and Presentation API for Unix) arayüzünü destekleyen bir kütüphanedir. Video oynatma ve kod çözme işlemlerini GPU üzerinden hızlandırmak için kullanılır. Linux sistemlerinde medya oynatıcılar ve uygulamalar tarafından donanım tabanlı video işleme için tercih edilir. Hafif ve açık kaynaklıdır, özellikle NVIDIA GPU'larla uyumludur.

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
