.. _libtiff:

**libtiff**
===========

 TIFF dosyalarını işlemek için kullanılan kütüphanedir.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="libtiff"
	version="4.6.0"
	description="Tag Image File Format (TIFF) library"
	source="https://gitlab.com/libtiff/libtiff/-/archive/v$version/libtiff-v$version.tar.gz"
	depends=""
	group="media.libs"

	setup(){
		cd $SOURCEDIR
		autoreconf -fvi
		./configure --prefix=/usr \
		    --libdir=/usr/lib64/ \
		    --disable-docs
	}

	build(){
		make
	}

	package(){
		make DESTDIR="${DESTDIR}" install
	}

**Not:** Burada verilen derleme talimatı(script) **kly Paket Sistemi**'ni kullanarak paketi derler ve oluştur. Oluşan paket(**.kly uzantılı dosya**)  **kly Paket Sistemi** kullanılarak siteme yüklenebilir. **kly Paket Sistemiyle Paket Yapma** konusunu okumak için `tıklayınız. <#klypaketyap>`_


 
.. raw:: pdf

   PageBreak
