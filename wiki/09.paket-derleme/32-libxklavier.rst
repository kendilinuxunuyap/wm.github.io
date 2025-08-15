.. _libxklavier:
**libxklavier**
===============

X11 sistemlerinde çalışan uygulamaların, sistemdeki klavye düzenlerini (keyboard layouts) ve XKB (X Keyboard Extension) yapılandırmalarını okumasına ve değiştirmesine imkan tanıyan bir kütüphanedir.

- Klavye düzenlerini (örneğin: Türkçe Q, ABD, Dvorak) listelemek, okumak, değiştirmek için bir API sunar.
- XKB altyapısını kullanır (X Keyboard Extension).
- GNOME ve diğer masaüstü ortamlarında klavye düzeni değiştirici araçlar tarafından kullanılır (örneğin: gnome-control-center, gsd-keyboard, lxde keyboard switcher).



**Paketi Derleme :**
--------------------

.. code-block:: bash

    #!/usr/bin/env bash
    name="libxklavier"
    version="5.4"
    description="High-level API for X Keyboard Extension"
    source="https://people.freedesktop.org/~svu/libxklavier-${version}.tar.bz2"
    depends="glib,iso-codes,libxml2"
    group="x11.libs"
    
    
    setup(){
    cd  $SOURCEDIR
    	autoreconf -fvi
        $SOURCEDIR/configure --prefix=/usr \
            --libdir=/usr/lib64/ \
    		--with-xkb-bin-base=/usr/bin \
          	--with-xkb-base=/usr/share/X11/xkb \
    		--enable-gtk-doc
    }
    
    build(){
        make
    }
    
    package(){
    #mkdir -p $DESTDIR/usr/share/X11/xkb
        make install DESTDIR=$DESTDIR $jobs
        mkdir -p $DESTDIR/usr/lib64/pkgconfig
        install $SOURCEDIR/libxklavier.pc $DESTDIR/usr/lib64/pkgconfig/libxklavier.pc
    
    }

**Not:** Burada verilen derleme talimatı(script) **kly Paket Sistemi**'ni kullanarak paketi derler ve oluştur. Oluşan paket(**.kly uzantılı dosya**)  **kly Paket Sistemi** kullanılarak siteme yüklenebilir. **kly Paket Sistemiyle Paket Yapma** konusunu okumak için `tıklayınız. <#klypaketyap>`_


.. raw:: pdf

   PageBreak
