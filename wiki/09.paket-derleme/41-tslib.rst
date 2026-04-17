.. _tslib:
**tslib**
=========

Yardımcı kütüphanedir.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="tslib"
	version="1.22"
	description="Touchscreen Access Library"
	source="https://github.com/libts/tslib/releases/download/${version}/tslib-${version}.tar.xz"
	depends=""
	group="x11.libs"


	setup () {
		autoreconf -fvi
		$SOURCEDIR/configure --prefix=/usr \
			--libdir=/usr/lib64/
	}

	build () {
		make
	}

	package () {
		make DESTDIR="$DESTDIR" install $jobs
	}

 
**Not:** Burada verilen derleme talimatı(script) **kly Paket Sistemi**'ni kullanarak paketi derler ve oluştur. Oluşan paket(**.kly uzantılı dosya**)  **kly Paket Sistemi** kullanılarak siteme yüklenebilir. **kly Paket Sistemiyle Paket Yapma** konusunu okumak için `tıklayınız. <#klypaketyap>`_


.. raw:: pdf

   PageBreak
