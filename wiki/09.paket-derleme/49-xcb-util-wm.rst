.. _xcb-util-wm:
**xcb-util-wm**
===============

XCB kütüphanesinin bir uzantısıdır.

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

**Not:** Burada verilen derleme talimatı(script) **kly Paket Sistemi**'ni kullanarak paketi derler ve oluştur. Oluşan paket(**.kly uzantılı dosya**)  **kly Paket Sistemi** kullanılarak siteme yüklenebilir. **kly Paket Sistemiyle Paket Yapma** konusunu okumak için `tıklayınız. <#klypaketyap>`_


.. raw:: pdf

   PageBreak
