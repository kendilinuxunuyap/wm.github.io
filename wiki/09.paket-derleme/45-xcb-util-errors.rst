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


**Not:** Burada verilen derleme talimatı(script) **kly Paket Sistemi**'ni kullanarak paketi derler ve oluştur. Oluşan paket(**.kly uzantılı dosya**)  **kly Paket Sistemi** kullanılarak siteme yüklenebilir. **kly Paket Sistemiyle Paket Yapma** konusunu okumak için `tıklayınız. <#klypaketyap>`_


 
.. raw:: pdf

   PageBreak
