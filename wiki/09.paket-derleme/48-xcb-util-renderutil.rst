.. _xcb-util-renderutil:
**xcb-util-renderutil**
=======================

xcb-util-renderutil, X11 sisteminde kullanılan bir yardımcı kütüphanedir ve XCB (X C Binding) adı verilen düşük seviyeli, modern bir X protokolü arayüzünün bir parçasıdır. Daha spesifik olarak, xcb-util-renderutil kütüphanesi, X11'in Render Extension (Render uzantısı) ile çalışmayı kolaylaştırmak için bazı yardımcı işlevler sağlar.

**Paketi Derleme :**
--------------------


.. code-block:: bash

	#!/usr/bin/env bash
	name="xcb-util-renderutil"
	version="0.3.10"
	description="X C-language Bindings sample implementations"
	source="https://www.x.org/releases/individual/xcb/xcb-util-renderutil-${version}.tar.xz"
	depends="libxcb,util-macros,xorgproto"
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
