.. _xcb-util-cursor:
**xcb-util-cursor**
===================

XCB kütüphanesinin bir uzantısıdır.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="xcb-util-cursor"
	version="0.1.4"
	description="X C-language Bindings sample implementations"
	source="https://www.x.org/releases/individual/xcb/xcb-util-cursor-${version}.tar.xz"
	depends="libxcb,xcb-util-image,xcb-util-renderutil,xorgproto"
	group="x11.libs"


	setup(){
		$SOURCEDIR/configure --prefix=/usr \
			--libdir=/usr/lib64 \
			--enable-shared \
			--enable-static \
			--disable-devel-docs \
			--without-doxygen
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
