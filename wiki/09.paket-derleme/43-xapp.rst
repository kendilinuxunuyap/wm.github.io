.. _xapp:
**xapp**
========

xapp, Linux Mint tarafından geliştirilen ve GTK tabanlı uygulamalarda ortak işlevleri kolaylaştırmak için kullanılan bir yardımcı kütüphanedir.

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

 
.. raw:: pdf

   PageBreak
