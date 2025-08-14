.. _libxkbcommon:
**libxkbcommon**
================

Klavye tuşlarının hangi karaktere veya işlevlere karşılık geldiğini belirler. xkb (X Keyboard Extension) sistemini kullanarak klavye haritalarını işler. Klavye düzenlerinin yorumlanmasını ve yönetilmesini sağlar (örn. QWERTY, Dvorak, Türkçe Q, Türkçe F). Uygulamaların hangi tuşa hangi karakterin karşılık geldiğini anlamasına yardımcı olur.

Nerelerde Kullanılır:
---------------------

- Wayland tabanlı sistemlerde (örneğin GNOME Shell, KDE Plasma Wayland oturumları)
- Modern X11 uygulamalarında
- Toolkit'lerde: GTK, Qt, WLRoots, Weston
- Terminal emülatörleri ve kompozit pencere yöneticileri

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

.. raw:: pdf

   PageBreak
