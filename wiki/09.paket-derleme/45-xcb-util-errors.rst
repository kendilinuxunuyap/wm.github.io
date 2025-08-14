.. _xcb-util-errors:
**xcb-util-errors**
===================

XCB (X C Binding) kütüphanesi için geliştirilen bir yardımcı (utility) kütüphanedir ve X11 hatalarını (error) daha okunabilir şekilde raporlamak için kullanılır.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="xcb-util-errors"
	version="1.0.1"
	description="Package xcb-util-errors"
	source="https://www.x.org/archive/individual/lib/xcb-util-errors-$version.tar.xz"
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
