.. _lxde-common:
**lxde-common**
===============

LXDE için gerekli temel kütüphanedir.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="lxde-common"
	version="0.99.2"
	description="LXDE Session default configuration files and nuoveXT2 iconset "
	source="https://github.com/lxde/lxde-common/archive/refs/tags/$version.tar.gz"
	depends=""
	builddepend=""
	group="lxde.base"


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
		make install DESTDIR=$DESTDIR
	}


**Not:** Burada verilen derleme talimatı(script) **kly Paket Sistemi**'ni kullanarak paketi derler ve oluştur. Oluşan paket(**.kly uzantılı dosya**)  **kly Paket Sistemi** kullanılarak siteme yüklenebilir. **kly Paket Sistemiyle Paket Yapma** konusunu okumak için `tıklayınız. <#klypaketyap>`_


.. raw:: pdf

   PageBreak
