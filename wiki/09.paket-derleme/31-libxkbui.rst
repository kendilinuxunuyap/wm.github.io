.. _libxkbui:
**libxkbui**
============

X Keyboard Extension (XKB) kullanıcı arayüzü bileşenlerini sağlayan bir kütüphanedir.X11 sistemlerinde klavye düzeni ve davranışlarını kontrol eden bir sistemdir. **libxkbui**, bu sistemin bir parçası olan grafik kullanıcısı arayüzü öğelerini içerir. Özellikle XKB yapılandırma araçlarının GUI bileşenlerini sağlar (örneğin: xkbcomp, xkbutils, xkbselect, vs.).

**Paketi Derleme :**
--------------------

.. code-block:: bash

    #!/usr/bin/env bash
    name="libxkbui"
    version="1.0.2"
    description="Package libxkbui"
    source="https://www.x.org/archive/individual/lib/libxkbui-$version.tar.gz"
    depends="libX11,libXt,libxkbfile"
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
