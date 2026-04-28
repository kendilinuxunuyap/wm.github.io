.. _xapp:

**xapp**
========

GTK tabanlı yardımcı kütüphanedir.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="xapp"
	version="2.8.0"
	description="Common library for X-Apps project"
	source="https://github.com/linuxmint/xapp/archive/$version/xapp-${version}.tar.gz"
	depends="libdbusmenu,libgnomekbd,vala,py3-pygobject,make,gobject-introspection"
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
