.. _lxrandr:

**lxrandr**
===========


Ekran çözünürlüğü ve monitör yapılandırması için  kullanılan kütüphanedir.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="lxrandr"
	version="0.3.2"
	description="Monitor configuration tool (part of LXDE)"
	source="https://downloads.sourceforge.net/lxde/lxrandr-$version.tar.xz"
	depends="gtk3,xrandr"
	builddepend="intltool"
	group="lxde.base"


	setup(){
		cd $SOURCEDIR
		autoreconf -fvi
		./configure --prefix=/usr \
			--enable-gtk3 \
			--enable-man \
		    --libdir=/usr/lib64/
	}

	build(){
		make DESTDIR=$DESTDIR
	}

	package(){
		make DESTDIR=$DESTDIR install
	}

**Not:** Burada verilen derleme talimatı(script) **kly Paket Sistemi**'ni kullanarak paketi derler ve oluştur. Oluşan paket(**.kly uzantılı dosya**)  **kly Paket Sistemi** kullanılarak siteme yüklenebilir. **kly Paket Sistemiyle Paket Yapma** konusunu okumak için `tıklayınız. <#klypaketyap>`_


 
.. raw:: pdf

   PageBreak
