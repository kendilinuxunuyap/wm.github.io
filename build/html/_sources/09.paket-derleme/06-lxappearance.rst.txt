.. _lxappearance:

**lxappearance**
================

GTK temalarını yapılandırma aracıdır.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="lxappearance"
	version="0.6.3"
	description="Feature-rich GTK+ theme switcher of the LXDE Desktop"
	source="https://downloads.sourceforge.net/lxde/$name-$version.tar.xz"
	depends="gtk3,dbus-glib"
	builddepend=""
	group="lxde.base"

	setup(){
		cp -prvf $PACKAGEDIR/00-gtk3-fix.patch /tmp/bps/build/
		cd $SOURCEDIR
		patch -Np1 -i ../00-gtk3-fix.patch
		./configure --prefix=/usr --enable-gtk3 \
		    --libdir=/usr/lib64/ \
		    --enable-dbus
		    
	}

	build(){
		make
	}

	package(){
		make install DESTDIR=$DESTDIR
	}

Ek dosyaları indirmek için `tıklayınız.. <https://kendilinuxunuyap.github.io/_static/files/lxappearance/files.tar>`_


**Not:** Burada verilen derleme talimatı(script) **kly Paket Sistemi**'ni kullanarak paketi derler ve oluştur. Oluşan paket(**.kly uzantılı dosya**)  **kly Paket Sistemi** kullanılarak siteme yüklenebilir. **kly Paket Sistemiyle Paket Yapma** konusunu okumak için `tıklayınız. <#klypaketyap>`_


 
.. raw:: pdf

   PageBreak
