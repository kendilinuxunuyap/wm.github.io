.. _xcb-util-keysyms:
**xcb-util-keysyms**
====================

XCB (X C Binding) kütüphanesi için geliştirilen bir yardımcı modüldür ve klavye tuş kodları ile tuş sembolleri (keysyms) arasında çeviri yapmayı kolaylaştırır.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="xcb-util-keysyms"
	version="0.4.1"
	description="X C-language Bindings sample implementations"
	source="https://www.x.org/archive/individual/lib/xcb-util-keysyms-$version.tar.xz"
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
