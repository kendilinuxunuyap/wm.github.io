.. _xcb-util-wm:
**xcb-util-wm**
===============

XCB (X C Binding) için geliştirilen bir yardımcı kütüphanedir ve X11 pencere yöneticisi protokolleriyle çalışmayı kolaylaştırır.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="xcb-util-wm"
	version="0.4.2"
	description="X C-language Bindings sample implementations"
	source="https://www.x.org/archive/individual/lib/xcb-util-wm-$version.tar.xz"
	depends=""
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
