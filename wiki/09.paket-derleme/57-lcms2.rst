.. _lcms2:
**lcms2**
=========

Görüntü işleme ve renk yönetimi için kullanılan bir kütüphanedir.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="lcms2"
	version="2.16"
	url="https://netix.dl.sourceforge.net/project/lcms/lcms/2.14/lcms2-2.14.tar.gz"
	description="Small-footprint color management engine, version 2"
	source="https://netix.dl.sourceforge.net/project/lcms/lcms/${version}/lcms2-${version}.tar.gz"
	depends="libtiff"
	group="media.libs"

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
