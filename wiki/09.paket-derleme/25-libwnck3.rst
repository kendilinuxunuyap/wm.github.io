.. _libwnck3:
**libwnck3**
============

GNOME masaüstü ortamı için kullanılan bir kütüphanedir. Uygulamaların açık pencereleri, çalışma alanlarını ve masaüstü görevlerini yönetmesini sağlar Pencere listeleme, değiştirme, simge durumuna küçültme gibi işlevler sunar. Hafif ve GTK+ tabanlı uygulamalarda sıkça kullanılır.

**Paketi Derleme :**
--------------------

.. code-block:: bash

    #!/usr/bin/env bash
    name="libwnck3"
    version="43.0"
    description="A window navigation construction kit "
    source="https://gitlab.gnome.org/GNOME/libwnck/-/archive/43.0/libwnck-43.0.tar.gz"
    depends="startup-notification"
    group="x11.libs"
    
    
    setup(){
    	cd $SOURCEDIR
    	meson setup $BUILDDIR --prefix=/usr \
            --libdir=/usr/lib64/ 
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
