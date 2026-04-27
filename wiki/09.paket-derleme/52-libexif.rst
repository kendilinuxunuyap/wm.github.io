.. _libexif:

**libexif**
===========

JPEG ve TIFF formatındaki dosyalar için bir kütüphanedir.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="libexif"
	version="0.6.25"
	description="Library to parse an EXIF file and read the data from those tags"
	source="https://github.com/libexif/libexif/archive/refs/tags/v${version}.tar.gz"
	depends=""
	group="media.libs"


	setup(){
		cd $SOURCEDIR
		autoreconf -fvi
		./configure --prefix=/usr \
		    --libdir=/usr/lib64/
	}

	build(){
		make
	}

	package(){
		make DESTDIR="$DESTDIR" install
	}

**Not:** Burada verilen derleme talimatı(script) **kly Paket Sistemi**'ni kullanarak paketi derler ve oluştur. Oluşan paket(**.kly uzantılı dosya**)  **kly Paket Sistemi** kullanılarak siteme yüklenebilir. **kly Paket Sistemiyle Paket Yapma** konusunu okumak için `tıklayınız. <#klypaketyap>`_


 
.. raw:: pdf

   PageBreak
