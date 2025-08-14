.. _tslib:
**tslib**
=========

tslib paketi, özellikle TypeScript projelerinde kullanılan bir yardımcı (utility) kütüphanedir. TypeScript derleyicisinin (tsc) ürettiği JavaScript kodlarında kullanılan bazı yardımcı fonksiyonları içerir.

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

 
.. raw:: pdf

   PageBreak
