.. _libnotify:
**libnotify**
=============

Masaüstü bildirimlerini göstermek için kullanılan bir kütüphanedir. GNOME ve diğer masaüstü ortamlarında uygulamaların kullanıcıya geçici, pop-up tarzı bildirimler göndermesini sağlar. `Freedesktop.org'un bildirim şartnamesine <https://specifications.freedesktop.org/notification-spec/1.3/>`_ dayanır ve hafif, kullanımı kolay bir API sunar. Genellikle GTK+ uygulamalarıyla entegre çalışır.

**Paketi Derleme :**
--------------------

.. code-block:: bash

    #!/usr/bin/env bash
    name="libnotify"
    version="0.8.2"
    description="Library for sending desktop notifications"
    source="https://download.gnome.org/sources/libnotify/${version%.*}/libnotify-${version}.tar.xz"
    depends=""
    group="x11.libs"
    
    setup(){
    	cd $SOURCEDIR
        meson setup $BUILDDIR --prefix=/usr \
            --libdir=/usr/lib64/ \
            -Dgtk_doc=false     \
            -Dman=false \
    		-Ddefault_library=both
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
